---
id: 2026-10-21-tim-dinh-dang-cau-hinh-provider
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, artefact nhìn được]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L3637", "claude:9514b261#L3698", "claude:9514b261#L3747", "claude:9514b261#L3751", "claude:9514b261#L3774", "claude:9514b261#L3819"]
hook: "Thiếu tài liệu, agent lục chuỗi trong file nhị phân 256 MB để tìm cấu hình"
tension: it_ma_nhieu
sides: ["Chỉ một lệnh strings lọc theo tên file", "Lộ ra định dạng models.yml, gọi thử trả OK"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tìm định dạng cấu hình provider của omp bằng chuỗi trong file nhị phân khi thiếu tài liệu

**Bối cảnh:** Người dùng muốn cài TheHive cho omp như pi. Tài liệu không mô tả cách khai provider tuỳ chọn.
**Chuyện gì xảy ra:** Binary omp nặng khoảng 256 MB. Agent dùng strings lọc theo tên file cấu hình và tìm được thông báo lỗi có nhắc tới models.yml và quy tắc khoá OAuth. Từ đó agent viết models.yml với khoá dạng lệnh và gọi thử thành công, trả OK. Một lệnh quét thư mục bị bộ lọc của công cụ chặn vì thư mục node_modules.
**Bài học:** Khi thiếu tài liệu, chuỗi trong binary, đặc biệt thông báo lỗi, thường nêu đúng tên trường cấu hình.
**Artefact:** Đoạn thông báo lỗi trích từ binary (không chứa khoá) và cấu trúc models.yml đã che giá trị khoá.
