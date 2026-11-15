---
id: 2026-11-03-hai-duong-gom-may-quet-rong
date: 2026-11-03
repo: repo
status: raw
signals: ["4"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L300", "claude:ab9a1dd8#L315", "claude:ab9a1dd8#L332"]
hook: "Máy quét sau phiên bỏ sót khoảnh khắc chỉ người làm mới biết"
tension: cam_ma_van_lot
sides: ["hook quét cả transcript sau mỗi phiên", "khoảnh khắc đáng kể chỉ người làm biết, phải đánh dấu bằng /bip"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai đường gom: máy quét rộng, người đánh dấu khoảnh khắc bằng /bip

**Bối cảnh:** Người dùng hỏi /bip là gì, sau khi đã có hook gom tự động sau phiên.
**Chuyện gì xảy ra:** /bip là lệnh tắt để người dùng đánh dấu ngay khoảnh khắc đáng kể đang làm, kèm một dòng ghi chú. Hook quét sau phiên chỉ bắt được dấu vết trong transcript như số đổi, lệnh lỗi hay git đảo ngược, còn /bip bắt được khoảnh khắc chỉ người làm biết.
**Bài học:** Máy gom rộng dựa trên dấu vết, người đánh dấu chính xác dựa trên điều chỉ họ biết. Cần cả hai để có chất liệu tốt.
**Artefact:** Prompt mẫu /bip, không có đường dẫn người dùng.
