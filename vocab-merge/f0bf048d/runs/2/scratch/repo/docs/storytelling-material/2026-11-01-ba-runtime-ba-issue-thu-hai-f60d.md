---
id: 2026-11-01-ba-runtime-ba-issue-thu-hai-f60d
code: M-J071
aliases: [M-J071]
date: 2026-11-01
repo: repo
status: raw
signals: [artefact, người duyệt máy]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
hook: "Ba loại agent chạy xong cả, Gemini chỉ mất 30 giây"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba runtime, ba issue thử: hai lượt Pi và Grok, một lượt Gemini hoàn thành trong 30 giây

**Bối cảnh:** Thử thật ba runtime sau khi chúng online, mỗi runtime một agent thử.
**Chuyện gì xảy ra:** Năm issue Pi và Grok chạy xong không lỗi: một issue bị CAPTCHA và tự chuyển blocked, một issue lấy đúng dữ liệu web, hai issue comment và đóng đúng yêu cầu, một issue gom kết quả con. Gemini chạy 30 giây, comment đúng một lần rồi chuyển in_review. Agent làm đúng vai trong quy trình.
**Bài học:** Thử runtime bằng issue thật có đủ quy trình (comment một lần, đổi trạng thái), không chỉ kiểm lệnh --version.
**Artefact:** Bảng năm issue với kết quả từng issue (che tên).
