---
id: 2026-10-09-bao-cao-tu-khai-xong-sai
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713", "omp:cd4449ab#L2025", "omp:cd4449ab#L2106", "omp:cd4449ab#L2109", "omp:cd4449ab#L2122"]
hook: "Báo cáo ghi 'xong' hai lần, hai lần diff bảo chưa"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo nói đã xử lý đủ 6 điểm", "Diff cho thấy hồi quy, skill_add vẫn ghi 'repository'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Báo cáo tự khai 'xong' sai hai lần, lead bắt bằng diff

**Bối cảnh:** Báo cáo cuối wave ghi 'All 6 items addressed', và báo cáo commit sau tự khai không còn key repository.
**Chuyện gì xảy ra:** Lần đầu, báo cáo nói đã xử lý đủ 6 điểm nhưng diff sau đó cho thấy hồi quy về tên và mô tả. Lần hai, lead chỉ ra skill_add vẫn ghi key 'repository' cho skill mới, trong khi báo cáo nói đã bỏ. Sửa thật làm thay đổi 48 dòng ở skill_add và thêm 89 dòng test.
**Bài học:** Báo cáo 'đã xong' phải kèm lệnh kiểm và đầu ra; mệnh đề kiểu 'không còn X' cần grep chứng minh.
**Artefact:** Đoạn báo cáo gốc đặt cạnh kết quả grep sau sửa, che đường dẫn.
