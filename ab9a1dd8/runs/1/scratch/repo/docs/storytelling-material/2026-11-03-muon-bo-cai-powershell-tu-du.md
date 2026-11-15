---
id: 2026-11-03-muon-bo-cai-powershell-tu-du
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1339", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1359", "claude:ab9a1dd8#L1360"]
hook: "PowerShell 5.1 đọc sai UTF-8, nên thông báo chỉ dùng ASCII"
tension: nho_ma_to
sides: ["Vài ký tự có dấu trong thông báo", "Bộ cài hỏng khi chạy qua irm và iex"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mượn bộ cài PowerShell từ dự án khác và bài học ASCII cho 5.1

**Bối cảnh:** Skill yêu cầu ưu tiên cách đã chạy được. User có một installer PowerShell chạy ổn ở dự án khác, còn máy này không có PowerShell để kiểm.
**Chuyện gì xảy ra:** Agent chép cấu trúc từ installer có sẵn đó. Thông báo trong file chỉ dùng ASCII, vì PowerShell 5.1 đọc sai UTF-8 khi chạy qua irm và iex. Lỗi thực tế chỉ lộ ra trên CI Windows.
**Bài học:** Một cách đã chạy được trên nền tảng này chưa chắc đúng cho nền tảng mới; PowerShell 5.1 có nhiều bẫy mã hoá.
**Artefact:** Đoạn installer có dòng thông báo ASCII.
**Góc người ngoài:** cách làm phổ biến là Dev cài đặt thường viết script từ đầu, hoặc dán từ Stack Overflow, rồi sửa tới khi chạy được; ở đây khác ở Có một bộ quy tắc đóng gói có mã số (MUST/SHOULD) cùng bản cài đã được kiểm chứng ở dự án khác của mình, nên audit ra checklist đo được và không phải thiết kế lại. Người đọc muốn có 'thư viện cách làm đã chứng minh của riêng mình' để tái dùng giữa các dự án.
