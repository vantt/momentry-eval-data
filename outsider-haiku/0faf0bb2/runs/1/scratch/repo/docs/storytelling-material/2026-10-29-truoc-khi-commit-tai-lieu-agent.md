---
id: 2026-10-29-truoc-khi-commit-tai-lieu-agent
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:0faf0bb2#L3913", "claude:0faf0bb2#L3914", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3917", "claude:0faf0bb2#L3924"]
hook: "Commit tài liệu mà không quét secret, thường chỉ biết khi CI báo hoặc đã push"
tension: nho_ma_to
sides: ["một commit tài liệu tưởng vô hại", "kéo theo token lọt lên repo, biết sau khi đã push"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi commit tài liệu, agent quét các file mới bằng regex tìm token, khoá và mật khẩu, đồng thời chỉ stage những file của mình khi repo đang có thay đổi chưa commit của người khác.

**Chuyện gì xảy ra:** Trước khi commit tài liệu, agent quét các file mới bằng regex tìm token, khoá và mật khẩu, đồng thời chỉ stage những file của mình khi repo đang có thay đổi chưa commit của người khác.
**Góc người ngoài:** cách làm phổ biến là Commit toàn bộ thay đổi trong working tree, và chỉ tình cờ phát hiện secret khi đã push hoặc khi tool quét CI báo; ở đây khác ở Secret và thay đổi không liên quan được chặn trước khi vào lịch sử git, nên không cần viết lại history sau đó.
