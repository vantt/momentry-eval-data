---
id: 2026-11-02-chon-model-nhung-chenh-lech-nho
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2919"]
hook: "Model nhúng lớn hơn không thắng: chênh lệch nhỏ hơn nhiễu của bộ đo"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng nghĩ model lớn hơn sẽ tốt hơn", "Chênh lệch chỉ vài câu, nhỏ hơn nhiễu bộ đo"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chọn model nhúng: chênh lệch nhỏ hơn nhiễu của bộ đo

**Bối cảnh:** Đo năm cấu hình model và hai tuỳ chọn trên cùng corpus 255 câu.
**Chuyện gì xảy ra:** Chênh lệch nDCG@5 giữa các model chỉ vài câu, nhỏ hơn nhiễu của bộ đo. Model lớn hơn không thắng rõ, nên đề xuất giữ model mặc định và chỉ dùng model lớn cho hồ sơ chất lượng cao, sau khi đo lại trên vault thật.
**Bài học:** Với bộ đo vài trăm câu, đừng chọn model dựa trên chênh lệch dưới vài phần trăm.
**Artefact:** Bảng nDCG@5 theo model và tuỳ chọn. Không cần che.
