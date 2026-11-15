---
id: 2026-10-21-ba-he-decision-document-context-va
date: 2026-10-21
repo: repo
status: raw
signals: [artefact nhìn được, ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1798", "claude:9514b261#L1801"]
hook: "Hai hệ quản lý tài liệu dùng nhau, thành vòng tròn không lối ra"
tension: hop_ma_tan
sides: ["Ba hệ decision, document, context, mỗi hệ đều chạy tốt", "Hai hệ dùng nhau tạo vòng phụ thuộc khi ghi"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba hệ decision, document, context và vòng phụ thuộc phải cắt theo lớp

**Bối cảnh:** Người dùng gợi ý nhìn tổng quan thành ba hệ liên quan nhau. Proposal hiện chỉ có hai engine.
**Chuyện gì xảy ra:** Agent lập bảng ba hệ theo trạng thái hiện có (tsk-1lv đã xong, Knowledge Registry chạy, instruction registry chỉ có hạt giống) và bảng ai dùng ai. Hai cột đầu dùng nhau thật ở mức dữ liệu, tạo vòng phụ thuộc khi quét lúc ghi. Đề xuất cắt theo lớp để đọc một chiều.
**Bài học:** Vẽ ma trận ai dùng ai trước khi đặt tên component; vòng phụ thuộc thường lộ ra ở đó.
**Artefact:** Ma trận 3x3 ai đọc gì, ghi gì, và sơ đồ lớp một chiều.
