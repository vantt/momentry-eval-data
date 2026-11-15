---
id: 2026-11-03-phat-hanh-co-cong-kiem-workflow-d5ef
code: M-K9B1
aliases: [M-K9B1]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L2981", "claude:ab9a1dd8#L3022", "claude:ab9a1dd8#L3042"]
hook: "Phát hành qua bản nháp: lỗi cài đặt bị bắt trước khi người dùng thấy"
tension: khac
sides: ["gắn tag rồi publish luôn", "cài thử bản nháp trên 3 hệ điều hành trước"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hành có cổng kiểm: workflow tạo bản nháp, cài thử bản nháp trên ba hệ điều hành, rồi mới công bố. Sau khi công bố, agent tải đúng lệnh cài một dòng trong README từ GitHub thật vào HOME tạm để kiểm.

**Chuyện gì xảy ra:** Phát hành có cổng kiểm: workflow tạo bản nháp, cài thử bản nháp trên ba hệ điều hành, rồi mới công bố. Sau khi công bố, agent tải đúng lệnh cài một dòng trong README từ GitHub thật vào HOME tạm để kiểm.
**Góc người ngoài:** cách làm phổ biến là Thường là gắn tag rồi publish luôn, và chỉ phát hiện lỗi cài đặt khi người dùng báo; ở đây khác ở Lỗi cài đặt bị chặn trước khi tới tay người dùng, và lệnh trong README được kiểm bằng đúng cách người dùng sẽ chạy. Người đọc sẽ hỏi làm sao để biết lệnh cài trong README thật sự chạy được.
