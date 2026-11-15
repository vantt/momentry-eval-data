---
id: 2026-11-02-dung-agent-khac-de-review-ma-3c6e
code: M-D8JE
aliases: [M-D8JE]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L615", "claude:2dfb5915#L1045", "claude:2dfb5915#L1046", "claude:2dfb5915#L1781"]
hook: "Agent review báo lỗi, agent viết code tự sửa"
tension: none
sides: []
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng agent khác để review mã và báo lỗi, rồi chuyển lỗi về đúng agent đã viết để nó tự sửa

**Chuyện gì xảy ra:** Dùng agent khác để review mã và báo lỗi, rồi chuyển lỗi về đúng agent đã viết để nó tự sửa
**Góc người ngoài:** cách làm phổ biến là Thường người viết tự sửa theo ý mình, hoặc người review sửa thẳng code của người khác; ở đây khác ở Vòng review-sửa lặp lại có ghi rõ đường dẫn báo cáo và mức độ lỗi (High/Medium), agent gốc tự nhận và sửa trên nhánh của nó, sau đó CI xác nhận. Người đọc muốn biết cách có vòng kiểm tra độc lập mà không mất công sức của người viết.
