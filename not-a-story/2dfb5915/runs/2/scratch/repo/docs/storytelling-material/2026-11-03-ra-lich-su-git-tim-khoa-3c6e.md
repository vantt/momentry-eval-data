---
id: 2026-11-03-ra-lich-su-git-tim-khoa-3c6e
code: M-6X2B
aliases: [M-6X2B]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3829", "claude:2dfb5915#L3835", "claude:2dfb5915#L3847"]
hook: "Rà khoá trước khi mở repo: bị chặn, agent thu hẹp lệnh thay vì lách"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Rà lịch sử git tìm khoá trước khi đổi repo sang public

**Bối cảnh:** Sau khi đổi repo sang public, cần chắc không có bí mật nằm trong lịch sử commit.
**Chuyện gì xảy ra:** Lệnh rà đầu tiên bị hook chặn vì đụng vào một file nhạy cảm. Agent không đi đường vòng mà thu hẹp lệnh: chỉ grep các mẫu token, khoá Anthropic, khoá AWS và private key trong lịch sử. Kết quả là 0 khớp.
**Bài học:** Khi hook chặn, thu hẹp phạm vi việc đang làm, đừng lách sang nguồn khác.
