---
id: 2026-10-29-commit-chi-phan-cua-minh-khi
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2176", "claude:0faf0bb2#L2184", "claude:0faf0bb2#L2191", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3924", "claude:0faf0bb2#L3927"]
hook: "Repo bừa bộn, mình vẫn commit đúng 20 file của mình"
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

# Commit chỉ phần của mình khi repo có thay đổi người khác đang stage

**Bối cảnh:** Repo ở nhánh main có sẵn thay đổi đã stage của người khác ở thư mục company. Mình cần commit tài liệu nghiên cứu mà không đụng vào phần đó.
**Chuyện gì xảy ra:** Mình tạo nhánh mới và dùng một file index Git tạm qua biến GIT_INDEX_FILE, chỉ nạp các file của mình, rồi commit. Commit đầu gồm 20 file, phần đang dở ở company không đổi. Lần thứ hai làm đúng cách này cho commit tài liệu Multica và nghiên cứu đóng gói.
**Bài học:** Khi cần commit một phần trong repo đang có thay đổi dở của người khác, dùng index tạm để tách phạm vi thay vì stash hay reset.
**Artefact:** Kết quả git show --stat cho commit, đã cắt tên nhánh nếu cần.
