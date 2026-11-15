---
id: 2026-10-29-paperclip-co-runtime-rieng-khong-chi
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1523", "claude:0faf0bb2#L1533", "claude:0faf0bb2#L1540", "claude:0faf0bb2#L1574"]
hook: "Tưởng Paperclip chỉ điều phối, hóa ra nó tự làm runtime, OpenClaw chỉ là thuê ngoài"
tension: tuong_ma_hoa_ra
sides: ["Paperclip chỉ là lớp điều phối", "Nó có runner Rust riêng, OpenClaw chỉ là nhân viên thuê ngoài"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Paperclip có runtime riêng, không chỉ là UI điều phối

**Bối cảnh:** Khi tạo agent trên UI, không thấy lựa chọn adapter OpenClaw, chỉ thấy các CLI khác.
**Chuyện gì xảy ra:** Trong code, OpenClaw có comingSoon và hideFromVisualSelection, và mọi khả năng bị đặt ALL_FALSE. Paperclip cũng đi kèm một native runner viết bằng Rust, chạy trực tiếp các CLI agent như Claude Code và Codex. Nhận định trước đó 'Paperclip chỉ điều phối' bị sửa lại: hướng mặc định của nó là tự làm runtime, còn OpenClaw là nhân viên thuê ngoài.
**Bài học:** Để đánh giá một sản phẩm có phải runtime không, đọc registry và capability trong UI code, không chỉ đọc phần mô tả 'control plane'.
**Artefact:** Đoạn code registry rút gọn, chỉ giữ các trường comingSoon, hideFromVisualSelection.
