---
id: 2026-11-02-routing-nam-tren-hub-khong-chep
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L1040", "claude:6a207191#L1183", "claude:6a207191#L1315", "claude:6a207191#L1396", "claude:6a207191#L1417", "claude:6a207191#L1441", "claude:6a207191#L1453"]
hook: "Agent kết luận skill chưa có routing, trong khi hub đã giữ 9 trigger"
tension: tuong_ma_hoa_ra
sides: ["Thư mục trên máy không có skill.yaml nên tưởng chưa có routing", "Routing nằm trên hub với 9 trigger, 5 example, 5 not_for"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Routing nằm trên hub, không chép về máy: agent khẳng định nhầm 'skill chưa có routing'

**Bối cảnh:** Người dùng thấy metadata của skill (topic, operations) trống trên hub. Agent phải tìm nguyên nhân và đề xuất cách sửa.
**Chuyện gì xảy ra:** Agent đọc thư mục skill trên máy này, thấy không có skill.yaml, kết luận là chưa có routing rồi soạn bản nháp đầy đủ. Người dùng hỏi lại vì trước đó đã có triggers, examples và not_for. Agent gọi skill_get trên hub và thấy 9 trigger, 5 example, 5 not_for do người duyệt đặt lúc duyệt bản trước. Các trường operations, topics, technologies, min_scope không hiển thị từ máy khách, và lệnh show --verbose bị từ chối vì skill được curate trên máy hub.
**Bài học:** Khi cùng một thông tin nằm ở hai nơi, hãy đọc từ nơi có thẩm quyền trước khi kết luận là trống. Cần có lệnh kéo routing về để không phải đoán.
**Artefact:** Bảng so sánh theo trường: 9 trigger thành 10, 5 not_for thành 6, các ô '—' cho thấy metadata đang thiếu.
**Góc người ngoài:** cách làm phổ biến là Agent thường bảo vệ kết luận đầu hoặc sửa nửa vời. Người dùng thường không có cách xem trạng thái ở máy từ xa nên cũng không bắt lỗi được; ở đây khác ở Nguồn sự thật nằm ở hub chứ không ở thư mục cục bộ. Thói quen đúng là đối chiếu với bản đang chạy trước khi nói 'chưa có'. Người đọc sẽ hỏi làm sao biết bản nào đang active, và làm sao khỏi ghi đè routing do người duyệt đặt.
