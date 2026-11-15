---
id: 2026-11-02-bon-repo-thanh-mot-bo-luat
date: 2026-11-02
repo: repo
status: raw
signals: ["số trước, số sau", người duyệt]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L5", "claude:6a207191#L117", "claude:6a207191#L143", "claude:6a207191#L317", "claude:6a207191#L319", "claude:6a207191#L328", "claude:6a207191#L339", "claude:6a207191#L415", "claude:6a207191#L538"]
hook: "11.900 từ luật bị chê dư, cắt còn 6.400 mà vẫn đủ"
tension: it_ma_nhieu
sides: ["Cắt gần một nửa, mỗi rule còn một dòng", "Vẫn giữ khoảng 190 rule, gọn hơn nên dễ dùng hơn"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bốn repo thành một bộ luật: bản đầu 11.900 từ, bị chê dài, cắt còn 6.400

**Bối cảnh:** Người dùng muốn một skill đóng gói packaging từ bốn repo (mdview, skillstation, herdr-go, forgent), mỗi repo làm một kiểu, và skill phải lớn dần mà không đổi cấu trúc.
**Chuyện gì xảy ra:** Bốn subagent đọc song song bốn repo. Bản đầu gồm bốn file case study và khoảng hai chục file hướng dẫn, mỗi rule có tiêu đề kèm 2 đến 6 dòng giải thích, tổng khoảng 11.900 từ. Người dùng nói bản này dư thừa. Agent sao lưu bản cũ rồi viết lại: mỗi rule còn một dòng, bốn case study thay bằng một bảng references.md, bỏ các rule trùng. Số từ còn khoảng 6.400 (giảm 46%), số rule khoảng 190.
**Bài học:** Viết mỗi quy tắc thành một dòng kèm con trỏ tới đoạn code đã chạy được, đừng viết văn xuôi giải thích cho từng quy tắc.
**Artefact:** Bảng so sánh số từ theo thư mục trước và sau khi cắt. Không cần đường dẫn máy.
