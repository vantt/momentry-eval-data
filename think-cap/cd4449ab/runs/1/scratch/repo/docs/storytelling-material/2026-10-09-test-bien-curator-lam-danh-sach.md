---
id: 2026-10-09-test-bien-curator-lam-danh-sach
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1928", "omp:cd4449ab#L1933", "omp:cd4449ab#L1943", "omp:cd4449ab#L1955", "omp:cd4449ab#L1958", "omp:cd4449ab#L3377", "omp:cd4449ab#L3488", "omp:cd4449ab#L3493", "omp:cd4449ab#L3500", "omp:cd4449ab#L3518", "omp:cd4449ab#L3595", "omp:cd4449ab#L3596", "omp:cd4449ab#L3614", "omp:cd4449ab#L3616", "omp:cd4449ab#L3617", "omp:cd4449ab#L3620", "omp:cd4449ab#L3622"]
hook: "Test đỏ 5 lần liên tiếp, và chính nó viết to-do cho agent"
tension: giup_ma_hai
sides: ["Test đỏ là tín hiệu lỗi", "Test đỏ lại thành danh sách việc cần làm"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test biên curator làm danh sách việc khi cắt tool

**Bối cảnh:** Test biên curator viết trước để giữ danh sách tool tương thích của vai trò curator.
**Chuyện gì xảy ra:** Test đỏ ở mỗi lần xoá tool, khoảng 4 đến 5 lượt. Mỗi lần test in ra tool còn thiếu hoặc còn thừa, nên danh sách đó trở thành to-do. Bản SKILL.md của curator có hai bản giống nhau, sau mỗi lần sửa phải cp sang bản thứ hai. Dòng O8 từ worktree D được thêm vào thân skill.
**Bài học:** Viết test biên trước để làm danh sách việc; giữ hai bản copy của một file bằng một lệnh cp có kiểm tra.
**Artefact:** Đầu ra test liệt kê tool thiếu và thừa, che nội dung skill.
