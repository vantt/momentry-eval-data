---
id: 2026-10-21-regex-tieng-viet-ky-tu-d
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L811"]
hook: "Regex tiếng Việt bỏ sót chữ 'đ' đứng đầu từ"
tension: nho_ma_to
sides: ["Một ký tự đ đứng đầu từ", "\\b coi hai phía là non-word nên không khớp"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Regex tiếng Việt: ký tự đ ở đầu từ không khớp với \b

**Bối cảnh:** Agent tìm trong code một hàm kiểm tra từ khoá, và thấy comment nguồn nói về cách biên từ không khớp với chữ đ.
**Chuyện gì xảy ra:** Comment ghi rằng trong regex, đ đứng đầu một từ có dấu không khớp, vì \b coi cả hai phía là non-word. Comment nói đã xác nhận bằng test trực tiếp. Agent chưa đi xa hơn vì đây chỉ là đọc code.
**Bài học:** \b trong regex JavaScript chỉ coi ASCII là chữ. Với tiếng Việt, dùng lookaround hoặc lớp Unicode thay vì \b.
**Artefact:** Đoạn regex minh hoạ với ví dụ từ, đã che nội dung nhạy cảm.
