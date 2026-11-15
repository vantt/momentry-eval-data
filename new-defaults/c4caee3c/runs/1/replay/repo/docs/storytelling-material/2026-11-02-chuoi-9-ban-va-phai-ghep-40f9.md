---
id: 2026-11-02-chuoi-9-ban-va-phai-ghep-40f9
code: M-K8WS
aliases: [M-K8WS]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L920", "claude:c4caee3c#L934", "claude:c4caee3c#L945", "claude:c4caee3c#L1076", "claude:c4caee3c#L1564", "claude:c4caee3c#L3210"]
hook: "Chín bản vá, hai bản sửa cùng một file, test tăng 2.049 lên 2.091"
tension: nho_ma_to
sides: ["Hai bản vá cùng sửa một file cli.ts", "Phải dựng lại cả chuỗi 9 bản và chạy lại mọi cổng mỗi lần"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi 9 bản vá phải ghép đúng thứ tự vì hai bản cùng sửa một file

**Bối cảnh:** Nhiều agent làm các bản vá lõi trên cùng một upstream tag.
**Chuyện gì xảy ra:** Patch P03 xung đột với P00 vì cả hai sửa cli.ts. Ghép tuần tự trên nhánh tích hợp rồi xuất lại mọi patch từ nhánh đó. Mỗi lần sửa phải dựng lại toàn chuỗi và chạy đủ cổng, số test tăng từ 2.049 lên 2.091. Khi sắp thứ tự, các bản vá được đánh số lại.
**Bài học:** Với chuỗi bản vá, nguồn sự thật là nhánh tích hợp đã dựng lại; đừng vá nối tiếp vào patch cũ.
