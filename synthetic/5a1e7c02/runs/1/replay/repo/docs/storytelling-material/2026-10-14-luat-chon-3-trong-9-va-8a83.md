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
hook: "Từ chối đổi nhắc nhở lấy giờ khám trẻ em, người dùng phải gọi người bảo trợ"
tension: chon_mot_mat_mot
sides: ["Giữ nhắc nhở: rẻ nhất, đứng đầu khảo sát", "Bỏ giờ khám trẻ em mà người bảo trợ quan tâm, xuống phụ lục"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một nhóm đang tìm vì sao bệnh nhân của một phòng khám nha khoa bỏ không quay lại, và sắp trình bày kết quả cho ban lãnh đạo trong 20 phút. Ban lãnh đạo từng đồng ý rằng giá là vấn đề, nhưng dữ liệu cho thấy đó là hai chuyện khác nhau: đối thủ có khuyến mãi rẻ hơn, còn khách bất ngờ với chi phí lúc thanh toán (88 so với 61 lượt chọn). Ai phải cắt nhiều phát hiện xuống vài điểm cho lãnh đạo sẽ gặp đúng kiểu này: một chữ \"giá\" có thể gom hai vấn đề khác nhau."
audience: người làm nghiên cứu người dùng phải trình bày kết quả cho lãnh đạo
spine_context: "Nghiên cứu vì sao bệnh nhân của một phòng khám nha khoa bỏ không quay lại, sắp có buổi trình bày cho ban lãnh đạo."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn chọn ba phát hiện có hành động rõ ràng để ban lãnh đạo ghi nhớ.
spine_want_lines: ["claude:5a1e7c02#L52"]
spine_obstacle: "Có 9 phát hiện ứng viên trong 20 phút, và lần trước ban lãnh đạo chỉ nhớ một việc dễ nhất."
spine_obstacle_lines: ["claude:5a1e7c02#L51", "claude:5a1e7c02#L52"]
spine_turn: "Ban lãnh đạo tưởng giá là một vấn đề; hoá ra là hai: đối thủ khuyến mãi (Price A) và khách bất ngờ với chi phí lúc thanh toán (Price B)."
spine_turn_lines: ["claude:5a1e7c02#L43", "claude:5a1e7c02#L49"]
spine_action: "Chọn ba phát hiện, đưa giờ khám trẻ em xuống phụ lục, và ghi việc báo trước cho người có câu hỏi đó."
spine_action_lines: ["claude:5a1e7c02#L54", "claude:5a1e7c02#L55"]
spine_outcome: Đã viết outline và thêm việc gọi người bảo trợ vào danh sách việc cần làm.
spine_outcome_lines: ["claude:5a1e7c02#L56", "claude:5a1e7c02#L59"]
spine_takeaway: "Khi cắt bớt phát hiện cho lãnh đạo, nói rõ tiêu chí chọn và báo trước cho người có câu hỏi bị chuyển xuống phụ lục."
spine_takeaway_lines: ["claude:5a1e7c02#L53", "claude:5a1e7c02#L54"]
completeness: 7
---

# Luật 'chọn 3 trong 9' và câu hỏi của người bảo trợ đi vào phụ lục

**Góc kể:** Một nhóm đang tìm vì sao bệnh nhân của một phòng khám nha khoa bỏ không quay lại, và sắp trình bày kết quả cho ban lãnh đạo trong 20 phút. Ban lãnh đạo từng đồng ý rằng giá là vấn đề, nhưng dữ liệu cho thấy đó là hai chuyện khác nhau: đối thủ có khuyến mãi rẻ hơn, còn khách bất ngờ với chi phí lúc thanh toán (88 so với 61 lượt chọn). Ai phải cắt nhiều phát hiện xuống vài điểm cho lãnh đạo sẽ gặp đúng kiểu này: một chữ "giá" có thể gom hai vấn đề khác nhau.
**Bối cảnh:** Buổi trình bày 20 phút trước CEO, Head of Sales và Head of Ops. Đội có 9 phát hiện ứng viên, từng được gom lại từ phỏng vấn và khảo sát.
**Chuyện gì xảy ra:** Agent đề xuất ba phát hiện: lễ tân, sốc khi thanh toán và nhắc nhở tự động. Agent cũng gợi ý đổi nhắc nhở lấy giờ khám cho trẻ em để giữ người bảo trợ, nhưng người dùng từ chối vì nhắc nhở là việc rẻ nhất và đứng đầu khảo sát. Giờ khám cho trẻ em (2 phỏng vấn, 57 phản hồi khảo sát) được đưa vào phụ lục kèm ước tính chi phí mở cửa thứ Bảy, và người dùng sẽ gọi trực tiếp người bảo trợ trước buổi họp để giải thích.
**Bài học:** Ràng buộc thời gian quyết định cấu trúc trình bày: chọn theo tiêu chí rõ ràng (hành động rẻ, ảnh hưởng lớn), và báo trước cho người bảo trợ về vị trí câu hỏi của họ thay vì để họ phát hiện trên slide.
**Artefact:** Outline với 3 slide chính và 1 slide phụ lục 'Giờ khám cho trẻ em: những gì đã tìm thấy'. Không cần ảnh chụp.
