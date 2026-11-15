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
hook: "Deploy gói mới âm thầm đưa 3 agent Coding về bản cũ"
tension: nho_ma_to
sides: ["Plan đọc xong, chỉ nhìn phần Marketing", "Gói Coding nằm sẵn trong gói Marketing, bị ghi đè về bản cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công ty phần mềm chỉ có một người, dùng nhiều AI agent trên Multica, đang muốn team marketing có agent làm SEO và đọc số liệu GA4. Khi deploy gói Marketing, người làm tin rằng lệnh chỉ đụng phần Marketing. Hoá ra gói Coding cũ nằm trong cùng workspace, nên deploy đã đưa các agent Coding về bản cũ và gỡ chúng khỏi squad. Ai có nhiều gói cấu hình trỏ vào một workspace nên đọc toàn bộ plan trước khi deploy."
audience: dev dùng nhiều AI agent và quản lý cấu hình nhiều gói
spine_context: "Một công ty phần mềm chỉ có một người, dùng nhiều AI agent trên Multica, đang muốn team marketing có agent làm SEO và đọc số liệu GA4."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L920"]
spine_want: "Muốn có agent SEO và GA4 trong team marketing, chạy được trên site của khách."
spine_want_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L675"]
spine_obstacle: Search Console chưa có số liệu vì quyền được cấp nhầm property.
spine_obstacle_lines: ["claude:f0bf048d#L915"]
spine_turn: Tưởng deploy gói Marketing chỉ đụng phần Marketing; hoá ra gói Coding cũ nằm trong cùng workspace và bị ghi đè về bản cũ.
spine_turn_lines: ["claude:f0bf048d#L902", "claude:f0bf048d#L915"]
spine_action: "Deploy lại gói Coding từ file gốc, bỏ phần Coding khỏi gói Marketing, rồi deploy 3 agent SEO và GA4."
spine_action_lines: ["claude:f0bf048d#L865", "claude:f0bf048d#L896", "claude:f0bf048d#L915"]
spine_outcome: "Plan Coding về 0 thay đổi; GA4 trả số liệu thật, kênh Direct có 58 session trong 7 ngày; Search Console vẫn chưa có số liệu."
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: "Khi nhiều gói cùng trỏ vào một workspace, mỗi gói chỉ giữ phần của nó; đọc toàn bộ plan trước khi deploy."
spine_takeaway_lines: ["claude:f0bf048d#L902"]
completeness: 7
---

# Deploy một gói ghi đè team của gói khác trong cùng workspace

**Góc kể:** Một công ty phần mềm chỉ có một người, dùng nhiều AI agent trên Multica, đang muốn team marketing có agent làm SEO và đọc số liệu GA4. Khi deploy gói Marketing, người làm tin rằng lệnh chỉ đụng phần Marketing. Hoá ra gói Coding cũ nằm trong cùng workspace, nên deploy đã đưa các agent Coding về bản cũ và gỡ chúng khỏi squad. Ai có nhiều gói cấu hình trỏ vào một workspace nên đọc toàn bộ plan trước khi deploy.
**Bối cảnh:** Hai gói (một gói của phiên song song, một gói của mình) cùng deploy vào một workspace Multica. Gói của mình vẫn giữ bản cũ của team Coding.
**Chuyện gì xảy ra:** Lần deploy đầu tiên của gói mới đưa instructions, model và skill của 3 agent Coding về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow cho một project. Lúc đọc plan, agent bỏ qua các dòng ngoài phần Marketing. Sau đó deploy lại gói Coding từ file gốc, plan báo 0 thay đổi. Nguyên nhân gốc là gói Coding nằm sẵn trong gói Marketing. Deploy không xoá thực thể trên server nên các agent đang chạy không bị ảnh hưởng.
**Bài học:** Khi nhiều gói cùng trỏ vào một workspace thì mỗi gói chỉ được giữ đúng phần của nó, và phải đọc toàn bộ plan trước khi deploy.
**Artefact:** Bảng plan trước và sau deploy, đã che tên workspace và id.
**Góc người ngoài:** cách làm phổ biến là Thường cấu hình thẳng trên giao diện hoặc chạy script một lần, mỗi lần chỉnh thì sửa tay trên server và ít khi có bước xem trước thay đổi; ở đây khác ở Người dùng thường chỉ có một bộ cấu hình dùng chung. Ở đây mỗi khách có manifest riêng, deploy luôn chạy plan trước và kiểm lại, nên gói ghi đè team khác (K1) và cài nhầm workspace chỉ xảy ra một lần rồi được chặn bằng cơ chế.
