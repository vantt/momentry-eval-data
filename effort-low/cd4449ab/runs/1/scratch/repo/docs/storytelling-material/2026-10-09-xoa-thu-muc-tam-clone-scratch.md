---
id: 2026-10-09-xoa-thu-muc-tam-clone-scratch
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1688", "omp:cd4449ab#L1837", "omp:cd4449ab#L1891"]
hook: "Kiểm tra xong là xoá ngay clone và binary trong /tmp"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá thư mục tạm (clone scratch và binary) ngay sau khi kiểm tra xong.

**Chuyện gì xảy ra:** Xoá thư mục tạm (clone scratch và binary) ngay sau khi kiểm tra xong.
**Góc người ngoài:** cách làm phổ biến là Dev thường để lại file tạm trong /tmp và không dọn, hoặc dọn không đều; ở đây khác ở Mỗi vòng kiểm tra trên bản clone của hub, agent xoá sạch clone, binary và file JSON tạm. Nhờ vậy không có dữ liệu thật nào còn sót ngoài workspace. Người đọc có thể muốn biết đây có phải thói quen chủ động hay do yêu cầu của người điều phối.
