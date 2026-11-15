---
id: 2026-10-21-chuoi-du-phong-la-danh-sach
date: 2026-10-21
repo: repo
status: raw
signals: ["gốc nhỏ, lỗi to", nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2630", "claude:9514b261#L2729"]
hook: "Chuỗi dự phòng có sáu family, nhưng hai cái không bao giờ được chọn"
tension: cam_ma_van_lot
sides: ["Đã cấu hình deepseek và glm sẵn sàng làm dự phòng", "Danh sách trắng chỉ có bốn family nên hai cái này không bao giờ được chọn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi dự phòng là danh sách trắng: deepseek và glm không bao giờ được chọn

**Bối cảnh:** Khi xai hỏng, hội đồng cần family dự phòng. Hai family chạy được vẫn không xuất hiện trong walk.
**Chuyện gì xảy ra:** Chuỗi dự phòng của tier flagship và frontier chỉ liệt kê bốn family. Walk chỉ được thu hẹp theo danh sách này, không mở rộng. Sau khi thêm deepseek và z-ai vào chuỗi, mô phỏng cho 11/11 ghế kể cả khi bỏ xai.
**Bài học:** Danh sách dự phòng là whitelist. Thêm executor vào hệ thì phải thêm cả vào chuỗi dự phòng, không chỉ vào cấu hình.
**Artefact:** Sơ đồ chuỗi dự phòng trước và sau, dạng danh sách tên family.
