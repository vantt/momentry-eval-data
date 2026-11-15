---
id: 2026-11-01-loi-pi-update-va-vi-sao
date: 2026-11-01
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L3031", "claude:f0bf048d#L3053"]
hook: "Ghim phiên bản mỗi runtime vào thư mục riêng, quay lại chỉ mất vài giây"
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

# Lỗi 'pi update' và vì sao phải ghim phiên bản

**Bối cảnh:** Runtime pi và omp cần nâng cấp; System Operator không được tự gọi 'pi update' hay 'omp update' vì lệnh này nâng cấp ngoài bản ghim.
**Chuyện gì xảy ra:** Thiết kế: mỗi phiên bản nằm trong thư mục riêng, bản cũ được giữ, quay lại chỉ mất vài giây. Nâng omp thử từ 18.12.6 lên 18.14.2 rồi quay lại, đều chạy đúng. Chuyển ba runtime sang cách cài mới không cần sudo sau khi tools-owner.sh cấp quyền. Ba lệnh bọc giờ trỏ vào thư mục theo phiên bản.
**Bài học:** Khi tự cập nhật ngoài kiểm soát, công cụ có thể phá bản ghim; chỉ cho phép cập nhật qua script ghim phiên bản và giữ bản cũ để quay lại.
**Artefact:** Kết quả 'status': bản ghim, bản đã cài, bản mới nhất; che đường dẫn home.
**Góc người ngoài:** cách làm phổ biến là Chạy lệnh cập nhật của chính công cụ hoặc ghi đè bản cũ, và muốn lùi về phải cài lại từ đầu; ở đây khác ở Cài song song theo phiên bản cho phép nâng cấp mà không gián đoạn lượt chạy đang dở và có đường lùi rõ ràng. Người đọc sẽ muốn áp dụng cho các công cụ họ tự cài.
