---
id: 2026-11-03-xem-cau-truc-transcript-khong-xem-d5ef
code: M-7B0S
aliases: [M-7B0S]
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L3502", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3510", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3529", "claude:ab9a1dd8#L3770"]
hook: "Xem cấu trúc transcript mà không đọc một giá trị nào"
tension: khac
sides: ["Cần biết schema của transcript thật", "Script chỉ in kiểu và khoá, không in nội dung"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xem cấu trúc transcript, không xem nội dung

**Bối cảnh:** Cần viết bộ đọc transcript cho pi, omp, agy, nhưng transcript có nội dung riêng tư và không được in ra.
**Chuyện gì xảy ra:** Agent viết script in cấu trúc JSONL: chỉ in kiểu, khoá, vai trò, không in giá trị. Một vài lệnh lỗi do đường dẫn glob không khớp hoặc node eval đoạn TypeScript, nên agent chuyển sang file .mjs. Sau đó các fixture giả được viết theo đúng schema đã đo.
**Bài học:** Để học schema từ dữ liệu thật mà không lộ nội dung, hãy in khung cấu trúc, không in giá trị. Fixture chỉ cần đúng hình dạng.
**Artefact:** Đầu ra của script shape (khoá và kiểu). Không có giá trị nào.
