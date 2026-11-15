---
id: 2026-10-09-test-evaluation-can-binary-build-san-4257
code: M-YGJ0
aliases: [M-YGJ0]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Chuyện lặt vặt trong test, nhưng minh hoạ test phụ thuộc vào artefact đã build và file ẩn trong workspace."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1071", "omp:cd4449ab#L1072", "omp:cd4449ab#L1074", "omp:cd4449ab#L1075", "omp:cd4449ab#L1077", "omp:cd4449ab#L1086", "omp:cd4449ab#L1087", "omp:cd4449ab#L1089", "omp:cd4449ab#L2845", "omp:cd4449ab#L2858", "omp:cd4449ab#L2860", "omp:cd4449ab#L2869", "omp:cd4449ab#L2881", "omp:cd4449ab#L2887", "omp:cd4449ab#L2888", "omp:cd4449ab#L2890"]
hook: "Test đỏ ba lần liền, chỉ vì thiếu một file schema-version"
tension: nho_ma_to
sides: ["test đỏ tưởng lỗi code lớn", "thiếu binary, manifest và một file nhỏ"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test evaluation: cần binary build sẵn, manifest, schema-version

**Bối cảnh:** Test evaluation chạy lệnh skillhub theo đường dẫn ./bin/skillhub và so với manifest đã commit.
**Chuyện gì xảy ra:** Lần đầu test đỏ vì chưa có ./bin/skillhub; agent thử chạy bằng subprocess Python và cũng lỗi vì không có binary. Sau đó rebuild, chạy trực tiếp, và cập nhật manifest: experiment_id thành cli-replay-v1. Thư mục overlay không có .skillhub/schema-version nên kiểm tra thất bại thêm một lần.
**Bài học:** Test chạy binary phải tự build hoặc báo rõ thiếu; đừng để agent đoán.
**Artefact:** Không cần ảnh.
