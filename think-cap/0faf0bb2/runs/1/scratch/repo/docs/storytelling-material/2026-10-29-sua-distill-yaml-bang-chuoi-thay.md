---
id: 2026-10-29-sua-distill-yaml-bang-chuoi-thay
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L249", "claude:0faf0bb2#L590", "claude:0faf0bb2#L599", "claude:0faf0bb2#L602", "claude:0faf0bb2#L603", "claude:0faf0bb2#L606", "claude:0faf0bb2#L608", "claude:0faf0bb2#L613", "claude:0faf0bb2#L1903", "claude:0faf0bb2#L2242"]
hook: "Một chuỗi 'domains:' khớp nhầm 'core_domains:' làm hỏng YAML, rồi 5 lỗi công cụ nối đuôi"
tension: nho_ma_to
sides: ["Một lần thay chuỗi đơn giản", "YAML hỏng, kéo theo ít nhất 5 lỗi công cụ trong một lượt"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa distill.yaml bằng chuỗi thay thế: khớp nhầm core_domains và công cụ lỗi nhiều lần

**Bối cảnh:** Công cụ distill ghi bài học vào YAML, và pass được cấu hình bằng một file YAML có các mục domains.
**Chuyện gì xảy ra:** Lần thay goal bằng python tìm chuỗi 'domains:' và khớp nhầm vào 'core_domains:' của goal cũ, làm YAML hỏng với lỗi indentation. Lần sửa tiếp theo dùng sed với biểu thức sai và báo 'unknown command'. Script ghi lesson qua node báo lỗi ESM loader. Lệnh gửi feedback lên skillstation cũng bị từ chối với invalid_request. Trong một pass có ít nhất 5 lỗi công cụ.
**Bài học:** Thay chuỗi trong YAML bằng substring dễ khớp nhầm; khớp theo đầu dòng hoặc dùng parser để sửa cấu trúc.
**Artefact:** Thông báo lỗi 'not valid YAML, bad indentation (38:3)' đã rút gọn.
