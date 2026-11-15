---
id: 2026-10-09-fixture-test-khong-duoc-viet-tay-4257
code: M-QAZ8
aliases: [M-QAZ8]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1609", "omp:cd4449ab#L1612", "omp:cd4449ab#L1615", "omp:cd4449ab#L1790"]
hook: "Fixture tự viết cho gọn, fixture sao nguyên byte mới đúng"
tension: giup_ma_hai
sides: ["fixture giả dễ đọc dễ sửa", "chỉ file thật mới bắt được lỗi thật"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture test không được viết tay mà sao chép nguyên byte từ file thật của hub, và agent chỉ đọc các file đó, không ghi.

**Chuyện gì xảy ra:** Fixture test không được viết tay mà sao chép nguyên byte từ file thật của hub, và agent chỉ đọc các file đó, không ghi.
**Góc người ngoài:** cách làm phổ biến là Viết fixture giả lập cho gọn, ví dụ một file YAML mẫu tự nghĩ ra, vì nó dễ đọc và dễ sửa; ở đây khác ở Fixture giữ đúng định dạng thật, nên các lỗi như `repo` lạ hay block scalar `>-` lộ ra trong test. Người đọc muốn biết vì sao fixture viết tay đã từng che lỗi.
