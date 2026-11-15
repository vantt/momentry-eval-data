---
id: 2026-11-02-mot-lan-agent-doi-nham-dong
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2494", "claude:c4caee3c#L2502", "claude:c4caee3c#L2508", "claude:c4caee3c#L2514"]
hook: "Sửa dòng L24 mà script lại đổi nhầm dòng N22"
tension: khac
sides: ["Script báo đã thay chuỗi", "Nhãn L24 không đổi, dòng N22 mới bị sửa"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một lần agent đổi nhầm dòng: sửa dòng N22 khi định sửa L24 trong PRD

**Bối cảnh:** Cập nhật nhãn một dòng trong bảng PRD bằng script Python tìm chuỗi.
**Chuyện gì xảy ra:** Agent viết script thay chuỗi cho dòng L24 nhưng nhãn không đổi; kiểm git show thấy đã sửa nhầm dòng N22 cùng commit. Sửa lại trong cùng commit.
**Bài học:** Sau khi sửa file bằng script tìm chuỗi, luôn xem diff đúng dòng trước khi commit.
**Artefact:** Không cần.
