---
id: 2026-10-09-ky-tu-4-lam-go-yaml
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2717", "omp:cd4449ab#L2719", "omp:cd4449ab#L2720", "omp:cd4449ab#L2722", "omp:cd4449ab#L2741", "omp:cd4449ab#L2743", "omp:cd4449ab#L2744", "omp:cd4449ab#L2746"]
hook: "Python đọc file YAML ngon, Go từ chối vì một ký tự"
tension: nho_ma_to
sides: ["Cùng một file YAML hợp lệ", "Go báo lỗi ngay dòng 1 vì '|4'"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ký tự '|4' làm Go yaml.v3 từ chối còn Python thì qua

**Bối cảnh:** Một artifact YAML sinh từ dữ liệu fixture cần được Go parser đọc được.
**Chuyện gì xảy ra:** Python yaml.safe_load đọc được file, nhưng Go yaml.v3 báo 'did not find expected key' ở dòng 1. Nguyên nhân là block scalar có chỉ báo thụt dòng '|4'. Đổi thành '|' thì Go decode thành công. Mất thêm vài lượt vì go run với heredoc và đọc artifact không ra kết quả.
**Bài học:** Hai parser YAML khác nhau về block scalar; test bằng đúng parser mà code thật dùng.
**Artefact:** Đoạn YAML trước/sau, không kèm nội dung lesson.
