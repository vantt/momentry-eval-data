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
hook: "Mac Intel bị bỏ rơi, ghim bản cũ để giữ lại"
tension: chon_mot_mat_mot
sides: ["Giữ Mac Intel bằng cách ghim bản cũ", "Chấp nhận hai mức lệch điểm, một mức +0,063"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mac Intel: onnxruntime 1.30 không còn file cho Intel, ghim 1.23.2 để giữ nền

**Bối cảnh:** Release đầu tiên có Windows, Mac ARM và Linux. Mac Intel không dựng được vì onnxruntime-node 1.30 không có binding darwin-x64.
**Chuyện gì xảy ra:** Lead hỏi người dùng: bỏ Mac Intel hay ghim bản cũ. Người dùng chọn ghim, với điều kiện smoke xanh trên runner Intel và lệch nDCG@5 không quá 0,01. Gói được phát hành với hai mức lệch đã chấp nhận: multilingual +0,063 và vi-synonym −0,017. Lead cũng xác định đời máy: Mac từ M1 (2020) trở đi dùng được, Mac Intel thì không.
**Bài học:** Khi upstream bỏ một nền, tính trước hệ quả với khách (đời máy nào dùng được) và đặt điều kiện đo được trước khi chọn ghim.
**Artefact:** Bảng mức lệch từng hạng mục, không kèm câu hỏi.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường chỉ phát hành một nền, hoặc bỏ hẳn nền khó để khỏi phải giải thích; ở đây khác ở Một nền Mac Intel bị chặn bởi thư viện upstream, nhưng thay vì cắt bỏ, agent ghim phiên bản cũ, đo lệch, và người dùng chọn luật đơn giản hơn. Người đọc sẽ hỏi cách tự kiểm tra một bản ghim thay đổi kết quả đến đâu.
