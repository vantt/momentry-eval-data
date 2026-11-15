---
id: 2026-11-02-powershell-5-1-lam-hong-tieng
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1237"]
hook: "PowerShell 5.1 làm hỏng dấu tiếng Việt, installer đành viết tiếng Anh"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PowerShell 5.1 làm hỏng tiếng Việt khi chạy script qua irm

**Bối cảnh:** Bộ cài Windows được viết để chạy bằng irm | iex.
**Chuyện gì xảy ra:** Theo agent, PowerShell 5.1 đọc script qua irm làm hỏng dấu tiếng Việt, nên thông báo của installer được viết tiếng Anh ASCII. Các script giữ ASCII thuần, và chưa chạy trên PowerShell 5.1 thật tại thời điểm đó.
**Bài học:** Với script cài Windows, giữ ASCII hoặc kiểm bằng PowerShell 5.1 thật.
**Artefact:** Ảnh terminal lỗi dấu nếu có.
