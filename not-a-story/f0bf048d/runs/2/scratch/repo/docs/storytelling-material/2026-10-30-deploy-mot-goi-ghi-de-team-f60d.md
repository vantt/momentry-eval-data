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
tension: nho_ma_to
sides: ["Chỉ deploy một gói Marketing, đọc plan phần Marketing", "Gói Coding nằm trong đó nên 3 agent bị ghi đè về bản cũ"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công ty phần mềm một người đang dựng đội AI agent gồm team coding và team marketing, và người làm muốn agent tự làm SEO và GA4 cho website của mình. Người làm tin deploy gói Marketing chỉ đụng phần Marketing, nhưng gói Coding nằm chung workspace nên lần deploy đầu tiên đưa 3 agent Coding về bản cũ. Điều đáng nghe: khi nhiều gói cùng trỏ vào một workspace, deploy có thể ghi đè âm thầm, nên phải đọc hết plan trước khi chạy."
audience: dev dựng hệ thống nhiều agent dùng chung một workspace
spine_context: "Một công ty phần mềm một người đang dựng đội AI agent gồm team coding và team marketing, và đang làm agent SEO và GA4 cho website của mình."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L897"]
spine_want: "Muốn có agent tự làm SEO, phân tích GA4 và đọc số liệu, thay vì để người làm tay."
spine_want_lines: ["claude:f0bf048d#L7"]
spine_obstacle: "Hai gói cùng deploy vào một workspace, nên deploy gói này có thể đè lên gói kia."
spine_obstacle_lines: ["claude:f0bf048d#L902"]
spine_turn: Tưởng deploy gói Marketing chỉ đụng phần Marketing; hoá ra gói Coding nằm chung workspace nên 3 agent Coding bị đưa về bản cũ.
spine_turn_lines: ["claude:f0bf048d#L902", "claude:f0bf048d#L915"]
spine_action: Deploy gói Marketing và bỏ qua các dòng ngoài phần Marketing trong plan; sau đó deploy lại gói Coding từ file gốc và xoá phần Coding khỏi gói Marketing.
spine_action_lines: ["claude:f0bf048d#L865", "claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915"]
spine_outcome: "Plan báo 0 thay đổi, 3 agent Coding trở lại; 3 agent SEO/GA4 chạy và gọi GA4 lấy được số liệu thật."
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: "Khi nhiều gói cùng chung một workspace, mỗi gói chỉ giữ phần của nó; đọc hết plan trước khi deploy."
spine_takeaway_lines: ["claude:f0bf048d#L902", "claude:f0bf048d#L915"]
completeness: 7
---

# Deploy một gói ghi đè team của gói khác trong cùng workspace

**Góc kể:** Một công ty phần mềm một người đang dựng đội AI agent gồm team coding và team marketing, và người làm muốn agent tự làm SEO và GA4 cho website của mình. Người làm tin deploy gói Marketing chỉ đụng phần Marketing, nhưng gói Coding nằm chung workspace nên lần deploy đầu tiên đưa 3 agent Coding về bản cũ. Điều đáng nghe: khi nhiều gói cùng trỏ vào một workspace, deploy có thể ghi đè âm thầm, nên phải đọc hết plan trước khi chạy.
**Bối cảnh:** Hai gói (một gói của phiên song song, một gói của mình) cùng deploy vào một workspace Multica. Gói của mình vẫn giữ bản cũ của team Coding.
**Chuyện gì xảy ra:** Lần deploy đầu tiên của gói mới đưa instructions, model và skill của 3 agent Coding về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow cho một project. Lúc đọc plan, agent bỏ qua các dòng ngoài phần Marketing. Sau đó deploy lại gói Coding từ file gốc, plan báo 0 thay đổi. Nguyên nhân gốc là gói Coding nằm sẵn trong gói Marketing. Deploy không xoá thực thể trên server nên các agent đang chạy không bị ảnh hưởng.
**Bài học:** Khi nhiều gói cùng trỏ vào một workspace thì mỗi gói chỉ được giữ đúng phần của nó, và phải đọc toàn bộ plan trước khi deploy.
**Artefact:** Bảng plan trước và sau deploy, đã che tên workspace và id.
**Góc người ngoài:** cách làm phổ biến là Thường cấu hình thẳng trên giao diện hoặc chạy script một lần, mỗi lần chỉnh thì sửa tay trên server và ít khi có bước xem trước thay đổi; ở đây khác ở Người dùng thường chỉ có một bộ cấu hình dùng chung. Ở đây mỗi khách có manifest riêng, deploy luôn chạy plan trước và kiểm lại, nên gói ghi đè team khác (K1) và cài nhầm workspace chỉ xảy ra một lần rồi được chặn bằng cơ chế.
