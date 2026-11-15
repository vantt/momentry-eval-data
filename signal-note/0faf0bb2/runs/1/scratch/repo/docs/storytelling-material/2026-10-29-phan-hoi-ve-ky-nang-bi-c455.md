---
id: 2026-10-29-phan-hoi-ve-ky-nang-bi-c455
code: M-D9HE
aliases: [M-D9HE]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L248", "claude:0faf0bb2#L249"]
hook: "API từ chối kỹ năng với retryable=false, mình không thử lại"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phản hồi về kỹ năng bị API từ chối vì lỗi validation

**Bối cảnh:** Sau khi distill gr8r xong, mình gửi phản hồi về kỹ năng distill-repo.
**Chuyện gì xảy ra:** API trả invalid_request với retryable=false, nghĩa là trạng thái đối tượng không khớp yêu cầu. Mình không thử lại và chỉ ghi nhận. Đây là phản hồi từ phía người dùng ngược về nơi cấp kỹ năng.
**Bài học:** Ghi kèm mã lỗi và trạng thái khi phản hồi thất bại, để phân biệt đối tượng đã đóng với lỗi schema.
**Artefact:** Đoạn JSON lỗi, bỏ ID.
