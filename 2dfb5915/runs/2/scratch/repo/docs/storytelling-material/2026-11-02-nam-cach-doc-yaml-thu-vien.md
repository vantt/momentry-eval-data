---
id: 2026-11-02-nam-cach-doc-yaml-thu-vien
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "Thư viện 'an toàn' bị loại vì panic ngay trên note thật"
tension: tuong_ma_hoa_ra
sides: ["thư viện tên safer, tưởng an toàn", "panic trên note thật"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Năm cách đọc YAML: thư viện libyaml-safer bị loại vì panic trên note thật

**Bối cảnh:** Phase 02 so năm cách đọc YAML frontmatter với PyYAML trên bộ ca biên và note sinh ngẫu nhiên.
**Chuyện gì xảy ra:** unsafe-libyaml cộng lớp tương thích cho 0 lệch trên 58 ca biên và 25.000 note sinh ngẫu nhiên. Dùng saphyr trực tiếp lệch 21.317 note, serde_norway lệch 20.916. libyaml-safer panic khi block scalar nằm cuối frontmatter, một hình dạng phổ biến trong note thật. Lỗi này đã được báo ở upstream.
**Bài học:** Thư viện đúng kiểu dữ liệu vẫn có thể lệch ở chi tiết. Kiểm bằng fuzz so với bản gốc, đừng kiểm bằng vài ví dụ.
**Artefact:** Bảng số lệch theo từng ứng viên. Không đưa nội dung note.
