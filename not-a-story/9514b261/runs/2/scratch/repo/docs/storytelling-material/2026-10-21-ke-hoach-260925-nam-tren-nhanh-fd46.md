---
id: 2026-10-21-ke-hoach-260925-nam-tren-nhanh-fd46
code: M-19PJ
aliases: [M-19PJ]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L957", "claude:9514b261#L1024", "claude:9514b261#L1048", "claude:9514b261#L1082"]
hook: "Kế hoạch 331 file nằm trên nhánh chưa push, agent không đọc được"
tension: cam_ma_van_lot
sides: ["Board ghi hai đầu nhánh, tưởng đọc được kế hoạch", "Nhánh chưa push nên phase 7, 8 và manifest không đọc được, agent không đoán"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent là nền tảng để xây ứng dụng agent, và người làm đang tìm cách gom các tài liệu nền tảng đang trùng lặp về một chủ. Ban đầu agent trả lời rằng kế hoạch có các thành phần chạy lâu dài như canonical-decision-projection, tức H2 và H3. Đọc kỹ thì sai: hai thành phần đó chỉ nằm trong đề xuất, chưa có mã, còn kế hoạch chỉ xây công cụ di trú dùng một lần. Ai đọc kế hoạch để biết có hệ thống gì sẽ dễ hiểu nhầm nếu không tách hai loại này."
audience: dev đọc kế hoạch hoặc đề xuất kỹ thuật của dự án agent
spine_context: "Forgent (fgOS) là nền tảng để xây và chạy các ứng dụng agent, đang ở bản alpha. Người làm đang tìm cách gom các tài liệu nền tảng đang trùng lặp về một chủ duy nhất."
spine_context_lines: [profile, "claude:9514b261#L917"]
spine_want: "Muốn biết kế hoạch 260925 có xây component gom nhóm, khử trùng lặp như canonical-decision-projection không."
spine_want_lines: ["claude:9514b261#L917"]
spine_obstacle: "Các phase file của kế hoạch chỉ có trên nhánh remote chưa merge, main checkout không có, nên phải đọc bằng git show."
spine_obstacle_lines: ["claude:9514b261#L957"]
spine_turn: "Tưởng kế hoạch có các component chạy lâu dài (H2, H3) như canonical-decision-projection; hoá ra H2 và H3 chỉ nằm trong đề xuất, chưa có mã, còn kế hoạch chỉ xây công cụ di trú dùng một lần."
spine_turn_lines: ["claude:9514b261#L1048", "claude:9514b261#L1082"]
spine_action: Chạy một agent chỉ đọc để đọc kế hoạch và đề xuất rồi viết báo cáo; sau đó agent kiểm lại các điểm chính trên main.
spine_action_lines: ["claude:9514b261#L957", "claude:9514b261#L1018"]
spine_outcome: Kế hoạch không có thành phần chạy lâu dài nào. Báo cáo dài 170 dòng. Bộ kiểm sau cutover chưa được phép xây.
spine_outcome_lines: ["claude:9514b261#L1024", "claude:9514b261#L1048", "claude:9514b261#L1082"]
spine_takeaway: "Trước khi hỏi một kế hoạch có xây thành phần X không, hãy tách công cụ dùng một lần khỏi hệ thống chạy lâu dài, và kiểm xem thiết kế nằm trong kế hoạch hay chỉ trong đề xuất."
spine_takeaway_lines: ["claude:9514b261#L1048", "claude:9514b261#L1082"]
completeness: 7
---

# Kế hoạch 260925 nằm trên nhánh chưa push: agent không đọc được manifest 331 file

**Góc kể:** Forgent là nền tảng để xây ứng dụng agent, và người làm đang tìm cách gom các tài liệu nền tảng đang trùng lặp về một chủ. Ban đầu agent trả lời rằng kế hoạch có các thành phần chạy lâu dài như canonical-decision-projection, tức H2 và H3. Đọc kỹ thì sai: hai thành phần đó chỉ nằm trong đề xuất, chưa có mã, còn kế hoạch chỉ xây công cụ di trú dùng một lần. Ai đọc kế hoạch để biết có hệ thống gì sẽ dễ hiểu nhầm nếu không tách hai loại này.
**Bối cảnh:** Plan hợp nhất thẩm quyền tài liệu có phase file chỉ tồn tại trên nhánh remote, không nằm trong main checkout.
**Chuyện gì xảy ra:** Agent dùng git show trên nhánh remote để đọc phase file, nhưng đầu nhánh chỉ có commit ngày 2026-10-13, và hai đầu nhánh được ghi trong board chưa được push. Vì vậy phase 7, phase 8 bước 3 đến 5 và manifest 331 file không đọc được. Agent báo rõ điều này và không suy đoán nội dung.
**Bài học:** Plan nằm trên nhánh chưa push là plan không ai khác thấy được. Kiểm xem đầu nhánh có tồn tại trên remote trước khi phân tích.
**Artefact:** Không cần ảnh.
