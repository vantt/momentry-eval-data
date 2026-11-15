---
id: 2026-11-05-agent-noi-skill-chua-co-routing-c4b4
code: M-7YQE
aliases: [M-7YQE]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1315", "claude:6a207191#L1341", "claude:6a207191#L1361", "claude:6a207191#L1396", "claude:6a207191#L1417", "claude:6a207191#L1441"]
hook: "Agent kết luận skill chưa có routing, trong khi hub có 9 trigger"
tension: tuong_ma_hoa_ra
sides: ["Thư mục trên máy không có skill.yaml", "Hub có 9 trigger, 5 example, 5 not_for do người duyệt đặt"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm skill cho agent đang đẩy một skill đóng gói cài đặt lên hub dùng chung để người khác duyệt. Agent tưởng skill chưa có phần routing vì chỉ đọc thư mục trên máy, nơi chưa có skill.yaml. Hoá ra hub đã có sẵn 9 trigger, 5 ví dụ và 5 trường hợp không dùng do người duyệt đặt. Ai đẩy metadata lên hub cần biết máy khách không thấy đủ, nên phải hỏi đúng nguồn trước khi kết luận thiếu."
audience: người làm agent skill và quy trình duyệt skill dùng chung
spine_context: "Một người làm skill cho agent, đang đẩy một skill đóng gói cài đặt lên hub dùng chung để người khác duyệt."
spine_context_lines: ["claude:6a207191#L1271"]
spine_want: Muốn skill có phần routing và metadata đầy đủ để agent tìm đúng skill khi cần.
spine_want_lines: ["claude:6a207191#L1341"]
spine_obstacle: "Hub báo bản skillstation cũ chưa kiểm tra routing, và lệnh show --verbose bị từ chối vì skill được quản lý trên máy hub."
spine_obstacle_lines: ["claude:6a207191#L1315", "claude:6a207191#L1417"]
spine_turn: "Tưởng skill chưa có routing vì chỉ đọc thư mục trên máy; hoá ra hub đã có 9 trigger, 5 ví dụ và 5 trường hợp không dùng do người duyệt đặt."
spine_turn_lines: ["claude:6a207191#L1396", "claude:6a207191#L1441"]
spine_action: "Soạn lại skill.yaml: giữ nguyên các mục routing đang có trên hub, thêm operations, topics, technologies, min_scope và counter_examples."
spine_action_lines: ["claude:6a207191#L1437"]
spine_outcome: "Bản nháp giữ đủ 9 trigger, 5 ví dụ và 5 trường hợp không dùng cũ, thêm một số mục mới. Chưa gửi lên hub."
spine_outcome_lines: ["claude:6a207191#L1441", "claude:6a207191#L1453"]
spine_takeaway: "Khi metadata nằm trên hub, máy khách không thấy đủ. Trước khi kết luận thiếu, hãy hỏi đúng nguồn."
spine_takeaway_lines: ["claude:6a207191#L1417", "claude:6a207191#L1441"]
completeness: 7
---

# Agent nói skill chưa có routing vì đọc thư mục trên máy khác với bản trên hub

**Góc kể:** Một người làm skill cho agent đang đẩy một skill đóng gói cài đặt lên hub dùng chung để người khác duyệt. Agent tưởng skill chưa có phần routing vì chỉ đọc thư mục trên máy, nơi chưa có skill.yaml. Hoá ra hub đã có sẵn 9 trigger, 5 ví dụ và 5 trường hợp không dùng do người duyệt đặt. Ai đẩy metadata lên hub cần biết máy khách không thấy đủ, nên phải hỏi đúng nguồn trước khi kết luận thiếu.
**Bối cảnh:** Chủ dự án thấy trên hub chưa có topic hay operations. Agent kết luận nhầm và soạn lại skill.yaml.
**Chuyện gì xảy ra:** Hub đang có 9 trigger, 5 example và 5 not_for do người duyệt đặt. Agent chỉ đọc thư mục trên máy này, nơi chưa có skill.yaml. Lệnh show --verbose bị từ chối vì project trỏ tới hub khác. skill_get không trả về operations, topics, technologies hay min_scope. Lệnh lint báo hub chưa kiểm tra routing vì chạy bản cũ.
**Bài học:** Khi metadata nằm trên hub, máy khách không đọc đủ. Trước khi kết luận chưa có, hãy hỏi đúng nguồn.
**Artefact:** Bảng so sánh cột trên hub và cột thêm vào trong skill.yaml. Không có thông tin cần che.
