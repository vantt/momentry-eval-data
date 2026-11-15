---
id: 2026-10-29-kho-bai-hoc-tang-tu-12-c455
code: M-2DWC
aliases: [M-2DWC]
date: 2026-10-29
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L207", "claude:0faf0bb2#L227", "claude:0faf0bb2#L243", "claude:0faf0bb2#L349", "claude:0faf0bb2#L361", "claude:0faf0bb2#L613", "claude:0faf0bb2#L621", "claude:0faf0bb2#L1341", "claude:0faf0bb2#L1561", "claude:0faf0bb2#L1789", "claude:0faf0bb2#L1897", "claude:0faf0bb2#L1903", "claude:0faf0bb2#L2018", "claude:0faf0bb2#L2113", "claude:0faf0bb2#L2242", "claude:0faf0bb2#L2312", "claude:0faf0bb2#L3134"]
hook: "Mỗi lần sửa lỗi YAML bằng sed lại đẻ thêm lỗi ở dòng khác"
tension: giup_ma_hai
sides: ["Sửa nhanh bằng sed cho từng lỗi", "Mỗi lần sửa lại gây lỗi mới, kho bài học từ 12 lên 52 vẫn phải ghi bằng script kiểm tra"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người chạy bằng AI agent trên Multica; người làm dùng một skill để rút bài học từ các repo khác rồi ghi vào kho YAML của dự án. Người làm tưởng sửa một lỗi YAML bằng sed là gọn, chỉ đụng đúng dòng đó. Hoá ra có lần sed vừa sửa xong thì một file khác báo lỗi cấu trúc, và việc ghi lại bằng script có bước kiểm tra mới giữ kho ổn định khi lên 52 bài học. Ai nhờ AI sửa dữ liệu có cấu trúc sẽ gặp đúng chuyện này."
audience: dev dùng AI agent để sửa file cấu hình hoặc dữ liệu có cấu trúc
spine_context: fgOPC là bộ dựng công ty một người chạy bằng AI agent trên Multica; người làm dùng skill để rút bài học từ repo rồi ghi vào kho YAML của dự án.
spine_context_lines: [profile, "claude:0faf0bb2#L5"]
spine_want: Muốn học từ repo gr8r và ghi bài học vào kho dùng được.
spine_want_lines: ["claude:0faf0bb2#L5"]
spine_obstacle: Mỗi lần sửa lỗi YAML có thể đẩy lỗi sang dòng hoặc file khác.
spine_obstacle_lines: ["claude:0faf0bb2#L228", "claude:0faf0bb2#L349"]
spine_turn: Tưởng sed sửa đúng một dòng là đủ; hoá ra sed sửa xong thì file khác báo lỗi cấu trúc.
spine_turn_lines: ["claude:0faf0bb2#L204", "claude:0faf0bb2#L228"]
spine_action: Chuyển sang ghi lại bằng script có kiểm tra trước khi ghi.
spine_action_lines: ["claude:0faf0bb2#L360", "claude:0faf0bb2#L361"]
spine_outcome: "Kho ghi thành công, lên 52 bài học trong 8 file domain."
spine_outcome_lines: ["claude:0faf0bb2#L361", "claude:0faf0bb2#L3134"]
spine_takeaway: Sửa dữ liệu có cấu trúc bằng sed dễ đẩy lỗi sang chỗ khác; sinh lại từ nguồn có validator an toàn hơn.
spine_takeaway_lines: ["claude:0faf0bb2#L228", "claude:0faf0bb2#L361"]
completeness: 7
---

# Kho bài học tăng từ 12 lên 52 qua nhiều lần ghi, lỗi YAML đến từ sed

**Góc kể:** fgOPC là bộ dựng công ty một người chạy bằng AI agent trên Multica; người làm dùng một skill để rút bài học từ các repo khác rồi ghi vào kho YAML của dự án. Người làm tưởng sửa một lỗi YAML bằng sed là gọn, chỉ đụng đúng dòng đó. Hoá ra có lần sed vừa sửa xong thì một file khác báo lỗi cấu trúc, và việc ghi lại bằng script có bước kiểm tra mới giữ kho ổn định khi lên 52 bài học. Ai nhờ AI sửa dữ liệu có cấu trúc sẽ gặp đúng chuyện này.
**Bối cảnh:** Công cụ distill ghi bài học vào các file YAML theo domain, có bước kiểm tra và chấm điểm.
**Chuyện gì xảy ra:** Lần distill đầu ghi 12 bài học. Các lần sau cộng dồn: 17 sau khi chấm lại theo goal mới, 30 sau Paperclip, 38 sau Kaneo, 47 sau Multica, và 52 sau spike Multica + Claude Code. Trong quá trình có ba lỗi YAML do giá trị chứa dấu hai chấm hoặc điểm effort ngoài khoảng 1 đến 3. Mỗi lần sửa bằng sed lại gây lỗi mới ở dòng khác. Ghi lại bằng script có kiểm tra trước khi ghi thì ổn định hơn.
**Bài học:** Sửa dữ liệu có cấu trúc bằng sed dễ đẩy lỗi sang chỗ khác. Sinh lại từ nguồn có validator thì an toàn hơn.
**Artefact:** Biểu đồ số bài học theo lần ghi (dữ liệu trên).
