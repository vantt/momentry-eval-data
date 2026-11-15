---
id: 2026-10-09-noi-schema-de-migration-qua-repo
date: 2026-10-09
repo: repo
status: raw
signals: ["3"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3966", "omp:cd4449ab#L3968", "omp:cd4449ab#L3969"]
hook: "Nới schema cho migration qua, rồi lead bắt siết lại đúng chuẩn"
tension: giup_ma_hai
sides: ["nới schema để dữ liệu cũ qua được", "schema mới mất strict, lead phải bắt siết lại"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nới schema để migration qua: repo@sha không kèm path, rồi siết lại

**Bối cảnh:** Regex evidence trong distill.schema.json đã được nới để nhận dạng cũ.
**Chuyện gì xảy ra:** Agent nới EvidencePattern để chấp nhận repo@sha không có :path, vì dữ liệu Phase 0 có dạng này. Lead yêu cầu giữ schema mới strict theo repo@<40-hex>:path[#Lx-Ly], chỉ migration v4 được chuyển dạng rút gọn sang repo@sha:<path> hoặc giữ trong legacy_where. Phần này được ghi nhận là một deviation trong phase-03.
**Bài học:** Nới schema để qua dữ liệu cũ là một quyết định đổi hợp đồng. Giữ schema mới chặt, đặt đường chuyển đổi trong lớp migration, và ghi lại deviation vào plan.
**Artefact:** Diff regex cũ và mới, kèm ví dụ hợp lệ và không hợp lệ.
**Góc người ngoài:** cách làm phổ biến là Nới ràng buộc để migration chạy được rồi bỏ quên, không ghi lại đã nới ở đâu; ở đây khác ở Agent thừa nhận phần nới lỏng trong báo cáo và yêu cầu ghi vào phase-03 kèm lý do. Người đọc sẽ hỏi làm sao để mỗi lần đổi ràng buộc đều có dấu vết và có thể rà lại.
