---
id: 2026-10-21-mo-phong-ghe-sai-vi-thieu
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định, điều tưởng đúng hoá sai]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1906", "claude:9514b261#L2612", "claude:9514b261#L2630", "claude:9514b261#L3987", "claude:9514b261#L3993"]
hook: "Bảng ghế đủ 11/11 trên giấy, chạy thật vẫn thất bại"
tension: tuong_ma_hoa_ra
sides: ["Mô phỏng báo đủ 11/11 ghế, trần flagship tưởng chặn được", "Chạy thật bước shaping vẫn lỗi vì mô phỏng thiếu một cờ"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô phỏng ghế sai vì thiếu cờ herdr, và 'trần flagship' hoá ra không chặn

**Bối cảnh:** Agent dựng bảng 11 ghế cho hội đồng bằng bộ mô phỏng gán vai, rồi kết luận trần maxTier flagship chặn các ghế critical.
**Chuyện gì xảy ra:** Bộ mô phỏng chạy không có herdr nên gán openai qua đường khác với phiên thật. Lệnh explain (có herdrPresent) cho thấy các capability critical nâng trần lên frontier. Bảng ghế trước đó sai ở các ghế critical. Khi chạy thật, bước shaping vẫn báo execution-failure dù bảng trên giấy đủ 11/11.
**Bài học:** Đo đường quyết định thật (explain, trong đúng môi trường) thay vì mô phỏng thiếu cờ. Bảng trên giấy không chứng minh ghế chạy được.
**Artefact:** Bảng ghế hai cột: mô phỏng và explain thật, đặt cạnh nhau.
