---
id: 2026-11-02-hook-chan-ghi-decisions-md-vi
date: 2026-11-02
repo: repo
status: raw
signals: [sự cố vặt]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L513", "claude:2dfb5915#L520"]
hook: "Hook chặn ghi nhật ký chỉ vì tên file có chữ build"
tension: nho_ma_to
sides: ["Chỉ vì một chữ 'build' trong pattern", "Hook chặn cả việc ghi nhật ký"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn ghi DECISIONS.md vì pattern ckignore có chữ build

**Bối cảnh:** Agent cần ghi quyết định mới vào docs.
**Chuyện gì xảy ra:** Lệnh nối vào file bị chặn kèm thông báo thêm !build vào ckignore. Agent không sửa cấu hình hook mà ghi nội dung vào file tạm rồi nối vào; kết quả giống nhau.
**Bài học:** Khi hook chặn, đi vòng qua file tạm là lựa chọn hợp lý, nhưng nên ghi lại để user biết.
**Artefact:** Không có.
