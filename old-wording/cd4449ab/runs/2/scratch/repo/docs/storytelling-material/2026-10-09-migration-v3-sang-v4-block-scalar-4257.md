---
id: 2026-10-09-migration-v3-sang-v4-block-scalar-4257
code: M-XYB3
aliases: [M-XYB3]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac, dao_quyet_dinh]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2717", "omp:cd4449ab#L2741", "omp:cd4449ab#L2744", "omp:cd4449ab#L2746", "omp:cd4449ab#L2770"]
hook: "Python đọc được, Go báo lỗi: chỉ vì một ký tự |4"
tension: nho_ma_to
sides: ["Python parse YAML trơn tru", "một chỉ báo thụt lề |4 làm Go không đọc nổi receipt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v3 sang v4: block scalar YAML sai làm receipt WAL không đọc được

**Bối cảnh:** Migration v3 sang v4 ghi receipt WAL chứa nội dung file cũ dạng YAML lồng nhau. Test đỏ qua hơn chục lần chạy với lỗi 'proposed mutation is invalid'.
**Chuyện gì xảy ra:** Python yaml parse được chuỗi, nhưng decoder yaml.v3 của Go báo 'did not find expected key' ở dòng 1. Nguyên nhân là chỉ báo thụt lề |4 sai trong block scalar. Đổi thành | thì decode thành công và phần migration được tiếp tục.
**Bài học:** Đừng tự ghép YAML bằng chuỗi cho thứ sẽ được đọc lại. Dùng marshaller hoặc kiểm bằng đúng decoder mà code dùng.
**Artefact:** Đoạn YAML receipt trước và sau khi đổi |4 thành |, che nội dung.
