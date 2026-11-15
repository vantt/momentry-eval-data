---
id: 2026-11-02-pyyaml-khong-nap-duoc-vi-co
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3242"]
hook: "Cờ cách ly Python giấu luôn thư viện PyYAML vừa cài"
tension: giup_ma_hai
sides: ["cờ -I thêm vào để cách ly cho an toàn", "nó ẩn luôn user site nơi PyYAML nằm"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PyYAML không nạp được vì cờ -I giấu user site

**Bối cảnh:** Probe YAML trên Windows không thấy PyYAML cài bằng pip --user.
**Chuyện gì xảy ra:** Cờ -I gồm -E, -s và -P. Cờ -s ẩn user site, đúng nơi pip --user cài thư viện. Đổi sang -E -P: vẫn bỏ biến môi trường PYTHON*, vẫn không đưa thư mục script hay cwd vào sys.path, nhưng thấy được user site. Yêu cầu Python từ 3.11 trở lên.
**Bài học:** Cờ -I không chỉ là chạy sạch. Nó tắt cả user site.
**Artefact:** Không có.
