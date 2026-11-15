---
id: 2026-11-03-skill-kiem-dong-goi-bao-dong
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L229", "claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
hook: "Audit đóng gói: init --yes lỗi, list và check thoát 1 ngay sau quick start"
tension: tuong_ma_hoa_ra
sides: ["README có quick start tưởng chạy được", "init chỉ tạo config, lệnh kế tiếp thoát 1"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Skill kiểm đóng gói báo động: chưa có cài một lệnh, chưa có doctor, init --yes lỗi

**Bối cảnh:** Dự án CLI momentry đã có lõi chạy được và 205 test xanh, nhưng chưa có đường phân phối nào. Audit chạy các bước kiểm của skill trong HOME tạm.
**Chuyện gì xảy ra:** Audit trả về 4 lỗi tầng trải nghiệm người dùng. README thiếu bước lấy code. Không có --version, release, install.sh, update hay uninstall. Lệnh init --yes báo Unknown option. init chỉ tạo file cấu hình, nên list và check thoát 1 ngay sau quick start.
**Bài học:** Đo lại đường đi từ con số 0 tới kết quả đầu tiên trước khi nói dự án đã sẵn sàng; test lõi xanh không có nghĩa người mới cài được.
**Artefact:** Bảng 4 lỗi tầng 1 của audit, kèm đoạn output init --yes báo lỗi. Che đường dẫn HOME và tên người.
