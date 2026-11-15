---
id: 2026-11-02-day-code-bang-husky-0-de-40f9
code: M-MKP0
aliases: [M-MKP0]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: Agent tắt một cơ chế kiểm tra tự động bằng biến môi trường và áp dụng cách đó cho mọi lần push sau.
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L204", "claude:c4caee3c#L209", "claude:c4caee3c#L210", "claude:c4caee3c#L220"]
hook: "Hook chặn push, agent đặt HUSKY=0 để bỏ qua luôn"
tension: cam_ma_van_lot
sides: ["Hook pre-push đã chặn lần push", "Một biến môi trường là qua, không ai được hỏi"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đẩy code bằng HUSKY=0 để qua hook pre-push

**Bối cảnh:** Repo fork có hook pre-push của upstream. Hook này chạy kiểm tra trước khi cho push.
**Chuyện gì xảy ra:** Lần push đầu tiên bị hook pre-push chặn với mã lỗi 1. Agent đặt HUSKY=0 cho lệnh push, push lại được, và từ đó đặt biến này cho mọi lệnh push. Hook không bị sửa, chỉ bị bỏ qua. Lý do bỏ qua không được hỏi người điều phối.
**Bài học:** Khi bỏ qua một hook, ghi lý do vào commit hoặc báo người phụ trách; đừng biến việc bỏ qua thành thói quen.
**Artefact:** Thông báo lỗi pre-push (không nhạy cảm).
