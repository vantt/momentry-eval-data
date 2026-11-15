---
id: 2026-11-02-diem-cham-dau-tien-la-cua
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L578", "claude:6a207191#L586", "claude:6a207191#L633"]
hook: "Điểm chạm đầu tiên là cửa hàng: README phải hứa ra kết quả trong 2 phút"
tension: khac
sides: ["người dùng chỉ cho vài phút đầu", "README thường kể công nghệ thay vì lợi ích"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điểm chạm đầu tiên là cửa hàng: đưa giới thiệu, quick start, cài đặt lên tầng đầu

**Bối cảnh:** Người dùng nói để bán hoặc quảng bá phần mềm, ma sát đầu tiên nằm ở chỗ cài đặt, đoạn giới thiệu và quick start.
**Chuyện gì xảy ra:** Agent thêm file first-contact với 16 rule: màn hình đầu README nêu lợi ích thay vì công nghệ, GIF không quá 40 giây, quick start mở bằng lời hứa kiểu 'from nothing to X in about N minutes'. Mục tiêu là tối đa 3 lệnh và khoảng 2 phút sau khi cài, và quick start phải chạy thật trong CI. Tầng 1 của skill được xếp đầu với các mục: first contact, cú pháp lệnh, agent-native, dễ dùng.
**Bài học:** Coi README đầu tiên và lệnh chạy đầu tiên là sản phẩm. Nếu người dùng mất hơn 2 phút thì sửa sản phẩm, không sửa tài liệu.
**Artefact:** Hai mẫu quick start đúng và sai, cùng sơ đồ hành trình: đọc giới thiệu, cài, quick start, thấy chạy được.
