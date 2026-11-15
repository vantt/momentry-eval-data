---
id: 2026-10-29-loi-nho-trong-spike-tao-agent
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L3486", "claude:0faf0bb2#L3569", "claude:0faf0bb2#L3571"]
hook: "Script tạo agent chết vì một màu thiếu mã hex 6 chữ số"
tension: nho_ma_to
sides: ["chỉ thiếu một mã màu hex", "API trả 400, cả script tạo workflow thất bại"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi nhỏ trong spike: tạo agent bằng script thất bại vì đọc JSON và tạo status cần màu hex

**Bối cảnh:** Khi dựng agent và workflow cho spike Multica + Claude, script tạo agent lỗi giải mã JSON, và script tạo trạng thái mới bị API từ chối.
**Chuyện gì xảy ra:** Lệnh CLI in ra output không phải JSON nên script Python ném JSONDecodeError. Sau đó tạo trạng thái 'sales review' bị API trả 400 vì màu phải là hex 6 chữ số. Mình thêm màu hex và chạy lại, lần này tạo được workflow và project.
**Bài học:** Khi gọi CLI từ script, kiểm kiểu output trước khi phân tích, và đọc kỹ yêu cầu định dạng của API trước khi gửi.
**Artefact:** Trích thông báo lỗi 400 đã cắt gọn.
