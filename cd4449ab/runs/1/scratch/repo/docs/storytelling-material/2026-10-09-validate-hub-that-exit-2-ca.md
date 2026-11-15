---
id: 2026-10-09-validate-hub-that-exit-2-ca
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1726", "omp:cd4449ab#L1729", "omp:cd4449ab#L1731", "omp:cd4449ab#L1732", "omp:cd4449ab#L1734", "omp:cd4449ab#L1870", "omp:cd4449ab#L1872"]
hook: "Tưởng migration làm hỏng hub, hoá ra binary main cũng exit 2"
tension: tuong_ma_hoa_ra
sides: ["Nghi migration gây lỗi validate", "Binary main chưa migrate cũng lỗi y hệt"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Validate hub thật exit 2 cả trên binary main: lỗi có sẵn, không do migration

**Bối cảnh:** Lead hỏi cảnh báo missing_examples có sẵn trước migration hay không.
**Chuyện gì xảy ra:** Agent chạy validate bằng binary main trên workspace hub, và lệnh thoát với code 2 cùng thông báo FIX. Điều này cho thấy lỗi validate tồn tại trước khi migration. Grep chỉ ra rule missing_examples nằm trong lint.go. Warning này vẫn cần xác nhận riêng.
**Bài học:** Trước khi quy lỗi cho thay đổi của mình, chạy cùng câu lệnh bằng binary cũ để có baseline.
**Artefact:** Đầu ra validate của binary main, che tên skill.
