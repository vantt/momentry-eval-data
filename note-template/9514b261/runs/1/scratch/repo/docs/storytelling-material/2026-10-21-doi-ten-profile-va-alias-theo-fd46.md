---
id: 2026-10-21-doi-ten-profile-va-alias-theo-fd46
code: M-SRM0
aliases: [M-SRM0]
date: 2026-10-21
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L2982", "claude:9514b261#L3070", "claude:9514b261#L3075", "claude:9514b261#L3118", "claude:9514b261#L3127", "claude:9514b261#L3153", "claude:9514b261#L3178", "claude:9514b261#L3579", "claude:9514b261#L3590", "claude:9514b261#L3600"]
hook: "Tạo xai-grok rồi xoá, đổi tên profile theo lệnh chủ dự án"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi tên profile và alias theo họ nhà cung cấp: tạo, xoá, rồi đổi lại theo lệnh chủ dự án

**Bối cảnh:** Chủ dự án muốn có alias omp cho xAI và đặt tên thống nhất. Trước đó alias omp-grok-vantt đã trỏ tới profile chưa có thư mục.
**Chuyện gì xảy ra:** Agent tạo profile xai-grok và alias, rồi chủ dự án yêu cầu thống nhất tên. Agent kiểm profile grok-vantt có 0 dòng đăng nhập trước khi đổi, xoá xai-grok, đổi tên thư mục pi và cập nhật config. Sau đó chủ dự án chọn tạo bốn profile omp còn thiếu, và agent tạo khung config không chứa đăng nhập.
**Bài học:** Hỏi trước khi tạo tên mới khi đã có tên đang dùng, và kiểm profile có dữ liệu đăng nhập trước khi đổi tên hay chuyển đi.
**Artefact:** Bảng alias sau khi thống nhất, chỉ tên alias và trạng thái có hay không đăng nhập.
