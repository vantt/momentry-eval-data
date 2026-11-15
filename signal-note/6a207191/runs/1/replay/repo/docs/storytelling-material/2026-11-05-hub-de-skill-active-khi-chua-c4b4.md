---
id: 2026-11-05-hub-de-skill-active-khi-chua-c4b4
code: M-MWGP
aliases: [M-MWGP]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, artefact_nhin_duoc]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1489", "claude:6a207191#L1515"]
hook: "Skill đang chạy bản chưa ai duyệt, trang web không báo gì"
tension: cam_ma_van_lot
sides: ["Cần có người bấm duyệt mới được active", "Bản cũ vẫn active, 3 bản chờ duyệt mà trang skill im lặng"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang xây một skill hướng dẫn đóng gói và phát hành cho agent, rồi gửi lên hub skillstation để dùng lại cho các dự án sau. Họ tưởng skill chỉ chạy khi có người bấm duyệt bản vừa gửi, nhưng hub vẫn phục vụ một bản cũ đã duyệt từ trước, có cùng routing. Trang skill không báo có bản mới đang chờ, nên ai mở trang sẽ tin bản đang chạy là mới nhất và dễ duyệt nhầm, nên bản chờ duyệt cần hiện ngay trên trang của chính skill đó."
audience: dev dùng agent để xây skill và gửi skill lên hub chung
spine_context: "Người làm đang xây một skill hướng dẫn đóng gói và phát hành cho agent, rồi gửi lên hub skillstation để dùng lại cho các dự án sau."
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L1483"]
spine_want: Muốn bản skill mới được duyệt trước khi hub chạy nó.
spine_want_lines: ["claude:6a207191#L1489"]
spine_obstacle: "Hub đang active một bản cũ đã duyệt trước đó, có cùng routing; trang skill không báo có bản mới đang chờ."
spine_obstacle_lines: ["claude:6a207191#L1501", "claude:6a207191#L1503", "claude:6a207191#L1507"]
spine_turn: "Tưởng skill chỉ lên active sau khi có người bấm duyệt bản vừa gửi; hoá ra hub vẫn phục vụ bản cũ, còn bản mới vẫn chờ duyệt."
spine_turn_lines: ["claude:6a207191#L1489", "claude:6a207191#L1503"]
spine_action: "Đối chiếu bản hub đang phục vụ với thư mục skill trên máy, rồi xác nhận bản mới vẫn chờ duyệt."
spine_action_lines: ["claude:6a207191#L1500", "claude:6a207191#L1503"]
spine_outcome: "Bản mới vẫn chờ duyệt, hub giữ bản cũ đang active. Người làm chọn sửa web skillstation để trang skill báo có bản chờ duyệt."
spine_outcome_lines: ["claude:6a207191#L1515", "claude:6a207191#L1520", "claude:6a207191#L1525"]
spine_takeaway: Trang của một item phải hiện bản chờ duyệt ngay cạnh bản đang active; để hai trạng thái tách rời thì dễ duyệt nhầm bản cũ.
spine_takeaway_lines: ["claude:6a207191#L1507", "claude:6a207191#L1515"]
completeness: 7
---

# Hub để skill active khi chưa ai bấm duyệt; web không báo có bản chờ

**Góc kể:** Người làm đang xây một skill hướng dẫn đóng gói và phát hành cho agent, rồi gửi lên hub skillstation để dùng lại cho các dự án sau. Họ tưởng skill chỉ chạy khi có người bấm duyệt bản vừa gửi, nhưng hub vẫn phục vụ một bản cũ đã duyệt từ trước, có cùng routing. Trang skill không báo có bản mới đang chờ, nên ai mở trang sẽ tin bản đang chạy là mới nhất và dễ duyệt nhầm, nên bản chờ duyệt cần hiện ngay trên trang của chính skill đó.
**Bối cảnh:** Chủ dự án hỏi vì sao chưa duyệt mà skill đã active.
**Chuyện gì xảy ra:** Bản đang active là bản của một lần duyệt trước, có cùng routing. Mỗi bản gửi là một mục trong Waiting for review và không gắn vào trang skill. Trang skill không có dấu hiệu nào cho biết có bản mới đang chờ. Lúc đó có ba bản gửi cho cùng một skill, nên dễ duyệt nhầm bản cũ.
**Bài học:** Đặt bản chờ duyệt ngay trên trang của chính item đó. Đừng để hai trạng thái tách rời nhau.
**Artefact:** Ảnh trang skill và mục Waiting for review, cần che địa chỉ hub.
