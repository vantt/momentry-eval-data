---
id: 2026-11-02-job-macos-build-bi-huy-vi
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3461", "claude:2dfb5915#L3551", "claude:2dfb5915#L3657", "claude:2dfb5915#L3684"]
hook: "Build đỏ không phải do code: macOS chờ máy chạy 15 phút rồi bị huỷ"
tension: tuong_ma_hoa_ra
sides: ["Build đỏ thì tưởng code có lỗi", "Thật ra chỉ là chờ runner quá lâu nên bị huỷ"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Job macOS build bị huỷ vì chờ runner quá lâu, không phải lỗi code

**Bối cảnh:** Nhiều lần CI đỏ, mỗi lần đều đến từ job dựng binary macOS Intel hoặc ARM.
**Chuyện gì xảy ra:** GitHub huỷ job sau khoảng 15 phút chờ runner. Agent chạy lại đúng job lỗi và qua. Một lần rerun trả HTTP 500 và phải thử lại.
**Bài học:** Phân biệt job huỷ vì hạ tầng với job lỗi code trước khi sửa code.
**Artefact:** Danh sách run CI đỏ và xanh.
