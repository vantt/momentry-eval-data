---
id: 2026-11-05-routing-qua-rong-skill-dong-goi-c4b4
code: M-35RX
aliases: [M-35RX]
date: 2026-11-05
repo: repo
status: raw
signals: [khac]
signal_note: "Lỗi định tuyến của hub xảy ra ngay lần đầu thử, với độ tin cậy trung bình. Đây là lỗi đo được dù chưa có số liệu tổng hợp."
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L1534", "claude:6a207191#L1555"]
hook: "Skill đóng gói bị chọn cho việc giao diện dù đã có not_for"
tension: cam_ma_van_lot
sides: ["Skill đã khai báo not_for để chặn", "Hub vẫn chọn nó cho việc frontend thuần"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang xây hub skillstation, nơi agent tra cứu skill theo việc cần làm, và nhờ agent sửa giao diện web của hub. Agent tin skill đó chưa có phần định tuyến, vì lệnh xem từ máy khách không hiện operations hay min_scope. Hoá ra dữ liệu đó có sẵn trong skill.yaml, chỉ là công cụ không cho xem. Ai dựng hay dùng công cụ cho agent nên nhớ: một trường bị ẩn trông giống như trường không tồn tại."
audience: dev dựng hoặc dùng công cụ tra cứu skill cho agent
spine_context: "Người làm đang xây hub skillstation để agent tra cứu skill, và nhờ agent sửa giao diện web của hub."
spine_context_lines: ["claude:6a207191#L1520", "claude:6a207191#L1534"]
spine_want: Muốn thêm banner và badge 'update pending' trên web hub khi có bản cập nhật chờ duyệt.
spine_want_lines: ["claude:6a207191#L1566"]
spine_obstacle: "Máy không có skill ak:frontend-development, và hub trả not_found."
spine_obstacle_lines: ["claude:6a207191#L1532", "claude:6a207191#L1533"]
spine_turn: "Agent tưởng skill chưa có phần định tuyến; hoá ra skill.yaml đã có operations và min_scope, chỉ là lệnh xem từ máy khách không hiện ra."
spine_turn_lines: ["claude:6a207191#L1555"]
spine_action: "Agent báo lại cho người làm, đề nghị thêm not_for cho việc giao diện, rồi chờ quyết định."
spine_action_lines: ["claude:6a207191#L1555"]
spine_outcome: "Người làm xác nhận đã có ak:frontend-development, và agent gọi skill đó với đề bài sửa web UI."
spine_outcome_lines: ["claude:6a207191#L1561", "claude:6a207191#L1566"]
spine_takeaway: Trường bị ẩn trong công cụ trông như trường không tồn tại; kiểm tra dữ liệu gốc trước khi kết luận.
spine_takeaway_lines: ["claude:6a207191#L1555"]
completeness: 7
---

# Routing quá rộng: skill đóng gói bị chọn cho việc frontend thuần

**Góc kể:** Người làm đang xây hub skillstation, nơi agent tra cứu skill theo việc cần làm, và nhờ agent sửa giao diện web của hub. Agent tin skill đó chưa có phần định tuyến, vì lệnh xem từ máy khách không hiện operations hay min_scope. Hoá ra dữ liệu đó có sẵn trong skill.yaml, chỉ là công cụ không cho xem. Ai dựng hay dùng công cụ cho agent nên nhớ: một trường bị ẩn trông giống như trường không tồn tại.
**Bối cảnh:** Agent nhờ hub tìm skill cho việc sửa web UI. Hub trả về skill đóng gói và phát hành.
**Chuyện gì xảy ra:** Lần đầu hub chọn skill đóng gói với độ tin cậy trung bình. Agent từ chối và hỏi lại, lần hai hub báo không có skill nào khớp. Skill đã có not_for nhưng vẫn bị chọn, nên cần thêm not_for cho việc giao diện.
**Bài học:** Đặt not_for cho những việc gần giống nhưng khác bản chất, rồi thử lại bằng các câu đối chứng.
**Artefact:** Phản hồi của hub đã che mã yêu cầu.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người viết skill chỉ viết một dòng mô tả và tin rằng máy sẽ tự chọn đúng; ở đây khác ở Routing là dữ liệu có cấu trúc để máy chọn skill, nên có thể viết, kiểm tra và sửa. Người đọc sẽ muốn biết vì sao một lần chọn nhầm (skill đóng gói bị chọn cho việc frontend) lại được coi là bằng chứng để siết lại.
