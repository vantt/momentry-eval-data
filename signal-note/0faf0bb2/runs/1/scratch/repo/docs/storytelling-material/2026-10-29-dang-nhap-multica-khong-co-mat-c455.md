---
id: 2026-10-29-dang-nhap-multica-khong-co-mat-c455
code: M-2MZS
aliases: [M-2MZS]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L3643", "claude:0faf0bb2#L3649", "claude:0faf0bb2#L3656", "claude:0faf0bb2#L3752", "claude:0faf0bb2#L3765", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3784", "claude:0faf0bb2#L3806", "claude:0faf0bb2#L3849", "claude:0faf0bb2#L3856"]
hook: "Multica không có mật khẩu: mã đăng nhập chỉ nằm trong log"
tension: khac
sides: ["Chủ muốn đặt mật khẩu cho dễ vào", "Multica không có mật khẩu, chỉ có mã trong log hết hạn sau vài phút"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đăng nhập Multica không có mật khẩu: mã nằm trong log, rồi đặt mã cố định cho bản test

**Bối cảnh:** Chủ cần vào web UI của stack trên tailnet. Multica chỉ có đăng nhập bằng mã email (send-code và verify-code, cộng Google).
**Chuyện gì xảy ra:** Vì chưa cấu hình gửi thư nên mã xác nhận chỉ xuất hiện trong log backend và hết hạn sau vài phút. Chủ hỏi có cách đặt mật khẩu. Multica không có mật khẩu, nên mình dùng cờ MULTICA_DEV_VERIFICATION_CODE cho bản test: cờ này bị bỏ qua khi APP_ENV là production, và chỉ mở trong tailnet.
**Bài học:** Hệ tự host dùng mã email có thể không có lối vào nếu chưa cấu hình gửi thư; cờ dev chỉ nên bật khi môi trường không phải production.
**Artefact:** Không chụp. Nếu cần minh hoạ, che hoàn toàn mã.
