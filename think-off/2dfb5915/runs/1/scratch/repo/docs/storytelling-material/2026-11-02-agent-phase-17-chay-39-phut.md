---
id: 2026-11-02-agent-phase-17-chay-39-phut
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2965", "claude:2dfb5915#L3266", "claude:2dfb5915#L3312"]
hook: "Agent chạy 39 phút, 170 lần gọi tool, rồi bị dừng giữa chừng"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent phase 17 chạy 39 phút và 170 lần gọi tool

**Bối cảnh:** Agent được giao làm phần nội bộ của phase 17 trên nhánh riêng, trong khi thiết kế chữ ký tool còn đang được bàn.
**Chuyện gì xảy ra:** Agent chạy khoảng 39 phút với 170 lần gọi tool và khoảng 540 nghìn token phụ. Nó phải dừng phần chốt chữ ký tool theo yêu cầu thay đổi phạm vi, rồi làm lại phần nội bộ. Các lần CI trên nhánh cũng chạy lại nhiều lần.
**Bài học:** Khi thiết kế giao diện chưa chốt, giới hạn agent ở phần nội bộ. Đo chi phí agent bằng số lần gọi tool và thời gian.
**Artefact:** Không có.
