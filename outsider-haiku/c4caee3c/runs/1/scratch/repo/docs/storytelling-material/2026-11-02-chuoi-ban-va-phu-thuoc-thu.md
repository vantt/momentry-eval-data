---
id: 2026-11-02-chuoi-ban-va-phu-thuoc-thu
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L902", "claude:c4caee3c#L921", "claude:c4caee3c#L945", "claude:c4caee3c#L1076", "claude:c4caee3c#L1083"]
hook: "Chèn một bản vá lên đầu chuỗi, bản vá số 3 bỗng xung đột"
tension: nho_ma_to
sides: ["chỉ thêm một bản vá P00 lên đầu", "P03 xung đột và P02 phải áp trước"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi bản vá phụ thuộc thứ tự: P03 xung đột khi đặt sau P00

**Bối cảnh:** Chuỗi bản vá lõi OHS áp lên tag upstream v0.17.2 theo thứ tự P00, P01, P02, P03, P04, P09, P05, P06, P07.
**Chuyện gì xảy ra:** Sau khi chèn P00 lên đầu, P03 xung đột ở cli.ts vì hai bản vá cùng sửa một khối import, và P02 phải được áp trước P03. Agent phải kiểm chuỗi bằng git am --3way trên tag gốc, rồi xuất lại từng bản vá từ nhánh đã ghép. Chuỗi cuối có 9 bản vá và hơn 2.000 test xanh.
**Bài học:** Mỗi lần đổi thứ tự phải áp lại từ tag gốc, không chỉ nối thêm vào cuối.
**Artefact:** Sơ đồ thứ tự các bản vá.
