---
id: 2026-10-29-multica-khong-chay-duoc-voi-openclaw-c455
code: M-MEZ1
aliases: [M-MEZ1]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2940", "claude:0faf0bb2#L3041", "claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3062", "claude:0faf0bb2#L3088", "claude:0faf0bb2#L3150", "claude:0faf0bb2#L3160", "claude:0faf0bb2#L3182", "claude:0faf0bb2#L3198"]
hook: "Giả phiên bản 2026.3.13 thành 2026.5.5 vẫn không qua nổi"
tension: cam_ma_van_lot
sides: ["Chỉ cần giả số phiên bản là chạy được", "Lỗi đường dẫn include và gateway khiến CLI thoát không output, phải sửa ba chỗ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica không chạy được với OpenClaw đóng gói: trượt vì phiên bản tối thiểu

**Bối cảnh:** Thử Multica với OpenClaw đi kèm AICoworker để kiểm tra bốn tiêu chí (workspace, ghi ngược, session, workflow).
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối với thông báo 'openclaw 2026.3.13 is below the minimum supported version 2026.5.5'. Thử giả phiên bản trong wrapper thì CLI báo lỗi đường dẫn include ngoài thư mục cấu hình, gọi gateway thất bại, rồi thoát không có output. Kết luận là cần đổi ba chỗ (kiểm tra phiên bản, cấu hình $include, định dạng JSON) và không có đường nào sạch. Agent OpenClaw riêng được tạo và trả lời đúng bộ nhớ, nhưng không điều khiển được qua Multica. Sau đó dọn stack Docker, 3 image khoảng 1,2 GB và thư mục cấu hình, giữ lại agent.
**Bài học:** Đọc điều kiện phiên bản tối thiểu của công cụ trước khi dựng stack. Vá giả phiên bản chỉ đẩy lỗi sang chỗ khác.
**Artefact:** Ảnh dòng thông báo 'below the minimum supported version'. Không có gì cần che.
