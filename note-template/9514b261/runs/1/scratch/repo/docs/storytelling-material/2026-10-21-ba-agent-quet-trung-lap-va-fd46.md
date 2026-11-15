---
id: 2026-10-21-ba-agent-quet-trung-lap-va-fd46
code: M-4DTQ
aliases: [M-4DTQ]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1417", "claude:9514b261#L1448", "claude:9514b261#L1467", "claude:9514b261#L1476", "claude:9514b261#L1482", "claude:9514b261#L1511"]
hook: "332 doc quá hạn gần 2 tháng, vì phép trừ ra NaN"
tension: cam_ma_van_lot
sides: ["Có check cảnh báo doc quá hạn", "Check không bao giờ bắn, 332 doc quá hạn 47-55 ngày không ai hay"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là nền tảng cho ứng dụng agent, đang ở alpha, và người làm cần biết Knowledge and Documentation Engine có trùng với Knowledge Registry đã chạy hay không. Ba agent phụ được giao quét tài liệu, và bản tổng hợp ghi '332 doc đã migrate vẫn provisional'; khi đếm lại, số thật là 479 doc với 332 provisional và 147 active. Điều đáng nói hơn là check cảnh báo doc quá hạn được tin là đang chạy, nhưng phép trừ chuỗi ISO cho NaN khiến nó không bao giờ báo, và 332 doc đã quá hạn 47-55 ngày mà không ai hay. Ai giao việc cho agent phụ nên đếm lại số liệu và đọc code, vì một check sai kiểu dữ liệu có thể im lặng suốt nhiều tuần."
audience: "dev dùng agent AI để làm việc hằng ngày, đặc biệt người giao việc cho sub-agent"
spine_context: "Forgent (fgOS) là nền tảng cho ứng dụng agent, đang ở alpha. Người làm đang xem Knowledge and Documentation Engine có trùng với Knowledge Registry đã chạy hay không."
spine_context_lines: [profile, "claude:9514b261#L1325"]
spine_want: "Muốn biết engine mới có chồng lên registry hiện có không, nên giao ba agent phụ quét tài liệu, lịch sử và mã."
spine_want_lines: ["claude:9514b261#L1325"]
spine_obstacle: "Registry không ghi sự kiện doc nào sau 2026-09-11, và chỉ phủ khoảng 15% trong 3146 file md."
spine_obstacle_lines: ["claude:9514b261#L1467"]
spine_turn: "Tưởng check cảnh báo doc quá hạn đang chạy; hoá ra phép trừ chuỗi ISO cho NaN nên check không bao giờ bắn, và 332 doc đã quá hạn 47-55 ngày mà không ai hay."
spine_turn_lines: ["claude:9514b261#L1417", "claude:9514b261#L1467"]
spine_action: Đếm lại số liệu trong registry và đối chiếu code của check doc-provisional-aged.
spine_action_lines: ["claude:9514b261#L1448", "claude:9514b261#L1476"]
spine_outcome: "Đếm lại được 479 doc, 332 provisional và 147 active; lỗi của check được báo cáo."
spine_outcome_lines: ["claude:9514b261#L1433", "claude:9514b261#L1448", "claude:9514b261#L1467"]
spine_takeaway: "Số liệu từ agent phụ phải đếm lại trước khi dùng, vì một check so sánh sai kiểu dữ liệu có thể im lặng không báo lỗi."
spine_takeaway_lines: ["claude:9514b261#L1476"]
completeness: 7
---

# Ba agent quét trùng lắp, và một check quá hạn không bao giờ bắn vì so sánh chuỗi thời gian

**Góc kể:** Forgent (fgOS) là nền tảng cho ứng dụng agent, đang ở alpha, và người làm cần biết Knowledge and Documentation Engine có trùng với Knowledge Registry đã chạy hay không. Ba agent phụ được giao quét tài liệu, và bản tổng hợp ghi '332 doc đã migrate vẫn provisional'; khi đếm lại, số thật là 479 doc với 332 provisional và 147 active. Điều đáng nói hơn là check cảnh báo doc quá hạn được tin là đang chạy, nhưng phép trừ chuỗi ISO cho NaN khiến nó không bao giờ báo, và 332 doc đã quá hạn 47-55 ngày mà không ai hay. Ai giao việc cho agent phụ nên đếm lại số liệu và đọc code, vì một check sai kiểu dữ liệu có thể im lặng suốt nhiều tuần.
**Bối cảnh:** Chủ dự án nghi Knowledge and Documentation Engine trùng với Knowledge Registry đã chạy. Ba agent researcher được giao quét plan và report, history và journals, rồi work item, mã và spec, mỗi agent một mảng.
**Chuyện gì xảy ra:** Agent tổng hợp ghi '332 doc đã migrate vẫn provisional'. Khi tự đếm lại, agent thấy đúng 479 doc, 365 role khác nhau, 332 provisional và 147 active, nên sửa lại cách nói. Đối chiếu code cho thấy check doc-provisional-aged trừ chuỗi ISO từ số, kết quả NaN, nên không bao giờ bắn. Có 332 doc đã quá hạn khoảng 47 đến 55 ngày mà không ai hay. Registry chỉ phủ khoảng 15% trong 3146 file md của docs.
**Bài học:** Số liệu từ agent phụ phải được đếm lại trước khi dùng. Một check so sánh sai kiểu dữ liệu có thể im lặng không bao giờ báo lỗi.
**Artefact:** Bảng số liệu đã đếm lại: 479 doc, 365 role, 332 provisional, 147 active, khoảng 15% của 3146 file. Không che gì.
**Góc người ngoài:** cách làm phổ biến là Thường tin luôn kết quả của sub-agent hoặc tự báo cáo theo trí nhớ, ít khi mở lại file để đối chiếu từng con số; ở đây khác ở Nhờ bước đối chiếu này, phiên bắt được lỗi thật: check quá hạn không bao giờ bắn, số 17 mục lệch, có config bị dùng sai. Người đọc sẽ hỏi vì sao agent cứ kiểm lại dù sub-agent đã nói 'xong'.
