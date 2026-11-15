---
id: 2026-11-03-agent-tu-kiem-chung-ket-qua
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L2116", "claude:ab9a1dd8#L2122", "claude:ab9a1dd8#L2198", "claude:ab9a1dd8#L2199"]
hook: "Reviewer báo xanh, agent vẫn chạy lại toàn bộ test"
tension: tuong_ma_hoa_ra
sides: ["subagent báo mọi thứ đã xanh", "agent không tin, tự chạy lại toàn bộ"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tự kiểm chứng kết quả bằng cách chạy lại test và script thay vì tin báo cáo của subagent; khi reviewer hoặc simplify báo "xanh", agent vẫn tự chạy lại toàn bộ.

**Chuyện gì xảy ra:** Agent tự kiểm chứng kết quả bằng cách chạy lại test và script thay vì tin báo cáo của subagent; khi reviewer hoặc simplify báo "xanh", agent vẫn tự chạy lại toàn bộ.
**Góc người ngoài:** cách làm phổ biến là Nhiều người dev tin báo cáo của trợ lý hoặc chỉ nhìn một dòng "pass", không chạy lại sau khi subagent sửa code; ở đây khác ở Agent không chỉ đọc báo cáo mà chạy lại đúng các bước kiểm, và khi CI đỏ thì kéo log từng job để tìm lỗi. Người đọc muốn có thói quen này.
