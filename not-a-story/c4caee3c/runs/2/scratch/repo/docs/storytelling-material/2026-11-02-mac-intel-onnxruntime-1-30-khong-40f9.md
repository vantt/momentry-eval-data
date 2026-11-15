---
id: 2026-11-02-mac-intel-onnxruntime-1-30-khong-40f9
code: M-8SXA
aliases: [M-8SXA]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L2546", "claude:c4caee3c#L2547", "claude:c4caee3c#L2553", "claude:c4caee3c#L2571", "claude:c4caee3c#L2604", "claude:c4caee3c#L2616", "claude:c4caee3c#L2894", "claude:c4caee3c#L2895"]
hook: "Một bản thư viện mới bỏ rơi cả đời máy Mac Intel"
tension: chon_mot_mat_mot
sides: ["Ghim bản cũ để giữ người dùng Mac Intel", "Đổi lại lệch điểm tìm kiếm +0,063 và −0,017"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho kho ghi chú Obsidian, chạy cục bộ dưới dạng plugin, server MCP và lệnh dòng lệnh, và người làm đang chuẩn bị bản phát hành đầu tiên cho Windows, Mac chip Apple và Linux. Mac Intel không dựng được vì thư viện onnxruntime-node 1.30 không còn bản cho chip Intel; người làm tưởng dựng qua Rosetta là cứu được, nhưng file đó không có trong gói npm. Thay vì bỏ hẳn Mac Intel, họ ghim bản 1.23.2 chỉ cho gói Intel, đo lệch trên cùng máy, rồi đưa quyết định cho người dùng. Ai phát hành phần mềm đa nền sẽ muốn biết cách tự đo mức lệch khi ghim một thư viện cũ."
audience: người làm release phần mềm đa nền
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho kho ghi chú Obsidian, chạy cục bộ dưới dạng plugin, server MCP và lệnh dòng lệnh. Người làm đang chuẩn bị bản phát hành đầu tiên cho Windows, Mac chip Apple và Linux."
spine_context_lines: [profile, "claude:c4caee3c#L2546"]
spine_want: "Giữ Mac Intel là nền bắt buộc, để mỗi bản phát hành có đủ 4 gói."
spine_want_lines: ["claude:c4caee3c#L2592"]
spine_obstacle: "Thư viện onnxruntime-node 1.30.0 mà upstream dùng không còn bản dựng cho Mac Intel, nên gói Intel không dựng được."
spine_obstacle_lines: ["claude:c4caee3c#L2546"]
spine_turn: "Tưởng dựng x64 qua Rosetta trên máy ARM sẽ cứu được Mac Intel; hoá ra file binding không có trong gói npm, nên cách đó không đi được."
spine_turn_lines: ["claude:c4caee3c#L2542", "claude:c4caee3c#L2546"]
spine_action: "Ghim onnxruntime-node 1.23.2 chỉ cho gói darwin-x64, đo lệch nDCG@5 trên cùng máy so với bản 1.30.0, rồi xin người dùng quyết."
spine_action_lines: ["claude:c4caee3c#L2585", "claude:c4caee3c#L2893"]
spine_outcome: "Gói Mac Intel dựng xong, smoke xanh. Người dùng chọn phát hành và chấp nhận hai mức lệch: multilingual +0,063, vi-synonym −0,017."
spine_outcome_lines: ["claude:c4caee3c#L2890", "claude:c4caee3c#L2899"]
spine_takeaway: "Khi upstream bỏ một nền, đo lệch trên cùng máy trước khi ghim bản cũ, và đặt ngưỡng chấp nhận trước khi đo."
spine_takeaway_lines: ["claude:c4caee3c#L2893"]
completeness: 7
---

# Mac Intel: onnxruntime 1.30 không còn file cho Intel, ghim 1.23.2 để giữ nền

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho kho ghi chú Obsidian, chạy cục bộ dưới dạng plugin, server MCP và lệnh dòng lệnh, và người làm đang chuẩn bị bản phát hành đầu tiên cho Windows, Mac chip Apple và Linux. Mac Intel không dựng được vì thư viện onnxruntime-node 1.30 không còn bản cho chip Intel; người làm tưởng dựng qua Rosetta là cứu được, nhưng file đó không có trong gói npm. Thay vì bỏ hẳn Mac Intel, họ ghim bản 1.23.2 chỉ cho gói Intel, đo lệch trên cùng máy, rồi đưa quyết định cho người dùng. Ai phát hành phần mềm đa nền sẽ muốn biết cách tự đo mức lệch khi ghim một thư viện cũ.
**Bối cảnh:** Release đầu tiên có Windows, Mac ARM và Linux. Mac Intel không dựng được vì onnxruntime-node 1.30 không có binding darwin-x64.
**Chuyện gì xảy ra:** Lead hỏi người dùng: bỏ Mac Intel hay ghim bản cũ. Người dùng chọn ghim, với điều kiện smoke xanh trên runner Intel và lệch nDCG@5 không quá 0,01. Gói được phát hành với hai mức lệch đã chấp nhận: multilingual +0,063 và vi-synonym −0,017. Lead cũng xác định đời máy: Mac từ M1 (2020) trở đi dùng được, Mac Intel thì không.
**Bài học:** Khi upstream bỏ một nền, tính trước hệ quả với khách (đời máy nào dùng được) và đặt điều kiện đo được trước khi chọn ghim.
**Artefact:** Bảng mức lệch từng hạng mục, không kèm câu hỏi.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường chỉ phát hành một nền, hoặc bỏ hẳn nền khó để khỏi phải giải thích; ở đây khác ở Một nền Mac Intel bị chặn bởi thư viện upstream, nhưng thay vì cắt bỏ, agent ghim phiên bản cũ, đo lệch, và người dùng chọn luật đơn giản hơn. Người đọc sẽ hỏi cách tự kiểm tra một bản ghim thay đổi kết quả đến đâu.
