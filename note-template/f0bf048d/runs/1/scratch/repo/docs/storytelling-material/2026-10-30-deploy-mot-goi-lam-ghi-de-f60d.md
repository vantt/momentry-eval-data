---
id: 2026-10-30-deploy-mot-goi-lam-ghi-de-f60d
code: M-YKTF
aliases: [M-YKTF]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915"]
hook: "Deploy gói Marketing, ba agent kỹ thuật của phiên khác lùi về bản cũ"
tension: giup_ma_hai
sides: ["Deploy một gói chỉ để làm phần Marketing", "Ghi đè cả team của phiên khác về bản cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Deploy một gói làm ghi đè cả team của phiên khác

**Bối cảnh:** Hai gói cùng deploy vào một workspace. Gói Marketing còn mang theo một bản Coding cũ.
**Chuyện gì xảy ra:** Lần deploy đầu tiên làm đưa instructions, model và skill của ba agent kỹ thuật về bản cũ, và gỡ ba agent này khỏi squad. Nguyên nhân là đã bỏ qua các dòng thay đổi ngoài phần Marketing khi đọc plan. Khôi phục bằng cách deploy lại gói của phiên kia (plan về 0 thay đổi), sau đó xoá phần Coding khỏi gói Marketing. Deploy không xoá thực thể trên server nên các agent đang chạy không bị ảnh hưởng.
**Bài học:** Đọc toàn bộ diff của plan trước khi deploy, không chỉ phần mình quan tâm. Mỗi gói chỉ giữ những gì nó sở hữu.
**Artefact:** Đoạn output plan có dòng thay đổi ngoài phạm vi, che tên workspace nếu cần.
**Góc người ngoài:** cách làm phổ biến là Thường người ta deploy trực tiếp, dùng cấu hình rải rác, hoặc deploy mặc định vào workspace dùng chung; ở đây khác ở Plan báo rõ thay đổi trước khi chạy, deploy không xóa, và mỗi khách có một manifest riêng. Người đọc sẽ muốn biết cơ chế này vì sự cố deploy ghi đè team khác đã xảy ra và được khắc phục bằng cách này.
