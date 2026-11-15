---
id: 2026-10-21-bo-probe-sau-ho-mo-hinh-fd46
code: M-W1Y2
aliases: [M-W1Y2]
date: 2026-10-21
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2191", "claude:9514b261#L2284", "claude:9514b261#L2357", "claude:9514b261#L2492", "claude:9514b261#L2557", "claude:9514b261#L2825", "claude:9514b261#L3219", "claude:9514b261#L3263", "claude:9514b261#L3342"]
hook: "Từ 1 lên 6 họ mô hình chạy được mà không sửa dòng code nào"
tension: tuong_ma_hoa_ra
sides: ["Tưởng lỗi nằm ở code probe", "Gốc là kho tài khoản chưa khai, sửa kho là chạy"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Forgent (fgOS) là nền tảng cho các ứng dụng agent, và trước khi mở một hội đồng kiến trúc, người làm cần biết họ mô hình nào thật sự chạy được. Ban đầu openai bị đánh dấu là hết phiên, cần đăng nhập lại. Hoá ra codex đã đăng nhập xong, chỉ bị chặn ở hộp thoại \"Trust this folder?\", và đường chạy được là pi với tài khoản đã khai trong fgOS. Dev dùng nhiều nhà cung cấp mô hình nên kiểm bằng lượt gọi thật, vì một cấu hình rỗng có thể làm họ lỗi mà không báo rõ."
audience: dev dùng nhiều nhà cung cấp mô hình AI qua CLI
spine_context: "Dự án Forgent (fgOS) là nền tảng cho các ứng dụng agent. Trước khi mở một hội đồng kiến trúc, người làm cần biết họ mô hình nào thật sự chạy được."
spine_context_lines: [profile, "claude:9514b261#L1815"]
spine_want: "Biết chắc họ nào chạy được và còn quota, để chọn các ghế cho hội đồng."
spine_want_lines: ["claude:9514b261#L1815", "claude:9514b261#L1940"]
spine_obstacle: "Kho tài khoản fgOS rỗng nên không theo dõi được quota. Codex đòi đăng nhập, còn gemini và xai lỗi ở khâu giao lệnh."
spine_obstacle_lines: ["claude:9514b261#L2191", "claude:9514b261#L2284"]
spine_turn: "Tưởng openai hết phiên, cần đăng nhập lại; hoá ra codex đã đăng nhập xong, chỉ dừng ở hộp thoại \"Trust this folder?\"."
spine_turn_lines: ["claude:9514b261#L2191", "claude:9514b261#L3263"]
spine_action: "Khai tài khoản vào config toàn cục, bỏ codex khỏi pool openai để pi đi trước, rồi probe lại từng họ."
spine_action_lines: ["claude:9514b261#L2492", "claude:9514b261#L2557"]
spine_outcome: "Ba tài khoản openai đều chạy được (24 đến 45 giây). Các họ đều gán được ghế, 11/11 ghế."
spine_outcome_lines: ["claude:9514b261#L3342", "claude:9514b261#L3353"]
spine_takeaway: "Trước khi kết luận hết phiên, hãy kiểm bằng lượt gọi thật qua đường đang dùng. Cấu hình rỗng có thể làm họ lỗi mà không báo rõ."
spine_takeaway_lines: ["claude:9514b261#L2191", "claude:9514b261#L3353"]
completeness: 7
---

# Bộ probe sáu họ mô hình: từ một họ chạy được lên đủ họ, nhờ sửa kho tài khoản chứ không nhờ đổi code

**Góc kể:** Dự án Forgent (fgOS) là nền tảng cho các ứng dụng agent, và trước khi mở một hội đồng kiến trúc, người làm cần biết họ mô hình nào thật sự chạy được. Ban đầu openai bị đánh dấu là hết phiên, cần đăng nhập lại. Hoá ra codex đã đăng nhập xong, chỉ bị chặn ở hộp thoại "Trust this folder?", và đường chạy được là pi với tài khoản đã khai trong fgOS. Dev dùng nhiều nhà cung cấp mô hình nên kiểm bằng lượt gọi thật, vì một cấu hình rỗng có thể làm họ lỗi mà không báo rõ.
**Bối cảnh:** Trước khi mở hội đồng kiến trúc, cần biết họ mô hình nào thật sự chạy được. Mỗi lượt probe là một lệnh rất ngắn, đọc-chỉ, trả lời OK.
**Chuyện gì xảy ra:** Lần probe đầu chỉ có claude chạy được, còn openai, gemini, xai, deepseek và glm đều lỗi. Sau khi chủ dự án copy lại session, deepseek và glm chạy được vì kho tài khoản có dữ liệu. Sau khi khai thêm tài khoản, openai chạy qua đường pi, xai qua omp sau 23 giây, và hai tài khoản dự phòng openai cũng chạy. Gemini chạy được nhưng run bị gắn inconclusive vì agent không trả đúng định dạng. Nguyên nhân gốc là fgOS không khai tài khoản nào, nên không biết quota và không tự chuyển.
**Bài học:** Với chuỗi nhà cung cấp, kiểm bằng lượt gọi thật là đáng tin nhất; cấu hình rỗng có thể làm các họ lỗi mà không báo rõ.
**Artefact:** Bảng sáu họ với cột kết quả và số giây, không kèm tên tài khoản hay email.
