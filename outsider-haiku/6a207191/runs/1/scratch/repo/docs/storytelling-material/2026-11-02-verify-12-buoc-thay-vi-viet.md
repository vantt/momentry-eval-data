---
id: 2026-11-02-verify-12-buoc-thay-vi-viet
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L900", "claude:6a207191#L910", "claude:6a207191#L922", "claude:6a207191#L929", "claude:6a207191#L934", "claude:6a207191#L937", "claude:6a207191#L951"]
hook: "Không viết script 30 check, chỉ 12 bước verify vì chuẩn còn đổi"
tension: khac
sides: ["script nhất quán và nhanh hơn", "chuẩn còn đổi nên khóa vào code là sớm"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Verify 12 bước thay vì viết script: chưa khóa quy tắc vào code khi chuẩn còn đổi

**Bối cảnh:** Skill tự kiểm tra chính nó bằng script, nhưng với dự án thật agent phải tự đánh done hoặc gap, dễ sai và mỗi lần một kiểu.
**Chuyện gì xảy ra:** Agent đề xuất script audit khoảng 25 đến 30 check. Người dùng hỏi không có script thì agent có làm được không, và agent trả lời là có. Script đổi lấy tính nhất quán và tốc độ, nhưng phải bảo trì và đi ngược mục tiêu giữ skill gọn. Quyết định cuối: 12 bước verify trong SKILL.md, trong đó chỉ hai bước cần phán đoán, phần còn lại là lệnh máy. Script được để dành cho lúc chuẩn đã ổn định.
**Bài học:** Đừng viết script kiểm tra khi quy tắc còn đổi. Viết danh sách lệnh cụ thể trước, script để sau khi chuẩn đã ổn định.
**Artefact:** Bảng 12 bước với hai cột: kiểm tra gì, và loại kiểm tra là máy hay phán đoán.
