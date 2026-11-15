---
id: 2026-11-06-voi-email-gui-nguoi-mua-ve-f922
code: M-PVS7
aliases: [M-PVS7]
date: 2026-11-06
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c06"
sessions: ["claude:5a1e7c06"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c06#L14", "claude:5a1e7c06#L15", "claude:5a1e7c06#L16", "claude:5a1e7c06#L17"]
hook: "Email cho người mua vé: agent chỉ viết nháp, không bao giờ gửi"
tension: cam_ma_van_lot
sides: ["Agent có công cụ tự động gửi email ngay", "Nó chỉ ghi nháp ra file để người đọc duyệt"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Với email gửi người mua vé, agent viết bản nháp ra file markdown để user đọc lại, không gửi đi và không dán vào chat. Việc gọi điện cho địa điểm do user tự làm.

**Chuyện gì xảy ra:** Với email gửi người mua vé, agent viết bản nháp ra file markdown để user đọc lại, không gửi đi và không dán vào chat. Việc gọi điện cho địa điểm do user tự làm.
**Góc người ngoài:** cách làm phổ biến là Soạn email trong chat rồi gửi luôn, hoặc gửi thẳng qua công cụ tự động; ở đây khác ở Nội dung gửi tới người ngoài là việc không rút lại được, nên agent tách 'soạn' khỏi 'gửi'. Bản nháp nằm sẵn trong thư mục để user chỉnh và gửi khi đã chắc.
