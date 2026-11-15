---
id: 2026-10-29-chuoi-thay-the-khop-nham-core
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L590", "claude:0faf0bb2#L599", "claude:0faf0bb2#L602", "claude:0faf0bb2#L606", "claude:0faf0bb2#L613", "claude:0faf0bb2#L2242"]
hook: "Một chuỗi 'domains:' khớp nhầm 'core_domains:' làm hỏng cả file YAML"
tension: nho_ma_to
sides: ["một chuỗi thay thế khớp nhầm chữ", "YAML hỏng, script crash, sed hỏng thêm file khác"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi thay thế khớp nhầm 'core_domains' làm hỏng YAML lesson, validator báo lỗi thụt đầu dòng

**Bối cảnh:** Sau khi thay goal trong file cấu hình bằng script Python, pass distill không chạy được vì YAML không hợp lệ.
**Chuyện gì xảy ra:** Chuỗi 'domains:' khớp nhầm vào 'core_domains:' của goal cũ, nên khối mới bị ghép lệch. Validator báo bad indentation ở dòng 38. Sau đó script ghi lessons chạy trên Node 24 bị crash ESM, và một sed thay đổi chuỗi trong knowledge-base làm hỏng thêm một file. Số lesson tăng dần 12 → 17 → 30 → 32 → 38 → 47 → 52 qua các lần sửa.
**Bài học:** Khi thay một khối bằng chuỗi khớp văn bản, kiểm lại cấu trúc bằng parser thật, đừng tin rằng chuỗi chỉ xuất hiện một lần.
**Artefact:** Bảng số lesson theo từng lần ghi, kèm dòng lỗi validator đã cắt gọn.
