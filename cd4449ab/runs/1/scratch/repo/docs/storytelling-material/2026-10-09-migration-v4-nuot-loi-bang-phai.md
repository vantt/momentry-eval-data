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
hook: "Migration nuốt lỗi bằng `_ =`, file hỏng vẫn chạy tiếp"
tension: cam_ma_van_lot
sides: ["Migration có validate, tưởng đã chặn file hỏng", "Một `_ =` cho file insight hỏng lọt qua"]
strength: 3
stakes: 2
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
**Góc người ngoài:** cách làm phổ biến là Bỏ qua lỗi bằng `_ =` hoặc log rồi chạy tiếp, ưu tiên cho migration chạy xong; ở đây khác ở Migration âm thầm nuốt file hỏng sẽ làm mất dữ liệu mà không ai biết. Lead bắt được lỗi này khi review, và dev một mình không có người review nên cần biết quy tắc này.
