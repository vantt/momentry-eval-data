---
id: 2026-10-31-tra-loi-sai-ve-quyen-read
date: 2026-10-31
repo: repo
status: raw
signals: ["3"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2354", "claude:f0bf048d#L2367"]
hook: "Phương án read-only đã chốt, nhưng GitHub không cấp read-only cho repo cá nhân"
tension: tuong_ma_hoa_ra
sides: ["Tưởng collaborator có thể chỉ được đọc", "Repo private cá nhân không có quyền chỉ đọc"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trả lời sai về quyền read-only của GitHub, và sửa

**Bối cảnh:** Đang chọn cách để bot GitHub chỉ đọc repo private của tài khoản cá nhân.
**Chuyện gì xảy ra:** Phương án ban đầu dựa vào quyền read-only cho collaborator. Đọc tài liệu GitHub thì thấy repo private của tài khoản cá nhân không cấp được quyền chỉ đọc. Nhận lỗi, đưa hai phương án thay thế kèm rủi ro, người dùng chọn hoãn.
**Bài học:** Đọc tài liệu nền tảng trước khi đề xuất cơ chế phân quyền; giả định về quyền thường sai ở chi tiết gói dịch vụ.
