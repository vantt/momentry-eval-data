---
id: 2026-11-03-dong-plan-o-45-45-khi-d5ef
code: M-G10Z
aliases: [M-G10Z]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Agent tự đánh dấu xong khi đếm việc đủ, nhưng hook nhắc lại ba lần vì còn việc chưa kiểm được."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2888", "claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3047"]
hook: "Plan đóng ở 45/45, CI xanh, mà lệnh cài trong README vẫn chưa chạy được"
tension: tuong_ma_hoa_ra
sides: ["45/45 việc xong, CI xanh, tưởng đã đóng được", "Chưa cắt v0.1.0 nên lệnh cài chưa chạy; hook Windows chưa đo"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang cố đưa nó tới tay người khác bằng lệnh cài một dòng. Plan đóng gói có 45 việc; khi đủ 45/45 và kiểm tự động (CI) báo xanh, agent đã báo là xong. Nhưng hook không cho dừng vì lệnh cài trong README chưa chạy được khi chưa có bản phát hành đầu tiên, và hook trên Windows chưa được đo trong phiên thật. Với ai build in public, checklist xanh chưa chắc là sản phẩm dùng được, nên cần liệt kê rõ điều chưa kiểm."
audience: dev dùng AI agent và build in public
spine_context: "Momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang đưa nó tới tay người khác bằng lệnh cài một dòng."
spine_context_lines: [profile]
spine_want: "Hoàn tất plan đóng gói 45 việc để lệnh cài một dòng chạy được trên Linux, macOS và Windows."
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2230"]
spine_obstacle: Hai việc cuối cần push lên GitHub để CI chạy lần đầu và cần một máy Windows thật; agent chưa được phép push nên phải hỏi lại.
spine_obstacle_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2240"]
spine_turn: "Tưởng plan đóng ở 45/45 với CI xanh là xong; hoá ra lệnh cài trong README chưa chạy được vì v0.1.0 chưa cắt, và hook Windows chưa được đo trong phiên thật."
spine_turn_lines: ["claude:ab9a1dd8#L2893", "claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L2948"]
spine_action: "Push lên main, sửa các lỗi Linux, macOS và Windows lộ ra khi CI chạy lần đầu, rồi cắt v0.1.0 và cài thử từ GitHub; sau đó thêm một workflow chỉ chạy tay để đo hook Windows."
spine_action_lines: ["claude:ab9a1dd8#L2939", "claude:ab9a1dd8#L2962", "claude:ab9a1dd8#L3042", "claude:ab9a1dd8#L3053"]
spine_outcome: "v0.1.0 đã phát hành, CI 9/9 tổ hợp xanh, lệnh cài thử từ GitHub chạy được; hook Windows vẫn chưa đo và được chuyển thành issue #1."
spine_outcome_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3042"]
spine_takeaway: "Số việc trong checklist không có nghĩa là đã xong. Trước khi báo đóng, liệt kê những gì chưa kiểm được và ghi rõ, đừng gộp vào trạng thái hoàn tất."
spine_takeaway_lines: ["claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3047"]
completeness: 7
---

# Đóng plan ở 45/45 khi điều kiện 'tốt đẹp' chưa đạt, hook phải nhắc ba lần

**Góc kể:** Momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang cố đưa nó tới tay người khác bằng lệnh cài một dòng. Plan đóng gói có 45 việc; khi đủ 45/45 và kiểm tự động (CI) báo xanh, agent đã báo là xong. Nhưng hook không cho dừng vì lệnh cài trong README chưa chạy được khi chưa có bản phát hành đầu tiên, và hook trên Windows chưa được đo trong phiên thật. Với ai build in public, checklist xanh chưa chắc là sản phẩm dùng được, nên cần liệt kê rõ điều chưa kiểm.
**Bối cảnh:** Một goal chạy tự động dùng /ak-cook cho plan đóng gói 45 việc, hook dừng agent cho đến khi điều kiện đạt.
**Chuyện gì xảy ra:** Lần nhắc đầu: agent dừng ở 43/45 để hỏi quyền push. Sau khi đạt 45/45 và CI xanh, agent vẫn báo plan đã đóng. Lần nhắc thứ hai: v0.1.0 chưa cắt nên lệnh cài trong README chưa chạy được. Lần thứ ba: hook trên Windows chưa được đo trong phiên thật.
**Bài học:** Số việc trong checklist khác với xong. Trước khi báo đóng, liệt kê những gì chưa kiểm được và ghi rõ, đừng gộp vào trạng thái hoàn tất.
**Artefact:** Chuỗi ba lần nhắc của hook, dùng làm ví dụ về điều kiện dừng.
