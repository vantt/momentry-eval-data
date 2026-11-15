---
id: 2026-11-02-khi-mot-agent-bao-loi-khong
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L614", "claude:2dfb5915#L820", "claude:2dfb5915#L1046", "claude:2dfb5915#L1787", "claude:2dfb5915#L1957"]
hook: "Agent báo lỗi thì không tự sửa, mà gửi báo cáo cho agent viết code"
tension: none
sides: []
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi một agent báo lỗi, không tự sửa mà gửi báo cáo review cho chính agent viết code, rồi chạy lại vòng kiểm tra trên cùng nhánh

**Chuyện gì xảy ra:** Khi một agent báo lỗi, không tự sửa mà gửi báo cáo review cho chính agent viết code, rồi chạy lại vòng kiểm tra trên cùng nhánh
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tự đọc lỗi, tự sửa, hoặc mở một phiên mới và dán lại toàn bộ ngữ cảnh; ở đây khác ở Phiên này dùng agent review độc lập, lưu báo cáo thành file, rồi gửi lại cho agent đã làm việc đó tiếp tục sửa trên đúng worktree cũ. Người đọc sẽ hỏi cách làm để agent nhớ ngữ cảnh và không phải giải thích lại.
