---
id: 2026-11-02-quyet-dinh-ky-thuat-duoc-ghi
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L244", "claude:2dfb5915#L423", "claude:2dfb5915#L505", "claude:2dfb5915#L520", "claude:2dfb5915#L819", "claude:2dfb5915#L2308", "claude:2dfb5915#L3921"]
hook: "Mọi chỗ lệch bản gốc có tên ngoại lệ; ngoại lệ thừa bị báo 'unused'"
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

# Quyết định kỹ thuật được ghi vào docs/DECISIONS.md và spec/PORTING.md ngay lúc chốt: ngày, lựa chọn, lý do, hệ quả. Mỗi chỗ lệch Python có tên ngoại lệ mà bộ so khớp đọc được, và ngoại lệ không dùng tới bị báo 'unused'.

**Chuyện gì xảy ra:** Quyết định kỹ thuật được ghi vào docs/DECISIONS.md và spec/PORTING.md ngay lúc chốt: ngày, lựa chọn, lý do, hệ quả. Mỗi chỗ lệch Python có tên ngoại lệ mà bộ so khớp đọc được, và ngoại lệ không dùng tới bị báo 'unused'.
**Góc người ngoài:** cách làm phổ biến là Quyết định nằm trong đầu, trong chat hoặc trong commit message. Chỗ lệch với bản gốc thường không ai ghi lại; ở đây khác ở Ngoại lệ là dữ liệu máy đọc được, không phải lời giải thích. Nên nếu có lệch ngoài danh sách thì harness báo ngay. Người đọc sẽ muốn nhật ký này để sau vài tuần còn nhớ vì sao.
