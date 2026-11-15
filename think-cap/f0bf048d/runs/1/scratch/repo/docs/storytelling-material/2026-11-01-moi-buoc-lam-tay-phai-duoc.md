---
id: 2026-11-01-moi-buoc-lam-tay-phai-duoc
date: 2026-11-01
repo: repo
status: raw
signals: ["4", "5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2880", "claude:f0bf048d#L2948", "claude:f0bf048d#L3014", "claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3441"]
hook: "Làm tay xong thì dạy lại System Operator, rồi plan phải báo 0 thay đổi"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi bước làm tay phải được dạy lại cho System Operator

**Bối cảnh:** System Operator là agent vận hành Multica; mỗi việc người dùng làm tay phải chuyển thành quy trình của nó.
**Chuyện gì xảy ra:** Sau nhiều bước làm tay (cài runtime, đổi tên lệnh, nâng cấp, tách user), người dùng yêu cầu mọi bước đều được dạy lại cho System Operator. Mỗi lần, agent ghi quy trình vào skill, deploy lại, rồi chạy plan xác nhận 0 thay đổi. Thêm tài liệu references/privileged.md cho việc cần root.
**Bài học:** Quy trình làm tay không được nằm trong đầu người vận hành; ghi vào skill của agent và deploy lại ngay.
