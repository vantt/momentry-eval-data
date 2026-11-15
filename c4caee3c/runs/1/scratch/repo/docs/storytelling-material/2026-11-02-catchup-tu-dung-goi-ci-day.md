---
id: 2026-11-02-catchup-tu-dung-goi-ci-day
date: 2026-11-02
repo: repo
status: raw
signals: [khác, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3228", "claude:c4caee3c#L3397", "claude:c4caee3c#L3415", "claude:c4caee3c#L3868"]
hook: "Sau nhiều lần đỏ, CI tự đẩy tag với 12 asset cho 4 nền"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Catchup tự dựng gói: CI đẩy tag và bundle trọn vẹn sau nhiều lần đỏ

**Bối cảnh:** Mỗi lần push vào master chạy catchup. Nếu xanh thì đẩy tag và kích hoạt bước dựng gói.
**Chuyện gì xảy ra:** Qua nhiều lần đỏ liên tiếp vì test, cổng chất lượng, pin-effect và tag fixture, catchup cuối cùng tự đẩy v0.17.2-vantt.3 với 12 asset cho 4 nền. Đây là lần đầu chuỗi catchup sang bundles chạy trọn vẹn. Các issue lỗi được mở tự động và đóng khi xanh.
**Bài học:** Mỗi lần đỏ nên có một issue ghi nguyên nhân, và đóng issue ngay khi xanh.
**Artefact:** Trang danh sách lần chạy Actions, che địa chỉ nếu cần.
