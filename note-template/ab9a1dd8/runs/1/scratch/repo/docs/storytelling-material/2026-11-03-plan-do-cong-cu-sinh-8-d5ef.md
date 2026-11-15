---
id: 2026-11-03-plan-do-cong-cu-sinh-8-d5ef
code: M-MTBS
aliases: [M-MTBS]
date: 2026-11-03
repo: repo
status: raw
signals: [artefact_nhin_duoc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L411", "claude:ab9a1dd8#L439", "claude:ab9a1dd8#L558", "claude:ab9a1dd8#L565", "claude:ab9a1dd8#L569"]
hook: "Plan 8 phase, 45 việc, agent đổi thành checkbox để đếm tiến độ"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Plan do công cụ sinh: 8 phase, 45 việc, validate qua ngay từ đầu

**Bối cảnh:** Plan đóng gói được tạo bằng lệnh ak plan create, rồi viết từng phase.
**Chuyện gì xảy ra:** Plan có tám phase và 45 việc, ước khoảng 9 ngày công. Sau khi validate qua, agent dùng awk để chuyển các mục đánh số trong phần Tasks thành checkbox, và đếm số checkbox của từng phase để theo dõi tiến độ.
**Bài học:** Plan có cấu trúc đủ để công cụ đếm tiến độ; đầu ra validate là thứ để kiểm nhanh trước khi bắt đầu việc.
**Artefact:** Bảng tám phase kèm số việc của từng phase.
