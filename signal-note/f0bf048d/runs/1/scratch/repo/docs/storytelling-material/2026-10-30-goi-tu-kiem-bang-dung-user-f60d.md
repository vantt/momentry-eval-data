---
id: 2026-10-30-goi-tu-kiem-bang-dung-user-f60d
code: M-AGT2
aliases: [M-AGT2]
date: 2026-10-30
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L968", "claude:f0bf048d#L975", "claude:f0bf048d#L1016", "claude:f0bf048d#L1017", "claude:f0bf048d#L1022"]
hook: "Lỗi agent không đọc được key giờ bị bắt ngay lúc cài"
tension: tuong_ma_hoa_ra
sides: ["ghi tay thấy file key là yên tâm", "kiểm bằng đúng user chạy agent mới bắt được lỗi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tự kiểm bằng đúng user chạy agent, thay vì ghi tay

**Bối cảnh:** Chủ nói việc của agent là đóng gói để deploy lại có đủ agent và công cụ, không phải làm thay.
**Chuyện gì xảy ra:** Manifest khai báo user chạy daemon và các file bí mật. MCP tham chiếu file bằng biến thay vì đường dẫn cứng. Lệnh tools chép file, cài MCP, rồi khởi động từng server dưới đúng user daemon để kiểm. Giá trị theo máy nằm trong file env quyền 600 và không commit. Lỗi 'agent không đọc được key' giờ bị bắt ngay khi cài, không lọt tới lúc agent chạy.
**Bài học:** Mỗi bước đóng gói nên có một bước kiểm chạy đúng môi trường thật của agent. Nếu chỉ kiểm dưới user của người phát triển thì sẽ bỏ sót lỗi quyền.
**Artefact:** Mẫu manifest (cấu trúc, không có giá trị).
