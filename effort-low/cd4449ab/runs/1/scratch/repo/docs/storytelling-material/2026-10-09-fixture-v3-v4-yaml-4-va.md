---
id: 2026-10-09-fixture-v3-v4-yaml-4-va
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2717", "omp:cd4449ab#L2741", "omp:cd4449ab#L2746", "omp:cd4449ab#L2761", "omp:cd4449ab#L2768", "omp:cd4449ab#L2800", "omp:cd4449ab#L2809"]
hook: "Một chữ số '4' sau dấu | làm cả loạt test đỏ"
tension: nho_ma_to
sides: ["một ký tự thừa trong YAML", "decode lỗi, test migration đỏ nhiều lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture v3→v4: YAML |4 và receipt làm test đỏ nhiều lần

**Bối cảnh:** Viết test migration v3→v4 với fixture distill chứa YAML lồng trong chuỗi.
**Chuyện gì xảy ra:** Decode báo 'did not find expected key'. Nguyên nhân là chỉ thị block scalar |4 bị lồng sai trong chuỗi test; đổi thành | thì decode thành công. Test migration còn đỏ thêm vài lần vì schema-version không khớp với binary và vì các receipt cũ. Sau khi sửa, go test ./internal/migration PASS.
**Bài học:** Lỗi YAML trong fixture nhúng trong code test là lỗi nhỏ nhưng tốn nhiều vòng chạy lại; kiểm tra fixture bằng một parser độc lập trước.
**Artefact:** Đoạn YAML fixture trước và sau khi sửa chỉ thị block scalar.
