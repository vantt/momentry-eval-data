---
id: 2026-11-02-khoi-phuc-dau-cho-embedding-hoi
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2842", "claude:c4caee3c#L2919"]
hook: "Khôi phục dấu biến Hội An thành hội ăn"
tension: giup_ma_hai
sides: ["Tính năng thêm dấu để tìm đúng hơn", "Hội An bị đổi thành hội ăn"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khôi phục dấu cho embedding: Hội An thành hội ăn

**Bối cảnh:** Với câu có dấu một phần, lớp khôi phục dấu đổi tên riêng chưa có dấu thành từ thông dụng hơn trong vault.
**Chuyện gì xảy ra:** Với câu Hội An, từ An có tỷ lệ 0,5 nên không được coi là câu có dấu, và được khôi phục thành ăn. Ngưỡng 50 % không sai; lỗi nằm ở cách dựng câu gửi cho model nhúng. Sửa bằng cách không đổi từ đã gõ dấu và chỉ khôi phục từ mà vault không bao giờ viết trần. Bật tuỳ chọn này mặc định đưa nDCG@5 tổng từ 0,932 lên 0,954 và sửa hạng mục snippet.
**Bài học:** Một ngưỡng đúng vẫn có thể gây lỗi nếu đầu ra của nó bị dùng sai; hãy chứng minh nguyên nhân bằng test thất bại trước khi sửa.
**Artefact:** Ví dụ Hội An trước và sau khi khôi phục, cùng bảng nDCG. Không cần che.
