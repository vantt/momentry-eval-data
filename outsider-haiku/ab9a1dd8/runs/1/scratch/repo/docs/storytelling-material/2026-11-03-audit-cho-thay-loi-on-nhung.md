---
id: 2026-11-03-audit-cho-thay-loi-on-nhung
date: 2026-11-03
repo: repo
status: raw
signals: [số trước/sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L229", "claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
hook: "Audit: 205/205 test qua, nhưng quick start vừa chạy xong là lỗi"
tension: tuong_ma_hoa_ra
sides: ["lõi ổn, 205/205 test qua", "init xong list và check thoát 1, phân phối gần bằng 0"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Audit cho thấy lõi ổn nhưng phân phối gần như bằng 0

**Bối cảnh:** momentry là CLI nhặt chuyện từ phiên coding agent. Trước audit, người mới không có đường nào từ con số 0 tới lần chạy đầu thành công.
**Chuyện gì xảy ra:** Audit theo skill cs-packaging-distribution chạy trên bản clone sạch cho 205/205 test qua. Trong bản làm việc, một test quét cả thư mục chưa commit nên báo 202/203. `init --yes` lỗi Unknown option. `init` chỉ tạo file cấu hình, không tạo hộp chuyện, nên `list` và `check` thoát 1 ngay sau quick start.
**Bài học:** Test chạy trên clone sạch mới cho biết repo thật sự ra sao; test quét file chưa commit sẽ nói dối.
**Artefact:** Bảng Đã đạt và Thiếu trong báo cáo audit.
