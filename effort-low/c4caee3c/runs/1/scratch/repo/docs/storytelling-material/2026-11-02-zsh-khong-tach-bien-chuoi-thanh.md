---
id: 2026-11-02-zsh-khong-tach-bien-chuoi-thanh
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L3520"]
hook: "File có thật, git vẫn báo không tồn tại vì zsh không tách chuỗi"
tension: tuong_ma_hoa_ra
sides: ["Lệnh đúng, file có thật", "zsh đưa cả chuỗi thành một đường dẫn duy nhất"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh không tách biến chuỗi thành mảng

**Bối cảnh:** Agent định chạy git diff trên danh sách file lưu trong một biến chuỗi có khoảng trắng.
**Chuyện gì xảy ra:** Trong zsh, biến chuỗi chứa nhiều đường dẫn không tự tách thành từng phần khi truyền cho lệnh. Git đọc cả chuỗi như một đường dẫn duy nhất và báo pathspec không tồn tại, nên lệnh thất bại dù file có thật. Sửa bằng cách khai báo mảng.
**Bài học:** Trong zsh khai báo danh sách file dưới dạng mảng, đừng dùng chuỗi có khoảng trắng.
**Artefact:** Dòng lệnh trước và sau khi sửa. Không cần che.
