---
id: 2026-10-09-test-xanh-nhung-description-thanh-va-4257
code: M-8PEM
aliases: [M-8PEM]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1779", "omp:cd4449ab#L1872", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Test xanh hết, nhưng mô tả của skill thành đúng chuỗi '>-'"
tension: tuong_ma_hoa_ra
sides: ["Toàn bộ test xanh", "Description thành '>-' làm hỏng việc định tuyến"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang xây một hub các skill cho agent và chuẩn bị chuyển dữ liệu sang định dạng mới. Họ tin test xanh là đủ, vì báo cáo ghi make check xanh. Hoá ra test chỉ so với giá trị kỳ vọng nên bỏ lọt hai lỗi mà agent nhìn thấy: mô tả của một skill thành đúng chuỗi '>-', và tên bị đảo thứ tự. Đối chiếu đầu ra của lệnh trước và sau migration trên dữ liệu thật là cách bắt được lỗi giống người dùng gặp phải."
audience: dev viết migration hoặc refactor có test
spine_context: "Người làm đang phát triển một hub chứa các skill cho agent, và đang ở Phase 4 của đợt migration dữ liệu sang schema 3."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Migration phải chạy được trên hub thật, và đầu ra của lệnh skill show không đổi so với bản cũ."
spine_want_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713"]
spine_obstacle: Fixture test đã qua nhưng không bắt được hai regression nhìn thấy được ở đầu ra.
spine_obstacle_lines: ["omp:cd4449ab#L1713"]
spine_turn: Tưởng test xanh là đủ; hoá ra test chỉ so với giá trị kỳ vọng nên bỏ lọt description thành '>-' và tên bị đảo thứ tự.
spine_turn_lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713"]
spine_action: "Đổi sang parser YAML thật cho frontmatter, đặt lại thứ tự ưu tiên tên, và thêm test so sánh trước sau cho ba skill."
spine_action_lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1776"]
spine_outcome: Tên test-audit trước và sau migration đều là 'test-audit'.
spine_outcome_lines: ["omp:cd4449ab#L1890"]
spine_takeaway: "Với migration hay refactor, hãy so đầu ra thật của lệnh trên dữ liệu thật trước và sau, đừng chỉ tin test xanh."
spine_takeaway_lines: ["omp:cd4449ab#L1713"]
completeness: 7
---

# Test xanh nhưng description thành '>-' và thứ tự tên bị đảo

**Góc kể:** Người làm đang xây một hub các skill cho agent và chuẩn bị chuyển dữ liệu sang định dạng mới. Họ tin test xanh là đủ, vì báo cáo ghi make check xanh. Hoá ra test chỉ so với giá trị kỳ vọng nên bỏ lọt hai lỗi mà agent nhìn thấy: mô tả của một skill thành đúng chuỗi '>-', và tên bị đảo thứ tự. Đối chiếu đầu ra của lệnh trước và sau migration trên dữ liệu thật là cách bắt được lỗi giống người dùng gặp phải.
**Bối cảnh:** Fixture test thật đã pass, nhưng so sánh skill show --json trước và sau migration cho thấy hai regression mà test không bắt được.
**Chuyện gì xảy ra:** Một skill dùng block scalar YAML trong frontmatter, parser đọc từng dòng nên description thành đúng chuỗi '>-'. Resolver dùng description để định tuyến, nên đây là regression thật. Thứ tự tên cũng sai vì H1 đè lên name trong meta. Sau khi dùng parser YAML thật và đặt lại thứ tự ưu tiên, diff trước sau của name khớp nhau.
**Bài học:** Test chỉ so với giá trị kỳ vọng sẽ bỏ lọt lỗi. So sánh trước và sau trên đầu ra thật của lệnh là cách bắt regression giống người dùng.
**Artefact:** Diff JSON trước và sau của lệnh show, che tên skill và đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Đa số dev chỉ chạy test rồi tin kết quả; ít ai đối chiếu đầu ra thật của hai phiên bản trên dữ liệu thật; ở đây khác ở Test có thể xanh nhưng hiển thị sai. Đối chiếu đầu ra trực tiếp là cách bắt được lỗi như description thành '>-' mà test không thấy.
