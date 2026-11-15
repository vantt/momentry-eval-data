---
id: 2026-11-02-skillstation-chan-gui-len-hub-roi-c4b4
code: M-GX29
aliases: [M-GX29]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L1007", "claude:6a207191#L1060", "claude:6a207191#L1102", "claude:6a207191#L1168", "claude:6a207191#L1489", "claude:6a207191#L1507", "claude:6a207191#L1515"]
hook: "Bị chặn gửi lên hub, nhưng khi gửi được thì skill tự bật chưa ai duyệt"
tension: cam_ma_van_lot
sides: ["Hub chặn gửi vì chưa tin cậy, lệnh gợi ý lại không tồn tại", "Gửi xong, bản trên hub đã active dù chưa ai bấm duyệt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang gom các skill đóng gói và phân phối để mọi agent dùng chung qua hub skillstation, và họ muốn skill mới vào được hub để agent tìm thấy. Họ tưởng skill đang active thì bản đó là bản mới nhất đã được duyệt. Hoá ra bản active là bản của lần duyệt trước, bản vừa gửi vẫn nằm trong hàng chờ, và trang skill không báo gì về bản chờ đó. Ai đưa công cụ có hàng chờ duyệt nên hiện trạng thái 'có bản mới đang chờ' ngay trên trang đích, để người duyệt không nhầm bản cũ là bản mới nhất."
audience: dev dùng công cụ có hàng chờ duyệt cho skill và agent
spine_context: "Người làm đang gom các skill đóng gói và phân phối (cài đặt, cập nhật, cấu hình) để mọi agent dùng chung qua hub skillstation."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: Đưa skill lên hub để agent ở mọi project tự tìm và dùng.
spine_want_lines: ["claude:6a207191#L967"]
spine_obstacle: Hub chặn lệnh gửi có --yes vì chưa tin cậy ở cấp user.
spine_obstacle_lines: ["claude:6a207191#L1007"]
spine_turn: "Tưởng skill đang active nghĩa là bản mới nhất đã được duyệt; hoá ra bản active là bản của lần duyệt trước, còn bản vừa gửi nằm trong Waiting for review và trang skill không báo."
spine_turn_lines: ["claude:6a207191#L1489", "claude:6a207191#L1503", "claude:6a207191#L1507"]
spine_action: "Gửi skill lên hàng chờ, sau đó gửi lại bản có routing; mỗi lần có một mã SUB mới."
spine_action_lines: ["claude:6a207191#L1167", "claude:6a207191#L1480"]
spine_outcome: "Bản mới vẫn chờ duyệt, trang vẫn hiện bản active cũ; người làm đề xuất dải thông báo 'có bản chờ duyệt' trên trang skill và giao việc làm UI."
spine_outcome_lines: ["claude:6a207191#L1515", "claude:6a207191#L1525"]
spine_takeaway: "Công cụ có hàng chờ duyệt phải hiện 'có bản mới đang chờ' ngay trên trang đích, nếu không người duyệt tưởng bản đang chạy là mới nhất."
spine_takeaway_lines: ["claude:6a207191#L1507", "claude:6a207191#L1515"]
completeness: 7
---

# Skillstation chặn gửi lên hub, rồi hub tự kích hoạt skill mà chưa ai duyệt

**Góc kể:** Một người làm đang gom các skill đóng gói và phân phối để mọi agent dùng chung qua hub skillstation, và họ muốn skill mới vào được hub để agent tìm thấy. Họ tưởng skill đang active thì bản đó là bản mới nhất đã được duyệt. Hoá ra bản active là bản của lần duyệt trước, bản vừa gửi vẫn nằm trong hàng chờ, và trang skill không báo gì về bản chờ đó. Ai đưa công cụ có hàng chờ duyệt nên hiện trạng thái 'có bản mới đang chờ' ngay trên trang đích, để người duyệt không nhầm bản cũ là bản mới nhất.
**Bối cảnh:** Skill packaging được đẩy từ máy làm việc lên hub skillstation trên máy khác, qua nhiều lần commit. Các cảnh báo an toàn và trạng thái hub làm quy trình rối.
**Chuyện gì xảy ra:** `skill commit --yes` bị chặn vì hub chưa được tin cậy ở cấp user. Lệnh `connect --user` gợi ý trong thông báo lỗi không tồn tại (bug của skillstation 0.8.0). Sau khi nâng lên 0.13.0 và connect global, gửi thành công SUB-…. Nhưng người dùng phát hiện bản trên hub đã active dù chưa bấm duyệt; trang skill không báo có bản chờ duyệt, nên người xem phải tự vào mục Waiting for review.
**Bài học:** Với công cụ có hàng chờ duyệt, trang đích phải hiện trạng thái 'có bản mới đang chờ', nếu không người duyệt sẽ tưởng bản đang chạy là mới nhất.
**Artefact:** Ảnh chụp dải thông báo 'An update to this skill is waiting for review' (đã che SUB id và tên máy).
**Góc người ngoài:** cách làm phổ biến là Hầu hết dev chỉ copy một file hướng dẫn vào thư mục của AI rồi dùng luôn, không có bước gửi, duyệt, hay kiểm tra bảo mật trước khi chia sẻ; ở đây khác ở Phiên này có quy trình gửi lên hub, quét bảo mật trước khi gửi, hàng chờ duyệt, và phân biệt rõ bản đang chạy với bản chờ duyệt. Người đọc sẽ hỏi vì sao cần nhiều bước như vậy và cách làm này tránh được rủi ro gì.
