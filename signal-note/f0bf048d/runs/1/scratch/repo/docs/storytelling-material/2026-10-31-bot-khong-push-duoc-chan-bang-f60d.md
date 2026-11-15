---
id: 2026-10-31-bot-khong-push-duoc-chan-bang-f60d
code: M-SQAK
aliases: [M-SQAK]
date: 2026-10-31
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2289", "claude:f0bf048d#L2351", "claude:f0bf048d#L2354", "claude:f0bf048d#L2367", "claude:f0bf048d#L2373", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
hook: "Muốn cấp bot quyền chỉ đọc, nhưng repo cá nhân không có quyền đó"
tension: tuong_ma_hoa_ra
sides: ["agent đề xuất quyền chỉ đọc", "GitHub không cho, bot có quyền ghi thì --no-verify vượt hook"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người dựng hệ agent Multica trên máy cá nhân, để bot System Operator làm việc trên repo mà không đẩy được thay đổi lên nhánh main. Agent đề xuất cấp cho bot quyền chỉ đọc, nghĩ rằng GitHub cho làm được. Đọc tài liệu mới biết repo private cá nhân không có quyền chỉ đọc cho collaborator, nên phương án này không chạy được. Người dùng agent nên kiểm tài liệu nền tảng trước khi tin một phương án phân quyền, và đặt giới hạn bằng quyền hệ thống chứ không bằng lời dặn."
audience: dev cho agent AI có quyền ghi vào repo
spine_context: "Một người dựng hệ agent Multica trên máy cá nhân, gồm System Operator và các agent của các dự án, làm việc trên repo fgOPC và opc-studio-app."
spine_context_lines: ["claude:f0bf048d#L2284"]
spine_want: Muốn System Operator không thể đẩy thay đổi lên repo mà không qua tay người duyệt.
spine_want_lines: ["claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
spine_obstacle: "Repo private của tài khoản cá nhân trên GitHub Free không cấp được quyền chỉ đọc cho collaborator, và không bảo vệ được nhánh main."
spine_obstacle_lines: ["claude:f0bf048d#L2354", "claude:f0bf048d#L3327"]
spine_turn: Tưởng cấp quyền chỉ đọc cho bot là làm được; hoá ra GitHub không cho quyền chỉ đọc với repo private cá nhân.
spine_turn_lines: ["claude:f0bf048d#L2354", "claude:f0bf048d#L2367"]
spine_action: "Agent kiểm tài liệu GitHub, nhận đã đề xuất sai và xin lỗi, rồi đưa ra hai hướng khác; chủ chọn giữ nguyên hiện trạng."
spine_action_lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L2373"]
spine_outcome: "Chưa đổi gì trên GitHub; repo giữ nguyên, việc chọn cơ chế chặn được hoãn."
spine_outcome_lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L2373"]
spine_takeaway: "Kiểm tài liệu của nền tảng trước khi đề xuất một phương án phân quyền; giới hạn an toàn phải nằm ở quyền hệ thống, không ở lời dặn."
spine_takeaway_lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L3340"]
completeness: 7
---

# Bot không push được: chặn bằng quyền, không bằng lời dặn

**Góc kể:** Một người dựng hệ agent Multica trên máy cá nhân, để bot System Operator làm việc trên repo mà không đẩy được thay đổi lên nhánh main. Agent đề xuất cấp cho bot quyền chỉ đọc, nghĩ rằng GitHub cho làm được. Đọc tài liệu mới biết repo private cá nhân không có quyền chỉ đọc cho collaborator, nên phương án này không chạy được. Người dùng agent nên kiểm tài liệu nền tảng trước khi tin một phương án phân quyền, và đặt giới hạn bằng quyền hệ thống chứ không bằng lời dặn.
**Bối cảnh:** Repo private của tài khoản cá nhân trên GitHub Free. Muốn bot làm việc an toàn trên repo.
**Chuyện gì xảy ra:** Agent đề xuất phương án (c): cấp quyền chỉ đọc. Khi kiểm tài liệu GitHub thì biết repo private cá nhân không cho quyền chỉ đọc, phương án này không làm được; agent đính chính và xin lỗi. Chủ chọn hoãn. Khi chủ hỏi vì sao không push, lý do là bot có quyền ghi thì ghi được main, hook pre-push vượt được bằng --no-verify. Phương án thay thế: deploy key chỉ đọc, bot commit nhánh riêng, chủ fetch và merge.
**Bài học:** Giới hạn an toàn phải là quyền hệ thống, không phải lời dặn. Kiểm tài liệu của nền tảng trước khi đề xuất một phương án.
**Artefact:** Câu đính chính của agent (không cần ảnh).
