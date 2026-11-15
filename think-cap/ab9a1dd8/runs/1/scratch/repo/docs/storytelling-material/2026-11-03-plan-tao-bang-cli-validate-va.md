---
id: 2026-11-03-plan-tao-bang-cli-validate-va
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L558", "claude:ab9a1dd8#L561", "claude:ab9a1dd8#L565", "claude:ab9a1dd8#L569"]
hook: "Plan hợp lệ, nhưng danh sách số phải đổi thành checkbox bằng awk"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Plan tạo bằng CLI: validate và checkbox tự chuyển từ danh sách số

**Bối cảnh:** Plan của packaging được tạo bằng ak plan create, với tám phase.
**Chuyện gì xảy ra:** ak plan validate báo hợp lệ. Các mục việc viết dạng danh sách số được đổi thành checkbox bằng một đoạn awk, và đếm cho ra 8 và 6 checkbox theo phase.
**Bài học:** Dùng CLI của plan để kiểm cấu trúc, và đổi định dạng bằng công cụ thay vì sửa tay.
**Artefact:** Đầu ra ak plan validate và ak plan status.
