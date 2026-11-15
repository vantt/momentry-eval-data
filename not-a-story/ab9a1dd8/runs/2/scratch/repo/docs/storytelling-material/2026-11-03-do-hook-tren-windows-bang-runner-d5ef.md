---
id: 2026-11-03-do-hook-tren-windows-bang-runner-d5ef
code: M-HZKJ
aliases: [M-HZKJ]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3068", "claude:ab9a1dd8#L3077", "claude:ab9a1dd8#L3091", "claude:ab9a1dd8#L3099", "claude:ab9a1dd8#L3149", "claude:ab9a1dd8#L3213", "claude:ab9a1dd8#L3239"]
hook: "Không có tài khoản, vẫn chứng minh hook Windows chạy nhờ một dòng log"
tension: it_ma_nhieu
sides: ["Runner không có khoá API, phiên báo lỗi đăng nhập", "Dòng hook.spawned chứng minh hook chạy trước lỗi; Codex vẫn chưa chứng minh được"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo hook trên Windows bằng runner CI không có tài khoản: hook.spawned trước lúc phiên báo lỗi đăng nhập

**Bối cảnh:** Chủ dự án muốn biết Claude Code và Codex thật có gọi hook momentry trên Windows không. Không có máy Windows thật để thử tay.
**Chuyện gì xảy ra:** Probe là workflow chạy tay trên windows-2025: cài Claude Code và Codex, cài momentry, init, rồi mở phiên không có khoá API. Dòng hook.spawned trong hook.log là bằng chứng hook được gọi trước khi phiên báo lỗi. Claude Code đạt bước này. Codex cần duyệt tin cậy qua trusted_hash sha256; agent đọc mã nguồn Codex, thử cờ bypass, nhưng lần chạy Codex vẫn thất bại nên chưa chứng minh được.
**Bài học:** Để đo công cụ AI mà không có tài khoản, đo tín hiệu xảy ra trước lỗi, như log hook được gọi, thay vì chờ phiên chạy thành công.
**Artefact:** Dòng hook.spawned trong log job Actions. Che tên runner nếu cần.
