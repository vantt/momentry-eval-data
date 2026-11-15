---
id: 2026-11-01-day-lai-cho-nguoi-van-hanh
date: 2026-11-01
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3304", "claude:f0bf048d#L3340", "claude:f0bf048d#L3345"]
hook: "Mọi bước làm tay đều phải dạy lại cho agent vận hành, 7 bước"
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

# Dạy lại cho người vận hành: mọi thao tác tay phải vào skill

**Bối cảnh:** Người vận hành (System Operator) là agent, và mọi bước đã làm tay trên máy cần được đưa vào skill của nó.
**Chuyện gì xảy ra:** Chủ ra quy tắc: mọi bước làm tay phải được dạy lại cho System Operator và deploy. Phiên ghi quy tắc này vào memory. Khi chuyển sang user riêng opc-ops, các script đọc MULTICA_HOME nên chuyển gọn. Có 7 bước, mỗi bước có phần dạy lại trong references/privileged.md.
**Bài học:** Nếu người vận hành là một agent, mọi thao tác làm tay mà không đưa vào skill thì agent đó sẽ không biết; ghi thành quy tắc, không để trong đầu.
**Artefact:** Bảng 7 bước phase 2 với cột 'anh làm gì'; che tên người và email.
