---
id: 2026-10-31-cong-cu-tra-phi-lot-vao-f60d
code: M-J6W5
aliases: [M-J6W5]
date: 2026-10-31
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1601", "claude:f0bf048d#L1620", "claude:f0bf048d#L1633", "claude:f0bf048d#L1635"]
hook: "Plan bỏ sót nhánh workspace mới, công cụ trả phí lọt vào"
tension: cam_ma_van_lot
sides: ["Bộ lọc add-on chặn công cụ khách chưa mua", "Nhánh workspace chưa tồn tại bỏ qua bộ lọc"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một bộ công cụ đang đóng gói các vai marketing (SEO, nội dung, quảng cáo) thành agent cho từng khách, và SEO được làm trước. Người làm tin bộ lọc add-on chưa mua sẽ chặn công cụ trả phí ở mọi đường đi; nhưng khi khách chưa có workspace, plan đi một nhánh riêng và vẫn tạo DataForSEO. Sau khi lọc ở nhánh đó, khách chưa mua chỉ còn PageSpeed. Ai viết script cấu hình có nhiều nhánh tuỳ trạng thái đều có thể dính lỗi này."
audience: dev viết công cụ tự động cấu hình agent hoặc dịch vụ theo gói cho khách
spine_context: "Một bộ công cụ đóng gói các vai marketing (SEO, nội dung, quảng cáo) thành agent cho từng khách, và người làm đang ưu tiên SEO."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1282"]
spine_want: "Đóng gói vai SEO, social, content và ads thành agent, làm SEO trước."
spine_want_lines: ["claude:f0bf048d#L1282"]
spine_obstacle: Khách chưa mua add-on DataForSEO vẫn bị tạo server đó khi chạy plan.
spine_obstacle_lines: ["claude:f0bf048d#L1603"]
spine_turn: Tưởng bộ lọc add-on chặn công cụ trả phí ở mọi trường hợp; hoá ra nhánh workspace chưa tồn tại bỏ qua bộ lọc.
spine_turn_lines: ["claude:f0bf048d#L1603", "claude:f0bf048d#L1619"]
spine_action: "Lọc add-on chưa mua ở nhánh đó, rồi plan thử ba trường hợp: có add-on, không có, và workspace đã tồn tại."
spine_action_lines: ["claude:f0bf048d#L1620", "claude:f0bf048d#L1625"]
spine_outcome: "PageSpeed được gắn, DataForSEO không được tạo; lint các gói đều ok."
spine_outcome_lines: ["claude:f0bf048d#L1623", "claude:f0bf048d#L1639"]
spine_takeaway: Mọi nhánh của một kịch bản cấu hình phải dùng cùng bộ lọc; kiểm từng nhánh riêng.
spine_takeaway_lines: ["claude:f0bf048d#L1603", "claude:f0bf048d#L1623"]
completeness: 7
---

# Công cụ trả phí lọt vào plan khi khách chưa mua

**Góc kể:** Một bộ công cụ đang đóng gói các vai marketing (SEO, nội dung, quảng cáo) thành agent cho từng khách, và SEO được làm trước. Người làm tin bộ lọc add-on chưa mua sẽ chặn công cụ trả phí ở mọi đường đi; nhưng khi khách chưa có workspace, plan đi một nhánh riêng và vẫn tạo DataForSEO. Sau khi lọc ở nhánh đó, khách chưa mua chỉ còn PageSpeed. Ai viết script cấu hình có nhiều nhánh tuỳ trạng thái đều có thể dính lỗi này.
**Bối cảnh:** Sau khi thêm add-on DataForSEO, plan cho một khách chưa mua vẫn tạo server dataforseo.
**Chuyện gì xảy ra:** Plan có một nhánh riêng cho workspace chưa tồn tại và nhánh đó bỏ qua bộ lọc add-on. Agent tìm ra nhánh này, lọc add-on chưa mua ở cả hai nhánh, rồi kiểm plan trên ba trường hợp: có add-on, không có, và workspace đã tồn tại. Kết quả đúng như mong đợi: PageSpeed được gắn, DataForSEO không được tạo.
**Bài học:** Mọi nhánh của plan phải dùng cùng một bộ lọc. Kiểm từng nhánh riêng.
**Artefact:** Kết quả plan hai lần: có và không có add-on.
