---
id: 2026-11-02-bay-agent-chay-song-song-so-3c6e
code: M-QFGD
aliases: [M-QFGD]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L120", "claude:2dfb5915#L860", "claude:2dfb5915#L1094", "claude:2dfb5915#L1209", "claude:2dfb5915#L1445", "claude:2dfb5915#L1572", "claude:2dfb5915#L1859"]
hook: "Bảy agent song song, số mục thiếu giảm từ 47 về 0"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bảy agent chạy song song, số mục chưa có đếm ngược từ 47 về 0

**Bối cảnh:** Port lõi sang Rust, bộ so khớp đối chiếu từng mục với đầu ra của bản Python ở cùng commit đặc tả.
**Chuyện gì xảy ra:** Sau đợt đầu, bộ so khớp báo 47 trên 64 mục 'chưa có'. Các đợt merge sau giảm dần: 44, 34, 15, 1, rồi 0 khi mọi phase lõi đã vào main. Mỗi lần merge đều chạy lại bộ so khớp, nên con số là kết quả đo chứ không phải tự báo.
**Bài học:** Dùng một bộ so khớp chạy được làm thước đo tiến độ thay cho lời tự báo cáo.
**Artefact:** Bảng số 'chưa có' qua từng lần merge (chỉ số, không có tên note).
**Góc người ngoài:** cách làm phổ biến là Thường báo 'xong' dựa trên cảm nhận hoặc vài test đơn lẻ; ở đây khác ở Mỗi phase có một lệnh so khớp đếm được số mục khớp và số lệch chưa đặt tên, được chạy lại trên CI mỗi lần push. Người đọc muốn biết cách đo 'xong' bằng con số thay vì lời nói của AI.
