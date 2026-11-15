---
id: 2026-10-29-paperclip-doi-giao-thuc-v4-gateway-c455
code: M-20ZP
aliases: [M-20ZP]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L959", "claude:0faf0bb2#L960", "claude:0faf0bb2#L968", "claude:0faf0bb2#L982", "claude:0faf0bb2#L990", "claude:0faf0bb2#L1016", "claude:0faf0bb2#L1021"]
hook: "Gateway chỉ nói giao thức 3, adapter đòi 4: sửa đúng một con số"
tension: it_ma_nhieu
sides: ["Một con số đổi từ 4 về 3", "Kết nối gateway thông suốt, nhưng bản vá mất khi nâng cấp"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Paperclip đòi giao thức v4, gateway chỉ có v3: vá bản đã cài và kiểm chứng bằng commit upstream

**Bối cảnh:** Adapter OpenClaw của Paperclip bị kẹt ở bước verifying, agent không sang được trạng thái ready.
**Chuyện gì xảy ra:** Adapter gửi PROTOCOL_VERSION 4 trong khi gateway AICoworker chỉ nhận 3. Commit upstream ec2d87d chỉ đổi số phiên bản, không đổi ngữ nghĩa khung, nên mình đổi minProtocol về 3 trong bản đã cài (có giữ file .orig), khởi động lại và thấy 'Gateway connect probe succeeded'. Bản vá này mất khi nâng cấp Paperclip.
**Bài học:** Trước khi vá lệch phiên bản giao thức, đọc commit gốc để chắc thay đổi chỉ là số, và ghi lại chỗ vá để lần nâng cấp sau không lặng lẽ làm vỡ.
**Artefact:** Dòng log probe thành công. Che địa chỉ máy và mọi token.
