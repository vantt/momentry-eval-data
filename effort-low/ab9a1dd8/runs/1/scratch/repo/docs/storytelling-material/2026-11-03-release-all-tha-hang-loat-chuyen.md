---
id: 2026-11-03-release-all-tha-hang-loat-chuyen
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3315", "claude:ab9a1dd8#L3333", "claude:ab9a1dd8#L3366", "claude:ab9a1dd8#L3397"]
hook: "Thả hàng loạt chuyện, nhưng chuyện còn lộ riêng tư vẫn bị giữ"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# --release all: thả hàng loạt chuyện nhưng giữ lại chuyện còn lộ thông tin riêng tư

**Bối cảnh:** Người dùng yêu cầu thêm lệnh thả tất cả chuyện đang giữ trong hàng quarantine. Chuyện vẫn chứa thông tin riêng tư không được đưa vào hộp.
**Chuyện gì xảy ra:** Lệnh mới kiểm lại từng chuyện trước khi thả. Chuyện sạch vào hộp, chuyện còn lộ vẫn bị giữ. Test có một chuyện sạch và một chuyện lộ để kiểm cả hai nhánh. Tham chiếu lệnh được sinh lại từ bảng lệnh.
**Bài học:** Thao tác hàng loạt không được phá rào kiểm riêng tư; mỗi phần tử phải được kiểm lại độc lập.
**Artefact:** Output của lệnh release all với một chuyện được thả và một chuyện bị giữ. Che tên người và nội dung.
