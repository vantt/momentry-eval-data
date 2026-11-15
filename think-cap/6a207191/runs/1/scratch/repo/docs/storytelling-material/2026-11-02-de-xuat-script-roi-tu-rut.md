---
id: 2026-11-02-de-xuat-script-roi-tu-rut
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L910", "claude:6a207191#L929", "claude:6a207191#L937", "claude:6a207191#L951"]
hook: "Agent đề xuất script 30 kiểm tra rồi tự bỏ vì phải bảo trì"
tension: giup_ma_hai
sides: ["Script tự động 25–30 kiểm tra cho chắc", "Thêm code phải bảo trì, đi ngược mục tiêu gọn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đề xuất script rồi tự rút lại: verify bằng 12 bước cho agent, không code phải bảo trì

**Bối cảnh:** Người dùng hỏi skill có tự verify việc đang làm không. Lúc đó skill chỉ tự kiểm cấu trúc của chính nó.
**Chuyện gì xảy ra:** Agent đề xuất scripts/audit-project.sh với khoảng 25 đến 30 kiểm tra, rồi đổi ý: script là code phải bảo trì và đi ngược mục tiêu skill gọn. Agent đề xuất bước Verify 12 điểm do agent tự chạy theo hướng dẫn. Người dùng đồng ý. SKILL.md có 12 bước, mỗi bước ghi lệnh, tiêu chí đạt và rule liên quan.
**Bài học:** Quyết định verifier là code hay hướng dẫn. Bắt đầu bằng hướng dẫn, chuyển thành script khi bộ kiểm tra đã ổn định.
**Artefact:** Danh sách 12 bước verify với cột tiêu chí.
