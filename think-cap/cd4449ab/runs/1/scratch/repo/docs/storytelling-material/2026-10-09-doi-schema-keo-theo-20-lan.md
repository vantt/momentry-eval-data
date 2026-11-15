---
id: 2026-10-09-doi-schema-keo-theo-20-lan
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L621", "omp:cd4449ab#L633", "omp:cd4449ab#L642", "omp:cd4449ab#L651", "omp:cd4449ab#L669", "omp:cd4449ab#L675", "omp:cd4449ab#L699", "omp:cd4449ab#L753", "omp:cd4449ab#L795", "omp:cd4449ab#L873", "omp:cd4449ab#L954", "omp:cd4449ab#L990", "omp:cd4449ab#L999", "omp:cd4449ab#L1050", "omp:cd4449ab#L1119", "omp:cd4449ab#L1161", "omp:cd4449ab#L1188", "omp:cd4449ab#L1221", "omp:cd4449ab#L1251", "omp:cd4449ab#L1278", "omp:cd4449ab#L1290", "omp:cd4449ab#L2079"]
hook: "Đổi schema một lần, hơn 20 lần go test đỏ rải rác"
tension: nho_ma_to
sides: ["Chỉ đổi một schema", "Hơn 20 lần test đỏ, mỗi lần một lỗi khác"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi schema kéo theo 20+ lần go test đỏ rải rác

**Bối cảnh:** Sau khi đổi schema và cách ghi metadata, nhiều package có fixture cũ.
**Chuyện gì xảy ra:** Qua nhiều vòng, go test ./... đỏ rồi test đơn lẻ vẫn đỏ với lỗi khác. Gặp lỗi thư mục .meta chưa có, metadata cũ chứa provenance và thiếu runtime. Hơn 20 lần go test đỏ trong vòng này, đa số sửa bằng cách cập nhật fixture theo schema mới.
**Bài học:** Khi đổi schema, chạy full suite sớm một lần để thấy hết bề mặt bị ảnh hưởng, đừng chạy từng test đơn.
**Artefact:** Danh sách package đỏ trước và sau một lần sửa.
**Góc người ngoài:** cách làm phổ biến là Dev thường sửa hàng loạt cùng lúc hoặc chạy toàn bộ suite liên tục, tốn thời gian và khó biết sửa cái nào làm xanh cái nào; ở đây khác ở Cách chạy đúng một test hoặc một package, mở rộng dần, giúp khoanh vùng nhanh. Đây là kỹ năng debug có thể làm được với mọi dự án.
