---
id: 2026-11-02-job-macos-bi-huy-vi-cho
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3461", "claude:2dfb5915#L3551", "claude:2dfb5915#L3684"]
hook: "Job macOS bị huỷ hai lần, lỗi hoá ra không nằm ở code"
tension: tuong_ma_hoa_ra
sides: ["job bị huỷ trông như lỗi code", "thật ra runner chờ quá 15 phút, rerun là qua"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Job macOS bị huỷ vì chờ runner, chạy lại thì qua

**Bối cảnh:** Release rc.2 và CI nhiều lần đỏ, không do code.
**Chuyện gì xảy ra:** Job dựng binary macOS chờ runner quá 15 phút rồi bị GitHub huỷ. Việc này lặp lại ở rc.1 và rc.2. Một lần rerun gặp lỗi HTTP 500 nên phải thử lại. Đọc log trước khi sửa giúp biết lỗi nằm ở hạ tầng hay ở code.
**Bài học:** Job đỏ vì hàng đợi runner khác với job đỏ vì code. Đọc log trước khi sửa.
**Artefact:** Không có.
**Góc người ngoài:** cách làm phổ biến là Thường người ta đẩy commit mới để thử lại, làm loãng lịch sử và đôi khi che mất lỗi thật; ở đây khác ở Người đọc sẽ hỏi làm sao phân biệt CI đỏ do code hay do hạ tầng, và rerun đúng job nào mà không tốn phút Actions.
