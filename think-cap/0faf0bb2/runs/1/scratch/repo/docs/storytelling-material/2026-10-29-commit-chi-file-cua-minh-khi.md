---
id: 2026-10-29-commit-chi-file-cua-minh-khi
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, artefact nhìn được]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:0faf0bb2#L2166", "claude:0faf0bb2#L2172", "claude:0faf0bb2#L2176", "claude:0faf0bb2#L2184", "claude:0faf0bb2#L2188", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3924"]
hook: "Repo đang có staged của người khác; một index tạm giúp commit đúng file của mình"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit chỉ file của mình khi repo có staged của người khác: dùng index file tạm

**Bối cảnh:** Repo đang ở main, có thay đổi đã stage và chưa stage thuộc phần việc khác, phần này không được commit cùng.
**Chuyện gì xảy ra:** Tạo nhánh mới, dùng biến GIT_INDEX_FILE trỏ tới một index tạm để stage đúng các file của mình, rồi commit. Staging gốc của repo giữ nguyên. Cách này được dùng lại lần thứ hai cho 20 file, và kết quả được kiểm bằng git show --stat.
**Bài học:** Dùng index file tạm để commit một tập file xác định mà không đụng vào staging của người khác.
**Artefact:** Đầu ra git show --stat của commit (danh sách file).
**Góc người ngoài:** cách làm phổ biến là Người ta hay git add -A hoặc commit toàn bộ, hoặc tự gỡ stage của người khác khi có xung đột; ở đây khác ở Agent tách commit theo file và giữ nguyên trạng thái của phần người khác; người đọc muốn biết cách làm này khi làm việc trong repo đang dở dang.
