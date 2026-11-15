---
id: 2026-11-05-may-quet-bao-mat-bao-11-c4b4
code: M-HTBC
aliases: [M-HTBC]
date: 2026-11-05
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1324", "claude:6a207191#L1331", "claude:6a207191#L1336"]
hook: "11 cảnh báo critical, nhưng tất cả chỉ là chữ trong tài liệu"
tension: tuong_ma_hoa_ra
sides: ["Máy quét báo 11 lỗi nghiêm trọng", "Đọc lại thì chỉ là văn bản, không chạy gì"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy quét bảo mật báo 11 critical, toàn chữ trong tài liệu; chủ dự án chọn gửi

**Bối cảnh:** Trước khi gửi, máy quét bảo mật của skillstation báo 7 critical, 1 high và 3 medium.
**Chuyện gì xảy ra:** Các critical là rule pipe-to-shell khớp với mẫu curl kèm sh trong tài liệu và installer mẫu. High là persist.autostart khớp chữ hook. Agent đọc lại hai script kiểm tra và xác nhận chúng không tự tải hay chạy gì. Chủ dự án chọn gửi và ghi chú cho người duyệt trên hub rằng các cảnh báo chỉ là văn bản.
**Bài học:** Máy quét sẽ luôn báo đỏ với tài liệu hướng dẫn cài đặt. Nên ghi sẵn lý do cho người duyệt, đừng viết lại tài liệu chỉ để qua máy quét.
**Artefact:** Bảng 3 nhóm rule và vị trí trong file. Cần che đường dẫn thư mục.
