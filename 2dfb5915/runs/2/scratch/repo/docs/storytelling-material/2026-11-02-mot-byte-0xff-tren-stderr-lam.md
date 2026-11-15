---
id: 2026-11-02-mot-byte-0xff-tren-stderr-lam
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L607", "claude:2dfb5915#L631"]
hook: "Một byte 0xFF trên stderr làm cả OHS treo cứng"
tension: nho_ma_to
sides: ["một byte 0xFF", "cả OHS treo, mỗi search chờ 60 giây"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một byte 0xFF trên stderr làm OHS treo

**Bối cảnh:** Reviewer đọc module OHS, nghĩ tới máy Windows dùng code page tiếng Việt.
**Chuyện gì xảy ra:** Hàm đọc stderr dừng khi gặp UTF-8 sai. Pipe đầy (khoảng 4 KB trên Windows), mọi console.error của OHS bị chặn và event loop đứng. Stdout vẫn mở nên không có sự kiện thoát, không restart, và mỗi search timeout 60 giây. Một mutex giữ khi ghi stdin không có giới hạn thời gian làm pkm không thoát được. Hai lỗi High được sửa bằng luồng ghi riêng và đọc stderr đến EOF.
**Bài học:** Đọc stderr của tiến trình con phải đọc đến hết và chịu được lỗi encoding. Một luồng dừng âm thầm có thể làm cả tiến trình treo.
**Artefact:** Sơ đồ luồng stdout, stderr, stdin.
