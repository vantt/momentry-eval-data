---
id: 2026-10-21-sua-tai-lieu-khi-ke-hoach
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1317", "claude:9514b261#L1789"]
hook: "Thêm một ghi chú vào tài liệu có thể làm lệch cả bản vá"
tension: nho_ma_to
sides: ["Một ghi chú nhỏ trong tài liệu", "Digest bị khoá ở phase 8 nên bản vá có thể lệch"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa tài liệu khi kế hoạch khoá digest: ghi chú thêm có thể làm lệch bản vá

**Bối cảnh:** Agent thêm ghi chú vào đề xuất kiến trúc và bảng kế hoạch trong lúc một nhánh khác của kế hoạch đang khoá digest các file bị vá.
**Chuyện gì xảy ra:** Đề xuất đã khác nhánh bảo trì 5 dòng thêm và 3 dòng xoá. Phase 8 khoá digest nên ghi chú có thể làm lệch bản vá nếu file nằm trong manifest. Agent không biết manifest thật vì chưa đọc được, nên ghi điều kiện đảo lại vào bảng và báo người dùng.
**Bài học:** Trước khi sửa tài liệu đang được khoá digest, kiểm manifest; nếu chưa rõ, ghi điều kiện đảo lại thay vì giả định.
**Artefact:** Không có artefact nhìn được; có thể dùng đoạn trích điều kiện đảo lại trong bảng.
