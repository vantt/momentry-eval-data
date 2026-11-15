---
id: 2026-11-02-ci-do-lien-tiep-vi-ba-40f9
code: M-8NZ2
aliases: [M-8NZ2]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3288", "claude:c4caee3c#L3312", "claude:c4caee3c#L3399", "claude:c4caee3c#L3405", "claude:c4caee3c#L3875", "claude:c4caee3c#L3912"]
hook: "CI đỏ ba lần liên tiếp, mỗi lần một nguyên nhân khác"
tension: nho_ma_to
sides: ["Mỗi lần chỉ sửa một lỗi", "Ba nguồn trôi khác nhau, CI đỏ ba lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đỏ liên tiếp vì ba nguồn khác nhau cùng trôi

**Bối cảnh:** Ba lần catchup liên tiếp hỏng, mỗi lần ở một chỗ khác nhau. Lỗi tự động tạo issue trên repo fork.
**Chuyện gì xảy ra:** Lần đầu: test tie-order làm hỏng. Lần hai: mục upstream-no-pack so điểm 0,735 đo trên máy này với 0,728 đo trên runner, vượt ngưỡng 0,005. Lần ba: hai workflow tải fixture ở tag v0.10.0 cố định, trong khi bộ eval đã chuyển sang v0.11.0. Việc sửa mục cổng đổi từ so với baseline đã ghi sang so với upstream đo trong cùng lần chạy. Cuối cùng catchup xanh và đẩy tag mới.
**Bài học:** Đừng hard-code tag hoặc baseline ở nhiều nơi. Lấy phiên bản từ một nguồn duy nhất, và so sánh trong cùng một lần chạy.
**Artefact:** Tiêu đề issue tự động (không nhạy cảm).
