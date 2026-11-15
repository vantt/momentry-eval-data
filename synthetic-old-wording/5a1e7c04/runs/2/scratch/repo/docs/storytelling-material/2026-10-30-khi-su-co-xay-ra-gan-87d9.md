---
id: 2026-10-30-khi-su-co-xay-ra-gan-87d9
code: M-NB5P
aliases: [M-NB5P]
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c04#L35", "claude:5a1e7c04#L36", "claude:5a1e7c04#L37", "claude:5a1e7c04#L39", "claude:5a1e7c04#L40"]
hook: "Sát giờ ra mắt, agent đo thiệt hại bằng tiền thật trước khi chọn"
tension: gap_ma_phai_chon
sides: ["Sự cố sát giờ ra mắt buộc phải quyết ngay", "Agent dừng lại tính tiền thật và kiểm tra trạng thái trước khi đổi"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm chiến dịch ra mắt serum vitamin C, ra mắt lúc 8 giờ tối mai. Tối nay influencer đăng mã GLOW30 (giảm 30%) thay vì GLOW15 (giảm 15%). Người làm tưởng mã test cho nhân viên đã vô hại vì chưa bao giờ xoá, nhưng hoá ra nó vẫn đang chạy và đã có 431 lượt dùng. Ai có mã test cũ chưa xoá nên kiểm tra trạng thái thật trước khi tin là nó đã chết."
audience: người làm marketing hoặc bán hàng trực tuyến dùng mã giảm giá
spine_context: "Một người làm chiến dịch ra mắt serum vitamin C, ra mắt lúc 8 giờ tối mai, đang chuẩn bị banner, bảng UTM và ngân sách tuần 2."
spine_context_lines: ["claude:5a1e7c04#L1"]
spine_want: Muốn xử lý được mã giảm giá lộn trước khi ra mắt.
spine_want_lines: ["claude:5a1e7c04#L35"]
spine_obstacle: "Influencer đăng mã GLOW30 (30%) lúc 8 giờ tối thay vì GLOW15 (15%), và một người khác đang trên máy bay nên không liên lạc được."
spine_obstacle_lines: ["claude:5a1e7c04#L35"]
spine_turn: "Mã test cho nhân viên được tạo tuần trước và chưa bao giờ xoá, nên người làm ngầm coi nó không còn dùng được. Hoá ra mã vẫn đang chạy ở 30% và đã có 431 lượt dùng, không phải 400 như Shopify báo lúc đầu."
spine_turn_lines: ["claude:5a1e7c04#L35", "claude:5a1e7c04#L40"]
spine_action: Đặt giới hạn 500 lượt cho GLOW30 và tắt mã STAFFTEST.
spine_action_lines: ["claude:5a1e7c04#L41"]
spine_outcome: "GLOW30 có giới hạn 500 lượt, đã dùng 431; STAFFTEST đã tắt."
spine_outcome_lines: ["claude:5a1e7c04#L42"]
spine_takeaway: "Trước khi xoá hay tin một mã cũ đã chết, xem số lượt dùng thật trên hệ thống."
spine_takeaway_lines: ["claude:5a1e7c04#L40"]
completeness: 7
---

# Khi sự cố xảy ra gần giờ ra mắt, agent tính chi phí bằng tiền thật, đưa hai phương án có đánh đổi rõ ràng, rồi kiểm tra trạng thái thật trước khi đổi. User chọn phương án.

**Góc kể:** Một người làm chiến dịch ra mắt serum vitamin C, ra mắt lúc 8 giờ tối mai. Tối nay influencer đăng mã GLOW30 (giảm 30%) thay vì GLOW15 (giảm 15%). Người làm tưởng mã test cho nhân viên đã vô hại vì chưa bao giờ xoá, nhưng hoá ra nó vẫn đang chạy và đã có 431 lượt dùng. Ai có mã test cũ chưa xoá nên kiểm tra trạng thái thật trước khi tin là nó đã chết.
**Chuyện gì xảy ra:** Khi sự cố xảy ra gần giờ ra mắt, agent tính chi phí bằng tiền thật, đưa hai phương án có đánh đổi rõ ràng, rồi kiểm tra trạng thái thật trước khi đổi. User chọn phương án.
**Góc người ngoài:** cách làm phổ biến là Hoặc tắt mã ngay không tính toán, hoặc để yên, hoặc sửa theo cảm tính khi đang hoảng; ở đây khác ở Quyết định được đặt trên con số cụ thể và có bước xem trạng thái hiện tại trước khi thay đổi. Người đọc muốn bắt chước cách ra quyết định dưới áp lực thời gian này.
