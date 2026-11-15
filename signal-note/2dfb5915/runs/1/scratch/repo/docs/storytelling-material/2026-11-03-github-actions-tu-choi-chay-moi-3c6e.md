---
id: 2026-11-03-github-actions-tu-choi-chay-moi-3c6e
code: M-CD1Z
aliases: [M-CD1Z]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3785", "claude:2dfb5915#L3794", "claude:2dfb5915#L3804"]
hook: "Lỗi thanh toán chặn mọi job CI, agent Linux không dựng nổi Windows và macOS"
tension: gap_ma_phai_chon
sides: ["Cần dựng rc.3 cho cả Windows và macOS", "GitHub Actions từ chối chạy vì thanh toán lỗi, đổi repo sang public mới chạy lại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# GitHub Actions từ chối chạy mọi job vì thanh toán lỗi: không dựng được rc.3 cho tới khi người dùng sửa

**Bối cảnh:** Repo private nên Actions tính phí theo phút. Tới lúc tag rc.3, mọi job đều bị từ chối trước khi chạy.
**Chuyện gì xảy ra:** Thông báo: job không khởi động vì thanh toán gần đây thất bại hoặc hết hạn mức. Agent không cross-compile được binary Windows và macOS trên máy Linux, nên không thay thế được. Người dùng đổi repo sang public, CI chạy lại xanh trên nhánh phase 17 và rc.3 được phát hành.
**Bài học:** Đừng dựa vào CI tính phí cho bước phát hành; kiểm hạn mức trước khi cần tag.
**Artefact:** Dòng thông báo lỗi của GitHub (không kèm thông tin tài khoản).
**Góc người ngoài:** cách làm phổ biến là Nhiều người sẽ sửa code hoặc chạy lại toàn bộ pipeline, mất thời gian và có thể tạo thêm commit không cần thiết; ở đây khác ở Lỗi hạ tầng được tách khỏi lỗi code bằng thông báo của GitHub, nên người dùng biết chính xác việc cần làm (kiểm tra billing) mà không phải tự điều tra.
