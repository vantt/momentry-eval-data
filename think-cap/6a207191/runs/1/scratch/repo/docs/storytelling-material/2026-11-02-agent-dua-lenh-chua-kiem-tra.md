---
id: 2026-11-02-agent-dua-lenh-chua-kiem-tra
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L996", "claude:6a207191#L1007", "claude:6a207191#L1074", "claude:6a207191#L1084", "claude:6a207191#L1086", "claude:6a207191#L1102", "claude:6a207191#L1112"]
hook: "Agent đưa lệnh có cờ --user, mà cờ đó không hề tồn tại"
tension: giup_ma_hai
sides: ["Gợi ý lệnh để người dùng kết nối nhanh", "Cờ không tồn tại, lỗi còn gợi ý đúng cờ đó"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent đưa lệnh chưa kiểm tra: --user không tồn tại, client 0.8.0 lệch hub 0.12.0

**Bối cảnh:** Người dùng muốn kết nối skillstation trên máy này tới một hub nằm trên máy khác.
**Chuyện gì xảy ra:** Agent gợi ý lệnh connect --hub với cờ --user mà không chạy --help trước. CLI báo lỗi unknown argument --user, và thông báo lỗi còn gợi ý đúng cờ không tồn tại. Client là 0.8.0 trong khi hub là 0.12.0. Sau khi update lên 0.13.0 và connect bằng token file với --global, doctor báo Healthy.
**Bài học:** Chạy --help trước khi đưa lệnh cho người dùng. Khi gặp lỗi lạ, kiểm phiên bản hai đầu trước khi debug.
**Artefact:** Đoạn thông báo lỗi của CLI, đã bỏ địa chỉ hub.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường làm theo gợi ý trong thông báo lỗi, rồi mất thời gian khi lệnh gợi ý vẫn sai; ở đây khác ở Agent xem lỗi công cụ là thông tin để chẩn đoán và tách nguyên nhân khỏi thao tác của người dùng. Người đọc sẽ muốn biết cách làm vậy để khỏi phí vòng lặp thử sai.
