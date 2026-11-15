---
id: 2026-11-02-loi-nam-ca-o-spec-python-3c6e
code: M-1PRG
aliases: [M-1PRG]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1091"]
hook: "Build lỗi giữa chừng, index sai mãi vì không ai tính lại"
tension: cam_ma_van_lot
sides: ["Parity test xanh, bản Python cũng làm y hệt", "Index sai vĩnh viễn cho tới khi chạy --full"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi nằm cả ở spec Python: build lỗi giữa chừng khiến index sai mãi

**Bối cảnh:** Review phase 09 tìm ra lỗi build không nguyên tử, và bản Python có cùng lỗi.
**Chuyện gì xảy ra:** Bản ghi note được commit trong transaction đầu, còn edges ở transaction sau. Nếu build lỗi giữa chừng, lần build tiếp theo không thấy note nào đổi nên không tính lại edges, và index sai mãi cho tới khi chạy --full. Parity không bắt được vì bản Python cũng làm vậy. Fix thêm cờ dirty trong meta và khoá file cho build đồng thời.
**Bài học:** Parity so với bản gốc chỉ chứng minh được là giống bản gốc, không chứng minh là đúng. Review độc lập vẫn cần.
