---
id: 2026-10-30-dat-ten-goi-theo-bo-ban-f60d
code: M-4K28
aliases: [M-4K28]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1146", "claude:f0bf048d#L1155"]
hook: "Gói đặt tên theo workspace nội bộ, nên suýt deploy nhầm chỗ"
tension: cam_ma_van_lot
sides: ["gói tên opc-studio mặc định vào workspace nội bộ", "đổi thành opc-content, thiếu env khách thì từ chối"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đặt tên gói theo bộ bán, không theo workspace: opc-studio đổi thành opc-content

**Bối cảnh:** Mỗi khách một workspace, khách mua bộ nào thì deploy bộ đó vào. Tên gói cũ dễ nhầm với workspace của chính mình.
**Chuyện gì xảy ra:** Đổi tên gói thành opc-content, bỏ deploy mặc định vào workspace nội bộ. Mọi deploy phải có file env của khách, thiếu thì công cụ từ chối. Kiểm bằng plan: bộ Content chỉ đổi phần Content và gỡ 3 agent SEO khỏi squad Marketing.
**Bài học:** Bắt buộc đích đến khi deploy (không có mặc định), và đặt tên gói theo thứ khách mua.
**Artefact:** Cây thư mục packages trước và sau.
