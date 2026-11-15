---
id: 2026-11-03-audit-205-205-test-qua-nhung-d5ef
code: M-EJA5
aliases: [M-EJA5]
date: 2026-11-03
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L146", "claude:ab9a1dd8#L157", "claude:ab9a1dd8#L167", "claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1226"]
hook: "205/205 test qua, nhưng người mới cài xong chẳng có gì dùng được"
tension: tuong_ma_hoa_ra
sides: ["Test xanh 205/205 trên clone sạch", "Quick start lỗi, init không tạo hook nào trong HOME trống"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Công cụ momentry đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang muốn đóng gói nó để người mới cài là dùng được. Bộ test báo 205/205 qua trên bản clone sạch, dễ tưởng là gần xong. Nhưng khi chạy quick start trong HOME trống, init --yes báo lỗi và không tạo gì dùng được, nên test xanh không đảm bảo người khác cài được. Ai đóng gói CLI cho người khác nên quan tâm, vì test xanh và cài được là hai việc khác nhau."
audience: dev đóng gói CLI hoặc công cụ cho agent để người khác cài
spine_context: "Một công cụ CLI đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, đang chuẩn bị đóng gói cho người khác cài."
spine_context_lines: [profile]
spine_want: "Muốn người mới cài xong là dùng được ngay, theo ưu tiên trải nghiệm người dùng."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Lệnh init --yes báo lỗi, và init không tạo hook hay gì dùng được trong HOME trống."
spine_obstacle_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_turn: Tưởng test xanh là đủ để người dùng cài được; hoá ra quick start từ HOME trống vẫn hỏng.
spine_turn_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232"]
spine_action: "Chạy quick start trong HOME tạm để không đụng cấu hình thật, rồi đối chiếu với kết quả test."
spine_action_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1225"]
spine_outcome: "Bộ test 205/205 qua trên clone sạch, nhưng init --yes thoát 1, list và check cũng thoát 1 vì chưa có hộp."
spine_outcome_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L1226"]
spine_takeaway: Test xanh trên clone sạch không chứng minh người dùng cài được; chạy quick start từ HOME trống mới lộ khoảng trống.
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 7
---

# Audit: 205/205 test qua nhưng người mới không cài được gì

**Góc kể:** Công cụ momentry đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang muốn đóng gói nó để người mới cài là dùng được. Bộ test báo 205/205 qua trên bản clone sạch, dễ tưởng là gần xong. Nhưng khi chạy quick start trong HOME trống, init --yes báo lỗi và không tạo gì dùng được, nên test xanh không đảm bảo người khác cài được. Ai đóng gói CLI cho người khác nên quan tâm, vì test xanh và cài được là hai việc khác nhau.
**Bối cảnh:** Audit đóng gói một CLI Node không phụ thuộc gói ngoài, chạy quick start trong HOME tạm để không đụng cấu hình thật.
**Chuyện gì xảy ra:** Bộ test báo 205/205 qua trên clone sạch, nhưng trong workspace chỉ còn 202/203 vì test quét cả thư mục chưa đưa vào git. Quick start cho thấy init --yes lỗi 'Unknown option', list và check thoát 1 vì chưa có hộp, và init không tạo hook hay lệnh bip nào trong HOME trống. Kết luận: phần lõi ổn, phần phân phối gần như bằng 0.
**Bài học:** Test xanh trên clone sạch không chứng minh người dùng cài được; chỉ chạy quick start từ HOME trống mới lộ khoảng trống.
**Artefact:** Bảng kết quả verify theo tầng ưu tiên, đạt và thiếu. Che đường dẫn HOME và tên người dùng.
