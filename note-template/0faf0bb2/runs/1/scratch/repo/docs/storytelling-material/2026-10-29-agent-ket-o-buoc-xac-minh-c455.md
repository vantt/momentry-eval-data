---
id: 2026-10-29-agent-ket-o-buoc-xac-minh-c455
code: M-7FWS
aliases: [M-7FWS]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L891", "claude:0faf0bb2#L947", "claude:0faf0bb2#L959", "claude:0faf0bb2#L972", "claude:0faf0bb2#L987", "claude:0faf0bb2#L989", "claude:0faf0bb2#L1021", "claude:0faf0bb2#L1036"]
hook: "Ba agent kẹt 'verifying' chỉ vì lệch giao thức 3 và 4"
tension: nho_ma_to
sides: ["Lỗi chung chung, không nói rõ nguyên nhân", "Nội dung giao thức không đổi, hạ mức tối thiểu ở ba chỗ là cả ba sang ready"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người chạy bằng AI agent; người làm đang thử Paperclip trên máy để dựng một công ty mẫu, và ba agent kẹt ở bước 'verifying' vì lệch phiên bản giao thức. Người làm tin adapter phải khớp đúng bản 4 với gateway, nhưng lịch sử commit cho thấy nội dung giao thức không đổi giữa bản 3 và 4. Hạ mức tối thiểu xuống 3 thì cả ba agent sang ready, nên ai nối hai hệ thống lệch phiên bản nên đọc commit trước khi vá."
audience: dev nối công cụ điều phối agent với runtime sẵn có
spine_context: fgOPC là bộ dựng công ty một người chạy bằng AI agent; người làm đang thử Paperclip trên máy này để dựng một công ty mẫu.
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: Chạy thử Paperclip và setup một công ty mẫu để xem có dùng được không.
spine_want_lines: ["claude:0faf0bb2#L724"]
spine_obstacle: Ba agent kẹt ở trạng thái 'verifying' vì adapter đòi giao thức bản 4 còn gateway chỉ nhận bản 3.
spine_obstacle_lines: ["claude:0faf0bb2#L948", "claude:0faf0bb2#L973"]
spine_turn: Tưởng adapter phải khớp đúng bản giao thức 4 với gateway; hoá ra nội dung giao thức không đổi giữa bản 3 và 4.
spine_turn_lines: ["claude:0faf0bb2#L960", "claude:0faf0bb2#L968"]
spine_action: "Hạ minProtocol từ 4 xuống 3 ở ba chỗ, giữ maxProtocol 4, lưu bản gốc .orig rồi khởi động lại Paperclip."
spine_action_lines: ["claude:0faf0bb2#L987", "claude:0faf0bb2#L988"]
spine_outcome: Probe kết nối pass và cả ba agent chuyển sang ready.
spine_outcome_lines: ["claude:0faf0bb2#L1016", "claude:0faf0bb2#L1034"]
spine_takeaway: "Khi nối hai hệ thống lệch phiên bản giao thức, đọc lịch sử commit bên kia xem thay đổi có chạm đến giao thức không trước khi vá, và giữ bản gốc để hoàn tác."
spine_takeaway_lines: ["claude:0faf0bb2#L968", "claude:0faf0bb2#L988"]
completeness: 7
---

# Agent kẹt ở bước xác minh vì lệch phiên bản giao thức 3 và 4

**Góc kể:** fgOPC là bộ dựng công ty một người chạy bằng AI agent; người làm đang thử Paperclip trên máy để dựng một công ty mẫu, và ba agent kẹt ở bước 'verifying' vì lệch phiên bản giao thức. Người làm tin adapter phải khớp đúng bản 4 với gateway, nhưng lịch sử commit cho thấy nội dung giao thức không đổi giữa bản 3 và 4. Hạ mức tối thiểu xuống 3 thì cả ba agent sang ready, nên ai nối hai hệ thống lệch phiên bản nên đọc commit trước khi vá.
**Bối cảnh:** Nối một công cụ điều phối với gateway của runtime agent đã có sẵn. Hai bên khai báo phiên bản giao thức khác nhau.
**Chuyện gì xảy ra:** Ba agent đứng ở trạng thái 'verifying' và báo lỗi chung, không nói rõ nguyên nhân. Bước kiểm tra cho thấy công cụ yêu cầu giao thức bản 4 trong khi gateway chỉ chấp nhận bản 3. Lịch sử commit của bên công cụ cho thấy nội dung giao thức không đổi giữa hai bản, nên hạ mức tối thiểu từ 4 xuống 3 ở ba chỗ trong bản đã cài, giữ bản 4 làm mức tối đa. Sau khi vá, probe kết nối báo pass và cả ba agent chuyển sang 'ready'. Lần đầu, script lấy token từ tiến trình đang chạy cũng lỗi KeyError vì biến môi trường không có trong shell.
**Bài học:** Khi nối hai hệ thống khác phiên bản, đọc lịch sử commit của bên kia để biết thay đổi có đụng đến giao thức không trước khi vá, và ghi lại bản gốc để hoàn tác.
**Artefact:** Ảnh dòng trạng thái 'verifying' chuyển sang 'ready' của ba agent. Che địa chỉ máy và token. Hoặc đoạn diff ba dòng minProtocol.
