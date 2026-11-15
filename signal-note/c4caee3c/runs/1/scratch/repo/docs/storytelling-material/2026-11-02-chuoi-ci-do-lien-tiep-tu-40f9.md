---
id: 2026-11-02-chuoi-ci-do-lien-tiep-tu-40f9
code: M-5HA3
aliases: [M-5HA3]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2663", "claude:c4caee3c#L3288", "claude:c4caee3c#L3491", "claude:c4caee3c#L3709", "claude:c4caee3c#L3745", "claude:c4caee3c#L3912"]
hook: "Bốn lỗi một dòng làm CI đỏ liên tiếp, mất nhiều giờ"
tension: nho_ma_to
sides: ["Mỗi lỗi chỉ một dòng", "Cộng lại mất nhiều giờ chờ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi CI đỏ liên tiếp: từ thứ tự kết quả đồng điểm đến khác biệt giữa npm 11 và npm 12

**Bối cảnh:** Mỗi lần sửa một lỗi CI phải chờ lượt chạy 10 đến 20 phút, và một số lỗi chỉ lộ ra trên runner.
**Chuyện gì xảy ra:** Các lỗi nối tiếp: hai note cùng điểm đổi thứ tự tuỳ máy; test đọc kết quả npm pack theo dạng mảng nhưng npm 12 trả object; fixture tải tag v0.10.0 cố định trong khi bộ eval đã lên v0.11.0; và test đóng gói đòi file build chưa có trên CI. Mỗi lỗi chỉ là một dòng, nhưng cộng lại mất nhiều giờ chờ.
**Bài học:** Ghim phiên bản công cụ trong CI, đọc tag fixture từ một nguồn duy nhất, và so kết quả đồng điểm theo tập hợp chứ không theo thứ tự.
**Artefact:** Danh sách các lần CI đỏ kèm nguyên nhân (không kèm log có đường dẫn).
