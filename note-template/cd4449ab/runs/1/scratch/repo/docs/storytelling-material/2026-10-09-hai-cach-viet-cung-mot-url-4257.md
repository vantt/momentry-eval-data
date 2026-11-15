---
id: 2026-10-09-hai-cach-viet-cung-mot-url-4257
code: M-NGJS
aliases: [M-NGJS]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1792", "omp:cd4449ab#L1794", "omp:cd4449ab#L1801", "omp:cd4449ab#L1803", "omp:cd4449ab#L1818", "omp:cd4449ab#L1827"]
hook: "Hai URL giống hệt trong Python, Go vẫn báo khác nhau"
tension: tuong_ma_hoa_ra
sides: ["Python chuẩn hoá cả hai ra cùng một chuỗi", "Go vẫn báo matches=false vì sai thứ tự trim"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một hub kỹ năng viết bằng Go, và người làm đang sửa bước migration để chạy được trên hub thật. Hai URL repo của cùng một kỹ năng, một có đuôi .git và một không, được chuẩn hoá bằng Python và cho ra cùng một chuỗi nên tưởng là xong. Nhưng code Go vẫn báo không khớp vì thứ tự trim khác nhau, và ai chuẩn hoá dữ liệu bằng ngôn ngữ khác rồi tin kết quả đó đều có thể gặp đúng lỗi này."
audience: dev viết công cụ migrate dữ liệu bằng Go
spine_context: "Một hub kỹ năng viết bằng Go, người làm đang sửa bước migration để chạy trên hub thật theo yêu cầu của lead."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1462"]
spine_want: "Gộp hai URL repo (một có đuôi .git, một không) thành một nguồn khi migrate metadata."
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Code Go vẫn báo matches=false cho hai URL đã được chuẩn hoá.
spine_obstacle_lines: ["omp:cd4449ab#L1818"]
spine_turn: "Tưởng: chuẩn hoá bằng Python cho ra cùng một chuỗi thì Go cũng khớp. Hoá ra: Go vẫn lệch vì thứ tự trim khác nhau."
spine_turn_lines: ["omp:cd4449ab#L1803", "omp:cd4449ab#L1818"]
spine_action: "Sửa thứ tự trim khoảng trắng và đuôi .git trong hàm chuẩn hoá Go, rồi chạy lại test."
spine_action_lines: ["omp:cd4449ab#L1824", "omp:cd4449ab#L1827"]
spine_outcome: Test migration v1→v2→v3 trên fixture pass.
spine_outcome_lines: ["omp:cd4449ab#L1827"]
spine_takeaway: Chuẩn hoá dữ liệu phải dùng đúng code của repo; kết quả thử bằng ngôn ngữ khác có thể không khớp.
spine_takeaway_lines: ["omp:cd4449ab#L1803", "omp:cd4449ab#L1818"]
completeness: 7
---

# Hai cách viết cùng một URL repo thành một nguồn

**Góc kể:** Dự án là một hub kỹ năng viết bằng Go, và người làm đang sửa bước migration để chạy được trên hub thật. Hai URL repo của cùng một kỹ năng, một có đuôi .git và một không, được chuẩn hoá bằng Python và cho ra cùng một chuỗi nên tưởng là xong. Nhưng code Go vẫn báo không khớp vì thứ tự trim khác nhau, và ai chuẩn hoá dữ liệu bằng ngôn ngữ khác rồi tin kết quả đó đều có thể gặp đúng lỗi này.
**Bối cảnh:** Metadata Phase 0 viết URL có đuôi .git, provenance ghi URL không có đuôi; cần gộp thành một nguồn.
**Chuyện gì xảy ra:** Ban đầu hai URL cho hai nguồn. Agent thử chuẩn hoá bằng Python và cả hai ra cùng chuỗi, nhưng debug trong Go vẫn báo matches=false (L1818). Sửa thứ tự trim khoảng trắng và đuôi .git rồi merge. Kết quả là một nguồn duy nhất có roles [upstream, learning] (L1827).
**Bài học:** Chuẩn hoá dữ liệu bằng code thật trong repo, đừng tin kết quả thử ở ngôn ngữ khác.
**Artefact:** Bảng hai URL đầu vào và kết quả chuẩn hoá; che tên người.
