---
id: 2026-11-02-phan-hoi-may-windows-that-bao
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt thứ máy soạn]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3242", "claude:2dfb5915#L3258", "claude:2dfb5915#L3999"]
hook: "Máy Windows thật tìm ra 4 lỗi mà CI ba nền không thấy"
tension: tuong_ma_hoa_ra
sides: ["CI xanh trên ba nền tảng", "máy Windows thật vẫn lộ bốn lỗi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phản hồi máy Windows thật: báo cáo được sửa trên main

**Bối cảnh:** Máy Windows thật cài bản rc và viết báo cáo thử. Agent sửa các lỗi trong báo cáo.
**Chuyện gì xảy ra:** Báo cáo nêu bốn việc: che đường dẫn trong JSON, lỗi in tiếng Việt qua pipe, PyYAML không được nhìn thấy, và bản bàn giao còn chỉ dẫn cũ. Agent sửa trên main và CI xanh trên ba nền. Sau đó người dùng hỏi còn việc gì khi máy Windows đã làm nhiều việc.
**Bài học:** Máy thật tìm ra lỗi mà CI không thấy. Cần có kênh báo cáo ngược về repo và một bản bàn giao được cập nhật.
**Artefact:** Không có.
