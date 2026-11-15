---
id: 2026-10-09-migration-phai-fail-closed-filepath-walkdir-4257
code: M-G2ST
aliases: [M-G2ST]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3978", "omp:cd4449ab#L3980", "omp:cd4449ab#L3984", "omp:cd4449ab#L3987", "omp:cd4449ab#L3989", "omp:cd4449ab#L3996", "omp:cd4449ab#L3998", "omp:cd4449ab#L3999"]
hook: "Một dấu gạch dưới nuốt lỗi của cả bước migration"
tension: nho_ma_to
sides: ["một ký tự `_ =` nhỏ xíu", "lỗi bị nuốt, migration chạy tiếp trên dữ liệu hỏng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án công cụ quản lý skill cho MCP đang dọn lại mô hình dữ liệu, và người làm ở Phase 3 phải làm bước migration fail closed: gặp file hỏng thì dừng và báo đúng tên file. Trong bước chuyển sang v4, người làm tưởng việc bỏ qua lỗi khi duyệt thư mục insight là vô hại, nhưng một file hỏng sẽ bị nuốt im lặng và migration vẫn chạy tiếp trên dữ liệu sai. Chỉ một dấu '_ =' đủ để chuyện đó xảy ra, nên người viết migration nên grep nó trước khi báo xong."
audience: dev viết migration hoặc đổi định dạng dữ liệu
spine_context: "Một dự án công cụ quản lý skill cho MCP (mcp-skill-hub), người làm đang ở Phase 3 của đợt dọn mô hình distill."
spine_context_lines: ["omp:cd4449ab#L2374"]
spine_want: "Migration phải fail closed: gặp lỗi đọc file thì dừng và báo đúng tên file, không chạy tiếp."
spine_want_lines: ["omp:cd4449ab#L3656"]
spine_obstacle: Bước migration v4 bỏ qua lỗi khi duyệt thư mục insight bằng một dấu '_ ='.
spine_obstacle_lines: ["omp:cd4449ab#L3656"]
spine_turn: Tưởng bỏ qua lỗi duyệt thư mục là chuyện nhỏ; hoá ra một file insight hỏng sẽ bị nuốt im lặng và migration vẫn đi tiếp trên dữ liệu hỏng.
spine_turn_lines: ["omp:cd4449ab#L3656"]
spine_action: "Viết lại bước v4 để trả lỗi kèm tên file, thêm test rằng file hỏng làm preview thất bại và workspace không đổi; test đầu đỏ, sửa import rồi gói pass."
spine_action_lines: ["omp:cd4449ab#L3978", "omp:cd4449ab#L3984", "omp:cd4449ab#L3993"]
spine_outcome: Gói migration chạy test pass sau khi sửa; đoạn này chưa có kết quả make check.
spine_outcome_lines: ["omp:cd4449ab#L4001"]
spine_takeaway: "Grep '_ =' trong code migration trước khi báo xong: một dấu gạch dưới có thể làm hỏng dữ liệu im lặng."
spine_takeaway_lines: ["omp:cd4449ab#L3960"]
completeness: 7
---

# Migration phải fail-closed: _ = filepath.WalkDir nuốt lỗi

**Góc kể:** Một dự án công cụ quản lý skill cho MCP đang dọn lại mô hình dữ liệu, và người làm ở Phase 3 phải làm bước migration fail closed: gặp file hỏng thì dừng và báo đúng tên file. Trong bước chuyển sang v4, người làm tưởng việc bỏ qua lỗi khi duyệt thư mục insight là vô hại, nhưng một file hỏng sẽ bị nuốt im lặng và migration vẫn chạy tiếp trên dữ liệu sai. Chỉ một dấu '_ =' đủ để chuyện đó xảy ra, nên người viết migration nên grep nó trước khi báo xong.
**Bối cảnh:** Lead nhận ra bước v4 bỏ qua lỗi khi duyệt thư mục insight; một file insight hỏng sẽ không báo gì.
**Chuyện gì xảy ra:** grep '_ =' trúng v4.go dòng 439: lỗi của WalkDir bị bỏ qua. Agent viết lại v4 để trả lỗi kèm tên file, và thêm test: một file insight hỏng làm preview thất bại với đúng tên file, workspace không đổi. Lần chạy test đầu đỏ, sửa tiếp.
**Bài học:** Một dấu '_ =' trong code migration đủ để hỏng dữ liệu im lặng; grep nó trước khi báo xong.
**Artefact:** Dòng code trước và sau, ngắn.
