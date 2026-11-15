---
id: 2026-11-02-diem-cham-dau-tien-la-cua-c4b4
code: M-BP36
aliases: [M-BP36]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L578", "claude:6a207191#L586", "claude:6a207191#L636", "claude:6a207191#L657", "claude:6a207191#L661", "claude:6a207191#L681", "claude:6a207191#L690"]
hook: "Skill xếp lại: trải nghiệm người dùng đứng trước cả an toàn"
tension: chon_mot_mat_mot
sides: ["Giới thiệu và quick start 3 lệnh lên đầu", "An toàn và đúng đắn bị đẩy xuống cuối"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một bộ hướng dẫn đóng gói và phân phối cho công cụ dòng lệnh, và người làm muốn dùng lại nó cho mọi dự án sau này. Họ tưởng skill đã đủ vì script kiểm tra cấu trúc chạy qua 230 rule. Một agent độc lập đọc theo đúng quy trình lại tìm ra các lệnh mâu thuẫn nhau, mẫu cài đặt vi phạm chính các rule đó, và phần 'cách đã kiểm chứng' trỏ sang dự án khác ngôn ngữ. Ai viết quy tắc cho agent cũng dễ mắc lỗi này, vì kiểm tra cấu trúc xanh không có nghĩa nội dung đã đúng."
audience: người viết skill hoặc tài liệu cho agent
spine_context: "Người làm đang viết một bộ skill hướng dẫn đóng gói và phân phối (cài, cập nhật, cấu hình, doctor) cho các công cụ dòng lệnh, để dùng lại cho các dự án sau."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: "Muốn điểm chạm đầu tiên (giới thiệu, cài đặt, quick start) đủ tốt để người dùng ở lại và phần mềm bán hoặc promote được."
spine_want_lines: ["claude:6a207191#L578"]
spine_obstacle: "Skill mới có một phần: thiếu câu giới thiệu, thời gian đến kết quả đầu tiên, quick start được test trong CI, demo và khoảnh khắc chạy được ngay lần đầu."
spine_obstacle_lines: ["claude:6a207191#L586"]
spine_turn: "Tưởng skill đã đủ vì script kiểm tra cấu trúc chạy qua 230 rule. Hoá ra review độc lập tìm ra lệnh mâu thuẫn (INS-13 bảo dùng 'setup', CMD-04 nói không có 'setup'), mẫu install.sh vi phạm chính các rule đó, và phần 'cách đã kiểm chứng' trỏ sang dự án khác ngôn ngữ."
spine_turn_lines: ["claude:6a207191#L653", "claude:6a207191#L690"]
spine_action: "Thêm file riêng cho điểm chạm đầu tiên, thêm nhóm rule agent-native (CMD-13 đến CMD-19), rồi giao một agent độc lập review toàn bộ skill."
spine_action_lines: ["claude:6a207191#L633", "claude:6a207191#L657", "claude:6a207191#L675"]
spine_outcome: "Review kết luận skill 'về cơ bản dùng được', nhưng nêu 9 điểm cần sửa, trong đó 3 điểm phải sửa ngay."
spine_outcome_lines: ["claude:6a207191#L690", "claude:6a207191#L697"]
spine_takeaway: Kiểm tra cấu trúc xanh không chứng minh nội dung nhất quán. Cần một agent độc lập đọc theo đúng quy trình để tìm mâu thuẫn trong nội dung.
spine_takeaway_lines: ["claude:6a207191#L653", "claude:6a207191#L690"]
completeness: 7
---

# Điểm chạm đầu tiên là cửa hàng: giới thiệu, quick start và agent-native đứng trước kỹ thuật

**Góc kể:** Dự án là một bộ hướng dẫn đóng gói và phân phối cho công cụ dòng lệnh, và người làm muốn dùng lại nó cho mọi dự án sau này. Họ tưởng skill đã đủ vì script kiểm tra cấu trúc chạy qua 230 rule. Một agent độc lập đọc theo đúng quy trình lại tìm ra các lệnh mâu thuẫn nhau, mẫu cài đặt vi phạm chính các rule đó, và phần 'cách đã kiểm chứng' trỏ sang dự án khác ngôn ngữ. Ai viết quy tắc cho agent cũng dễ mắc lỗi này, vì kiểm tra cấu trúc xanh không có nghĩa nội dung đã đúng.
**Bối cảnh:** Chủ dự án nói điểm chạm đầu tiên của người dùng là cài đặt, phần giới thiệu và quick start, nên đó là nơi bán được hay mất người dùng.
**Chuyện gì xảy ra:** Skill được xếp lại theo tầng: UX trước, rồi cú pháp lệnh và agent-native, cuối cùng mới đến an toàn, đúng đắn, nhanh gọn. Thêm rule cho README: tagline nói về lợi ích, quick start tối đa 3 lệnh trong khoảng 2 phút, quick start chạy thật trong CI. Thêm bài kiểm tra: một agent mới chỉ được đọc --help, phải tự cài và làm cho tool chạy được.
**Bài học:** Với công cụ dùng cho agent, coi --help là tài liệu chính, và đo bằng việc một agent sạch có tự cài xong không.
**Artefact:** Dòng mẫu 'cài X từ <url>, rồi làm theo x init --help'. Cần che URL và tên tool trước khi đăng.
**Góc người ngoài:** cách làm phổ biến là README viết cho người đọc. Hướng dẫn cài đặt thường là vài đoạn văn, và `--help` thường chỉ liệt kê cờ mà không có bước tiếp theo hay ví dụ chạy được; ở đây khác ở Ở đây `--help` được coi là hợp đồng với agent: có ví dụ copy được, mã thoát, và dòng 'Next:' chỉ bước tiếp. Người đọc sẽ muốn biết vì sao một lệnh đọc được lại thay cho cả tài liệu.
