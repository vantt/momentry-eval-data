---
id: 2026-11-05-hoc-quy-tac-config-mot-cua
date: 2026-11-05
repo: repo
status: raw
signals: [khác, "số trước, số sau"]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2264", "claude:6a207191#L2294", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2349", "claude:6a207191#L2358", "claude:6a207191#L2385", "claude:6a207191#L2393", "claude:6a207191#L2407"]
hook: "Học quy tắc 'config một cửa' từ commit chưa phát hành"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Học quy tắc 'config một cửa' từ project khác: thêm 3 rule, nâng CFG-12 lên MUST

**Bối cảnh:** Project momentry thêm quy tắc mới trong cùng ngày: mọi cài đặt đổi qua lệnh config, kể cả cài đặt riêng từng dự án.
**Chuyện gì xảy ra:** Agent đọc commit và tài liệu của momentry, rồi so sáu ý với skill. Skill có các mảnh rời như thứ tự ưu tiên CFG-04, config explain UX-12, set/unset UX-14 nhưng thiếu quy tắc 'một cửa'. Agent thêm CMD-22 đến CMD-24 (một cửa, phạm vi --project và --repo, không tự bật dự án), nâng CFG-12 từ MAY lên MUST, và thêm UX-17 để giao diện gọi cùng hàm ghi. Số rule từ 212 lên 215. Commit bên momentry chưa nằm trong bản phát hành nào nên agent ghi chú đây là cách làm chưa được chứng minh.
**Bài học:** Khi đưa cách làm từ project khác vào chuẩn chung, phân biệt 'đã có test' với 'đã phát hành' và ghi nhãn mức tin cậy ngay trong tài liệu.
**Artefact:** Bảng đối chiếu sáu ý: ý của project khác, skill trước đó có gì, và đánh giá.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng tự sửa file hướng dẫn, hoặc để AI sửa xong mà không có bước kiểm tra cấu trúc và đường dẫn trước khi chia sẻ; ở đây khác ở Mỗi bài học mới đi qua cùng một quy trình có kiểm tra máy móc, nên tài liệu tích lũy không bị lệch hay gãy link. Người đọc sẽ muốn biết cách làm để kiến thức từ nhiều project không thành một đống ghi chú rời.
