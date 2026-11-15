---
id: 2026-10-21-mo-phong-ghe-hoi-dong-sai-fd46
code: M-1K6Q
aliases: [M-1K6Q]
date: 2026-10-21
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L2584", "claude:9514b261#L2600", "claude:9514b261#L2612", "claude:9514b261#L2630", "claude:9514b261#L2645"]
hook: "Bảng mô phỏng chọn sai ghế vì thiếu herdr, agent tự đính chính"
tension: tuong_ma_hoa_ra
sides: ["Mô phỏng cho thấy openai qua codex, trần flagship chặn được", "Chạy thật: critical nâng lên fable, openai chỉ có codex-herdr, deepseek và glm không vào chuỗi"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là lớp nền để dựng ứng dụng agent, và người làm đang chọn model cho 11 ghế của một hội đồng nhiều bước. Agent tin bảng mô phỏng đúng và trần flagship trong config giới hạn được hội đồng. Khi chạy explain thật trên môi trường có herdr, các việc mức critical lại được nâng lên tầng frontier, còn openai chỉ chạy được qua một đường khác, nên bảng cũ sai ở nhiều ghế. Ai dựng agent nhiều bước nên học từ đây: đừng tin config hay mô phỏng thiếu điều kiện, hãy hỏi công cụ trên đúng môi trường."
audience: dev dựng agent chạy nhiều model theo bước
spine_context: "Forgent (fgOS) là lớp nền để dựng ứng dụng agent, đang ở giai đoạn alpha. Người làm đang chọn model cho 11 ghế của một hội đồng gồm nhiều bước."
spine_context_lines: [profile]
spine_want: "Có bảng model cho từng ghế hội đồng, cập nhật cho chủ dự án."
spine_want_lines: ["claude:9514b261#L2612"]
spine_obstacle: "Bảng mô phỏng chạy không có herdr, và openai cùng xai vẫn chưa chạy được."
spine_obstacle_lines: ["claude:9514b261#L2577", "claude:9514b261#L2630"]
spine_turn: "Tưởng trần maxTier flagship chặn được hội đồng và bảng mô phỏng là đúng. Hoá ra capability mức critical nâng lên frontier, còn openai chỉ đi được qua codex-herdr."
spine_turn_lines: ["claude:9514b261#L2605", "claude:9514b261#L2623", "claude:9514b261#L2630"]
spine_action: "Đính chính bảng cũ rồi đề xuất sửa cấu hình. Người làm đồng ý, và agent bắt đầu áp dụng ba thay đổi."
spine_action_lines: ["claude:9514b261#L2630", "claude:9514b261#L2645", "claude:9514b261#L2652"]
spine_takeaway: "Dùng công cụ explain thật trên đúng môi trường, đừng tin config hay mô phỏng thiếu điều kiện. Trần trong config có thể bị capability nâng lên."
spine_takeaway_lines: ["claude:9514b261#L2588", "claude:9514b261#L2630"]
completeness: 6
---

# Mô phỏng ghế hội đồng sai vì thiếu herdr, và trần flagship không chặn như agent tưởng

**Góc kể:** Forgent (fgOS) là lớp nền để dựng ứng dụng agent, và người làm đang chọn model cho 11 ghế của một hội đồng nhiều bước. Agent tin bảng mô phỏng đúng và trần flagship trong config giới hạn được hội đồng. Khi chạy explain thật trên môi trường có herdr, các việc mức critical lại được nâng lên tầng frontier, còn openai chỉ chạy được qua một đường khác, nên bảng cũ sai ở nhiều ghế. Ai dựng agent nhiều bước nên học từ đây: đừng tin config hay mô phỏng thiếu điều kiện, hãy hỏi công cụ trên đúng môi trường.
**Bối cảnh:** Agent đã đưa bảng model cho 11 ghế của hội đồng dựa trên mô phỏng gán vai và trần maxTier flagship trong config.
**Chuyện gì xảy ra:** Chủ dự án chưa đồng ý ngay. Agent chạy fgos dispatch explain thật và thấy capability mức critical nâng tầng lên frontier, nên shape, synthesize và explain chạy fable. Mô phỏng chạy không có herdr nên chọn openai qua codex, trong khi phiên thật có herdr thì openai chỉ có codex-herdr. Deepseek và glm không bao giờ vào chuỗi dự phòng vì walk chỉ được thu hẹp trong danh sách tierFallback. Agent tự đính chính bảng cũ rồi chủ dự án đồng ý đề xuất sửa.
**Bài học:** Dùng công cụ giải thích thật trên đúng môi trường, không tin config hay mô phỏng thiếu điều kiện. Một trần trong config có thể bị capability nâng lên.
**Artefact:** Bảng ghế theo explain, các cột bước, tầng, ghế chính, dự phòng. Không kèm tên tài khoản.
