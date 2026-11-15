---
id: 2026-11-01-copy-phien-dang-nhap-claude-sang
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3505", "claude:f0bf048d#L3516"]
hook: "Copy phiên đăng nhập Claude sang user khác chạy được, rồi hỏng sau vài giờ"
tension: tuong_ma_hoa_ra
sides: ["Chép xong chạy đúng, tưởng đã xong", "Token tự làm mới làm bản kia hỏng, lỗi 401 giữa việc khách"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Copy phiên đăng nhập Claude sang user khác: vì sao sẽ hỏng sau vài giờ

**Bối cảnh:** Mỗi user Linux có phiên đăng nhập Claude riêng. Chủ muốn chép file credential sang user mới để khỏi phải /login lại.
**Chuyện gì xảy ra:** Chép được, chạy đúng lúc đầu. Nhưng token OAuth tự làm mới theo chu kỳ, và khi user này làm mới, bản của user kia thành hỏng. Nếu đây là user agent đang chạy việc khách, sẽ lỗi 401 giữa chừng mà không báo trước. Đề xuất /login riêng cho mỗi user, tốn khoảng một phút.
**Bài học:** Token OAuth tự làm mới là trạng thái, không phải cấu hình; hai tiến trình dùng chung một bản chép sẽ đá nhau.
**Artefact:** Sơ đồ hai user dùng chung một file credential và thời điểm làm mới.
