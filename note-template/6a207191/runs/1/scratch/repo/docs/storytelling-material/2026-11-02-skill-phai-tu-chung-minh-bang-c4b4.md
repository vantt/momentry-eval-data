---
id: 2026-11-02-skill-phai-tu-chung-minh-bang-c4b4
code: M-138W
aliases: [M-138W]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Tiêu chí đo UX mới lạ: agent cold-start chỉ đọc --help phải tự cài xong, đảo ngược thói quen viết README trước."
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L636", "claude:6a207191#L639", "claude:6a207191#L657", "claude:6a207191#L900", "claude:6a207191#L910", "claude:6a207191#L929"]
hook: "Agent đề xuất 25 check bằng script, một câu hỏi cắt còn 0 script"
tension: it_ma_nhieu
sides: ["Kế hoạch 25–30 check bằng script", "Chỉ cần 12 bước trong SKILL.md và một agent mới không đọc README"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người đang gom các cách đóng gói và phát hành tốt từ vài dự án CLI thành một skill cho agent, để mỗi dự án mới chỉ cần gọi skill. Agent tưởng phải viết 25–30 script mới kiểm được skill một cách nhất quán, nhưng người làm hỏi lại thì hoá ra không cần: agent tự chạy --help, doctor --json và đọc rule là đủ. Script chỉ đáng viết khi tiêu chí đã ổn định, nên bước kiểm cuối cùng được thay bằng khoảng 10 lệnh trong SKILL.md, và bước quan trọng nhất là bật một agent mới chỉ giao 'cài X giúp tôi'. Dev làm CLI hoặc đang dùng agent để viết quy chuẩn sẽ thấy đây là cách đo UX rẻ hơn hẳn việc viết thêm script."
audience: dev làm CLI và dùng agent để viết quy chuẩn
spine_context: "Người làm gom cách đóng gói và phát hành tốt từ nhiều dự án CLI (mdview, skillstation, herdr-go, forgent) thành một skill cho agent."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: "Muốn skill chứa các thực hành tốt, và agent có thể cài đặt một công cụ chỉ bằng --help."
spine_want_lines: ["claude:6a207191#L5", "claude:6a207191#L636"]
spine_obstacle: Chưa biết cách kiểm tra xem agent có làm đúng theo skill mà không phải đọc tay từng rule.
spine_obstacle_lines: ["claude:6a207191#L910"]
spine_turn: Agent tưởng phải có 25–30 script mới kiểm được nhất quán; hoá ra agent tự làm được mà không cần script.
spine_turn_lines: ["claude:6a207191#L910", "claude:6a207191#L929"]
spine_action: "Bỏ đề xuất script, thêm khoảng 10 lệnh kiểm vào SKILL.md, và bật một agent mới chỉ giao 'cài X giúp tôi' để thử."
spine_action_lines: ["claude:6a207191#L922", "claude:6a207191#L929", "claude:6a207191#L934", "claude:6a207191#L937"]
spine_outcome: Đã gọi lệnh sửa SKILL.md để thêm bước Verify; trích đoạn không có kết quả của lệnh đó.
spine_outcome_lines: ["claude:6a207191#L937"]
spine_takeaway: "Chỉ viết script kiểm khi tiêu chí đã ổn định; trước đó, đo UX bằng một agent mới là đủ."
spine_takeaway_lines: ["claude:6a207191#L929"]
completeness: 7
---

# Skill phải tự chứng minh bằng agent mới: test 'cài X giúp tôi' chỉ bằng --help

**Góc kể:** Một người đang gom các cách đóng gói và phát hành tốt từ vài dự án CLI thành một skill cho agent, để mỗi dự án mới chỉ cần gọi skill. Agent tưởng phải viết 25–30 script mới kiểm được skill một cách nhất quán, nhưng người làm hỏi lại thì hoá ra không cần: agent tự chạy --help, doctor --json và đọc rule là đủ. Script chỉ đáng viết khi tiêu chí đã ổn định, nên bước kiểm cuối cùng được thay bằng khoảng 10 lệnh trong SKILL.md, và bước quan trọng nhất là bật một agent mới chỉ giao 'cài X giúp tôi'. Dev làm CLI hoặc đang dùng agent để viết quy chuẩn sẽ thấy đây là cách đo UX rẻ hơn hẳn việc viết thêm script.
**Bối cảnh:** Người dùng muốn 'agent-native': chỉ cần nói 'cài X giúp tôi' là agent tự làm được, không cần README. Skill được bổ sung tiêu chí này làm bước verify số 12.
**Chuyện gì xảy ra:** Ban đầu agent đề xuất ~25–30 check bằng script. Người dùng hỏi 'không có script thì agent vẫn làm được?', và câu trả lời là có. Quyết định cuối: không viết script, thay bằng 12 bước verify trong SKILL.md, trong đó bước quan trọng nhất là bật một agent mới không cho đọc README.
**Bài học:** Đo UX của công cụ CLI bằng một agent mới chỉ đọc --help, thay vì chỉ kiểm tra bằng script; script chỉ nên được viết khi tiêu chí đã ổn định.
**Artefact:** Danh sách 12 bước verify trong SKILL.md; không có ảnh nhạy cảm.
