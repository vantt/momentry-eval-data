---
id: 2026-11-03-dao-quyet-dinh-prd-tu-chi-d5ef
code: M-W7CX
aliases: [M-W7CX]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L251", "claude:ab9a1dd8#L256", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L615"]
hook: "Từ 'chỉ in đoạn hook' sang tự ghi settings.json, đảo PRD ở 3 mục"
tension: chon_mot_mat_mot
sides: ["Chỉ in đoạn hook: đơn giản, không đụng settings.json của người dùng", "Tự cài tốn 200-300 dòng cộng test nhưng người dùng khỏi tự dán"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đảo quyết định PRD: từ 'chỉ in đoạn hook' sang 'công cụ tự ghi vào settings.json'

**Bối cảnh:** PRD mục 3.2 và 6.4 ghi công cụ không bao giờ tự sửa ~/.claude/settings.json; người dùng tự dán đoạn in ra.
**Chuyện gì xảy ra:** Agent đưa hai phương án và ước việc tự cài khoảng 200 đến 300 dòng cộng test. Chủ dự án chọn tự cài, có --dry-run và sao lưu trước khi ghi. Phương án chỉ in được giữ lại dưới dạng doctor kiểm hook hỏng. Quyết định này đảo PRD ở 3 mục và được ghi vào plan.
**Bài học:** Khi một quyết định đã chốt trong PRD bị đảo, sửa PRD ngay trong cùng lượt. Nếu không, tài liệu sẽ nói ngược với code.
**Artefact:** Bảng hai cột đánh đổi của phương án in và phương án tự cài.
