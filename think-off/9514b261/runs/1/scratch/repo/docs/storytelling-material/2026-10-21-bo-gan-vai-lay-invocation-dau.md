---
id: 2026-10-21-bo-gan-vai-lay-invocation-dau
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2557", "claude:9514b261#L2630", "claude:9514b261#L2734", "claude:9514b261#L2825"]
hook: "Tài khoản đầu tiên chưa từng được dùng vì một đường thừa chiếm lượt"
tension: nho_ma_to
sides: ["một đường codex thừa đứng trước trong thứ tự", "tài khoản đầu tiên chưa bao giờ được dùng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ gán vai lấy invocation đầu tiên: một đường thừa chiếm lượt của đường khác

**Bối cảnh:** Để openai dùng đường pi có tài khoản đã đăng nhập, em phải hiểu thứ tự chọn invocation.
**Chuyện gì xảy ra:** Đường codex đứng trước pi trong thứ tự nên codex chiếm lượt, và tài khoản đầu tiên chưa bao giờ được dùng. Explain cho thấy openai chỉ có một invocation herdr là codex, và đường pi bị loại vì không có kho codex. Em thêm invocation pi-herdr đặt trước codex-herdr; probe trả OK với exit 0 sau 26 giây.
**Bài học:** Thứ tự invocation là luật chọn; một đường thừa đặt trước có thể chiếm lượt âm thầm. Dùng explain để xem đường được chọn thật.
**Artefact:** Đoạn thứ tự invocation trước và sau khi sửa, không ghi khoá.
