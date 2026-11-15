---
id: 2026-11-03-hook-ghi-cung-duong-dan-node
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L1171"]
hook: "Nâng Node một lần, hook chết im lặng, không một dòng lỗi"
tension: nho_ma_to
sides: ["Chỉ nâng Node qua nvm hoặc fnm", "Hook thoát 0 và hỏng mà không ai biết"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook ghi cứng đường dẫn Node: nâng Node là hook chết im lặng

**Bối cảnh:** Cấu hình hook in ra đường dẫn node tuyệt đối. Lệnh hook luôn thoát 0 nên không ai biết khi hook đã hỏng.
**Chuyện gì xảy ra:** Nâng Node qua nvm hoặc fnm, hay chuyển thư mục clone, sẽ làm hook hỏng. Hook chỉ thoát 0 và không ghi gì nên lỗi không lộ ra. Sau khi đổi sang shim momentry cài trong PATH, hook gọi qua tên lệnh ổn định.
**Bài học:** Hook nên gọi một tên lệnh đã cài ổn định, không gọi đường dẫn runtime; hook im lặng cần doctor để lộ lỗi.
**Artefact:** Dòng command trong hooks.json trước và sau, che đường dẫn.
