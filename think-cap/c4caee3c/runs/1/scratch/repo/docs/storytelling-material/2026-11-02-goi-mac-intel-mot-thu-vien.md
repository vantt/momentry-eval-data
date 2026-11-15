---
id: 2026-11-02-goi-mac-intel-mot-thu-vien
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, Đảo quyết định có lý do, Người duyệt thứ máy soạn]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2547", "claude:c4caee3c#L2604", "claude:c4caee3c#L2617", "claude:c4caee3c#L2894", "claude:c4caee3c#L2981", "claude:c4caee3c#L3903", "claude:c4caee3c#L3919"]
hook: "Rosetta không cứu được: gói npm Intel thiếu đúng một file"
tension: cam_ma_van_lot
sides: ["Có Rosetta, tưởng máy Intel chạy được", "File darwin-x64 không có trong gói nên vẫn lỗi"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói Mac Intel: một thư viện npm không còn file cho darwin-x64, và cách ghim bản cũ kèm điều kiện đạt

**Bối cảnh:** Gói dựng sẵn cho 4 nền (Windows, macOS ARM, macOS Intel, Linux). Thư viện onnxruntime-node 1.30.0 của upstream không kèm binding darwin-x64.
**Chuyện gì xảy ra:** Smoke test trên runner Intel lỗi 'Cannot find module ... darwin/x64'. Đề xuất Rosetta không cứu được vì file thiếu trong gói npm. Người dùng chọn ghim 1.23.2 chỉ cho gói Intel. Đo cùng máy: multilingual +0,063, vi-synonym −0,017. Sau đó trên bản vantt.4 vi-snippet +0,024; người dùng đổi luật thành 'chỉ chặn khi tụt quá 0,01', nên danh sách cho phép không còn lỗi thời mỗi lần gói đổi.
**Bài học:** Khi một nền bị thư viện bỏ, ghim bản cũ là được, nhưng đặt luật 'chỉ chặn khi tụt' thay vì danh sách cho phép cố định, nếu không sẽ phải duyệt lại mỗi lần đổi.
**Artefact:** Bảng delta theo hạng mục (locked 1.30.0 vs pinned 1.23.2); không có dữ liệu riêng tư.
