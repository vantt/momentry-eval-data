---
id: 2026-11-03-simplify-8-cho-sau-khi-viet
date: 2026-11-03
repo: repo
status: raw
signals: [số trước số sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2174", "claude:ab9a1dd8#L2198", "claude:ab9a1dd8#L2200"]
hook: "Rút gọn 8 chỗ trong 7 file, test vẫn 232/232"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Simplify 8 chỗ sau khi viết xong: tests giữ nguyên 232/232

**Bối cảnh:** Sau khi các module mới xong, một agent được giao rà lại để rút gọn code trùng lặp mà không đổi hành vi.
**Chuyện gì xảy ra:** Agent rút gọn 8 chỗ trong 7 file: gộp đoạn lặp ra helper, tính điều kiện một lần, đổi tên biến trung gian. Chạy lại test, lifecycle và vòng agent đều xanh, số test vẫn 232 qua và không fail.
**Bài học:** Tách bước rút gọn ra khỏi bước viết và kiểm chặt bằng test trước và sau; số test không đổi là bằng chứng hành vi không đổi.
**Artefact:** Bảng 8 chỗ rút gọn, cột file và cột tóm tắt. Không cần che gì.
