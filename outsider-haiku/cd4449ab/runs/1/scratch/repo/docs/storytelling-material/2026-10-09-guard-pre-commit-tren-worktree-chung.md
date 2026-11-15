---
id: 2026-10-09-guard-pre-commit-tren-worktree-chung
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1364", "omp:cd4449ab#L1694", "omp:cd4449ab#L1728", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345", "omp:cd4449ab#L2374"]
hook: "Quy tắc 'git status phải sạch' khiến agent dừng 3 lần vì file của người khác"
tension: giup_ma_hai
sides: ["quy tắc an toàn: worktree phải sạch", "agent dừng vì file không phải của mình"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Guard pre-commit trên worktree chung: dừng vì file không phải của mình

**Bối cảnh:** Nhiều worktree dùng chung một main checkout.
**Chuyện gì xảy ra:** Quy tắc 'git status phải sạch' khiến agent dừng ba lần vì có file của worktree khác và file prompt untracked trong main checkout. Lead nới rule: chỉ dừng khi file của chính mình xuất hiện. Một lệnh go run từ worktree trỏ module ngoài bị từ chối 'outside main module', phải dùng go -C để build.
**Bài học:** Guard cho môi trường nhiều agent nên hỏi 'file của tôi có bị đụng không' thay vì 'repo có sạch không'.
**Artefact:** Đầu ra git status của hai checkout, che tên file.
**Góc người ngoài:** cách làm phổ biến là Dev thường bỏ qua file lạ không thuộc mình rồi commit tiếp, hoặc stash/reset để dọn cho sạch; ở đây khác ở Agent không tự ý xử lý file của người khác; báo cáo đúng nguyên nhân và chờ. Người đọc sẽ hỏi làm sao tách công việc song song nhiều agent trên cùng một repo mà không giẫm chân nhau.
