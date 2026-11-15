---
id: 2026-11-01-runtime-theo-tai-khoan-pi-omp
date: 2026-11-01
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, "số trước, số sau", người duyệt thứ máy soạn]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L2809", "claude:f0bf048d#L2862", "claude:f0bf048d#L2885", "claude:f0bf048d#L2938", "claude:f0bf048d#L2950", "claude:f0bf048d#L3049", "claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
hook: "Runtime offline chỉ vì đổi tên profile sau khi tạo lệnh bọc"
tension: nho_ma_to
sides: ["chỉ đổi tên một profile", "runtime OpenAI offline, daemon bỏ qua lệnh cũ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Runtime theo tài khoản: pi, omp và tên lệnh bọc

**Bối cảnh:** Multica gọi các CLI agent khác Claude (pi cho Codex và Grok, omp cho Gemini) qua runtime profile, mỗi tài khoản một lệnh bọc riêng.
**Chuyện gì xảy ra:** Runtime OpenAI ban đầu offline vì profile được đổi tên sau khi lệnh bọc được tạo, nên daemon bỏ qua lệnh cũ; chỉ tắt bật lại profile là lên. Model thật (gpt-6.1-sol, grok-4.7) khác model cấu hình (gpt-5.5, grok-4.6), do lúc đăng nhập chọn khác. Lượt chạy đầu tiên với 3 runtime đều hoàn thành: STU-10…14 không lỗi, trong đó Google và DuckDuckGo chặn truy cập từ máy chủ, chỉ Bing trả kết quả.
**Bài học:** Đặt tên lệnh bọc theo <công cụ>-<nhà cung cấp>-<tài khoản> để không trùng khi thêm tài khoản; sau khi đổi profile phải kiểm daemon có nhận lại không.
**Artefact:** Bảng ba runtime với lệnh, model mặc định và trạng thái online; che runtime ID và token.
**Góc người ngoài:** cách làm phổ biến là Cài một CLI duy nhất trên PATH, đăng nhập một tài khoản, hoặc chép credential giữa các user; ở đây khác ở Mỗi tài khoản là một runtime tách biệt, quota và credential không dẫm nhau; nâng cấp có đường lui. Người đọc muốn dùng nhiều tài khoản/model cho agent mà không rối.
