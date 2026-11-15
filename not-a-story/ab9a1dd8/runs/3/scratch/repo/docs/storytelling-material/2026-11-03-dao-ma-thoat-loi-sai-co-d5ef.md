---
id: 2026-11-03-dao-ma-thoat-loi-sai-co-d5ef
code: M-84HM
aliases: [M-84HM]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L1253", "claude:ab9a1dd8#L1797"]
hook: "Đổi mã thoát 1 thành 2 theo chuẩn, pre-commit có thể đọc nhầm"
tension: chon_mot_mat_mot
sides: ["Theo chuẩn: lỗi sai cờ là mã 2", "Script pre-commit dùng 'momentry check' có thể đọc nhầm, sai im lặng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đảo mã thoát: lỗi sai cờ đổi từ 1 sang 2 để theo chuẩn, vì script pre-commit có thể đọc nhầm

**Bối cảnh:** Bảng cũ: 1 là gõ sai lệnh, 2 là check thấy vi phạm riêng tư. Skill chuẩn: 0 xong, 1 có lỗi, 2 sai cú pháp. README và PRD đã công bố bảng cũ.
**Chuyện gì xảy ra:** Agent đề xuất giữ bảng cũ vì có thể ai đó dùng 'momentry check' làm pre-commit hook. Đổi mã ở chỗ kiểm riêng tư sẽ sai im lặng. Chủ dự án chọn theo chuẩn. Đổi đồng bộ code, test, bảng lệnh và CHANGELOG mục Breaking. Test check thấy vi phạm đổi từ 2 sang 1.
**Bài học:** Đổi mã thoát là đổi hợp đồng công khai. Phải ghi vào CHANGELOG và đổi đồng bộ với test, vì script ngoài không báo lỗi khi đọc sai mã.
**Artefact:** Bảng mã thoát trước và sau trong CHANGELOG. Không có dữ liệu nhạy cảm.
