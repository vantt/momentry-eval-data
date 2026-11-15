---
id: 2026-11-02-doc-giay-phep-du-lieu-truoc
date: 2026-11-02
repo: repo
status: raw
signals: [Đảo quyết định có lý do, Ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2160", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "20.523 từ ghép học từ ba bộ dữ liệu mở, điểm 0,632 lên 0,983"
tension: it_ma_nhieu
sides: ["Chỉ đếm cặp âm tiết trên dữ liệu CC BY mở", "Từ điển vượt danh sách pyvi ở mọi hạng mục"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc giấy phép dữ liệu trước khi học từ điển từ ghép

**Bối cảnh:** Từ điển từ ghép ban đầu lấy từ pyvi (MIT) nhưng có ~95% trùng với Viet74K (GPL), nguồn gốc không rõ.
**Chuyện gì xảy ra:** Người dùng yêu cầu học từ điển mới bằng thống kê cặp âm tiết trên ba bộ CC BY 4.0 (ALT, Nemotron-Personas-Vietnam, văn bản pháp luật). Kết quả 20.523 từ, vi-compound từ 0,632 lên 0,983, và tốt hơn hoặc bằng danh sách pyvi ở mọi hạng mục.
**Bài học:** Kiểm nguồn gốc một danh sách 'giấy phép MIT' trước khi phát hành; học lại từ dữ liệu có giấy phép rõ có thể bằng hoặc hơn.
**Artefact:** Bảng vi-compound trước sau; không có dữ liệu riêng tư.
