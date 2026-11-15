---
id: 2026-10-21-kiem-doc-qua-han-khong-bao
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, "gốc nhỏ, lỗi to"]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1476", "claude:9514b261#L1477", "claude:9514b261#L1511"]
hook: "332 doc quá hạn 47–55 ngày, vì phép trừ ra NaN nên không ai được báo"
tension: nho_ma_to
sides: ["Một phép trừ chuỗi ISO với số", "332 doc quá hạn gần hai tháng mà không có cảnh báo nào"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm 'doc quá hạn' không bao giờ báo, vì so chuỗi ISO với số

**Bối cảnh:** Một check trong Knowledge Registry cảnh báo doc provisional quá hạn. Check có trong code và có test, và không ai thấy nó im lặng.
**Chuyện gì xảy ra:** Code trừ Date.now() cho trường updatedAt là chuỗi ISO, kết quả là NaN, nên điều kiện luôn sai. Hiện 332 doc provisional đã 47 đến 55 ngày không được cảnh báo.
**Bài học:** Kiểm kiểu dữ liệu đầu vào của phép so sánh thời gian; một check không bao giờ bắn thì cũng là lỗi.
**Artefact:** Một dòng code: chuỗi ISO trừ số ra NaN, kèm kết quả so sánh false.
