---
id: 2026-11-02-moi-module-loi-xong-thi-mo
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L614", "claude:2dfb5915#L768", "claude:2dfb5915#L819", "claude:2dfb5915#L989", "claude:2dfb5915#L1045", "claude:2dfb5915#L1728", "claude:2dfb5915#L1780"]
hook: "Agent review chỉ đọc, không viết, mà bắt được alias bomb ăn hết bộ nhớ"
tension: khac
sides: ["agent review chỉ đọc, không sửa dòng nào", "vẫn bắt được lỗi treo, alias bomb và index cũ vĩnh viễn"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mỗi module lõi xong thì mở thêm một agent review độc lập, chỉ đọc. Báo cáo review được gửi lại cho agent đã viết để sửa trên nhánh của nó. Review tìm ra lỗi thật như treo khi stderr có byte không phải UTF-8, alias bomb làm hết bộ nhớ, build lỗi nửa chừng để lại index cũ vĩnh viễn.

**Chuyện gì xảy ra:** Mỗi module lõi xong thì mở thêm một agent review độc lập, chỉ đọc. Báo cáo review được gửi lại cho agent đã viết để sửa trên nhánh của nó. Review tìm ra lỗi thật như treo khi stderr có byte không phải UTF-8, alias bomb làm hết bộ nhớ, build lỗi nửa chừng để lại index cũ vĩnh viễn.
**Góc người ngoài:** cách làm phổ biến là Tự đọc diff, hoặc nhờ AI review chung chung trên PR. Người viết và người review thường là một phiên; ở đây khác ở Tách người viết khỏi người review, rồi dùng SendMessage để agent viết tự sửa theo báo cáo có mức High/Medium. Những lỗi này test thường không bắt được. Người đọc muốn có bước kiểm chất lượng này mà không tốn công của mình.
