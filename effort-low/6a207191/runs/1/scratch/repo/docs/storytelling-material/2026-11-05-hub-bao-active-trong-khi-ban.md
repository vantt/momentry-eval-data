---
id: 2026-11-05-hub-bao-active-trong-khi-ban
date: 2026-11-05
repo: repo
status: raw
signals: [artefact nhìn được, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L1480", "claude:6a207191#L1489", "claude:6a207191#L1500", "claude:6a207191#L1503", "claude:6a207191#L1507", "claude:6a207191#L1515"]
hook: "Hub báo 'active', nhưng bản mới vẫn nằm chờ duyệt"
tension: tuong_ma_hoa_ra
sides: ["Hub báo skill đang active, nội dung khớp bản local", "Bản mới đang chờ duyệt mà trang web không hiện gì"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hub báo 'active' trong khi bản mới chờ duyệt, trang web không báo

**Bối cảnh:** Sau khi gửi bản mới, user thấy skill đã active dù chưa ai bấm duyệt.
**Chuyện gì xảy ra:** Agent so sánh bản hub đang phục vụ với thư mục local. Nội dung giống hệt, chỉ khác một dòng trống. Có một lần duyệt trước đó đã kích hoạt bản có routing. Agent ban đầu đoán cơ chế duyệt và kích hoạt, và nói là chưa biết chắc ai duyệt vì không xem được lịch sử từ máy khách. Trang skill không hiện gì về bản chờ duyệt, người dùng phải vào mục Waiting for review.
**Bài học:** Trạng thái active và bản gửi đang chờ phải hiện cạnh nhau. Nếu không, người duyệt sẽ tưởng bản đang chạy là bản mới nhất.
**Artefact:** Ảnh trang skill và mục Waiting for review. Che tên skill và địa chỉ hub.
**Góc người ngoài:** cách làm phổ biến là Người làm thường tin vào thông báo thành công hoặc giả định trạng thái, và chỉ phát hiện sai khi có người báo lại; ở đây khác ở Đối chiếu thông báo với trạng thái thật trên đĩa và trên máy khác. Người đọc sẽ hỏi: làm sao biết lệnh báo thành công nhưng thật ra chưa làm gì?.
