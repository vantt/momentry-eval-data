---
id: 2026-10-30-deploy-goi-marketing-ghi-de-team-f60d
code: M-QCJ4
aliases: [M-QCJ4]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L903", "claude:f0bf048d#L915"]
hook: "Deploy gói marketing đưa 6 agent Coding về bản cũ"
tension: giup_ma_hai
sides: ["deploy để thêm bộ marketing", "6 agent Coding bị ghi đè, 3 agent bị gỡ khỏi squad"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công ty phần mềm một người đang dựng team marketing bằng agent AI, cần agent làm SEO, GA4 và Search Console. Lúc deploy, agent đọc plan nhưng bỏ qua các dòng ngoài phần marketing, tưởng chỉ đụng phần của mình. Hoá ra hai gói cùng deploy vào một workspace, và gói marketing còn giữ bản Coding cũ nên kéo ngược team Coding. Ai deploy nhiều gói vào chung một nơi cần đọc hết diff của plan trước khi áp dụng."
audience: "dev dùng agent AI, deploy nhiều gói cấu hình vào chung một workspace"
spine_context: "Một công ty phần mềm một người đang dựng team marketing bằng agent AI, cần agent làm SEO, GA4 và Search Console."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L897"]
spine_want: "Muốn có agent SEO và phân tích GA4, Search Console để làm marketing."
spine_want_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L675"]
spine_obstacle: "Hai gói cùng deploy vào một workspace, và gói marketing vẫn giữ bản Coding cũ."
spine_obstacle_lines: ["claude:f0bf048d#L902"]
spine_turn: Tưởng deploy gói marketing chỉ đụng phần marketing; hoá ra nó kéo ngược team Coding.
spine_turn_lines: ["claude:f0bf048d#L915"]
spine_action: "Deploy lại gói Coding từ file gốc, bỏ phần Coding khỏi gói marketing, rồi deploy 3 agent SEO và GA4."
spine_action_lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915"]
spine_outcome: Plan báo 0 thay đổi cho Coding; GA4 trả số liệu thật (kênh Direct 58 session trong 7 ngày); Search Console chưa có số liệu.
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: "Mỗi gói deploy chung workspace chỉ khai phần của nó, và phải đọc toàn bộ diff của plan trước khi áp dụng."
spine_takeaway_lines: ["claude:f0bf048d#L902", "claude:f0bf048d#L915"]
completeness: 7
---

# Deploy gói marketing ghi đè team Coding trong cùng workspace

**Góc kể:** Một công ty phần mềm một người đang dựng team marketing bằng agent AI, cần agent làm SEO, GA4 và Search Console. Lúc deploy, agent đọc plan nhưng bỏ qua các dòng ngoài phần marketing, tưởng chỉ đụng phần của mình. Hoá ra hai gói cùng deploy vào một workspace, và gói marketing còn giữ bản Coding cũ nên kéo ngược team Coding. Ai deploy nhiều gói vào chung một nơi cần đọc hết diff của plan trước khi áp dụng.
**Bối cảnh:** Hai gói cùng deploy vào một workspace Multica. Gói marketing vẫn giữ bản cũ của phần Coding, nên deploy gói marketing kéo ngược phần Coding.
**Chuyện gì xảy ra:** Agent đã đọc plan nhưng bỏ qua các dòng ngoài phần marketing. Lần deploy đầu tiên đưa 6 agent Coding về bản cũ, gỡ 3 agent khỏi squad Coding và gắn sai workflow cho một project. Agent khôi phục bằng cách deploy lại từ gói gốc của phiên kia, plan báo 0 thay đổi. Sau đó xoá phần Coding khỏi gói marketing (commit 0c4d9ce). Deploy không xoá thực thể trên server nên agent đang chạy không bị ảnh hưởng.
**Bài học:** Khi nhiều gói cùng deploy vào một workspace, mỗi gói chỉ được khai phần của nó. Đọc toàn bộ diff của plan trước khi deploy, không chỉ phần mình quan tâm.
**Artefact:** Bảng plan trước và sau khi khôi phục, dòng ~ + - (che tên workspace và ID).
