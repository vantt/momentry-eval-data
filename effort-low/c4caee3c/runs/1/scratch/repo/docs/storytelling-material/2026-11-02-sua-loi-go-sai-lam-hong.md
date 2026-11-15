---
id: 2026-11-02-sua-loi-go-sai-lam-hong
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1470"]
hook: "Sửa lỗi gõ sai lại làm kết quả đồng nghĩa tụt từ hạng 4 xuống 7"
tension: giup_ma_hai
sides: ["Bộ sửa gõ sai để tìm kiếm tốt hơn", "Đổi phone thành từ lạ, đồng nghĩa tụt hạng 4 xuống 7"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa lỗi gõ sai làm hỏng lexicon: đồng nghĩa tụt từ hạng 4 xuống 7

**Bối cảnh:** Bộ sửa lỗi gõ sai chạy trước lexicon, và cả hai cùng biến đổi từ người dùng gõ.
**Chuyện gì xảy ra:** Bộ sửa gõ sai đổi từ phone thành một từ gần trong vault trước khi lexicon kịp nhận ra, kéo kết quả đồng nghĩa từ hạng 4 xuống 7 và Hit@5 hạng mục đồng nghĩa xuống 0,73. Sửa bằng cách lexicon khớp cả câu gốc lẫn câu đã sửa, và các từ đã có trong lexicon được coi là từ đã biết.
**Bài học:** Hai lớp biến đổi truy vấn phải nhìn cùng một câu gốc; lớp sau không được xoá dấu vết của lớp trước.
**Artefact:** Bảng thứ hạng đồng nghĩa trước và sau. Không cần che.
