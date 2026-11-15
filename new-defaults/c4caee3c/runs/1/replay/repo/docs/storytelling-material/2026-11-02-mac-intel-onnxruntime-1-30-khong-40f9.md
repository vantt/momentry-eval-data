---
id: 2026-11-02-mac-intel-onnxruntime-1-30-khong-40f9
code: M-8SXA
aliases: [M-8SXA]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh, khac, nguoi_duyet_may_soan]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2585", "claude:c4caee3c#L2894", "claude:c4caee3c#L2981", "claude:c4caee3c#L3333", "claude:c4caee3c#L3919"]
hook: "Ghim onnxruntime cho Mac Intel: mỗi bản đo lại đổi hạng mục tụt"
tension: khac
sides: ["Danh sách cho phép chốt theo số đo", "Bản mới đo ra hạng mục tụt khác, danh sách lỗi thời ngay"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mac Intel: onnxruntime 1.30 không còn binding darwin-x64, ghim 1.23.2 và đổi luật chặn

**Bối cảnh:** Upstream dùng onnxruntime-node 1.30.0, bản này không có file cho macOS Intel nên gói Intel không dựng được.
**Chuyện gì xảy ra:** Người dùng chọn ghim 1.23.2 chỉ cho gói Intel. Đo trên cùng máy: đa ngôn ngữ +0,063, vi-synonym -0,017, nên ban đầu dùng danh sách cho phép theo từng hạng mục. Bản vantt.4 đo ra thêm vi-snippet +0,024 và vi-synonym -0,021, khiến danh sách cho phép lỗi thời. Người dùng đổi luật: chỉ chặn khi một hạng mục tụt quá 0,01. Một lần catchup khác đỏ vì fixture tag cứng.
**Bài học:** Danh sách chấp nhận theo con số đo sẽ hỏng khi gói đổi; đặt luật theo hướng xấu đi thay vì khớp từng số.
**Artefact:** Bảng delta theo hạng mục, trước và sau khi đổi luật.
