---
id: 2026-10-09-agent-tach-mot-loi-lon-thanh
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1377", "omp:cd4449ab#L1388", "omp:cd4449ab#L1397", "omp:cd4449ab#L1409", "omp:cd4449ab#L2110", "omp:cd4449ab#L2352", "omp:cd4449ab#L2963", "omp:cd4449ab#L3368", "omp:cd4449ab#L3957"]
hook: "Một lỗi lớn tách thành nhiều commit nhỏ, mỗi cái đều xanh"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tách một lỗi lớn thành nhiều commit nhỏ theo quy ước conventional commit, mỗi commit có make check xanh, và báo cáo hash sau mỗi bước.

**Chuyện gì xảy ra:** Agent tách một lỗi lớn thành nhiều commit nhỏ theo quy ước conventional commit, mỗi commit có make check xanh, và báo cáo hash sau mỗi bước.
**Góc người ngoài:** cách làm phổ biến là Dev thường gom nhiều thay đổi thành một commit lớn 'wip' hoặc 'fix' khi kết thúc việc, khó review và khó rollback; ở đây khác ở Commit nhỏ, có nghĩa, kiểm tra xanh từng bước giúp lead có thể merge từng checkpoint. Người đọc muốn biết cách chia commit khi làm việc dài.
