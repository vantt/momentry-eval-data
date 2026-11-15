---
id: 2026-10-31-github-repo-ca-nhan-khong-cap-f60d
code: M-44Y2
aliases: [M-44Y2]
date: 2026-10-31
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L2373", "claude:f0bf048d#L3324", "claude:f0bf048d#L3340"]
hook: "Repo cá nhân không cấp được quyền chỉ đọc, nên bot bị chặn bằng cơ chế"
tension: tuong_ma_hoa_ra
sides: ["Tưởng cấp được quyền chỉ đọc cho bot", "Repo cá nhân chỉ có quyền ghi, đề xuất phải rút lại"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng hệ agent AI trên máy riêng, muốn bot chỉ đọc repo để nó không ghi được vào nhánh chính. Agent đề xuất cấp quyền chỉ đọc, tưởng GitHub làm được với repo cá nhân; tra tài liệu thì hoá ra repo private của tài khoản cá nhân chỉ cho quyền ghi, nên đề xuất phải rút lại. Điều đáng để dev khác để ý: muốn giới hạn agent thì kiểm giới hạn của nền tảng trước, và quyền không có là cơ chế chặn tốt hơn lời dặn."
audience: dev dùng agent AI cho repo cá nhân
spine_context: "Người làm đang dựng hệ agent AI trên máy riêng (Multica), muốn agent tự làm nhiều việc mà không gây hậu quả nghiêm trọng hay mất dữ liệu."
spine_context_lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L3320"]
spine_want: Muốn bot chỉ đọc repo để nó không ghi được vào nhánh chính.
spine_want_lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L3327"]
spine_obstacle: Repo private của tài khoản cá nhân trên GitHub không cấp được quyền chỉ đọc; gói Free không bảo vệ được nhánh main.
spine_obstacle_lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L3327"]
spine_turn: Tưởng cấp được quyền chỉ đọc cho bot trên repo cá nhân; hoá ra GitHub không cho quyền chỉ đọc với repo private của tài khoản cá nhân.
spine_turn_lines: ["claude:f0bf048d#L2362", "claude:f0bf048d#L2365", "claude:f0bf048d#L2367"]
spine_action: "Đề xuất phương án (c), rồi tra tài liệu; khi thấy giới hạn thì rút lại đề xuất và nêu hai đường thay thế: tạo tổ chức miễn phí hoặc GitHub Pro."
spine_action_lines: ["claude:f0bf048d#L2367"]
spine_outcome: "Người làm chọn để nguyên hiện trạng, hoãn phương án tổ chức miễn phí; bot vẫn có khả năng ghi vào main."
spine_outcome_lines: ["claude:f0bf048d#L2373", "claude:f0bf048d#L3327"]
spine_takeaway: Kiểm giới hạn của nền tảng trước khi đề xuất cơ chế; quyền không có là cơ chế chặn tốt hơn lời dặn.
spine_takeaway_lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L3340"]
completeness: 7
---

# GitHub repo cá nhân không cấp được quyền chỉ đọc; chặn bằng cơ chế thay vì lời dặn

**Góc kể:** Người làm đang dựng hệ agent AI trên máy riêng, muốn bot chỉ đọc repo để nó không ghi được vào nhánh chính. Agent đề xuất cấp quyền chỉ đọc, tưởng GitHub làm được với repo cá nhân; tra tài liệu thì hoá ra repo private của tài khoản cá nhân chỉ cho quyền ghi, nên đề xuất phải rút lại. Điều đáng để dev khác để ý: muốn giới hạn agent thì kiểm giới hạn của nền tảng trước, và quyền không có là cơ chế chặn tốt hơn lời dặn.
**Bối cảnh:** Muốn bot chỉ đọc repo để nó không ghi được vào main.
**Chuyện gì xảy ra:** Agent đề xuất cấp quyền chỉ đọc cho bot. Kiểm tài liệu GitHub thì repo private của tài khoản cá nhân chỉ cấp được quyền ghi. Agent rút lại đề xuất. Còn hai lựa chọn: organization miễn phí (chưa rõ gói Free có cài đặt fork và CI cho PR từ fork hay không), hoặc GitHub Pro khoảng 4 USD một tháng. Chủ chọn hoãn. Khi đẩy script đặc quyền, agent giải thích rằng chỉ cần bot không có quyền ghi là đủ, không cần dặn nó đừng push.
**Bài học:** Kiểm giới hạn của nền tảng trước khi đề xuất cơ chế. Không có quyền ghi là cơ chế, còn đừng push là lời dặn.
**Artefact:** Bảng ba phương án với chi phí và điểm chưa chắc.
