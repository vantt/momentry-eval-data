---
id: 2026-10-09-go-test-run-khong-khop-ten
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2693", "omp:cd4449ab#L2695"]
hook: "Test trỏ tới tên không tồn tại, vẫn in PASS xanh"
tension: tuong_ma_hoa_ra
sides: ["PASS nghĩa là test đã chạy và qua", "Không có test nào chạy cả"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# go test -run không khớp tên vẫn in PASS

**Bối cảnh:** Chạy test migration receipt sau khi đổi tên test.
**Chuyện gì xảy ra:** Lệnh go test -v với -run chỉ tới một tên không còn tồn tại. Output in 'testing: warning: no tests to run' rồi PASS, nên trông như xanh. Agent đọc đây là kết quả và đi tiếp, mãi về sau mới chạy lại đúng tên test.
**Bài học:** Với go test -run, luôn đọc dòng 'no tests to run'. PASS không có test nào không chứng minh gì.
**Artefact:** Hai dòng output, không cần che.
