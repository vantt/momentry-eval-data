---
id: 2026-10-30-dataforseo-kiem-gia-thay-vi-tra-f60d
code: M-3315
aliases: [M-3315]
date: 2026-10-30
repo: repo
status: raw
signals: [dao_quyet_dinh, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1376", "claude:f0bf048d#L1414", "claude:f0bf048d#L1601", "claude:f0bf048d#L1603"]
hook: "Plan bật DataForSEO cho khách chưa mua, sửa đúng một dòng"
tension: nho_ma_to
sides: ["Một nhánh xử lý workspace bị thiếu", "Server trả phí được tạo cho khách chưa mua"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang dựng bộ agent marketing (SEO, social, content, ads) cho khách finejapan trong hệ thống OPC, và muốn hỗ trợ từ gói dữ liệu SEO miễn phí đến trả tiền. Người làm tưởng lệnh plan chỉ bật add-on trả phí cho khách đã mua; khi chạy thử cho khách chưa mua, plan vẫn tạo server DataForSEO trả phí, vì nhánh xử lý workspace chưa tồn tại chạy một đường khác. Ai làm công cụ có tính năng trả phí theo khách nên kiểm từng nhánh, nhất là nhánh cho trạng thái mới, vì một nhánh đúng không bảo đảm nhánh khác cũng đúng."
audience: dev làm công cụ có tính năng trả phí theo khách
spine_context: "Một người làm đang dựng bộ agent marketing (SEO, social, content, ads) cho khách finejapan trong hệ thống OPC, và muốn hỗ trợ từ gói dữ liệu SEO miễn phí đến trả tiền."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1282", "claude:f0bf048d#L1439"]
spine_want: Muốn hỗ trợ từ gói dữ liệu SEO miễn phí đến trả tiền (DataForSEO).
spine_want_lines: ["claude:f0bf048d#L1439"]
spine_obstacle: "Phải chọn nguồn dữ liệu từ khoá giữa serper và DataForSEO, và DataForSEO yêu cầu nạp tối thiểu $50."
spine_obstacle_lines: ["claude:f0bf048d#L1373"]
spine_turn: "Tưởng lệnh plan chỉ bật add-on trả phí cho khách đã mua; hoá ra khi workspace chưa tồn tại, plan chạy một nhánh khác và vẫn tạo server DataForSEO cho khách chưa mua."
spine_turn_lines: ["claude:f0bf048d#L1597", "claude:f0bf048d#L1603"]
spine_action: "Chạy thử plan cho finejapan ở mức miễn phí và có add-on, rồi tìm nhánh xử lý workspace chưa tồn tại trong mã của công cụ."
spine_action_lines: ["claude:f0bf048d#L1597", "claude:f0bf048d#L1603", "claude:f0bf048d#L1604"]
spine_takeaway: "Khi công cụ có nhánh riêng cho trạng thái chưa tồn tại, phải kiểm từng nhánh, không chỉ nhánh chính, vì nhánh chính đúng không bảo đảm nhánh phụ cũng đúng."
spine_takeaway_lines: ["claude:f0bf048d#L1603"]
completeness: 6
---

# DataForSEO: kiểm giá thay vì trả lời theo trí nhớ, và plan bật add-on cho khách chưa mua

**Góc kể:** Một người làm đang dựng bộ agent marketing (SEO, social, content, ads) cho khách finejapan trong hệ thống OPC, và muốn hỗ trợ từ gói dữ liệu SEO miễn phí đến trả tiền. Người làm tưởng lệnh plan chỉ bật add-on trả phí cho khách đã mua; khi chạy thử cho khách chưa mua, plan vẫn tạo server DataForSEO trả phí, vì nhánh xử lý workspace chưa tồn tại chạy một đường khác. Ai làm công cụ có tính năng trả phí theo khách nên kiểm từng nhánh, nhất là nhánh cho trạng thái mới, vì một nhánh đúng không bảo đảm nhánh khác cũng đúng.
**Bối cảnh:** Bộ SEO cần dữ liệu từ khoá. Hai lựa chọn: serper.dev và DataForSEO.
**Chuyện gì xảy ra:** Agent kiểm lại giá của serper (2.500 lượt miễn phí, khoảng 1 USD cho 1.000 lượt, không có search volume) và của DataForSEO (nạp tối thiểu 50 USD, không hết hạn, SERP từ 0,0006 USD). Ước tính một khách vừa và nhỏ khoảng 2 đến 5 USD mỗi tháng. Đề xuất đổi: bỏ serper, chỉ dùng DataForSEO. Trong lúc làm, plan tạo server DataForSEO cho khách chưa mua, vì nhánh xử lý workspace chưa tồn tại không lọc add-on. Sửa một dòng và kiểm đủ ba trường hợp.
**Bài học:** Khi số liệu đổi, đổi đề xuất kèm lý do. Khi plan có nhánh riêng cho trạng thái chưa tồn tại, phải test từng nhánh.
**Artefact:** Bảng giá ước tính theo tác vụ, ghi rõ là ước tính.
