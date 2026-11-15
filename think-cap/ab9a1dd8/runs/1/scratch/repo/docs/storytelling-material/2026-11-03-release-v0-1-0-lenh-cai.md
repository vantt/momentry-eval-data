---
id: 2026-11-03-release-v0-1-0-lenh-cai
date: 2026-11-03
repo: repo
status: raw
signals: ["6"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2968", "claude:ab9a1dd8#L2981", "claude:ab9a1dd8#L3015", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3022", "claude:ab9a1dd8#L3025"]
hook: "Lệnh cài một dòng trong README chạy thật từ GitHub, ra v0.1.0"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release v0.1.0: lệnh cài một dòng chạy được từ GitHub thật

**Bối cảnh:** Sau khi CI xanh, người dùng đồng ý cắt tag đầu tiên.
**Chuyện gì xảy ra:** Release chạy xanh từ đầu tới cuối trên chín tổ hợp, tạo bản nháp, cài thử trên ba hệ điều hành, rồi công bố. Agent chạy đúng lệnh cài một dòng trong README với GitHub thật trong HOME tạm, cài được v0.1.0.
**Bài học:** Kiểm lệnh cài từ asset phát hành thật trong HOME tạm, không kiểm từ thư mục nguồn.
**Artefact:** Trang release với danh sách asset và đầu ra lệnh cài, che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ kiểm bản phát hành bằng cách nhìn trang release có file hay không, không tự chạy đúng lệnh mà người dùng sẽ gõ; ở đây khác ở Việc đo sau công bố với môi trường cô lập cho thấy lệnh README thật sự chạy. Người đọc sẽ hỏi vì sao không tin vào CI đã xanh.
