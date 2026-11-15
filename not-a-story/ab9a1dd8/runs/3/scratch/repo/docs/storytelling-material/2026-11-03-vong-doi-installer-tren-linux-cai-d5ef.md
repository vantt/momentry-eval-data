---
id: 2026-11-03-vong-doi-installer-tren-linux-cai-d5ef
code: M-5QXR
aliases: [M-5QXR]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1409", "claude:ab9a1dd8#L1423", "claude:ab9a1dd8#L2125", "claude:ab9a1dd8#L2147"]
hook: "Cài, cài lại, update, uninstall trên Linux: một lần kiểm sai vì gói cũ"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng đời installer trên Linux: cài, cài lại không đổi gì, update báo mã 10, uninstall giữ dữ liệu

**Bối cảnh:** Test vòng đời installer chạy trong HOME tạm, sau mỗi lần sửa installer và đóng gói.
**Chuyện gì xảy ra:** Chuỗi kiểm: cài v0.1.0, cài lại không đổi gì, init và doctor ok, update --check báo mã thoát 10 khi có bản mới, cập nhật giữ cấu hình và hộp chuyện, uninstall gỡ đúng phần của momentry và giữ dữ liệu. Có một lần kết quả sai vì chạy bằng gói đóng gói trước khi sửa, phải đóng gói lại.
**Bài học:** Vòng đời installer cần chạy từ đầu đến cuối trong HOME trống sau mỗi lần sửa, và đóng gói lại trước mỗi lần kiểm tra.
**Artefact:** Đầu ra terminal của chuỗi lệnh. Che đường dẫn HOME.
