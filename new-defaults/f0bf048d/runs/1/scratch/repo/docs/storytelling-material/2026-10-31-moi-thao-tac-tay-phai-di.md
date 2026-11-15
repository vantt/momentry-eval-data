---
id: 2026-10-31-moi-thao-tac-tay-phai-di
date: 2026-10-31
repo: repo
status: raw
signals: [người duyệt máy, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:f0bf048d#L1759", "claude:f0bf048d#L2814", "claude:f0bf048d#L3022", "claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3304", "claude:f0bf048d#L3320", "claude:f0bf048d#L3441"]
hook: "Mỗi thao tác tay phải vào skill rồi plan ra 0 thay đổi"
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

# Mỗi thao tác tay phải đi vào skill của System Operator, rồi deploy và kiểm plan

**Bối cảnh:** Người dùng yêu cầu: mọi bước làm tay đều phải dạy lại cho System Operator.
**Chuyện gì xảy ra:** Ghi quy tắc vào memory. Mỗi bước phải có phần hướng dẫn trong skill, deploy lại, và plan ra 0 thay đổi trước khi kết thúc. Giai đoạn 2 gồm 7 bước, mỗi bước nêu rõ người vận hành cần làm gì. Viết references/privileged.md liệt kê các lệnh sudo phải soạn sẵn, cùng quy trình nâng cấp có tóm tắt changelog và đường quay lại.
**Bài học:** Biến thao tác tay thành tài liệu cho agent vận hành ngay khi làm, không để sau.
**Artefact:** Bảng 7 bước của Giai đoạn 2, cột việc người vận hành cần làm.
**Góc người ngoài:** cách làm phổ biến là Làm tay xong thì thôi, hoặc ghi chú vào README mà agent không đọc; ở đây khác ở Tri thức vận hành nằm trong công cụ của agent, không nằm trong đầu người. Người đọc muốn biết cơ chế này và cách giữ nó đồng bộ.
