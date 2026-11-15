---
id: 2026-11-03-205-test-xanh-tren-ban-clone-d5ef
code: M-P5XC
aliases: [M-P5XC]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L177", "claude:ab9a1dd8#L236"]
hook: "Bản clone sạch 205 test xanh, bản đang làm việc lại đỏ"
tension: tuong_ma_hoa_ra
sides: ["Test xanh 205/205 trên bản clone sạch", "Bản làm việc đỏ vì test quét cả thư mục chưa commit"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một người làm momentry, công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, đang audit cách đóng gói công cụ theo skill cs-packaging-distribution."
spine_context_lines: [profile, "claude:ab9a1dd8#L9"]
spine_want: "Muốn công cụ đóng gói được cho người mới và agent: cài đặt, cập nhật, chữa lỗi đều chạy được bằng một lệnh."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Phần phân phối gần như chưa có: không có installer, không có doctor, init --yes báo Unknown option."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_action: "Chạy các bước kiểm của skill trong HOME tạm, và chạy test trên bản clone sạch để so với bản làm việc."
spine_action_lines: ["claude:ab9a1dd8#L167", "claude:ab9a1dd8#L170"]
spine_outcome: Bản clone sạch qua 205/205 test; bản làm việc chỉ 202/203 vì test quét thư mục chưa commit.
spine_outcome_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L236"]
spine_takeaway: "Test kiểm import phải quét đúng tập file đã commit, hoặc chạy trên clone sạch trong CI."
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 6
---

# 205 test xanh trên bản clone sạch, 202/203 trên bản làm việc: test quét cả thư mục chưa commit

**Bối cảnh:** Audit đóng gói momentry theo skill cs-packaging-distribution, chạy test trên bản làm việc và trên bản clone sạch.
**Chuyện gì xảy ra:** Bản clone sạch chạy 205/205 test xanh. Bản làm việc chỉ được 202/203 vì imports.test.mjs quét cả .claude và .agentkit chưa đưa vào git. Audit cũng cho thấy không có installer, không có doctor, init --yes báo Unknown option, và hook có thể chết im lặng.
**Bài học:** Test kiểm import phải quét đúng tập file đã commit, hoặc chạy trên clone sạch trong CI; nếu không, test xanh trên máy này nhưng đỏ ở nơi khác.
**Artefact:** Bảng so sánh hai lần chạy test (205/205 clone sạch, 202/203 bản làm việc). Không có thông tin riêng tư.
