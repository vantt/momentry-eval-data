---
id: 2026-11-02-dieu-phoi-25-viec-qua-chuoi-40f9
code: M-P96J
aliases: [M-P96J]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L902", "claude:c4caee3c#L927", "claude:c4caee3c#L933", "claude:c4caee3c#L945", "claude:c4caee3c#L1076", "claude:c4caee3c#L1083", "claude:c4caee3c#L1558", "claude:c4caee3c#L1564"]
hook: "Áp bản vá sai thứ tự, P03 đụng P00 ở cùng một file"
tension: hop_ma_tan
sides: ["Các bản vá riêng lẻ đều chạy tốt", "Ghép sai thứ tự thì xung đột"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điều phối 25 việc qua chuỗi bản vá: thứ tự áp và xung đột git am

**Bối cảnh:** Chín bản vá cùng chỉnh một số file lõi, nên thứ tự áp quan trọng.
**Chuyện gì xảy ra:** Bản vá P03 xung đột với P00 ở cùng một file CLI khi áp theo thứ tự sai. Lead dựng một nhánh tích hợp, áp tuần tự P00, P01, P02, P03, P04, P09, P05, P06, P07 bằng git am --3way, và xuất lại từng bản vá từ nhánh đó. Toàn chuỗi xanh với 2083 test.
**Bài học:** Với bản vá cùng chạm một file, cố định thứ tự trong manifest và kiểm bằng một nhánh tích hợp thay vì tin từng bản riêng lẻ.
**Artefact:** Sơ đồ thứ tự chuỗi bản vá (không kèm đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Thường một dev làm tuần tự từng việc trong một nhánh; nhiều việc cùng lúc dễ đụng file và xung đột, nên hiếm người chạy song song nhiều luồng AI như vậy; ở đây khác ở Người đọc sẽ hỏi làm sao tránh đụng file và xung đột khi nhiều agent cùng sửa một repo; câu trả lời nằm ở việc tách worktree, xuất patch vào thư mục chung và một lead duy nhất ghép theo thứ tự phụ thuộc.
