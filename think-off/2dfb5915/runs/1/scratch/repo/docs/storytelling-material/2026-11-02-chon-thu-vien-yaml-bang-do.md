---
id: 2026-11-02-chon-thu-vien-yaml-bang-do
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L335"]
hook: "Cả 5 thư viện YAML đều 0 lệch, đến khi thử 25.000 note"
tension: tuong_ma_hoa_ra
sides: ["bộ kiểm cũ cho cả năm ứng viên 0 lệch", "25.000 note ngẫu nhiên lộ lệch hơn 20.000 ca"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chọn thư viện YAML bằng đo: 0 lệch so với 35 đến 36 lệch

**Bối cảnh:** Cần thư viện YAML khớp với PyYAML. Có năm ứng viên.
**Chuyện gì xảy ra:** Bộ kg-solo không phân biệt được các ứng viên, cả năm đều 0 lệch. Dùng 58 ca biên và 25.000 note sinh ngẫu nhiên thì khác: unsafe-libyaml cộng lớp tương thích cho 0 lệch. libyaml-safer panic khi khối block là giá trị cuối (242 note). serde_norway lệch 35 ca biên và 20.916 note. saphyr lệch 36 ca và 21.317 note.
**Bài học:** Ứng viên kém lộ ra ở ca biên, không ở bộ chuẩn thông thường. Cần bộ ca biên có chủ đích.
**Artefact:** Bảng năm ứng viên với số lệch ở từng bộ.
**Góc người ngoài:** cách làm phổ biến là Thường chọn thư viện theo độ phổ biến hoặc cảm nhận, quyết định kiến trúc theo lời khuyên chung, ít khi đo đối chiếu với hành vi gốc; ở đây khác ở Người đọc muốn thấy cách biến một câu hỏi 'cái nào tốt hơn' thành con số so sánh có thể kiểm lại, kể cả khi phải chạy song song hai bản.
