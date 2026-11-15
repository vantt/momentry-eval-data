---
id: 2026-10-29-commit-dung-phan-cua-minh-khi-c455
code: M-8QWK
aliases: [M-8QWK]
date: 2026-10-29
repo: repo
status: raw
signals: [lỗi quy trình]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:0faf0bb2#L2176", "claude:0faf0bb2#L2184", "claude:0faf0bb2#L2189", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3924"]
hook: "Index git riêng giúp commit đúng 20 file mà không đụng phần đã stage của người khác"
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

# Commit đúng phần của mình khi repo có thay đổi người khác đã stage: dùng index file riêng

**Bối cảnh:** Repo có thay đổi chưa commit của người khác, và một phần đã được stage sẵn.
**Chuyện gì xảy ra:** Agent tạo nhánh mới và dùng GIT_INDEX_FILE riêng để commit đúng 20 file của mình, không đụng index chung. Thay đổi trong company/ vẫn để nguyên và không lẫn vào commit. Lần commit sau cũng làm như vậy.
**Bài học:** Dùng GIT_INDEX_FILE riêng để commit mà không xoá phần staging của người khác.
**Artefact:** Kết quả git show --stat. Đã che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường git add . rồi commit, dễ kéo theo thay đổi dở của chính mình hoặc lộ token; ở đây khác ở Agent giữ nguyên phần `company/` đang dở, quét token trong docs, và chỉ commit đúng phần của phiên. Người đọc sẽ muốn biết cách làm này an toàn hơn commit thường.
