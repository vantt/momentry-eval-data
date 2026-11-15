---
id: 2026-10-09-migration-v3-sang-v4-block-scalar-4257
code: M-XYB3
aliases: [M-XYB3]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac, dao_quyet_dinh]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2717", "omp:cd4449ab#L2741", "omp:cd4449ab#L2744", "omp:cd4449ab#L2746", "omp:cd4449ab#L2770"]
hook: "Python đọc được file, Go thì không: một ký tự '|4' sai"
tension: tuong_ma_hoa_ra
sides: ["Python parse file YAML thành công nên tưởng file đúng", "Go từ chối đọc vì chỉ báo thụt lề |4 sai, receipt không đọc được"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang được rút gọn, người làm đang viết bước migration từ schema v3 sang v4 và cần test fixture chạy qua. Họ tin file YAML ghép bằng chuỗi là đúng vì Python đọc được. Hoá ra Go yaml.v3 từ chối vì chỉ báo thụt lề |4 sai; đổi thành | thì decode được. Ai ghép YAML bằng chuỗi rồi chỉ kiểm bằng ngôn ngữ khác nên để ý."
audience: dev Go viết migration hoặc ghép YAML bằng chuỗi
spine_context: Dự án mcp-skill-hub đang được rút gọn; người làm đang viết bước migration từ schema v3 sang v4 theo kế hoạch Phase 3.
spine_context_lines: ["omp:cd4449ab#L2374"]
spine_want: Muốn test fixture migration v3 sang v4 chạy qua.
spine_want_lines: ["omp:cd4449ab#L2374", "omp:cd4449ab#L2687"]
spine_obstacle: "Test migration đỏ, thoát với mã lỗi 1."
spine_obstacle_lines: ["omp:cd4449ab#L2713"]
spine_turn: Tưởng file YAML ghép bằng chuỗi là đúng vì Python đọc được; hoá ra Go yaml.v3 từ chối vì chỉ báo thụt lề |4 sai.
spine_turn_lines: ["omp:cd4449ab#L2719", "omp:cd4449ab#L2743"]
spine_action: Đổi chỉ báo |4 thành | rồi decode lại bằng yaml.v3.
spine_action_lines: ["omp:cd4449ab#L2744"]
spine_outcome: "Receipt decode được trong Go, nhưng go test của migration vẫn đỏ ở lần chạy sau."
spine_outcome_lines: ["omp:cd4449ab#L2746", "omp:cd4449ab#L2770"]
spine_takeaway: "YAML ghép bằng chuỗi cần kiểm bằng đúng decoder mà code dùng, vì Python đọc được không có nghĩa là Go đọc được."
spine_takeaway_lines: ["omp:cd4449ab#L2743", "omp:cd4449ab#L2746"]
completeness: 7
---

# Migration v3 sang v4: block scalar YAML sai làm receipt WAL không đọc được

**Góc kể:** Dự án mcp-skill-hub đang được rút gọn, người làm đang viết bước migration từ schema v3 sang v4 và cần test fixture chạy qua. Họ tin file YAML ghép bằng chuỗi là đúng vì Python đọc được. Hoá ra Go yaml.v3 từ chối vì chỉ báo thụt lề |4 sai; đổi thành | thì decode được. Ai ghép YAML bằng chuỗi rồi chỉ kiểm bằng ngôn ngữ khác nên để ý.
**Bối cảnh:** Migration v3 sang v4 ghi receipt WAL chứa nội dung file cũ dạng YAML lồng nhau. Test đỏ qua hơn chục lần chạy với lỗi 'proposed mutation is invalid'.
**Chuyện gì xảy ra:** Python yaml parse được chuỗi, nhưng decoder yaml.v3 của Go báo 'did not find expected key' ở dòng 1. Nguyên nhân là chỉ báo thụt lề |4 sai trong block scalar. Đổi thành | thì decode thành công và phần migration được tiếp tục.
**Bài học:** Đừng tự ghép YAML bằng chuỗi cho thứ sẽ được đọc lại. Dùng marshaller hoặc kiểm bằng đúng decoder mà code dùng.
**Artefact:** Đoạn YAML receipt trước và sau khi đổi |4 thành |, che nội dung.
