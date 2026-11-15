---
id: 2026-10-30-loi-nho-sua-xong-da-quen
date: 2026-10-30
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L254", "claude:f0bf048d#L480", "claude:f0bf048d#L521", "claude:f0bf048d#L586", "claude:f0bf048d#L1601", "claude:f0bf048d#L1987", "claude:f0bf048d#L2314", "claude:f0bf048d#L2674", "claude:f0bf048d#L2778", "claude:f0bf048d#L3370", "claude:f0bf048d#L3382", "claude:f0bf048d#L3410"]
hook: "Hàng loạt lệnh báo lỗi, đều sửa xong trong cùng lượt"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi nhỏ, sửa xong đã quên: kiểm chéo sau lệnh sudo

**Bối cảnh:** Các lệnh kiểm tra và tìm kiếm trong phiên thường thất bại vì glob, tên file hoặc đường dẫn không đúng, sau đó được sửa ngay.
**Chuyện gì xảy ra:** Hàng loạt lệnh báo exit 1 hoặc 127 do glob zsh không khớp, gcloud chưa cài, dirname thiếu tham số, hoặc file đã đổi tên. Mỗi lần đều được sửa bằng lệnh khác trong cùng lượt và không ảnh hưởng tiến độ.
**Bài học:** Với zsh, glob không khớp sẽ báo lỗi ngay; dùng find hoặc bọc quote để tránh.
