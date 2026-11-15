---
id: 2026-10-29-reviewpolicy-khong-phai-cong-duyet-agent
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L1327", "claude:0faf0bb2#L1328", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313", "claude:0faf0bb2#L2328"]
hook: "Đặt 'chỉ người duyệt' mà agent vẫn tự đóng task, vì mình bật nhầm cơ chế"
tension: cam_ma_van_lot
sides: ["đã đặt reviewPolicy chỉ người duyệt", "agent vẫn tự đóng task, cổng thật là executionPolicy"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# reviewPolicy không phải cổng duyệt: agent tự đóng task dù đặt 'chỉ người duyệt'

**Bối cảnh:** Spike đặt reviewPolicy human_only cho task ngân sách. Agent finance vẫn chuyển task sang done trong 26 giây.
**Chuyện gì xảy ra:** Activity log cho thấy agent tự đổi trạng thái. Đọc lại code, mình thấy reviewPolicy chỉ được kiểm khi trả lời một lời xin xác nhận. Cổng review thật là executionPolicy với các bước review và approval, nhưng spike chưa đặt nó. Mình đính chính trong tài liệu so sánh và báo cáo rằng spike mới thử cái đầu tiên trong hai cơ chế.
**Bài học:** Hai cơ chế có tên gần giống có thể làm việc khác nhau. Trước khi kết luận một cổng 'có' hoặc 'không', kiểm tra đúng trường nào thực sự chặn hành động đó.
**Artefact:** Bảng hai trường reviewPolicy và executionPolicy, cạnh nhau, kèm trạng thái SEN-3 trong activity log.
