---
id: 2026-11-03-quarantine-release-all-tha-lai-chuyen-d5ef
code: M-6RMJ
aliases: [M-6RMJ]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L3315", "claude:ab9a1dd8#L3327", "claude:ab9a1dd8#L3333", "claude:ab9a1dd8#L3366", "claude:ab9a1dd8#L3388", "claude:ab9a1dd8#L3400"]
hook: "Một lệnh thả chuyện sạch, vẫn giữ chuyện lộ thông tin riêng"
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

# quarantine --release all: thả lại chuyện sạch, giữ chuyện còn lộ thông tin riêng

**Bối cảnh:** Giữa lúc agent nghiên cứu ba host mới, user thêm vào goal lệnh momentry quarantine --release all.
**Chuyện gì xảy ra:** Lệnh kiểm lại mọi chuyện đang giữ, thả chuyện sạch vào hộp, chuyện còn vi phạm riêng tư vẫn bị giữ. Test mới có một chuyện sạch và một chuyện lộ thông tin riêng. Test kiểm tài liệu sinh ra cũng đỏ vì bảng lệnh đổi, phải sinh lại cli-reference. Tổng 235 test pass.
**Bài học:** Lệnh thả hàng loạt chỉ an toàn khi mỗi mục được kiểm lại bằng đúng bộ kiểm riêng tư. Test cả hai nhánh: sạch được thả, bẩn bị giữ.
**Artefact:** Output mẫu thả 1, giữ 1. Không chụp nội dung chuyện.
