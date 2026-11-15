---
id: 2026-10-09-migration-v4-nuot-loi-bang-va
date: 2026-10-09
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3980", "omp:cd4449ab#L3989", "omp:cd4449ab#L3996", "omp:cd4449ab#L3998"]
hook: "Migration báo thành công trên dữ liệu hỏng vì nuốt lỗi"
tension: tuong_ma_hoa_ra
sides: ["migration báo thành công", "lỗi bị `_ =` nuốt, dữ liệu hỏng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v4 nuốt lỗi bằng `_ =` và lead bắt fail-closed

**Bối cảnh:** Migration v4 duyệt cây thư mục insight bằng filepath.WalkDir nhưng bỏ qua lỗi bằng `_ =`.
**Chuyện gì xảy ra:** Lead chỉ ra lỗi trả về bị nuốt, khiến migration có thể báo thành công trên dữ liệu hỏng. Agent thay mọi lỗi đọc, duyệt và parse trong v4.go bằng lỗi có tên file. Test mới đưa một file insight hỏng và xác nhận preview thất bại và workspace không đổi.
**Bài học:** Đừng dùng `_ =` cho lỗi của thao tác ghi hoặc duyệt dữ liệu trong migration; lỗi phải nêu tên file để người dùng sửa được.
**Artefact:** Đoạn code trước và sau, dạng `_ = Walk...` và `if err != nil { return fmt.Errorf(...) }`.
