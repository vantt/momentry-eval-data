---
id: 2026-11-05-dung-parity-harness-so-dau-ra
date: 2026-11-05
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L1", "claude:2dfb5915#L2", "claude:2dfb5915#L3", "claude:2dfb5915#L4", "claude:2dfb5915#L5", "claude:2dfb5915#L6", "claude:2dfb5915#L7", "claude:2dfb5915#L8", "claude:2dfb5915#L9", "claude:2dfb5915#L10"]
hook: "CI so từng byte với bản Python mà không cần Python hay token"
tension: it_ma_nhieu
sides: ["golden commit sẵn trong repo, CI không cần Python hay token", "so được từng bảng, từng dòng, từng byte của tools/list"]
strength: 2
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng parity harness so đầu ra bản Rust với 'golden' sinh từ bản Python ghim ở một commit cụ thể (spec.lock). So từng bảng, từng dòng, từng câu trả lời, từng lời gọi tool, từng byte của tools/list. CI chạy so này không cần Python hay token, vì golden đã commit vào repo.

**Chuyện gì xảy ra:** Dùng parity harness so đầu ra bản Rust với 'golden' sinh từ bản Python ghim ở một commit cụ thể (spec.lock). So từng bảng, từng dòng, từng câu trả lời, từng lời gọi tool, từng byte của tools/list. CI chạy so này không cần Python hay token, vì golden đã commit vào repo.
**Góc người ngoài:** cách làm phổ biến là Port sang ngôn ngữ khác thường chỉ viết lại rồi test tay hoặc viết unit test mới theo cách hiểu của mình. Ít ai dựng bộ so khớp tự động với bản gốc; ở đây khác ở Biến 'port có đúng không' thành một con số (64 mục, 0 lệch chưa có tên). Mọi lệch có chủ ý phải ghi tên và lý do trong PORTING.md. Người đọc một mình port dự án sẽ muốn cách này để khỏi phải tin cảm giác.
