---
id: 2026-10-29-chon-nen-ui-circle-hay-kaneo
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế, artefact nhìn được]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3279", "claude:0faf0bb2#L3287", "claude:0faf0bb2#L3288", "claude:0faf0bb2#L3290"]
hook: "Chọn Kaneo thay Circle vì build tĩnh và tiếng Việt, không vì đẹp"
tension: tuong_ma_hoa_ra
sides: ["Tưởng thẩm mỹ quyết định nền UI", "Build tĩnh và sẵn vi-VN.json mới quyết định"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chọn nền UI: Circle hay Kaneo, thứ quyết định là build tĩnh và tiếng Việt chứ không phải thẩm mỹ

**Bối cảnh:** Circle có giao diện kiểu Linear đẹp và nhiều màn hình hơn cho agent. Kaneo là SPA trên Vite. Mục tiêu là chạy trên Cloudflare Workers.
**Chuyện gì xảy ra:** Circle dùng Next.js app router với khoảng 60 trang có route động, nên muốn đưa lên Workers phải thêm adapter hoặc xuất tĩnh từng trang. Kaneo build ra file tĩnh, đặt được thẳng lên Workers Static Assets, và có sẵn vi-VN.json cùng khoảng 20 ngôn ngữ khác. Đề xuất cuối cùng là lấy Kaneo làm nền và mượn màn hình từ Circle.
**Bài học:** Khi chọn nền cho một ứng dụng cần đặt lên hạ tầng cụ thể, kiểm build tĩnh và i18n trước, thẩm mỹ là tiêu chí sau.
**Artefact:** Bảng so sánh Circle và Kaneo theo license, kiến trúc, lên Cloudflare, tiếng Việt.
