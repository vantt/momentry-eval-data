---
id: 2026-11-03-hook-tu-cai-hay-chi-in
date: 2026-11-03
repo: repo
status: raw
signals: [đảo quyết định, người duyệt]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L251", "claude:ab9a1dd8#L256", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340"]
hook: "PRD đã chốt chỉ in lệnh, nhưng tôi chọn tự cài 200-300 dòng"
tension: khac
sides: ["quyết định đã chốt trong PRD: chỉ in", "user chọn tự sửa file cấu hình"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook tự cài hay chỉ in? Đảo quyết định đã chốt trong PRD

**Bối cảnh:** PRD ghi công cụ không bao giờ tự sửa settings của Claude Code hay Codex. Người mới phải tự dán JSON vào file.
**Chuyện gì xảy ra:** Agent đưa hai phương án: chỉ in kèm doctor kiểm tra, hoặc tự cài. Ước tự cài khoảng 200 đến 300 dòng cộng test. User chọn tự cài. Cách làm an toàn gồm sao lưu trước khi sửa, từ chối nếu file đang hỏng, ghi qua file tạm rồi đổi tên, và chỉ đụng mục có lệnh momentry hook.
**Bài học:** Khi tool muốn tự sửa file cấu hình chung, việc khó không nằm ở số dòng mà ở chỗ nhận diện đúng mục của mình để gỡ.
**Artefact:** Đoạn settings.json trước và sau khi init, che đường dẫn.
