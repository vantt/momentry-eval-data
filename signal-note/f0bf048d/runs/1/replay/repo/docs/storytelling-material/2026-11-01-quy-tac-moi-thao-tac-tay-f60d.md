---
id: 2026-11-01-quy-tac-moi-thao-tac-tay-f60d
code: M-ZDJK
aliases: [M-ZDJK]
date: 2026-11-01
repo: repo
status: raw
signals: [nguoi_duyet_may_soan]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3294", "claude:f0bf048d#L3304", "claude:f0bf048d#L3305", "claude:f0bf048d#L3320", "claude:f0bf048d#L3441"]
hook: "Mọi thao tác tay của chủ phải được dạy lại cho agent"
tension: khac
sides: ["chủ làm tay cho nhanh", "mỗi việc tay phải thành kiến thức cho agent"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc: mọi thao tác tay cho ops phải được dạy lại cho System Operator

**Bối cảnh:** Chủ muốn tách System Operator khỏi user có docker, và yêu cầu mọi bước sẽ làm phải được dạy lại cho agent.
**Chuyện gì xảy ra:** Agent ghi nguyên tắc vào memory, viết kế hoạch 7 bước cho Giai đoạn 2, và mỗi bước đều có cột việc chủ cần làm. Agent thêm tài liệu về quyền qua cổng riêng (privileged.md) và cập nhật SKILL.md. Kế hoạch được ghi vào repo để chủ duyệt trước khi chạy gì trên máy.
**Bài học:** Mỗi thao tác tay trên máy phải có một dòng trong hướng dẫn của agent vận hành. Nếu không, lần sau agent không làm được việc đó.
**Artefact:** Bảng 7 bước với cột 'Anh làm gì'.
