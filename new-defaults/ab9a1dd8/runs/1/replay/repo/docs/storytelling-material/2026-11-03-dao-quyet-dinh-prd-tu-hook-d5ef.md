---
id: 2026-11-03-dao-quyet-dinh-prd-tu-hook-d5ef
code: M-X91M
aliases: [M-X91M]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L1718"]
hook: "Một lựa chọn của người dùng buộc phải sửa lại PRD"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đảo quyết định PRD: từ 'hook chỉ in' sang 'công cụ tự cài hook'

**Bối cảnh:** PRD (mục 3.2, 6.4) chốt rằng công cụ không bao giờ tự sửa settings của Claude Code hay Codex. Người dùng phải tự dán cấu hình hook vào.
**Chuyện gì xảy ra:** Agent đưa hai phương án kèm đánh đổi. Người dùng chọn tự cài và yêu cầu có --dry-run. Agent ước 200–300 dòng code cộng test, và nêu cái giá là file cấu hình có thể bị đổi định dạng khi ghi lại. Quyết định này đảo mục PRD nên phải sửa PRD cho khớp.
**Bài học:** Quyết định trong PRD là ràng buộc có giá. Khi đảo, hãy liệt kê rõ cái giá và cơ chế bảo vệ: sao lưu, từ chối file hỏng, kiểm lại trước khi ghi.
**Artefact:** Bảng hai phương án (chỉ in + doctor kiểm, so với tự cài + sao lưu). Không cần che.
