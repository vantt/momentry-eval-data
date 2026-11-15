---
id: 2026-10-30-cai-mcp-xong-nhung-buoc-chep-f60d
code: M-FPB5
aliases: [M-FPB5]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:f0bf048d#L480", "claude:f0bf048d#L963", "claude:f0bf048d#L975"]
hook: "Cài MCP xong mà quên chép key: agent chạy mà mù"
tension: nho_ma_to
sides: ["Lệnh cài server chạy thành công", "Lệnh chép key đứng sau bị sót, agent không có key"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một team đang dựng agent AI trên nền tảng multica, người làm đang đóng gói để deploy lại được đủ agent và công cụ. Họ tưởng bước cài MCP là đủ, nhưng lần chạy thử cho thấy agent vẫn thiếu file key, vì lệnh chép key là bước tay riêng và bị sót, nên agent chạy mà không đọc được key. Ai đóng gói agent có file bí mật trên máy đều dễ dính lỗi này, và cách sửa là kiểm bằng đúng user mà agent chạy."
audience: dev dựng agent AI và đóng gói công cụ cho team
spine_context: Một team đang dựng agent AI trên nền tảng multica; người làm đang đóng gói để deploy lại được đủ agent và công cụ.
spine_context_lines: ["claude:f0bf048d#L175", "claude:f0bf048d#L968"]
spine_want: "Deploy lại từ đầu thì có đủ agent lẫn công cụ, với tối thiểu bước tay."
spine_want_lines: ["claude:f0bf048d#L975"]
spine_obstacle: "Chạy thử, agent không tìm thấy file key vì bước chép key bị sót."
spine_obstacle_lines: ["claude:f0bf048d#L963"]
spine_turn: "Tưởng cài MCP là xong; hoá ra file key là bước chép riêng và bị sót, nên agent chạy mà không có key."
spine_turn_lines: ["claude:f0bf048d#L963", "claude:f0bf048d#L975"]
spine_action: "Khai báo file bí mật trong manifest, để lệnh tools tự chép và chạy kiểm tra dưới đúng user daemon."
spine_action_lines: ["claude:f0bf048d#L975"]
spine_takeaway: "Kiểm thứ agent cần dưới đúng user mà agent đó chạy, không kiểm dưới user của người deploy."
spine_takeaway_lines: ["claude:f0bf048d#L975"]
completeness: 6
---

# Cài MCP xong nhưng bước chép key bị sót: agent bị mù

**Góc kể:** Một team đang dựng agent AI trên nền tảng multica, người làm đang đóng gói để deploy lại được đủ agent và công cụ. Họ tưởng bước cài MCP là đủ, nhưng lần chạy thử cho thấy agent vẫn thiếu file key, vì lệnh chép key là bước tay riêng và bị sót, nên agent chạy mà không đọc được key. Ai đóng gói agent có file bí mật trên máy đều dễ dính lỗi này, và cách sửa là kiểm bằng đúng user mà agent chạy.
**Bối cảnh:** Deploy MCP cần hai lệnh root: cài server, rồi chép file key cho user daemon.
**Chuyện gì xảy ra:** Chạy thử issue STU-6, agent báo không có file key. Lệnh cài server đã chạy, nhưng lệnh chép key đứng sau thì không. Agent không có sudo nên mọi bước root phải nhờ chủ chạy. Sửa gói: khai báo file bí mật trong manifest, lệnh tools tự chép, rồi kiểm lại dưới đúng user daemon. Lỗi kiểu này từ nay được bắt trước khi agent chạy.
**Bài học:** Kiểm thứ agent cần dưới đúng user mà agent đó chạy, không kiểm dưới user của người deploy.
**Artefact:** Output của lần chạy thử, che đường dẫn và id.
**Góc người ngoài:** cách làm phổ biến là Nhiều người dừng hẳn, hoặc làm lại từ đầu, hoặc không có cách kiểm xác nhận sau khi làm; ở đây khác ở Mỗi lệnh sudo đi kèm điều kiện thành công (vd in ra KEY_OK) và bước kế tiếp được tính sẵn. Người đọc muốn biết vì sao phiên luôn đưa được việc gọn cho người dùng và tránh lặp việc.
