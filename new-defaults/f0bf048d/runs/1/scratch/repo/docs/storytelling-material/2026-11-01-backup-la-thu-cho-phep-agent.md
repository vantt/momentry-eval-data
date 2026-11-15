---
id: 2026-11-01-backup-la-thu-cho-phep-agent
date: 2026-11-01
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L2606"]
hook: "Agent chỉ dám tự làm khi có backup ngoài máy mà nó không xoá được"
tension: khac
sides: ["việc đảo ngược được thì khỏi hỏi", "không có backup, mọi việc thành nút thắt chờ người"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Backup là thứ cho phép agent tự làm: việc đảo ngược được thì không cần hỏi

**Bối cảnh:** Sau khi người vận hành hỏi mục tiêu của backup.
**Chuyện gì xảy ra:** Thiết kế phân loại việc theo tiêu chí đảo ngược được. Nếu có backup thì agent làm không cần hỏi; nếu không thì phải hỏi người. Không có backup, mọi việc sửa cấu hình, deploy lại, xoá issue đều thành nút thắt. Backup phải nằm ngoài máy, agent không được xoá, và phải diễn tập khôi phục.
**Bài học:** Đo số việc agent phải hỏi người trước và sau khi có backup; đó là thước đo thật của backup.
**Artefact:** Bảng phân loại việc theo đảo ngược được.
**Góc người ngoài:** cách làm phổ biến là Hoặc hỏi mọi thứ, hoặc để agent làm hết mà không có lưới an toàn; ở đây khác ở Ranh giới 'đảo ngược được hay không' do backup quyết định. Người đọc muốn biết cách đưa ra quy tắc này và vì sao backup mỗi giờ bị bỏ.
