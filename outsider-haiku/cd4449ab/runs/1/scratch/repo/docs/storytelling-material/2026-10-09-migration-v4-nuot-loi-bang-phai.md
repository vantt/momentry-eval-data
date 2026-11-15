---
id: 2026-10-09-migration-v4-nuot-loi-bang-phai
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3978", "omp:cd4449ab#L3987", "omp:cd4449ab#L3999"]
hook: "Migration gọi WalkDir bằng `_ =`: file hỏng bị bỏ qua mà vẫn chạy"
tension: cam_ma_van_lot
sides: ["migration có validate để chặn dữ liệu hỏng", "một ký tự `_ =` nuốt lỗi, file hỏng lọt qua"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v4 nuốt lỗi bằng `_ =`: phải fail-closed và nêu tên file

**Bối cảnh:** Migration v3→v4 đọc insight và distill từ nhiều thư mục.
**Chuyện gì xảy ra:** Lead phát hiện filepath.WalkDir trong v4.go được gọi với `_ =`, nghĩa là file insight hỏng bị bỏ qua và migration vẫn chạy. Agent viết lại mọi walk, read và parse trong v4 để trả lỗi kèm tên file, rồi thêm test: file insight hỏng thì preview fail và workspace không đổi. Lúc phiên dừng, test này đang được chạy lần đầu.
**Bài học:** Trong migration, mọi lỗi bị nuốt là mất dữ liệu im lặng. Hãy fail-closed và đưa tên file vào thông báo lỗi.
**Artefact:** Thông báo lỗi preview có tên file, không kèm nội dung insight.
**Góc người ngoài:** cách làm phổ biến là Bỏ qua lỗi cho chạy được trong lúc phát triển và quên sửa; ở đây khác ở Thay vì nuốt lỗi, migration báo đúng file hỏng và giữ workspace không đổi. Người đọc muốn biết thiết kế này để không mất dữ liệu khi migrate hub thật.
