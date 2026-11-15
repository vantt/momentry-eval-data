---
id: 2026-11-05-merge-thang-len-main-5-test
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2046", "claude:6a207191#L2063", "claude:6a207191#L2073", "claude:6a207191#L2080", "claude:6a207191#L2103", "claude:6a207191#L2122", "claude:6a207191#L2158", "claude:6a207191#L2190", "claude:6a207191#L2203", "claude:6a207191#L2221", "claude:6a207191#L2246"]
hook: "5 test Go chỉ lỗi trên máy tác giả vì test vô tình đọc file thật trong HOME"
tension: cam_ma_van_lot
sides: ["test đã đổi HOME sang thư mục tạm", "thư mục làm việc vẫn nằm trong repo, đọc được file cấu hình thật"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Merge thẳng lên main, 5 test Go chỉ lỗi trên máy tác giả: test không cách ly HOME và thư mục làm việc

**Bối cảnh:** Commit web đã qua test web. make check của repo chạy thêm test Go, và 5 test trong gói cli lỗi trên máy này.
**Chuyện gì xảy ra:** Agent stash để chứng minh lỗi có sẵn trên main trước commit. Điều tra cho thấy: test đổi HOME sang thư mục tạm nhưng thư mục làm việc vẫn nằm trong repo, nên status và doctor đi ngược lên tìm cấu hình dự án và gặp ~/.codex/config.toml và ~/.gemini/settings.json vừa được ghi lúc connect --global. Code coi thư mục nhà là một dự án, so đường dẫn binary và báo Connection files FAILED. CI không có hai file đó nên xanh. Trong lúc làm, ba commit từ một phiên khác đã vào main.
**Bài học:** Test xanh trên CI nhưng đỏ trên máy thường là rò rỉ môi trường. Test phải đổi cả thư mục làm việc và không được đọc cấu hình agent thật của máy.
**Artefact:** Bảng 5 test gồm kỳ vọng và lý do lỗi. Che đường dẫn và địa chỉ hub.
