---
id: 2026-10-14-luat-chon-3-trong-9-va-8a83
code: M-06RY
aliases: [M-06RY]
date: 2026-10-14
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c02#L50", "claude:5a1e7c02#L51", "claude:5a1e7c02#L52", "claude:5a1e7c02#L53", "claude:5a1e7c02#L54", "claude:5a1e7c02#L55", "claude:5a1e7c02#L56", "claude:5a1e7c02#L58"]
hook: "Bỏ giờ khám trẻ em để giữ nhắc nhở rẻ nhất, rồi phải gọi người bảo trợ"
tension: chon_mot_mat_mot
sides: ["Giữ nhắc nhở: việc rẻ nhất, đứng đầu khảo sát", "Giờ khám trẻ em (57 phản hồi) xuống phụ lục, có thể mất người bảo trợ"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm nghiên cứu đang chuẩn bị báo cáo 20 phút cho ban điều hành về lý do bệnh nhân nha khoa không quay lại, dựa trên phỏng vấn và khảo sát. Cả phòng tin rằng vấn đề giá chỉ là một chuyện, nhưng khi tách ra thì đó là hai nguyên nhân khác nhau: khuyến mãi của đối thủ và phí bất ngờ lúc thanh toán. Khảo sát cho thấy phí bất ngờ được nhắc nhiều hơn (88 so với 61), nên đây là điều đáng để ý. Dev làm phân tích dữ liệu cần nhớ: một nhãn chung có thể che hai nguyên nhân khác nhau, nên hãy tách trước khi xếp hạng."
audience: dev dùng AI để phân tích phỏng vấn và khảo sát
spine_context: "Nghiên cứu lý do bệnh nhân nha khoa không quay lại, dựa trên 14 phỏng vấn và một khảo sát."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn có bản tổng hợp và dàn ý cho buổi trình bày 20 phút vào thứ Năm.
spine_want_lines: ["claude:5a1e7c02#L1", "claude:5a1e7c02#L52"]
spine_obstacle: Chỉ có 20 phút và 9 phát hiện ứng viên; lần trước khán giả chọn cái dễ nhất và bỏ phần còn lại.
spine_obstacle_lines: ["claude:5a1e7c02#L52"]
spine_turn: "Tưởng cả nhóm đã đồng ý một điều về giá; hoá ra đó là hai vấn đề: khuyến mãi của đối thủ và phí bất ngờ khi thanh toán."
spine_turn_lines: ["claude:5a1e7c02#L43", "claude:5a1e7c02#L49"]
spine_action: "Tách mục giá thành 'Giá A: khuyến mãi đối thủ' và 'Giá B: phí bất ngờ khi thanh toán' trong bản tổng hợp."
spine_action_lines: ["claude:5a1e7c02#L43"]
spine_outcome: "Khảo sát: phí cao hơn dự kiến được nhắc 88 lần, đối thủ rẻ hơn 61 lần, nên Giá B lớn hơn Giá A; danh sách có 9 phát hiện ứng viên với hai mục giá tách riêng."
spine_outcome_lines: ["claude:5a1e7c02#L49", "claude:5a1e7c02#L51"]
spine_takeaway: "Khi cả nhóm gọi chung một vấn đề, hãy tách thành các nguyên nhân riêng và đếm từng cái trước khi xếp hạng."
spine_takeaway_lines: ["claude:5a1e7c02#L43", "claude:5a1e7c02#L49"]
completeness: 7
---

# Luật 'chọn 3 trong 9' và câu hỏi của người bảo trợ đi vào phụ lục

**Góc kể:** Một người làm nghiên cứu đang chuẩn bị báo cáo 20 phút cho ban điều hành về lý do bệnh nhân nha khoa không quay lại, dựa trên phỏng vấn và khảo sát. Cả phòng tin rằng vấn đề giá chỉ là một chuyện, nhưng khi tách ra thì đó là hai nguyên nhân khác nhau: khuyến mãi của đối thủ và phí bất ngờ lúc thanh toán. Khảo sát cho thấy phí bất ngờ được nhắc nhiều hơn (88 so với 61), nên đây là điều đáng để ý. Dev làm phân tích dữ liệu cần nhớ: một nhãn chung có thể che hai nguyên nhân khác nhau, nên hãy tách trước khi xếp hạng.
**Bối cảnh:** Buổi trình bày 20 phút trước CEO, Head of Sales và Head of Ops. Đội có 9 phát hiện ứng viên, từng được gom lại từ phỏng vấn và khảo sát.
**Chuyện gì xảy ra:** Agent đề xuất ba phát hiện: lễ tân, sốc khi thanh toán và nhắc nhở tự động. Agent cũng gợi ý đổi nhắc nhở lấy giờ khám cho trẻ em để giữ người bảo trợ, nhưng người dùng từ chối vì nhắc nhở là việc rẻ nhất và đứng đầu khảo sát. Giờ khám cho trẻ em (2 phỏng vấn, 57 phản hồi khảo sát) được đưa vào phụ lục kèm ước tính chi phí mở cửa thứ Bảy, và người dùng sẽ gọi trực tiếp người bảo trợ trước buổi họp để giải thích.
**Bài học:** Ràng buộc thời gian quyết định cấu trúc trình bày: chọn theo tiêu chí rõ ràng (hành động rẻ, ảnh hưởng lớn), và báo trước cho người bảo trợ về vị trí câu hỏi của họ thay vì để họ phát hiện trên slide.
**Artefact:** Outline với 3 slide chính và 1 slide phụ lục 'Giờ khám cho trẻ em: những gì đã tìm thấy'. Không cần ảnh chụp.
