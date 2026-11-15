---
id: 2026-10-09-dung-vi-file-worktree-khac-nam
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L13", "omp:cd4449ab#L15", "omp:cd4449ab#L18", "omp:cd4449ab#L1342", "omp:cd4449ab#L1344", "omp:cd4449ab#L1363", "omp:cd4449ab#L1364", "omp:cd4449ab#L1376"]
hook: "Agent dừng vì file lạ, hoá ra file đó được phép sửa"
tension: cam_ma_van_lot
sides: ["Agent cẩn thận dừng khi thấy file đã sửa", "File thuộc worktree khác, vốn được phép, nên dừng là thừa"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dừng vì file worktree khác nằm trong checkout chung

**Bối cảnh:** Quy tắc ban đầu: trước mỗi commit, git status ở checkout chung phải chỉ có file prompt của mình.
**Chuyện gì xảy ra:** Agent dừng lần đầu vì checkout chung có telemetry_funnel.go đã sửa, do worktree khác làm. Lead trả lời các file đó thuộc worktree D, được phép làm ở checkout chung, không phải blocker. Quy tắc được đổi thành: chỉ dừng khi một file mình sở hữu xuất hiện trong danh sách.
**Bài học:** Kiểm tra 'bẩn' phải dựa trên quyền sở hữu file thay vì yêu cầu sạch tuyệt đối khi nhiều agent làm song song.
**Artefact:** Đầu ra git status, che tên file nếu cần.
**Góc người ngoài:** cách làm phổ biến là Nhiều người sẽ bỏ qua file lạ không liên quan hoặc tự stash, reset; ở đây khác ở Agent tách bạch file của mình với file của worktree khác, không đụng vào chúng, và báo cáo minh bạch. Đây là kỷ luật phối hợp nhiều agent trên cùng repo mà người đọc có thể áp dụng.
