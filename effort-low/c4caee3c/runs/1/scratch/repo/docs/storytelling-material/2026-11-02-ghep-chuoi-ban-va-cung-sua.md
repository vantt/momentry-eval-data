---
id: 2026-11-02-ghep-chuoi-ban-va-cung-sua
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L902", "claude:c4caee3c#L945", "claude:c4caee3c#L1076"]
hook: "Chín bản vá sửa chung file, áp sai thứ tự là xung đột"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ghép chuỗi bản vá: cùng sửa một file nên phải đúng thứ tự

**Bối cảnh:** Chuỗi bản vá P00 đến P09 phải áp lên một tag upstream, và các bản vá cùng chạm vào cli.ts.
**Chuyện gì xảy ra:** Áp P03 sau P00 gây xung đột vì cả hai đều sửa cli.ts. Agent dựng lại nhánh ghép theo đúng thứ tự P00, P01, P02, P03, P09 và kiểm bằng git am trên tag. Nhánh ghép có 2.049 test xanh trước khi xuất lại các bản vá. Sau này chuỗi đủ 9 bản vá và mỗi bản mới phải được áp lại theo thứ tự.
**Bài học:** Thứ tự áp bản vá là một phần của thiết kế; kiểm bằng git am trên tag sạch, đừng tin vào áp thủ công.
**Artefact:** Sơ đồ thứ tự 9 bản vá và file bị chạm. Không cần che.
