---
id: 2026-11-03-do-cau-truc-transcript-that-ma-d5ef
code: M-Z1G3
aliases: [M-Z1G3]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L3502", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3510", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3521", "claude:ab9a1dd8#L3529", "claude:ab9a1dd8#L3539"]
hook: "Đọc cấu trúc transcript thật mà không in một chữ nội dung"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo cấu trúc transcript thật mà không in nội dung

**Bối cảnh:** Transcript của pi, omp và Antigravity là phiên làm việc thật, chứa nội dung riêng tư.
**Chuyện gì xảy ra:** Agent viết script chỉ in kiểu và tên khoá của từng bản ghi JSONL, không in giá trị. Lần đầu lệnh lỗi vì pi và omp là hàm shell bọc, phải tìm đường dẫn chương trình thật. Một probe gọi thật tới API và báo lỗi khoá, nên các probe sau chạy trong namespace mạng rỗng. Từ schema thật, bộ đọc được viết và đọc được năm transcript Antigravity.
**Bài học:** Khi đo định dạng dữ liệu riêng tư, chỉ in cấu trúc. Khi chạy thử một CLI lạ, chặn mạng để đảm bảo không có yêu cầu nào ra ngoài.
**Artefact:** Ví dụ output cấu trúc, mọi giá trị đã thay bằng kiểu dữ liệu.
