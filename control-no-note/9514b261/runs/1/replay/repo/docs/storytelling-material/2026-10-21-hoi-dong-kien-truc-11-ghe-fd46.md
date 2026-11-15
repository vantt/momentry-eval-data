---
id: 2026-10-21-hoi-dong-kien-truc-11-ghe-fd46
code: M-0FJZ
aliases: [M-0FJZ]
date: 2026-10-21
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L3362", "claude:9514b261#L3423", "claude:9514b261#L3518", "claude:9514b261#L3966", "claude:9514b261#L3987", "claude:9514b261#L3993"]
hook: "Hội đồng 11 ghế chạy lần đầu, bước thứ hai đã hỏng"
tension: khac
sides: ["Hội đồng 11 ghế đã dựng và đẩy lên", "Bước shaping lỗi ngay lần chạy đầu"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Forgent (fgOS) là nền tảng để xây app agent, và người làm đang dựng hội đồng kiến trúc 11 ghế để phân ranh giới giữa ba hệ decision, document và context. Họ tưởng việc gán đủ 11 ghế là đủ để hội đồng chạy, nên mở hội đồng ngay. Lần chạy đầu, bước shaping lỗi execution-failure, và chỉ khi đọc trạng thái từng ghế mới thấy. Ai dùng nhiều model cho một quy trình nhiều bước nên đọc trạng thái từng bước ngay từ đầu, không đợi đến cổng cuối."
audience: dev dùng nhiều model cho quy trình nhiều bước
spine_context: "Dự án Forgent (fgOS) là nền tảng để xây app agent. Người làm đang dựng hội đồng kiến trúc 11 ghế để phân ranh giới giữa ba hệ decision, document và context."
spine_context_lines: [profile, "claude:9514b261#L3502"]
spine_want: Muốn hội đồng cấp cao chốt cách phân authority và ranh giới giữa ba hệ đó.
spine_want_lines: ["claude:9514b261#L3502"]
spine_obstacle: Bước shaping (ba panelist đề xuất mù) lỗi execution-failure ngay lần chạy đầu.
spine_obstacle_lines: ["claude:9514b261#L3993"]
spine_turn: Tưởng 11/11 ghế gán được thì hội đồng sẽ chạy; hoá ra unit shape-proposals lỗi khi chạy thật.
spine_turn_lines: ["claude:9514b261#L3353", "claude:9514b261#L3993"]
spine_action: "Commit và push .fgos/config.json, mở hội đồng, rồi đọc trạng thái từng bước."
spine_action_lines: ["claude:9514b261#L3407", "claude:9514b261#L3518", "claude:9514b261#L3988"]
spine_outcome: "Framing pass; shaping dừng ở execution-failure, chưa có kết luận hội đồng."
spine_outcome_lines: ["claude:9514b261#L3993", "claude:9514b261#L4010"]
spine_takeaway: "Chạy bước rẻ trước và đọc trạng thái từng ghế ngay khi bắt đầu, đừng đợi đến cổng người."
spine_takeaway_lines: ["claude:9514b261#L3988", "claude:9514b261#L3993"]
completeness: 7
---

# Hội đồng kiến trúc 11 ghế: bước shaping lỗi ngay lần chạy đầu

**Góc kể:** Dự án Forgent (fgOS) là nền tảng để xây app agent, và người làm đang dựng hội đồng kiến trúc 11 ghế để phân ranh giới giữa ba hệ decision, document và context. Họ tưởng việc gán đủ 11 ghế là đủ để hội đồng chạy, nên mở hội đồng ngay. Lần chạy đầu, bước shaping lỗi execution-failure, và chỉ khi đọc trạng thái từng ghế mới thấy. Ai dùng nhiều model cho một quy trình nhiều bước nên đọc trạng thái từng bước ngay từ đầu, không đợi đến cổng cuối.
**Bối cảnh:** Chủ chọn commit config trước rồi mới mở hội đồng gồm framing, shaping ba panelist đề xuất mù, critique, synthesis, explanation và một cổng người.
**Chuyện gì xảy ra:** Agent commit và push 42 dòng .fgos/config.json sau khi quét bí mật, rồi rebase lên 28 commit mới của remote. Workflow architecture-advisory chạy được bước framing, nhưng shaping kết thúc với execution-failure. Lần đầu agent không đọc được status vì lỗi parse, sau đó mới thấy ghế shape-proposals lỗi.
**Bài học:** Chạy bước rẻ trước và đọc trạng thái từng ghế ngay khi bắt đầu, đừng đợi đến cổng người mới phát hiện hỏng.
**Artefact:** Bảng các bước workflow và trạng thái pass hoặc execution-failure. Không cần ảnh.
