---
id: 2026-11-02-cua-hang-cua-phan-mem-la
date: 2026-11-02
repo: repo
status: raw
signals: [khác, "số trước, số sau"]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L578", "claude:6a207191#L586", "claude:6a207191#L604", "claude:6a207191#L612", "claude:6a207191#L625", "claude:6a207191#L633", "claude:6a207191#L636", "claude:6a207191#L639", "claude:6a207191#L657"]
hook: "README là cửa hàng của phần mềm: 16 rule cho màn hình đầu"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 'Cửa hàng' của phần mềm là màn hình đầu README: người dùng nói, skill thêm 16 rule

**Bối cảnh:** Người dùng nói điểm chạm đầu tiên (đọc giới thiệu, cài, quick start) quyết định người ta có dùng tiếp hay không, mà skill chưa có gì về phần này.
**Chuyện gì xảy ra:** Agent thêm common/03-first-contact.md với 16 rule: tagline nói về nỗi đau của người dùng, GIF không quá 40 giây, quick start có lời hứa thời gian, tối đa ba lệnh tới kết quả đầu tiên, quick start chạy trong CI. Sau đó người dùng nhờ agent-native, agent thêm CMD-13 đến CMD-19 và một dòng cài đặt nhờ agent trong README. Số rule đi từ 220 lên 230.
**Bài học:** Biến 'cảm giác lần đầu' thành tiêu chí kiểm được: đưa một agent mới vào máy sạch, chỉ cho đọc --help, rồi xem nó có tự cài xong không.
**Artefact:** Dòng 'Install with your agent' mẫu cho README, một câu lệnh copy được.
