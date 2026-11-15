---
id: 2026-10-29-model-mac-dinh-cua-aicoworker-da
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1079", "claude:0faf0bb2#L1080", "claude:0faf0bb2#L1115", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1129", "claude:0faf0bb2#L1137"]
hook: "Model mặc định đã bị ngừng, nên agent main hỏng dù bạn không làm gì"
tension: tuong_ma_hoa_ra
sides: ["cấu hình mặc định tưởng an toàn", "trỏ tới model đã ngừng, agent main hỏng khi dùng thường"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model mặc định của AICoworker đã bị ngừng: spike phát hiện agent main hỏng khi dùng bình thường

**Bối cảnh:** Khi chạy spike, agent được gọi qua gateway không trả lời được. Lỗi không nằm ở Paperclip mà ở cấu hình model của OpenClaw.
**Chuyện gì xảy ra:** Cấu hình mặc định đang trỏ tới một model đã bị ngừng ('gemini-3-pro-low'). Spike không sửa openclaw.json mà đổi model riêng cho session của task bằng lệnh patch session, không in token. Hệ quả là lỗi này làm hỏng agent main ngay cả khi không liên quan đến spike.
**Bài học:** Trước khi nối một hệ thống điều phối vào runtime, kiểm model mặc định của runtime đó. Đổi model theo session khi cần để không đụng cấu hình chung.
**Artefact:** Bảng session: model cũ, model mới theo từng session. Không đưa token vào.
