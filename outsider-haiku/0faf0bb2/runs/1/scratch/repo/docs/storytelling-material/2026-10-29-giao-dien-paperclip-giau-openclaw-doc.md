---
id: 2026-10-29-giao-dien-paperclip-giau-openclaw-doc
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1523", "claude:0faf0bb2#L1533", "claude:0faf0bb2#L1540", "claude:0faf0bb2#L1550", "claude:0faf0bb2#L1574"]
hook: "Giao diện giấu OpenClaw, đọc registry mới biết nó chỉ là nhân viên thuê ngoài"
tension: tuong_ma_hoa_ra
sides: ["OpenClaw trông như agent được hỗ trợ", "registry ghi mọi capability đều tắt, chỉ là thuê ngoài"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giao diện Paperclip giấu OpenClaw: đọc registry mới biết ai được hỗ trợ thật

**Bối cảnh:** Khi tạo agent trên UI, Paperclip không cho chọn adapter OpenClaw và chỉ hiện các CLI khác. Cảm giác là Paperclip tự là runtime.
**Chuyện gì xảy ra:** Registry hiển thị OpenClaw với comingSoon và hideFromVisualSelection. Capability của OpenClaw là ALL_FALSE, tức không có bundle chỉ dẫn, không đồng bộ skill, không chọn model, trong khi claude_local và codex_local bật đủ. Hướng mặc định của Paperclip là tự chạy agent qua một Runner viết bằng Rust. Vì vậy OpenClaw chỉ là nhân viên thuê ngoài.
**Bài học:** Thứ người dùng thấy trên menu không phản ánh đầy đủ mức hỗ trợ. Đọc registry và capability của UI để biết tính năng nào thật sự có.
**Artefact:** Đoạn cấu hình registry có chú thích comingSoon, đã cắt gọn.
