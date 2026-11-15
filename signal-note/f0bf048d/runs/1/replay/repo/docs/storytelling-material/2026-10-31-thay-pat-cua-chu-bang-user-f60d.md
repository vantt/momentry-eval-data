---
id: 2026-10-31-thay-pat-cua-chu-bang-user-f60d
code: M-68HB
aliases: [M-68HB]
date: 2026-10-31
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1987", "claude:f0bf048d#L1998", "claude:f0bf048d#L2400", "claude:f0bf048d#L2409", "claude:f0bf048d#L2439", "claude:f0bf048d#L2457", "claude:f0bf048d#L2536", "claude:f0bf048d#L2543", "claude:f0bf048d#L2549", "claude:f0bf048d#L2550", "claude:f0bf048d#L2569", "claude:f0bf048d#L2578"]
hook: "PAT của chủ nằm ở ba chỗ trong cấu hình, không phải một"
tension: tuong_ma_hoa_ra
sides: ["tưởng PAT chỉ nằm một chỗ", "grep thấy 3 chỗ, thu hồi PAT cũ sớm là hỏng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng hệ agent AI trên Multica và muốn các agent chạy dưới user riêng thay vì giữ PAT của chủ. Khi tắt daemon thử nghiệm, họ tin có thể bật lại bằng `enable --now`, nhưng daemon này chạy dạng transient unit nên không có unit nào để bật lại. Ai vận hành daemon hay agent AI sẽ thấy vì sao cần ghi cách khôi phục trước khi tắt một service."
audience: dev vận hành daemon và agent AI
spine_context: Người làm đang dựng hệ agent AI trên Multica và muốn cấp quyền cho agent và user trên máy mà không gây hậu quả nghiêm trọng.
spine_context_lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L2394"]
spine_want: "Agent chạy dưới user riêng, không giữ PAT của chủ."
spine_want_lines: ["claude:f0bf048d#L2394"]
spine_obstacle: "Daemon thử nghiệm chạy dạng transient unit, không có unit để bật lại."
spine_obstacle_lines: ["claude:f0bf048d#L1987", "claude:f0bf048d#L1998"]
spine_turn: Tưởng tắt daemon thử nghiệm là bật lại được bằng enable; hoá ra daemon này là transient unit nên không có gì để enable.
spine_turn_lines: ["claude:f0bf048d#L1983", "claude:f0bf048d#L1987", "claude:f0bf048d#L1998"]
spine_action: "Tắt daemon ops và spike, rồi kiểm tra unit và trạng thái còn lại."
spine_action_lines: ["claude:f0bf048d#L1984", "claude:f0bf048d#L1989"]
spine_outcome: Daemon ops và spike đã dừng; System Operator tạm ngừng đến Giai đoạn 2.
spine_outcome_lines: ["claude:f0bf048d#L2578"]
spine_takeaway: "Trước khi tắt một service, kiểm xem nó có unit để bật lại không; daemon transient cần ghi cách khôi phục trước khi tắt."
spine_takeaway_lines: ["claude:f0bf048d#L1983", "claude:f0bf048d#L1998"]
completeness: 7
---

# Thay PAT của chủ bằng user daemon riêng, PAT nằm ở ba chỗ, daemon thử nghiệm không bật lại được

**Góc kể:** Người làm đang dựng hệ agent AI trên Multica và muốn các agent chạy dưới user riêng thay vì giữ PAT của chủ. Khi tắt daemon thử nghiệm, họ tin có thể bật lại bằng `enable --now`, nhưng daemon này chạy dạng transient unit nên không có unit nào để bật lại. Ai vận hành daemon hay agent AI sẽ thấy vì sao cần ghi cách khôi phục trước khi tắt một service.
**Bối cảnh:** Giai đoạn 0 của kế hoạch quyền: agent không được giữ PAT của chủ.
**Chuyện gì xảy ra:** Daemon thử nghiệm là transient unit nên không có lệnh bật lại; tắt rồi là hết. Tạo user Multica riêng chỉ là member của hai workspace. Script login lần đầu chạy thành công rồi xoá file PAT, nên lần chạy sau báo lỗi. Grep trong home tìm được PAT ở 3 chỗ trong cấu hình CLI. Agent tạo PAT mới, cập nhật 3 chỗ, kiểm PAT mới chạy rồi mới thu hồi PAT cũ (cũ trả 401). Chuyển 12 agent sang runtime mới, 2 lần đầu bị 405 vì dùng sai method, sửa sang PUT.
**Bài học:** Trước khi thu hồi một token, cập nhật mọi nơi đang dùng nó. Tìm bằng grep theo giá trị bí mật, không chỉ theo tên file. Daemon thử nghiệm dạng transient cần ghi cách khôi phục trước khi tắt.
**Artefact:** Kết quả 'old still works: False / new works: True' (che token).
