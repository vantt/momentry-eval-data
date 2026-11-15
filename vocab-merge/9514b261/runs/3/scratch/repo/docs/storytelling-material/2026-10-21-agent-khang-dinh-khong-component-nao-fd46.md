---
id: 2026-10-21-agent-khang-dinh-khong-component-nao-fd46
code: M-NP8Q
aliases: [M-NP8Q]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L363", "claude:9514b261#L383", "claude:9514b261#L394", "claude:9514b261#L542"]
hook: "Agent khẳng định 'không component nào quản', người duyệt nhắc ra một việc đã xong"
tension: nguoi_dung_may_sai
sides: ["Agent tra hai tài liệu, không thấy hàng chủ, kết luận ba máy kiểm không ai quản", "Người duyệt nhắc đúng: tsk-1lv đã done cùng sáu item con, hai trong ba máy thuộc nó"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent khẳng định 'không component nào quản' rồi người dùng nhắc ra một component đã xong

**Bối cảnh:** Agent lập plan cho ba máy kiểm vệ sinh repo và cần biết chủ của từng máy theo bản đồ kiến trúc.
**Chuyện gì xảy ra:** Agent tra architecture-manifest và reading-map, không thấy hàng chủ, rồi kết luận ba máy kiểm không thuộc component nào. Người duyệt hỏi lại «kiểm là kiểm gì» và nhắc một component đã gom và làm tươi luật. Tìm trong work items thì thấy tsk-1lv đã done cùng sáu item con, và state có 699 quyết định. Hai trong ba máy thuộc dòng việc này, nên agent phải đính chính.
**Bài học:** Trước khi kết luận chưa ai quản, tìm trong work item đã done và lịch sử thiết kế, đừng chỉ tìm trong bản đồ kiến trúc.
**Artefact:** Bảng ba máy kiểm: cái nó canh, lúc nào chạy, chủ theo bằng chứng. Không kèm đường dẫn nội bộ.
