---
id: 2026-10-30-deploy-goi-marketing-ghi-de-team-f60d
code: M-QCJ4
aliases: [M-QCJ4]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915"]
hook: "Deploy gói Marketing lặng lẽ đưa 3 agent Coding về bản cũ"
tension: nho_ma_to
sides: ["Chỉ đọc phần Marketing của plan", "Gói chứa bản Coding cũ ghi đè team khác"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Deploy gói Marketing ghi đè team Coding của gói khác trong cùng workspace

**Bối cảnh:** Hai bộ agent (gói) cùng deploy vào một workspace Multica. Gói Marketing được deploy trong lúc gói Coding vẫn nằm ở nhánh chưa commit của một phiên khác.
**Chuyện gì xảy ra:** Lần deploy đầu tiên đưa instructions, model và skill của 3 agent Coding về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow cho một project. Nguyên nhân: gói Marketing vẫn chứa bản Coding cũ, còn khi đọc plan chỉ xem phần Marketing. Khôi phục bằng cách deploy lại đúng gói của phiên kia, plan trả 0 thay đổi. Deploy không xoá thực thể trên server nên agent đang chạy không mất.
**Bài học:** Khi nhiều gói cùng trỏ vào một đích, đọc hết diff của plan chứ không chỉ phần mình quan tâm; mỗi gói chỉ được giữ phần của nó.
**Artefact:** Đầu ra plan trước và sau, các dòng dạng ~ agent ... (che tên workspace và tên người).
**Góc người ngoài:** cách làm phổ biến là Nhiều người deploy thẳng, hoặc chỉ kiểm bằng mắt rồi mong kết quả đúng; ở đây khác ở Có một lệnh xem trước thay đổi và một tiêu chí kiểm sau deploy, nên lỗi ghi đè lộ ra trước khi xảy ra. Người đọc sẽ hỏi vì sao bản đầu tiên vẫn ghi đè được dù đã có plan.
