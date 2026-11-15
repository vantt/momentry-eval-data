---
id: 2026-10-09-migrate-thu-tren-ban-clone-rebuild
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1870", "omp:cd4449ab#L1872", "omp:cd4449ab#L1873", "omp:cd4449ab#L1875", "omp:cd4449ab#L1876", "omp:cd4449ab#L1878", "omp:cd4449ab#L1879", "omp:cd4449ab#L1881", "omp:cd4449ab#L1882", "omp:cd4449ab#L1884", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Thử migrate trên bản clone, repo thật không bị đụng tới"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migrate thử trên bản clone: rebuild trạng thái v2 để có baseline

**Bối cảnh:** Live hub không có runtime/catalog/pointer.json nên binary cũ không show được skill trực tiếp.
**Chuyện gì xảy ra:** skill show của binary main báo thiếu pointer và yêu cầu rebuild. Agent đưa bản clone về schema 2, khôi phục thư mục .meta của một skill rồi rebuild để lấy snapshot trước. Bản clone thứ hai được migrate lên v3 để lấy snapshot sau. Mọi thao tác chỉ chạy trên các bản clone trong thư mục tạm.
**Bài học:** Muốn baseline 'trước' cho dữ liệu thật, dựng lại trạng thái cũ trên bản sao rồi rebuild; đừng suy đoán.
**Artefact:** Bảng trước/sau theo skill (name, routing), che id.
**Góc người ngoài:** cách làm phổ biến là Thường dev sẽ chạy migration thẳng trên dữ liệu thật hoặc chỉ chạy unit test với fixture tự viết, rồi tin kết quả; ở đây khác ở Agent dùng bản clone làm sandbox cho dữ liệu thật, có preview trước khi apply, và luôn xoá sạch sau đó. Người đọc muốn biết vì sao cách này an toàn hơn và làm sao lặp lại được.
