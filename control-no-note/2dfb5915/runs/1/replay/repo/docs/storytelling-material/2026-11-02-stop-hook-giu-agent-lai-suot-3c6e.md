---
id: 2026-11-02-stop-hook-giu-agent-lai-suot-3c6e
code: M-NVFX
aliases: [M-NVFX]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L477", "claude:2dfb5915#L2147", "claude:2dfb5915#L2539", "claude:2dfb5915#L2572", "claude:2dfb5915#L2872"]
hook: "Hook giữ agent hơn 20 lượt vì điều kiện không bao giờ đạt"
tension: giup_ma_hai
sides: ["Hook đòi xong cả plan mới cho dừng", "Phần còn lại chỉ người mới mở được, agent lặp «vẫn đang chờ»"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ agent lại suốt nhiều lượt vì điều kiện 'xong cả plan' không đạt được

**Bối cảnh:** Người dùng đặt điều kiện cho phiên: hoàn tất toàn bộ plan. Stop hook sẽ chặn dừng cho tới khi điều kiện đúng.
**Chuyện gì xảy ra:** Phần còn lại của plan phụ thuộc vào máy Windows, vault thật và một tuần dùng song song, tức các cổng chỉ người mới mở được. Hook chặn dừng hơn 20 lượt với cùng một lý do, còn agent lặp lại câu «vẫn đang chờ». Người dùng phải tự xoá goal thì mới dừng được.
**Bài học:** Đừng đặt điều kiện dừng mà một phần của nó nằm ngoài tầm tay agent, vì agent sẽ bị kẹt vòng lặp. Hãy ghi rõ phần nào là cổng của người.
**Artefact:** Trích các thông báo hook lặp lại (chụp, không lộ nội dung vault).
