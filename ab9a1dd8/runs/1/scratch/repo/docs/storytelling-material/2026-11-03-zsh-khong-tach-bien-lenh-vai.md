---
id: 2026-11-03-zsh-khong-tach-bien-lenh-vai
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L105", "claude:ab9a1dd8#L109", "claude:ab9a1dd8#L1199", "claude:ab9a1dd8#L1226", "claude:ab9a1dd8#L3770", "claude:ab9a1dd8#L3884", "claude:ab9a1dd8#L3891"]
hook: "Bốn lần zsh hiểu sai KEY=value, lỗi không nằm ở sản phẩm"
tension: khac
sides: ["Lệnh đúng, sản phẩm đúng", "zsh báo no such file, tốn nhiều lượt chạy"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh không tách biến lệnh: vài lần no such file và glob không khớp

**Bối cảnh:** Shell tương tác của user là zsh, còn các lệnh kiểm thử được viết theo kiểu bash.
**Chuyện gì xảy ra:** Ít nhất bốn lần lệnh có biến KEY=value bị zsh hiểu sai và báo no such file. Một glob không khớp trong zsh báo no matches found và thoát 1. Agent chuyển sang bash -c hoặc script .sh. Các lỗi này không phải lỗi sản phẩm nhưng tốn nhiều lượt chạy.
**Bài học:** Đặt script kiểm thử trong bash -c hoặc file .sh, đừng dựa vào shell tương tác của user.
**Artefact:** Dòng zsh no matches found trong output.
