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
hook: "Cắt 46% chữ, rule vẫn lên 230, rồi chính installer mẫu vi phạm rule"
tension: giup_ma_hai
sides: ["Rút gọn skill để gọn và nhất quán hơn", "Agent review vẫn thấy lệnh mâu thuẫn và installer mẫu vi phạm chính rule của nó"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Chủ đang xây một bộ hướng dẫn phân phối (đóng gói, cài, cập nhật, cấu hình, doctor) để agent dùng lại trên nhiều dự án. Bản đầu tưởng đã ổn vì script kiểm tra cấu trúc đều chạy qua, nhưng một agent review độc lập chỉ ra cùng một việc được ghi bằng hai lệnh khác nhau. Kiểm tra cấu trúc không bắt được lỗi nội dung kiểu này, mà chính lỗi đó sẽ khiến agent dựng ra CLI khác nhau ở mỗi dự án."
audience: dev làm công cụ dòng lệnh và viết hướng dẫn cho agent AI
spine_context: "Chủ đang gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của nhiều dự án thành một skill để agent dùng lại."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: Muốn mỗi dự án mới chỉ cần gọi agent dùng skill là có đủ hướng dẫn phân phối.
spine_want_lines: ["claude:6a207191#L5"]
spine_obstacle: "Bản đầu quá dài và dư thừa chữ, cần rút gọn."
spine_obstacle_lines: ["claude:6a207191#L319"]
spine_turn: "Tưởng skill đã nhất quán vì script kiểm tra cấu trúc chạy qua; hoá ra cùng một việc được ghi bằng hai lệnh khác nhau: có chỗ bảo gọi setup, có chỗ bảo không có lệnh setup."
spine_turn_lines: ["claude:6a207191#L657", "claude:6a207191#L681"]
spine_action: "Chuẩn hoá lại: init là lệnh khởi đầu duy nhất, setup chỉ còn là alias ẩn, rồi sửa các điểm review."
spine_action_lines: ["claude:6a207191#L690", "claude:6a207191#L897"]
spine_outcome: "Script kiểm tra chạy qua với 212 rule, và mọi đường dẫn code mẫu đều có thật trên GitHub."
spine_outcome_lines: ["claude:6a207191#L892", "claude:6a207191#L897"]
spine_takeaway: "Kiểm tra cấu trúc chỉ biết format đúng, không biết hai quy tắc có mâu thuẫn; cần một reviewer đọc các quy tắc cùng lúc để bắt lỗi nội dung."
spine_takeaway_lines: ["claude:6a207191#L681"]
completeness: 7
---

# Một skill packaging ban đầu 212 rule, dư thừa 46% chữ, và phải viết lại theo tầng ưu tiên UX

**Góc kể:** Chủ đang xây một bộ hướng dẫn phân phối (đóng gói, cài, cập nhật, cấu hình, doctor) để agent dùng lại trên nhiều dự án. Bản đầu tưởng đã ổn vì script kiểm tra cấu trúc đều chạy qua, nhưng một agent review độc lập chỉ ra cùng một việc được ghi bằng hai lệnh khác nhau. Kiểm tra cấu trúc không bắt được lỗi nội dung kiểu này, mà chính lỗi đó sẽ khiến agent dựng ra CLI khác nhau ở mỗi dự án.
**Bối cảnh:** Chủ muốn gom cách đóng gói, cài đặt, cập nhật, cấu hình và doctor của 4 dự án thành một skill tái dùng. Agent soạn bản đầu rất dài, chủ phản hồi là dư thừa, rồi hướng dẫn dần về UX và agent-native.
**Chuyện gì xảy ra:** Bản đầu có khoảng 11.900 từ và 183 rule. Sau lần rút gọn đầu, còn khoảng 6.400 từ (−46%), rule chuyển sang một dòng. Qua các vòng chủ góp ý, số rule lên 230 rồi chuốt về 212, và tầng ưu tiên UX → an toàn → đúng đắn → nhanh được đưa lên đầu. Một agent review độc lập chỉ ra các lệnh mâu thuẫn nhau (setup vs init) và installer mẫu vi phạm chính rule của nó.
**Bài học:** Viết guide cho agent: mỗi ý chỉ được có một chỗ chứa, và phải có thứ tự ưu tiên rõ ngay đầu file, nếu không agent sẽ tạo ra các CLI khác nhau ở mỗi dự án.
**Artefact:** Bảng so số từ trước/sau (11.900 → 6.400) và cây thư mục skill; che đường dẫn máy và địa chỉ hub.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev làm việc này theo kiểu ghi chú rải rác trong README hoặc wiki từng repo, mỗi dự án tự quyết định cách cài và cập nhật; không có chuẩn chung, và kinh nghiệm từ dự án cũ thường không được đưa sang dự án mới; ở đây khác ở Ở đây kinh nghiệm được chưng cất thành các quy tắc có ID, có lý do và có chỉ dẫn 'dùng lại code mẫu đã chạy tốt', nên agent khi làm dự án mới không phải tự thiết kế lại từ đầu. Người đọc sẽ muốn biết cách tổ chức để một tập quy tắc có thể mở rộng mà không phình ra, vì đây là điều họ thường bỏ dở.
