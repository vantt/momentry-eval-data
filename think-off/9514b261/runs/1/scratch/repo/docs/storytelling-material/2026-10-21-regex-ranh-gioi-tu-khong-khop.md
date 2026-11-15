---
id: 2026-10-21-regex-ranh-gioi-tu-khong-khop
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L811", "claude:9514b261#L816"]
hook: "Chữ đ trong 'để' làm regex ranh giới từ không khớp"
tension: tuong_ma_hoa_ra
sides: ["tưởng ranh giới từ hoạt động với mọi chữ", "trước đ có dấu, cả hai phía đều bị coi là không phải chữ"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Regex ranh giới từ không khớp chữ đ tiếng Việt: chú thích trong code ghi kết quả test trực tiếp

**Bối cảnh:** Agent đọc code cửa retrospective để tìm cách kiểm nội dung tài liệu.
**Chuyện gì xảy ra:** Chú thích trong retrospective-doors nói rằng ranh giới từ không khớp trước một ký tự có dấu như đ của chữ để, vì cả hai phía đều bị đọc là không phải chữ. Chú thích ghi đã xác nhận bằng test trực tiếp, không phải suy đoán. Agent chỉ đọc chú thích này trong lúc tìm code.
**Bài học:** Ranh giới từ trong regex không đáng tin với chữ Việt; kiểm bằng test trước khi dựa vào nó.
**Artefact:** Đoạn chú thích trong code, không kèm nội dung tài liệu.
