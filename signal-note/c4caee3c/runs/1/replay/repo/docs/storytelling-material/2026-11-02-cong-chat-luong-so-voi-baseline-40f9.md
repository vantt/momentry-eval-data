---
id: 2026-11-02-cong-chat-luong-so-voi-baseline-40f9
code: M-KDBG
aliases: [M-KDBG]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L3288", "claude:c4caee3c#L3312", "claude:c4caee3c#L3349", "claude:c4caee3c#L3415"]
hook: "CI đỏ vì baseline ghi trên máy khác, đo luôn trong cùng lần chạy"
tension: cam_ma_van_lot
sides: ["Baseline ghi sẵn để làm cổng chặn", "Máy khác nhau làm cổng đỏ oan"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cổng chất lượng so với baseline ghi trên máy khác làm CI đỏ: đo upstream trong cùng lần chạy

**Bối cảnh:** Cổng upstream-no-pack so điểm đo trên máy này (0,735) với baseline đã ghi, trong khi runner GitHub đo được 0,728, vượt tolerance 0,005.
**Chuyện gì xảy ra:** Catchup đỏ vì một mục duy nhất. Thay vì hạ baseline, agent đổi cổng sang so với upstream đo ngay trong cùng lần chạy, trên cùng máy; baseline ghi sẵn chỉ còn dùng để báo độ trôi và không bao giờ làm hỏng cổng. Lượt sau đó xanh và tự đẩy tag mới cùng bộ gói.
**Bài học:** Baseline lưu trữ không mang sang máy khác được; so sánh phải diễn ra trong cùng một lần chạy.
**Artefact:** JSON báo cáo cổng với hai con số 0,735 và 0,728 (không có đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Dev thường tin test chạy trên máy mình và chỉ sửa khi CI đỏ; ít người tự dựng cổng so sánh với bản upstream đo trong cùng lần chạy để tránh phụ thuộc vào máy; ở đây khác ở Người đọc muốn biết vì sao 'đúng trên máy tôi' không đủ khi kết quả phụ thuộc loại CPU, và cách làm cổng không cần con số ghi sẵn.
