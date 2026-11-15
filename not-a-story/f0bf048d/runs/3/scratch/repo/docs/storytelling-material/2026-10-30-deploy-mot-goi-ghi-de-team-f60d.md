---
id: 2026-10-30-deploy-mot-goi-ghi-de-team-f60d
code: M-6CCS
aliases: [M-6CCS]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:f0bf048d#L865", "claude:f0bf048d#L868", "claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L904", "claude:f0bf048d#L915", "claude:f0bf048d#L1158"]
hook: "Deploy gói mới lặng lẽ đưa 3 agent Coding về bản cũ"
tension: giup_ma_hai
sides: ["Deploy gói Marketing mới, plan chỉ đọc phần Marketing", "Gói Coding nằm sẵn bên trong, nên 3 agent bị đưa về bản cũ và gắn sai workflow"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Deploy một gói ghi đè team của gói khác trong cùng workspace

**Bối cảnh:** Hai gói (một gói của phiên song song, một gói của mình) cùng deploy vào một workspace Multica. Gói của mình vẫn giữ bản cũ của team Coding.
**Chuyện gì xảy ra:** Lần deploy đầu tiên của gói mới đưa instructions, model và skill của 3 agent Coding về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow cho một project. Lúc đọc plan, agent bỏ qua các dòng ngoài phần Marketing. Sau đó deploy lại gói Coding từ file gốc, plan báo 0 thay đổi. Nguyên nhân gốc là gói Coding nằm sẵn trong gói Marketing. Deploy không xoá thực thể trên server nên các agent đang chạy không bị ảnh hưởng.
**Bài học:** Khi nhiều gói cùng trỏ vào một workspace thì mỗi gói chỉ được giữ đúng phần của nó, và phải đọc toàn bộ plan trước khi deploy.
**Artefact:** Bảng plan trước và sau deploy, đã che tên workspace và id.
**Góc người ngoài:** cách làm phổ biến là Thường cấu hình thẳng trên giao diện hoặc chạy script một lần, mỗi lần chỉnh thì sửa tay trên server và ít khi có bước xem trước thay đổi; ở đây khác ở Người dùng thường chỉ có một bộ cấu hình dùng chung. Ở đây mỗi khách có manifest riêng, deploy luôn chạy plan trước và kiểm lại, nên gói ghi đè team khác (K1) và cài nhầm workspace chỉ xảy ra một lần rồi được chặn bằng cơ chế.
