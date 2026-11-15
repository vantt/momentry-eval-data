---
id: 2026-11-02-release-ci-hong-nhieu-lan-vi
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L3288", "claude:c4caee3c#L3297", "claude:c4caee3c#L3312", "claude:c4caee3c#L3520", "claude:c4caee3c#L3709", "claude:c4caee3c#L3735", "claude:c4caee3c#L3745"]
hook: "Release CI đỏ ba lần, mỗi lần một lý do vặt khác nhau"
tension: nho_ma_to
sides: ["Mỗi lỗi chỉ là chi tiết vặt: định dạng, phiên bản, file chưa dựng", "Cả quy trình phát hành đỏ liên tiếp"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release CI hỏng nhiều lần vì npm 12 đổi định dạng và bản dựng chưa biên dịch

**Bối cảnh:** Workflow catchup chạy đủ các tầng test, eval, invariance và phát hành gói, dùng npm 12. Mỗi lần sửa phải chờ 10 đến 20 phút để CI chạy.
**Chuyện gì xảy ra:** Lần đỏ đầu do test npm pack đọc mảng trong khi npm 12 trả về object. Một lần khác do fixture ghim v0.10.0 trong khi bộ eval đã sang v0.11.0. Một lần khác, test đóng gói đòi file build/index.js trong khi tầng lang_vi chưa biên dịch gói. Mỗi lỗi mở một issue tự động, và agent đóng issue sau khi xanh.
**Bài học:** Đổi phiên bản công cụ có thể đổi định dạng đầu ra; ghim phiên bản fixture và tách rõ điều kiện đã biên dịch.
**Artefact:** Bảng các lần đỏ và nguyên nhân, không kèm log đầy đủ.
