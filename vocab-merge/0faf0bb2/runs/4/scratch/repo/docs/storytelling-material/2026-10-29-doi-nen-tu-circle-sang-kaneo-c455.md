---
id: 2026-10-29-doi-nen-tu-circle-sang-kaneo-c455
code: M-Y38R
aliases: [M-Y38R]
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3271", "claude:0faf0bb2#L3279", "claude:0faf0bb2#L3287", "claude:0faf0bb2#L3288", "claude:0faf0bb2#L3290"]
hook: "Circle đẹp nhưng 60 trang động không xuất tĩnh được; Kaneo có sẵn tiếng Việt"
tension: chon_mot_mat_mot
sides: ["Giữ Circle với màn hình Triage và Agent đã ưng", "Đổi sang Kaneo build tĩnh được và có vi-VN"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi nền từ Circle sang Kaneo web: kiến trúc build và tiếng Việt quyết định

**Bối cảnh:** Ban đầu nghiêng về Circle vì phong cách Linear. Người dùng hỏi có nên làm nền từ Circle không.
**Chuyện gì xảy ra:** Circle dùng Next.js, không có API route và không có middleware. Khoảng 60 trang có route động cần đổi nếu muốn export tĩnh. Kaneo web build ra file tĩnh để đặt lên Workers Static Assets, và có 20 ngôn ngữ kể cả vi-VN. Đề xuất đổi thành Kaneo làm nền, mượn màn hình Triage và Agent từ Circle.
**Bài học:** Kiểu build quyết định chi phí hosting. Kiểm tra kiến trúc build và i18n trước khi chọn theo thẩm mỹ.
**Artefact:** Bảng so sánh Circle và Kaneo web.
