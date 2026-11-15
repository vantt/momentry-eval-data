---
id: 2026-11-02-chin-ban-va-phai-ap-dung-40f9
code: M-BK44
aliases: [M-BK44]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L865", "claude:c4caee3c#L902", "claude:c4caee3c#L920", "claude:c4caee3c#L934", "claude:c4caee3c#L945", "claude:c4caee3c#L950", "claude:c4caee3c#L1076"]
hook: "Chín bản vá, đảo một cặp thứ tự là xung đột"
tension: nho_ma_to
sides: ["Chín bản vá đều đúng riêng lẻ", "Chỉ cần đổi thứ tự là xung đột vì một dòng import"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chín bản vá phải áp đúng thứ tự, đảo thứ tự là xung đột

**Bối cảnh:** Chín bản vá lõi đều chạm các file chung như cli.ts. Mỗi bản được viết trên một tag upstream nên chỉ ghép được theo một thứ tự.
**Chuyện gì xảy ra:** Bản P03 xung đột khi đứng sau P00, vì cả hai cùng sửa dòng import của cli.ts. Lead dựng lại nhánh ghép theo thứ tự P00, P01, P02, P03, P09 bằng git reset rồi git am, và chạy full test: 2049 test xanh. Các bản vá xuất lại từ nhánh ghép được chèn đúng vị trí trong series.toml.
**Bài học:** Thứ tự của chuỗi bản vá phải được kiểm bằng cách áp lại đúng thứ tự trên tag gốc, đừng tin vào thứ tự viết.
