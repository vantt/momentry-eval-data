---
id: 2026-10-09-xoa-revision-package-intake-va-6-4257
code: M-DZRX
aliases: [M-DZRX]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3058", "omp:cd4449ab#L3083", "omp:cd4449ab#L3085", "omp:cd4449ab#L3233", "omp:cd4449ab#L3235", "omp:cd4449ab#L3287", "omp:cd4449ab#L3289", "omp:cd4449ab#L3368", "omp:cd4449ab#L3485", "omp:cd4449ab#L3487", "omp:cd4449ab#L3956"]
hook: "Xoá 6 schema và 2 file, diff rút đúng 1650 dòng"
tension: it_ma_nhieu
sides: ["xoá vài file và schema", "diff rút 1650 dòng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá revision package, intake và 6 schema: diff rút 1650 dòng

**Bối cảnh:** Theo contract table mới, bỏ insight và run lifecycle, revision package, file LINK và intake. Docs design 07 phải đổi trong cùng commit.
**Chuyện gì xảy ra:** Xoá 6 schema JSON và 2 file revision_package. So với origin/main, workspace_validation.go giảm 51 dòng và thêm 18. Một số bước sau phải đổi thêm để validate không còn phụ thuộc runtime packages. Commit đổi MCP và web có diff 19 file, +350 và -1650 dòng.
**Bài học:** Khi xoá tính năng, đối chiếu contract table và docs trong cùng commit, và đếm số dòng xoá để kiểm chứng phạm vi.
**Artefact:** Git diff --stat trước và sau khi xoá. Không cần ảnh.
