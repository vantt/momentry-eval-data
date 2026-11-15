---
id: 2026-11-02-ci-doc-fixture-tag-cung-v0-40f9
code: M-ECR2
aliases: [M-ECR2]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3868", "claude:c4caee3c#L3875", "claude:c4caee3c#L3912"]
hook: "Eval đỏ không phải do bản ghim, mà do fixture ghi cứng v0.10.0"
tension: nho_ma_to
sides: ["Một tag ghi cứng trong CI, golden set đã lên v0.11.0", "Hai lượt eval chết, trông như bản ghim làm tệ đi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đọc fixture tag cứng v0.10.0 trong khi golden set đã lên v0.11.0

**Bối cảnh:** Hai workflow bundles và pin-effect clone fixture ở một tag cố định đã cũ.
**Chuyện gì xảy ra:** Eval trên Intel và pin-effect trên EPYC chết với lỗi golden set không khớp phiên bản fixture. Đây là lỗi hạ tầng chứ không phải delta của bản ghim. Sửa: đọc tag từ FIXTURE_TAG trong run-eval.mjs, thiếu thì fail rõ ràng.
**Bài học:** Một hằng số phiên bản nằm ở hai nơi sẽ lệch nhau; hãy đọc từ một nguồn duy nhất.
**Artefact:** Dòng lỗi về golden set không khớp, không chứa nội dung.
