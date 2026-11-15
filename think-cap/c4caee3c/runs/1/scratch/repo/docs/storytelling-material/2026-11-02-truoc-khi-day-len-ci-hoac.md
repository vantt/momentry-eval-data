---
id: 2026-11-02-truoc-khi-day-len-ci-hoac
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:c4caee3c#L1094", "claude:c4caee3c#L1323", "claude:c4caee3c#L2964", "claude:c4caee3c#L3210", "claude:c4caee3c#L3302", "claude:c4caee3c#L3311", "claude:c4caee3c#L3708", "claude:c4caee3c#L3723"]
hook: "Agent thử trên nhánh ghép riêng trước, không để CI đỏ rồi mới sửa"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi đẩy lên CI hoặc gộp vào nhánh chính, agent kiểm tra trên một nhánh ghép riêng (chk-series) rồi mới chuyển kết quả sang master; khi CI đỏ thì chẩn đoán nguyên nhân từ artifact và log trước khi đề xuất sửa.

**Chuyện gì xảy ra:** Trước khi đẩy lên CI hoặc gộp vào nhánh chính, agent kiểm tra trên một nhánh ghép riêng (chk-series) rồi mới chuyển kết quả sang master; khi CI đỏ thì chẩn đoán nguyên nhân từ artifact và log trước khi đề xuất sửa.
**Góc người ngoài:** cách làm phổ biến là Dev thường push thẳng lên nhánh chính rồi xem CI, hoặc sửa theo cảm tính khi thấy đỏ, mỗi lần sửa chờ CI vài chục phút; ở đây khác ở Lead tách rõ việc kiểm trên nhánh ghép với việc gộp, tải artifact CI về để đọc báo cáo JSON thay vì đoán, và phân loại lỗi (hạ tầng, thứ tự kết quả, khác CPU) trước khi giao việc sửa. Người đọc muốn biết cách làm để CI ít đỏ oan.
