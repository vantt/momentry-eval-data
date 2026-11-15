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
hook: "Hai URL chỉ khác đuôi .git nên không gộp được"
tension: nho_ma_to
sides: ["Hai URL trỏ cùng một repo", "Đuôi .git khiến hàm so khớp trả về false"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một hub quản lý skill đang được chuyển sang schema mới, và người làm viết bước migration để đưa dữ liệu cũ lên. Họ tưởng so sánh chuỗi URL là đủ để nhận ra hai nguồn cùng một repo, nhưng hai URL chỉ khác đuôi .git vẫn bị coi là khác nhau. Ai viết so khớp định danh giữa các nguồn dữ liệu cũng có thể dính đúng lỗi này."
audience: dev viết migration hoặc so khớp định danh giữa các nguồn dữ liệu
spine_context: "Một hub quản lý skill, người làm đang viết bước migration đưa dữ liệu cũ lên schema v3."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Muốn migration chạy đúng trên bản sao của hub thật, không mất dữ liệu."
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Hai nguồn cùng một repo nhưng chỉ khác đuôi .git nên so chuỗi thô cho kết quả không khớp.
spine_obstacle_lines: ["omp:cd4449ab#L1818"]
spine_turn: "Tưởng so sánh chuỗi URL là đủ để nhận ra cùng một repo; hoá ra https://github.com/openclaw/openclaw.git và https://github.com/openclaw/openclaw là một nguồn."
spine_turn_lines: ["omp:cd4449ab#L1812", "omp:cd4449ab#L1818"]
spine_action: Viết thêm hàm normalizeRepoURL và dùng nó khi so khớp nguồn.
spine_action_lines: ["omp:cd4449ab#L1845", "omp:cd4449ab#L1846", "omp:cd4449ab#L1848"]
spine_outcome: "Sau chuẩn hoá, cả hai URL cho ra cùng một chuỗi."
spine_outcome_lines: ["omp:cd4449ab#L1803"]
spine_takeaway: Khoá định danh như URL cần hàm chuẩn hoá riêng và test cho biến thể .git; đừng so chuỗi thô.
spine_takeaway_lines: ["omp:cd4449ab#L1812", "omp:cd4449ab#L1818"]
completeness: 7
---

# Một hậu tố .git làm hỏng việc gộp nguồn; key repo và repository lệch nhau

**Góc kể:** Một hub quản lý skill đang được chuyển sang schema mới, và người làm viết bước migration để đưa dữ liệu cũ lên. Họ tưởng so sánh chuỗi URL là đủ để nhận ra hai nguồn cùng một repo, nhưng hai URL chỉ khác đuôi .git vẫn bị coi là khác nhau. Ai viết so khớp định danh giữa các nguồn dữ liệu cũng có thể dính đúng lỗi này.
**Bối cảnh:** File Phase 0 dùng key repo trong sources, còn schema v3 chỉ nhận repository. Cùng một repo lại xuất hiện lúc có .git, lúc không.
**Chuyện gì xảy ra:** Test migration báo 'invalid source entry: unknown field repo'. Sau khi sửa key, việc gộp nguồn vẫn không khớp: debug in ra matches=false cho hai URL chỉ khác đuôi .git. Hàm chuẩn hoá bỏ .git và dấu / cuối rồi đưa host về chữ thường, sau đó hai URL cho cùng kết quả và nguồn được gộp thành một với hai role.
**Bài học:** Khoá so sánh định danh như URL phải có hàm chuẩn hoá riêng và có test cho biến thể .git, đừng so chuỗi thô.
**Artefact:** Bảng ba dòng: URL gốc, URL đã chuẩn hoá, kết quả so khớp.
