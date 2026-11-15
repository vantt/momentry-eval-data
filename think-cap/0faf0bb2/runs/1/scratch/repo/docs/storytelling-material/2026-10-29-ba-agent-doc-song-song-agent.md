---
id: 2026-10-29-ba-agent-doc-song-song-agent
date: 2026-10-29
repo: repo
status: raw
signals: [người duyệt thứ máy soạn]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L577", "claude:0faf0bb2#L578", "claude:0faf0bb2#L588", "claude:0faf0bb2#L1773", "claude:0faf0bb2#L1774", "claude:0faf0bb2#L1886", "claude:0faf0bb2#L1887"]
hook: "Ba agent đọc code thay tôi, nhưng chỉ ghi lesson sau khi mở lại từng dòng"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba agent đọc song song, agent chính kiểm trích dẫn trước khi ghi lesson

**Bối cảnh:** Cần kiểm kê Paperclip và Kaneo theo nhiều mảng, mỗi mảng là một tầng khác nhau.
**Chuyện gì xảy ra:** Ba agent con đọc song song các mảng schema, runtime và giao diện. Agent chính không tin kết quả ngay: nó mở lại từng đường dẫn và số dòng được trích, so khớp, rồi mới ghi lesson. Các trích dẫn chính đều khớp, và các lesson được gắn bằng chứng với số commit đã ghim.
**Bài học:** Tách việc đọc khỏi việc kiểm chứng: người tổng hợp nên mở lại nguồn cho mọi trích dẫn quan trọng trước khi ghi kết luận.
**Artefact:** Bảng ba mảng kiểm kê với số dòng trích dẫn.
**Góc người ngoài:** cách làm phổ biến là Thường người ta đọc repo tay hoặc hỏi AI một câu rồi tin luôn kết quả; ít ai chia việc đọc song song theo chủ đề và kiểm lại từng dòng trích dẫn trước khi lưu thành ghi chú dài hạn; ở đây khác ở Kết quả có bằng chứng dòng code có thể kiểm chứng, nên tài liệu so sánh không chỉ là ý kiến; người đọc muốn biết cách làm để tránh AI bịa tên hàm hay số dòng.
