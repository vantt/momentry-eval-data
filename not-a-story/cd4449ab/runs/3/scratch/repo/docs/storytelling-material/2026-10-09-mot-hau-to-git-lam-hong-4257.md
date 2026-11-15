---
id: 2026-10-09-mot-hau-to-git-lam-hong-4257
code: M-2D0H
aliases: [M-2D0H]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1627", "omp:cd4449ab#L1794", "omp:cd4449ab#L1803", "omp:cd4449ab#L1815", "omp:cd4449ab#L1845"]
hook: "Hai URL chỉ khác đuôi .git nên không gộp được nguồn"
tension: nho_ma_to
sides: ["Hai URL chỉ khác đuôi .git và dấu / cuối", "Máy coi là hai nguồn khác nhau, việc gộp hỏng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang đơn giản hoá schema của mcp-skill-hub và chuyển một hub thật từ v1 sang v3. Họ tưởng so sánh chuỗi URL là đủ để gộp hai nguồn cùng repo, nhưng một bên có đuôi .git nên không khớp và hai nguồn không gộp được. Dev làm công cụ đồng bộ hay di chuyển dữ liệu nào cũng có thể dính đúng kiểu lỗi này."
audience: dev làm công cụ đồng bộ hoặc di chuyển dữ liệu
spine_context: Người làm đang đơn giản hoá schema của mcp-skill-hub và chuyển một hub thật từ v1 sang v3.
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Gộp provenance.origin với các nguồn Phase 0 theo URL repo đã chuẩn hoá, để openclaw thành một nguồn với hai role."
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: "Migration trên hub thật lỗi, và so khớp chuỗi thô không nhận ra hai URL cùng repo khi một bên có đuôi .git."
spine_obstacle_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1818"]
spine_turn: Tưởng so sánh chuỗi URL là đủ để gộp nguồn; hoá ra đuôi .git làm hai URL cùng repo bị coi là khác.
spine_turn_lines: ["omp:cd4449ab#L1812", "omp:cd4449ab#L1818"]
spine_action: "Thêm hàm normalizeRepoURL bỏ .git và dấu / cuối, đưa host về chữ thường, rồi dùng để so khớp khi gộp."
spine_action_lines: ["omp:cd4449ab#L1846", "omp:cd4449ab#L1848"]
spine_outcome: Hai URL chuẩn hoá ra cùng một giá trị khi kiểm bằng script; chưa thấy kết quả test Go sau khi sửa.
spine_outcome_lines: ["omp:cd4449ab#L1803"]
spine_takeaway: "So khớp định danh như URL cần hàm chuẩn hoá riêng và test cho biến thể .git, đừng so chuỗi thô."
spine_takeaway_lines: ["omp:cd4449ab#L1818"]
completeness: 7
---

# Một hậu tố .git làm hỏng việc gộp nguồn; key repo và repository lệch nhau

**Góc kể:** Người làm đang đơn giản hoá schema của mcp-skill-hub và chuyển một hub thật từ v1 sang v3. Họ tưởng so sánh chuỗi URL là đủ để gộp hai nguồn cùng repo, nhưng một bên có đuôi .git nên không khớp và hai nguồn không gộp được. Dev làm công cụ đồng bộ hay di chuyển dữ liệu nào cũng có thể dính đúng kiểu lỗi này.
**Bối cảnh:** File Phase 0 dùng key repo trong sources, còn schema v3 chỉ nhận repository. Cùng một repo lại xuất hiện lúc có .git, lúc không.
**Chuyện gì xảy ra:** Test migration báo 'invalid source entry: unknown field repo'. Sau khi sửa key, việc gộp nguồn vẫn không khớp: debug in ra matches=false cho hai URL chỉ khác đuôi .git. Hàm chuẩn hoá bỏ .git và dấu / cuối rồi đưa host về chữ thường, sau đó hai URL cho cùng kết quả và nguồn được gộp thành một với hai role.
**Bài học:** Khoá so sánh định danh như URL phải có hàm chuẩn hoá riêng và có test cho biến thể .git, đừng so chuỗi thô.
**Artefact:** Bảng ba dòng: URL gốc, URL đã chuẩn hoá, kết quả so khớp.
