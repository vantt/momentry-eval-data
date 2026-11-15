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
sides: ["Test xanh nên tưởng không có lỗi", "Description thành '>-' và làm hỏng việc định tuyến skill"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ quản lý skill cho agent AI đang chuyển dữ liệu của hub thật sang định dạng mới trước khi merge. Người làm tin rằng fixture test đã xanh và báo cáo đã kiểm đủ sáu mục thì migration giữ nguyên nội dung skill. Khi so sánh đầu ra lệnh show trước và sau, description của một skill thành đúng hai ký tự '>-' và thứ tự tên bị đảo, dù test vẫn xanh. Ai làm công cụ có migration dữ liệu nên biết rằng test kiểm giá trị kỳ vọng có thể bỏ sót lỗi hiển thị."
audience: dev làm công cụ có migration dữ liệu và test fixture
spine_context: "Một công cụ quản lý skill cho agent AI, có workspace và các bước migration; người làm đang đưa phase 4 qua review trước khi merge."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1713"]
spine_want: Muốn migration chạy được trên bản sao hub thật.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Migration thật lỗi ở bước v1 sang v2 vì .meta/** bị kiểm tra như một entity.
spine_obstacle_lines: ["omp:cd4449ab#L1462"]
spine_turn: "Tưởng fixture test đã xanh và sáu mục review đều đã kiểm, nên migration giữ nguyên nội dung skill. Hoá ra so sánh đầu ra show trước và sau cho thấy description thành '>-' và tên bị đảo thứ tự, test không bắt được."
spine_turn_lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713"]
spine_action: Viết lại fixture test và đọc lại logic gộp routing trong migration v3 để tìm nguyên nhân.
spine_action_lines: ["omp:cd4449ab#L1714", "omp:cd4449ab#L1776", "omp:cd4449ab#L1780"]
spine_outcome: "Với test-audit, tên trước và sau migration đều là 'test-audit'. Các skill còn lại và phần diff đầy đủ chưa được xác nhận trong đoạn này."
spine_outcome_lines: ["omp:cd4449ab#L1890"]
spine_takeaway: "Test xanh chỉ chứng minh những gì test kiểm tra. Để bắt lỗi hiển thị, hãy so sánh đầu ra thật của hai phiên bản trên dữ liệu thật."
spine_takeaway_lines: ["omp:cd4449ab#L1713"]
completeness: 7
---

# Test xanh nhưng description thành '>-' và thứ tự tên bị đảo

**Góc kể:** Một công cụ quản lý skill cho agent AI đang chuyển dữ liệu của hub thật sang định dạng mới trước khi merge. Người làm tin rằng fixture test đã xanh và báo cáo đã kiểm đủ sáu mục thì migration giữ nguyên nội dung skill. Khi so sánh đầu ra lệnh show trước và sau, description của một skill thành đúng hai ký tự '>-' và thứ tự tên bị đảo, dù test vẫn xanh. Ai làm công cụ có migration dữ liệu nên biết rằng test kiểm giá trị kỳ vọng có thể bỏ sót lỗi hiển thị.
**Bối cảnh:** Fixture test thật đã pass, nhưng so sánh skill show --json trước và sau migration cho thấy hai regression mà test không bắt được.
**Chuyện gì xảy ra:** Một skill dùng block scalar YAML trong frontmatter, parser đọc từng dòng nên description thành đúng chuỗi '>-'. Resolver dùng description để định tuyến, nên đây là regression thật. Thứ tự tên cũng sai vì H1 đè lên name trong meta. Sau khi dùng parser YAML thật và đặt lại thứ tự ưu tiên, diff trước sau của name khớp nhau.
**Bài học:** Test chỉ so với giá trị kỳ vọng sẽ bỏ lọt lỗi. So sánh trước và sau trên đầu ra thật của lệnh là cách bắt regression giống người dùng.
**Artefact:** Diff JSON trước và sau của lệnh show, che tên skill và đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Đa số dev chỉ chạy test rồi tin kết quả; ít ai đối chiếu đầu ra thật của hai phiên bản trên dữ liệu thật; ở đây khác ở Test có thể xanh nhưng hiển thị sai. Đối chiếu đầu ra trực tiếp là cách bắt được lỗi như description thành '>-' mà test không thấy.
