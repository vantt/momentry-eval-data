---
id: 2026-11-02-uoc-luong-token-theo-so-ky
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3088", "claude:2dfb5915#L3100"]
hook: "Agent ước lượng 1.9 nghìn token, thực tế gấp đôi"
tension: tuong_ma_hoa_ra
sides: ["ước lượng danh sách tool khoảng 1.9 nghìn token", "file thực tế 13.381 ký tự, 3.3 đến 3.8 nghìn token"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ước lượng token theo số ký tự: một bên thấp hơn gần một nửa

**Bối cảnh:** Mỗi phương án được ước lượng token định nghĩa tool, chỉ bằng độ dài chuỗi.
**Chuyện gì xảy ra:** Một agent ước lượng danh sách tool khoảng 7 KB, tương đương 1.9 nghìn token. File golden thực tế dài 13.381 ký tự, tương đương 3.3 đến 3.8 nghìn token. Ngưỡng test kích thước phải đổi từ khoảng 11 KB lên khoảng 17 KB. Thứ hạng phương án không đổi nhưng con số tuyệt đối sai.
**Bài học:** Đếm token bằng tokenizer thật trước khi chốt ngân sách. Ước lượng theo ký tự có thể sai cả con số.
**Artefact:** Bảng hai con số ước lượng và đo.
