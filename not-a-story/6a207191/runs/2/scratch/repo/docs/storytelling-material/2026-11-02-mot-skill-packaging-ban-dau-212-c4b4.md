---
id: 2026-11-02-mot-skill-packaging-ban-dau-212-c4b4
code: M-R2XJ
aliases: [M-R2XJ]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L319", "claude:6a207191#L339", "claude:6a207191#L545", "claude:6a207191#L578", "claude:6a207191#L636", "claude:6a207191#L661", "claude:6a207191#L675", "claude:6a207191#L690", "claude:6a207191#L701", "claude:6a207191#L897"]
hook: "Rút 46% chữ, rồi ba vòng góp ý đẩy rule từ 183 lên 230"
tension: giup_ma_hai
sides: ["Rút gọn 46% để skill gọn hơn", "Các vòng góp ý lại làm rule phình lên 230, và còn lệnh mâu thuẫn nhau"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của nhiều dự án CLI thành một skill cho agent dùng lại. Bản đầu qua được kiểm tra cấu trúc và thử cài đặt, nên họ tin là xong. Một agent khác đọc độc lập thì thấy hai lệnh mâu thuẫn nhau (setup và init), và installer mẫu lại vi phạm chính các quy tắc của nó. Ai viết hướng dẫn cho agent nên biết: kiểm tra cấu trúc chỉ bắt lỗi hình thức, còn lỗi nhất quán phải có một lượt đọc độc lập."
audience: dev viết hướng dẫn hoặc skill cho agent
spine_context: "Người làm đang gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của nhiều dự án CLI thành một skill cho agent dùng lại."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: Muốn có một bộ chuẩn để agent làm được việc này cho mọi dự án mới.
spine_want_lines: ["claude:6a207191#L5"]
spine_obstacle: Bản đầu quá dài và có nhiều rule dư thừa.
spine_obstacle_lines: ["claude:6a207191#L319"]
spine_turn: "Tưởng đã xong vì script kiểm tra cấu trúc và thử cài đặt đều đạt; hoá ra hai lệnh mâu thuẫn nhau (setup và init), và installer mẫu lại vi phạm chính các quy tắc của nó."
spine_turn_lines: ["claude:6a207191#L317", "claude:6a207191#L690"]
spine_action: "Giao một agent khác đọc độc lập toàn bộ skill, rồi sửa theo kết quả review."
spine_action_lines: ["claude:6a207191#L675"]
spine_outcome: Số rule từ 230 còn 212; mâu thuẫn về lệnh được sửa và installer mẫu được test lại.
spine_outcome_lines: ["claude:6a207191#L657", "claude:6a207191#L897"]
spine_takeaway: Kiểm tra cấu trúc chỉ bắt được lỗi hình thức; cần một lượt đọc độc lập để bắt lỗi nhất quán giữa các tài liệu.
spine_takeaway_lines: ["claude:6a207191#L690"]
completeness: 7
---

# Một skill packaging ban đầu 212 rule, dư thừa 46% chữ, và phải viết lại theo tầng ưu tiên UX

**Góc kể:** Người làm đang gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của nhiều dự án CLI thành một skill cho agent dùng lại. Bản đầu qua được kiểm tra cấu trúc và thử cài đặt, nên họ tin là xong. Một agent khác đọc độc lập thì thấy hai lệnh mâu thuẫn nhau (setup và init), và installer mẫu lại vi phạm chính các quy tắc của nó. Ai viết hướng dẫn cho agent nên biết: kiểm tra cấu trúc chỉ bắt lỗi hình thức, còn lỗi nhất quán phải có một lượt đọc độc lập.
**Bối cảnh:** Chủ muốn gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của 4 dự án thành một skill tái dùng. Agent soạn bản đầu rất dài, chủ phản hồi là dư thừa, rồi hướng dẫn dần về UX và agent-native.
**Chuyện gì xảy ra:** Bản đầu có khoảng 11.900 từ và 183 rule. Sau lần rút gọn đầu, còn khoảng 6.400 từ (−46%), rule chuyển sang một dòng. Qua các vòng chủ góp ý, số rule lên 230 rồi chuốt về 212, và tầng ưu tiên UX → an toàn → đúng đắn → nhanh được đưa lên đầu. Một agent review độc lập chỉ ra các lệnh mâu thuẫn nhau (setup vs init) và installer mẫu vi phạm chính rule của nó.
**Bài học:** Viết guide cho agent: mỗi ý chỉ được có một chỗ chứa, và phải có thứ tự ưu tiên rõ ngay đầu file, nếu không agent sẽ tạo ra các CLI khác nhau ở mỗi dự án.
**Artefact:** Bảng so số từ trước/sau (11.900 → 6.400) và cây thư mục skill; che đường dẫn máy và địa chỉ hub.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev làm việc này theo kiểu ghi chú rải rác trong README hoặc wiki từng repo, mỗi dự án tự quyết định cách cài và cập nhật; không có chuẩn chung, và kinh nghiệm từ dự án cũ thường không được đưa sang dự án mới; ở đây khác ở Ở đây kinh nghiệm được chưng cất thành các quy tắc có ID, có lý do và có chỉ dẫn 'dùng lại code mẫu đã chạy tốt', nên agent khi làm dự án mới không phải tự thiết kế lại từ đầu. Người đọc sẽ muốn biết cách tổ chức để một tập quy tắc có thể mở rộng mà không phình ra, vì đây là điều họ thường bỏ dở.
