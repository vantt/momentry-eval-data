---
id: 2026-11-02-so-khop-voi-ban-python-bang
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L397", "claude:2dfb5915#L1859"]
hook: "47 mục chưa có, đến cuối còn 64 khớp và 0 lệch"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# So khớp với bản Python bằng golden: từ 47 mục chưa có về 0 lệch

**Bối cảnh:** Đặc tả Python được ghim theo commit. Golden được dump từ bản Python trên vault tổng hợp kg-solo. CI so bản Rust với golden mà không cần Python.
**Chuyện gì xảy ra:** Bộ so khớp gồm 64 mục: bảng index, 81 câu đáp án, 712 lời gọi tool và đầu ra CLI. Giữa đợt, có 47 mục còn ghi chưa có. Khi các phase xong, kết quả là 64 mục khớp, 0 lệch, 0 mục chưa có. Vault thật không lên CI.
**Bài học:** Lấy hành vi của bản cũ làm golden rồi viết bộ so khớp trước. Đo tiến độ bằng số mục khớp, không bằng cảm giác.
**Artefact:** Biểu đồ số mục chưa có theo từng đợt merge, từ 64 xuống 0.
**Góc người ngoài:** cách làm phổ biến là Thường viết lại một phần mềm rồi kiểm bằng vài ca thử thủ công, hoặc tin là đúng khi test qua; ít khi có bộ so sánh đầy đủ theo từng bảng và từng câu trả lời; ở đây khác ở Người đọc sẽ hỏi làm sao biết bản mới giống bản cũ, và cách ghim golden theo commit để khi bản gốc đổi thì bản đối chiếu vẫn còn đúng.
