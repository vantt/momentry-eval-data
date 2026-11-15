---
id: 2026-11-03-dao-quyet-dinh-prd-init-tu
date: 2026-11-03
repo: repo
status: raw
signals: ["3", "4"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L1718"]
hook: "Tự cài hook tốn 300 dòng, nhưng cứu người mới khỏi dán sai"
tension: khac
sides: ["chỉ in cấu hình thì an toàn, code ít", "người mới dễ dán sai nên user chọn tự cài, thêm 200-300 dòng"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đảo quyết định PRD: init tự cài hook thay vì chỉ in đoạn cấu hình

**Bối cảnh:** PRD chốt rằng công cụ không bao giờ tự sửa settings.json của agent. Skill đóng gói lại yêu cầu init tự cài.
**Chuyện gì xảy ra:** Agent đưa hai phương án với đánh đổi cụ thể: chỉ in thì an toàn nhưng người mới dễ dán sai, còn tự cài thì phải sao lưu và giữ phần của người dùng. Người dùng chọn tự cài. Ước lượng khoảng 200 đến 300 dòng code cộng test, và PRD được sửa ở ba mục.
**Bài học:** Khi người dùng đảo một quyết định đã chốt trong PRD, sửa PRD cùng lúc và nói rõ cái giá của việc đảo (ví dụ file có thể đổi định dạng khi ghi lại).
**Artefact:** Bảng hai phương án: chỉ in và tự cài, với cột ưu nhược.
