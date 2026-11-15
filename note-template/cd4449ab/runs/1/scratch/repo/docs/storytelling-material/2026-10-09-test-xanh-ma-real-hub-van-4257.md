---
id: 2026-10-09-test-xanh-ma-real-hub-van-4257
code: M-5ZZF
aliases: [M-5ZZF]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1484", "omp:cd4449ab#L1496", "omp:cd4449ab#L1498", "omp:cd4449ab#L1523", "omp:cd4449ab#L1712"]
hook: "Test xanh hết, nhưng hub thật vẫn báo thiếu ID"
tension: tuong_ma_hoa_ra
sides: ["Test xanh, tưởng đã ổn", "Chạy trên hub thật vẫn lỗi 'missing an ID'"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ quản lý skill (skill hub) đang chuyển dữ liệu từ schema v1 lên v3, và người làm tin rằng test xanh trên fixture viết tay là đủ để báo xong. Hoá ra file metadata của hub thật dùng trường khác và thiếu id, nên migration vẫn hỏng khi chạy trên dữ liệu thật. Dev nào viết test trên dữ liệu tự tạo nên chạy thử trên dữ liệu thật trước khi báo xong."
audience: dev viết test và migration cho dữ liệu thật
spine_context: "Một công cụ quản lý skill (skill hub) viết bằng Go, đang chuyển dữ liệu từ schema v1 lên v3."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1462"]
spine_want: Migrate được hub thật từ v1 lên v3.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Dry-run trên bản sao hub thật báo 'canonical entity is missing an ID'; fixture viết tay không chứa dữ liệu thật.
spine_obstacle_lines: ["omp:cd4449ab#L1462"]
spine_turn: "Tưởng fixture viết tay và make check xanh là đủ; hoá ra hub thật có .meta/skill.yaml dùng trường repo, learn_paths và thiếu id, nên migration vẫn hỏng."
spine_turn_lines: ["omp:cd4449ab#L1461", "omp:cd4449ab#L1462"]
spine_action: "Bỏ qua .meta ở workspace v1/v2, lấy id từ tên thư mục, chấp nhận trường repo, gộp nguồn theo URL chuẩn hoá, thay fixture bằng bản sao thật."
spine_action_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1523"]
spine_outcome: "Migrate chạy được trên bản sao hub thật (schema 3, validate qua, trust không đổi); nhưng vòng review sau lộ hồi quy: description thành '>-'."
spine_outcome_lines: ["omp:cd4449ab#L1713"]
spine_takeaway: Test xanh trên fixture tự viết chưa chứng minh gì về dữ liệu thật; chạy migration trên bản sao dữ liệu thật trước khi báo xong.
spine_takeaway_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713"]
completeness: 7
---

# Test xanh mà real hub vẫn hỏng: 'canonical entity is missing an ID'

**Góc kể:** Một công cụ quản lý skill (skill hub) đang chuyển dữ liệu từ schema v1 lên v3, và người làm tin rằng test xanh trên fixture viết tay là đủ để báo xong. Hoá ra file metadata của hub thật dùng trường khác và thiếu id, nên migration vẫn hỏng khi chạy trên dữ liệu thật. Dev nào viết test trên dữ liệu tự tạo nên chạy thử trên dữ liệu thật trước khi báo xong.
**Bối cảnh:** Migrate v1 sang v3 trên bản sao hub thật, trong khi fixture viết tay vẫn xanh.
**Chuyện gì xảy ra:** Dry-run của lead trên clone hub thật báo lỗi ở bước v1 sang v2: 'canonical entity is missing an ID'. Gốc là .meta/** thuộc hub-meta nhưng validator vẫn đọc nó như canonical entity. Agent sửa canonical và schema để bỏ qua .meta khi schema dưới 3 (L1523-1537). Báo cáo đầu tiên ghi schema 1 sang 3.
**Bài học:** Fixture viết tay không bắt được lỗi dữ liệu thật; chạy migrate trên bản sao dữ liệu thật trước khi báo xong.
**Artefact:** Dòng log lỗi migrate; che đường dẫn và tên skill.
