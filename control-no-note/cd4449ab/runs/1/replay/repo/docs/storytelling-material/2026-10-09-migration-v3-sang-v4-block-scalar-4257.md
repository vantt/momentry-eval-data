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
hook: "Python đọc được file YAML, Go thì không: lỗi nằm ở một ký tự thụt lề"
tension: nho_ma_to
sides: ["Python parse chuỗi YAML bình thường", "Go từ chối vì một chỉ báo thụt lề |4"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang được rút gọn qua nhiều phase, và người làm đang viết migration chuyển dữ liệu từ schema v3 sang v4. Họ kiểm chuỗi YAML bằng Python, thấy đọc được nên tin là đúng. Go decoder lại từ chối chỉ báo thụt lề |4; đổi thành | thì decode được, nhưng test migration vẫn đỏ vì một lỗi schema khác. Ai ghép YAML bằng chuỗi cho thứ sẽ được đọc lại nên kiểm bằng đúng decoder mà code dùng."
audience: dev viết migration hoặc test dữ liệu YAML bằng Go
spine_context: Dự án mcp-skill-hub đang được rút gọn qua nhiều phase; người làm viết migration chuyển dữ liệu từ schema v3 sang v4.
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: Muốn fixture trước Phase 3 chuyển được từ v3 sang v4 và chứng minh được điều đó.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: Test TestPrePhase3FixtureMigrationV3ToV4 đỏ (exit 1).
spine_obstacle_lines: ["omp:cd4449ab#L2713"]
spine_turn: Tưởng chuỗi YAML đúng vì Python đọc được; hoá ra decoder yaml.v3 của Go từ chối chỉ báo thụt lề |4.
spine_turn_lines: ["omp:cd4449ab#L2719", "omp:cd4449ab#L2743"]
spine_action: Thử đổi |4 thành | trong đoạn YAML rồi decode lại.
spine_action_lines: ["omp:cd4449ab#L2744"]
spine_outcome: "Decode thành công với |, nhưng go test ./internal/migration vẫn đỏ với lỗi 'Canonical schema version is incompatible with this binary'."
spine_outcome_lines: ["omp:cd4449ab#L2746", "omp:cd4449ab#L2771"]
spine_takeaway: Đừng tự ghép YAML bằng chuỗi cho thứ sẽ được đọc lại; kiểm bằng đúng decoder mà code dùng.
spine_takeaway_lines: ["omp:cd4449ab#L2743"]
completeness: 7
---

# Migration v3 sang v4: block scalar YAML sai làm receipt WAL không đọc được

**Góc kể:** Dự án mcp-skill-hub đang được rút gọn qua nhiều phase, và người làm đang viết migration chuyển dữ liệu từ schema v3 sang v4. Họ kiểm chuỗi YAML bằng Python, thấy đọc được nên tin là đúng. Go decoder lại từ chối chỉ báo thụt lề |4; đổi thành | thì decode được, nhưng test migration vẫn đỏ vì một lỗi schema khác. Ai ghép YAML bằng chuỗi cho thứ sẽ được đọc lại nên kiểm bằng đúng decoder mà code dùng.
**Bối cảnh:** Migration v3 sang v4 ghi receipt WAL chứa nội dung file cũ dạng YAML lồng nhau. Test đỏ qua hơn chục lần chạy với lỗi 'proposed mutation is invalid'.
**Chuyện gì xảy ra:** Python yaml parse được chuỗi, nhưng decoder yaml.v3 của Go báo 'did not find expected key' ở dòng 1. Nguyên nhân là chỉ báo thụt lề |4 sai trong block scalar. Đổi thành | thì decode thành công và phần migration được tiếp tục.
**Bài học:** Đừng tự ghép YAML bằng chuỗi cho thứ sẽ được đọc lại. Dùng marshaller hoặc kiểm bằng đúng decoder mà code dùng.
**Artefact:** Đoạn YAML receipt trước và sau khi đổi |4 thành |, che nội dung.
