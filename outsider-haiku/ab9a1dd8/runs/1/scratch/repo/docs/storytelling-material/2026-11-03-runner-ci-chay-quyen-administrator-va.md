---
id: 2026-11-03-runner-ci-chay-quyen-administrator-va
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2614", "claude:ab9a1dd8#L2615", "claude:ab9a1dd8#L2674", "claude:ab9a1dd8#L2810"]
hook: "Runner CI chạy Administrator và PowerShell 5.1 làm hỏng JSON; sửa xong 231 pass"
tension: khac
sides: ["môi trường CI làm hỏng JSON và quyền chạy", "sửa test xong 231 pass, 0 fail"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Runner CI chạy quyền Administrator và PowerShell 5.1 làm hỏng JSON

**Bối cảnh:** Lifecycle installer trên Windows chạy trong CI. Lần đầu bước này treo tới timeout 600 giây rồi đỏ.
**Chuyện gì xảy ra:** Installer từ chối chạy khi đang là Administrator, nên test bật biến cho phép root. PowerShell 5.1 làm hỏng JSON truyền cho chương trình ngoài, nên test Windows dùng momentry config privacy-add thay cho config set kèm JSON. Lần chạy cuối trên Windows: 231 pass, 0 fail.
**Bài học:** Đối số có dấu nháy kép đi qua PowerShell 5.1 dễ hỏng; tránh truyền JSON thô qua đó.
**Artefact:** Dòng log lifecycle OK trên Windows.
