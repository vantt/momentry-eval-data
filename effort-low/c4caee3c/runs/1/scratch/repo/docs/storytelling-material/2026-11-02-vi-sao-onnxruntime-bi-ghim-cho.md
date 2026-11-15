---
id: 2026-11-02-vi-sao-onnxruntime-bi-ghim-cho
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định, ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2547", "claude:c4caee3c#L2981", "claude:c4caee3c#L3903"]
hook: "Định bỏ Mac Intel, cuối cùng chỉ ghim một bản onnxruntime"
tension: it_ma_nhieu
sides: ["Đề xuất ban đầu là bỏ hẳn Mac Intel", "Ghim bản 1.23.2 chỉ cho gói Intel là giữ được"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vì sao onnxruntime bị ghim cho macOS Intel

**Bối cảnh:** Bản onnxruntime-node mới nhất không còn file dựng sẵn cho darwin-x64, nên gói Intel không dựng được.
**Chuyện gì xảy ra:** Ban đầu đề xuất bỏ Mac Intel; chủ dự án chọn ghim bản 1.23.2 chỉ cho gói Intel. Đo trên cùng máy thì multilingual lệch +0,063 và vi-synonym lệch -0,017. Số đo này phụ thuộc loại CPU của runner, nên bước kiểm chỉ tính kết quả trên EPYC. Khi gói vi đổi, danh sách mức lệch cho phép thành lỗi thời, nên quy tắc đổi thành chỉ chặn khi tụt quá 0,01.
**Bài học:** Số eval chỉ tái lập được trên cùng loại CPU; quy tắc cho phép nên viết theo hướng chỉ chặn khi tụt, không liệt kê từng hạng mục.
**Artefact:** Bảng lệch theo hạng mục giữa bản ghim và bản gốc. Không cần che.
