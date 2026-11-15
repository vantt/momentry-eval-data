---
id: 2026-10-09-cong-cu-edit-tu-choi-15-4257
code: M-V876
aliases: [M-V876]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Sự cố vặt của agent, nhưng lặp lại nhiều lần và tốn vòng đọc lại; đáng ghi như một mẹo dùng công cụ."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L240", "omp:cd4449ab#L241", "omp:cd4449ab#L655", "omp:cd4449ab#L657", "omp:cd4449ab#L885", "omp:cd4449ab#L1003", "omp:cd4449ab#L1005", "omp:cd4449ab#L1108", "omp:cd4449ab#L1110", "omp:cd4449ab#L1167", "omp:cd4449ab#L1579", "omp:cd4449ab#L1951", "omp:cd4449ab#L2192", "omp:cd4449ab#L2642", "omp:cd4449ab#L2644", "omp:cd4449ab#L2668", "omp:cd4449ab#L2677", "omp:cd4449ab#L2678", "omp:cd4449ab#L2680", "omp:cd4449ab#L3130", "omp:cd4449ab#L3725", "omp:cd4449ab#L3818"]
hook: "Công cụ sửa file từ chối 15 lần, lần sau vẫn được nhận"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Công cụ edit từ chối ~15 lần vì nội dung đã đổi

**Bối cảnh:** Công cụ edit yêu cầu neo khớp với lần đọc gần nhất; khi chỉ đọc một đoạn ngắn hoặc kết quả tìm kiếm, neo dòng không khớp.
**Chuyện gì xảy ra:** Khoảng 15 lần edit bị từ chối: thiếu hunk header, neo vào dòng chưa từng hiển thị, hoặc ranh giới không xác định. Mỗi lần agent đọc lại vùng đó rồi gửi lại edit, và lần sau thì được chấp nhận.
**Bài học:** Đọc đúng vùng cần sửa trước khi edit, và neo vào dòng đã thấy; đỡ được vòng lặp từ chối.
**Artefact:** Không cần ảnh; có thể dán một mẫu lỗi đã che.
