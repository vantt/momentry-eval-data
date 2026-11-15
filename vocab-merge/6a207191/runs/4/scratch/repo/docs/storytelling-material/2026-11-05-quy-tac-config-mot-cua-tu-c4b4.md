---
id: 2026-11-05-quy-tac-config-mot-cua-tu-c4b4
code: M-CS50
aliases: [M-CS50]
date: 2026-11-05
repo: repo
status: raw
signals: [ràng buộc thiết kế, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2264", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2358", "claude:6a207191#L2385", "claude:6a207191#L2393", "claude:6a207191#L2407"]
hook: "Quy tắc config một cửa thiếu cấm cờ lẻ, nên skill thêm 3 rule"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc config một cửa từ momentry đưa vào skill: CMD-22..24, CFG-12 lên MUST

**Bối cảnh:** Người dùng nhắc có quy tắc mới ở momentry: mọi cài đặt đổi qua lệnh config, kể cả cài đặt riêng từng dự án.
**Chuyện gì xảy ra:** Agent đối chiếu sáu quy tắc của momentry với skill và thấy skill thiếu quy tắc cấm cờ lẻ, thiếu --project và --repo, và file config của repo có thể chứa khóa chỉ dành cho máy. Agent thêm ba rule CMD-22..24, nâng CFG-12 lên MUST (file repo không được chứa khóa máy, bí mật hay ngân sách), và thêm UX-17 yêu cầu giao diện gọi đúng hàm ghi của CLI. Lint tăng từ 212 lên 215 rule. Agent ghi chú rằng commit của momentry chưa nằm trong bản phát hành nào.
**Bài học:** Khi một dự án thêm quy tắc mới, hãy chép nguyên tắc (không chép code) vào skill chung và ghi rõ trạng thái chưa phát hành.
**Artefact:** Bảng đối chiếu 'Ý của momentry / Skill hiện có / Đánh giá' ở L2324. Không chứa tên người.
