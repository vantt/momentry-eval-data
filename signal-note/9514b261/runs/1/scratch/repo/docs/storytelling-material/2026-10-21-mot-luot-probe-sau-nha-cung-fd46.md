---
id: 2026-10-21-mot-luot-probe-sau-nha-cung-fd46
code: M-BZ9B
aliases: [M-BZ9B]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L2129", "claude:9514b261#L2148", "claude:9514b261#L2191", "claude:9514b261#L2284", "claude:9514b261#L2526"]
hook: "Copy một phiên đăng nhập: từ 1 lên 3 nhà cung cấp, nhưng một tài khoản treo 300 giây"
tension: khac
sides: ["Copy session đưa số nhà cung cấp chạy được từ 1 lên 3", "Một tài khoản thiếu file làm probe treo 200–300 giây"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Forgent (fgOS) là nền tảng để xây và chạy ứng dụng agent. Chủ dự án đang kiểm tra các tài khoản nhà cung cấp mô hình trước khi mở hội đồng kiến trúc.
spine_context_lines: [profile, "claude:9514b261#L1815"]
spine_want: Biết tài khoản nào còn dùng được.
spine_want_lines: ["claude:9514b261#L1940"]
spine_obstacle: "fgOS không quản lý tài khoản của các CLI, kho tài khoản rỗng; lượt probe đầu chỉ claude chạy được."
spine_obstacle_lines: ["claude:9514b261#L2148", "claude:9514b261#L2191"]
spine_action: "Chạy probe sáu family, copy lại session, rồi chạy lại đúng bộ kiểm cũ."
spine_action_lines: ["claude:9514b261#L2206", "claude:9514b261#L2212"]
spine_outcome: "Ba family chạy được là claude, deepseek và glm; openai, gemini và xai vẫn lỗi."
spine_outcome_lines: ["claude:9514b261#L2284"]
completeness: 5
---

# Một lượt probe sáu nhà cung cấp: từ một family chạy được lên ba sau khi copy session, và một tài khoản OAuth treo 300 giây

**Bối cảnh:** Owner muốn biết tài khoản nào còn dùng được trước khi mở hội đồng kiến trúc. fgOS không quản lý tài khoản của CLI (codex, claude, omp, pi), nên kho tài khoản rỗng.
**Chuyện gì xảy ra:** Lượt đầu chỉ claude chạy được, openai ra exit 11 vì màn hình đòi đăng nhập OAuth. Sau khi owner copy session, kho tài khoản có hai nhà cung cấp và deepseek, glm chạy được (từ 1 lên 3 family). Gemini và xai vẫn lỗi giao lệnh. Một tài khoản xai thiếu agent.db làm probe treo 200–300 giây.
**Bài học:** Probe bằng một lượt ngắn 'trả lời OK' cho kết quả thật nhanh hơn đọc cấu hình; và một kho đăng nhập rỗng khiến lệnh treo thay vì báo lỗi nhanh.
**Artefact:** Bảng family, invocation, kết quả probe qua các lượt (lần 1, sau copy session, sau khai tài khoản). Che email, tên tài khoản và mọi giá trị đăng nhập.
**Góc người ngoài:** cách làm phổ biến là Chạy một lệnh thử, đọc đầu ra trên màn hình, rồi đoán nguyên nhân khi lỗi, và ghi đè kết quả cũ; ở đây khác ở Kết quả so sánh được qua nhiều lượt, và có lịch sử để truy về lần trước. Người đọc sẽ hỏi làm sao để chạy lại kiểm tra cùng một cách mà không mất dấu vết cũ.
