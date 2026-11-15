---
id: 2026-11-05-viec-frontend-bi-dinh-tuyen-vao
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1520", "claude:6a207191#L1534", "claude:6a207191#L1540", "claude:6a207191#L1555", "claude:6a207191#L1561", "claude:6a207191#L1585", "claude:6a207191#L1592"]
hook: "Hub chọn nhầm skill đóng gói cho việc frontend, skill đúng không được nạp"
tension: cam_ma_van_lot
sides: ["Có not_for để chặn skill chọn nhầm", "Vẫn chọn nhầm, còn skill frontend có sẵn thì không được nạp"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Việc frontend bị định tuyến vào skill đóng gói; skill có sẵn trong dự án không được nạp

**Bối cảnh:** Người dùng yêu cầu dùng skill ak-frontend-development để làm UI của skillstation. Agent gọi skill_resolve với mô tả việc frontend thuần.
**Chuyện gì xảy ra:** Lần đầu hub trả về cs-packaging-distribution với độ tin cậy medium, tức là chọn nhầm. Agent từ chối và hỏi lại, lần hai không có skill nào khớp. Mục not_for hiện có không đủ để chặn skill này. Skill ak-frontend-development nằm trong .claude/skills của dự án nhưng không được nạp vào phiên, nên agent đọc thẳng SKILL.md và làm theo.
**Bài học:** not_for chỉ làm giảm điểm chứ chưa chặn. Skill có nhiều chữ install hay deploy dễ bị kéo nhầm. Thử skill_resolve với một câu thuộc việc khác là cách kiểm tra routing rẻ nhất.
**Artefact:** Hai đoạn kết quả skill_resolve (medium rồi no_skill), che ID.
