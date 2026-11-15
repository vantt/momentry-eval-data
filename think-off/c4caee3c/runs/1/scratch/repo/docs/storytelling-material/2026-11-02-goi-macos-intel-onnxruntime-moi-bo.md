---
id: 2026-11-02-goi-macos-intel-onnxruntime-moi-bo
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2561", "claude:c4caee3c#L2604", "claude:c4caee3c#L2894", "claude:c4caee3c#L2981", "claude:c4caee3c#L3903", "claude:c4caee3c#L3919"]
hook: "Ghim onnxruntime cũ cho Intel: một hạng mục lên 0,063, một tụt 0,017"
tension: giup_ma_hai
sides: ["Ghim bản cũ để gói Intel chạy được", "Số đo lệch: hạng mục này tăng, hạng mục kia tụt"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói macOS Intel: onnxruntime mới bỏ Intel, ghim bản cũ và đổi quy tắc chặn

**Bối cảnh:** Bốn nền phát hành đều phải có gói dựng sẵn. onnxruntime-node 1.30.0 mà upstream dùng không có file nhị phân cho darwin-x64, nên không dựng được gói Mac Intel.
**Chuyện gì xảy ra:** Lead đề xuất ghim 1.23.2 chỉ cho gói Intel; người duyệt chấp nhận. Trên cùng máy, bản ghim cho multilingual cao hơn 0,063 và vi-synonym thấp hơn 0,017. Gói tiếng Việt sau đó đổi, và đo lại thì vi-snippet cao hơn 0,024, vi-synonym thấp hơn 0,021. Người duyệt đổi quy tắc thành chỉ chặn khi tụt quá 0,01 thay vì danh sách cho phép từng hạng mục. Kích thước gói giải nén 280 đến 330 MB, vượt mục tiêu 250 MB và được chấp nhận có ghi chú.
**Bài học:** Danh sách cho phép theo số đo cụ thể sẽ lỗi thời mỗi khi dữ liệu đổi; quy tắc chỉ chặn tụt điểm bền hơn.
**Artefact:** Bảng chênh lệch theo hạng mục giữa bản ghim và bản gốc, bỏ tên hạng mục nếu không cần.
