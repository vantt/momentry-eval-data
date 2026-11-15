---
id: 2026-11-02-ghep-chuoi-9-ban-va-thu-40f9
code: M-DBBE
aliases: [M-DBBE]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Nhiều bản vá tách từ nhánh song song cùng chạm một file, nên thứ tự áp dụng quyết định xung đột, và chuỗi phải dựng lại nhiều lần."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L902", "claude:c4caee3c#L920", "claude:c4caee3c#L934", "claude:c4caee3c#L945", "claude:c4caee3c#L950", "claude:c4caee3c#L1076", "claude:c4caee3c#L1083", "claude:c4caee3c#L1559", "claude:c4caee3c#L1564"]
hook: "Bản vá P03 áp sạch trước P00, nhưng xung đột nếu đứng sau"
tension: nho_ma_to
sides: ["Cùng một bản vá P03", "Đổi vị trí là xung đột, phải dựng lại chuỗi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một fork của công cụ tìm kiếm Obsidian chạy cục bộ giữ tính năng riêng dưới dạng chuỗi bản vá trên các phiên bản upstream. Bản vá P03 áp sạch khi đứng trước P00 nên người làm tưởng nó đứng đâu trong chuỗi cũng được. Hoá ra cả hai cùng sửa cli.ts, nên P03 xung đột khi đứng sau P00 và còn phải đứng sau P02. Ai ghép nhiều bản vá vào cùng một file dễ mắc đúng bẫy này: áp được riêng chưa có nghĩa là áp được cả chuỗi."
audience: dev duy trì fork hoặc nhiều bản vá trên cùng một upstream
spine_context: "Một fork của công cụ tìm kiếm Obsidian chạy cục bộ, giữ tính năng riêng dưới dạng chuỗi bản vá trên các phiên bản upstream."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn chuỗi bản vá của fork áp sạch lên upstream và test xanh.
spine_want_lines: ["claude:c4caee3c#L1075"]
spine_obstacle: "P03 áp sạch khi đứng trước P00 nhưng xung đột khi đứng sau, vì cả hai cùng sửa cli.ts."
spine_obstacle_lines: ["claude:c4caee3c#L920"]
spine_turn: Tưởng bản vá đã áp sạch thì đứng đâu trong chuỗi cũng được; hoá ra P03 xung đột khi đứng sau P00 và phải đứng sau P02.
spine_turn_lines: ["claude:c4caee3c#L902", "claude:c4caee3c#L920", "claude:c4caee3c#L944"]
spine_action: "Giữ cả hai dòng import rồi dựng lại nhánh ghép theo thứ tự P00, P01, P02, P03, P09."
spine_action_lines: ["claude:c4caee3c#L933", "claude:c4caee3c#L944"]
spine_outcome: "Nhánh ghép xanh: 117 file, 2049 test, lint đạt."
spine_outcome_lines: ["claude:c4caee3c#L1075"]
spine_takeaway: "Với nhiều bản vá cùng sửa một file, đừng chỉ nối vào cuối: giữ một nhánh ghép duy nhất và chạy lại toàn chuỗi mỗi khi thêm bản vá."
spine_takeaway_lines: ["claude:c4caee3c#L920"]
completeness: 7
---

# Ghép chuỗi 9 bản vá: thứ tự quyết định có áp được không

**Góc kể:** Một fork của công cụ tìm kiếm Obsidian chạy cục bộ giữ tính năng riêng dưới dạng chuỗi bản vá trên các phiên bản upstream. Bản vá P03 áp sạch khi đứng trước P00 nên người làm tưởng nó đứng đâu trong chuỗi cũng được. Hoá ra cả hai cùng sửa cli.ts, nên P03 xung đột khi đứng sau P00 và còn phải đứng sau P02. Ai ghép nhiều bản vá vào cùng một file dễ mắc đúng bẫy này: áp được riêng chưa có nghĩa là áp được cả chuỗi.
**Bối cảnh:** Mỗi tính năng của fork là một bản vá riêng, nằm trên một tag upstream. Hai bản vá sửa cùng một file CLI.
**Chuyện gì xảy ra:** Bản vá P03 áp sạch khi đứng trước P00 nhưng xung đột khi đứng sau. Agent dựng nhánh tích hợp tuần tự, sửa xung đột ở dòng import rồi xuất lại bản vá. Chuỗi đã được dựng lại nhiều lần, mỗi lần thêm bản vá mới vào đúng vị trí. Lần dựng cuối có 8 bản vá và 2083 test xanh, và sau đó thêm P07 thành 9 bản vá.
**Bài học:** Với nhiều bản vá cùng chạm một file, có một nhánh tích hợp duy nhất và kiểm lại toàn chuỗi mỗi khi thêm bản vá, đừng chỉ nối vào cuối.
**Artefact:** Danh sách thứ tự bản vá trong series (không nhạy cảm).
