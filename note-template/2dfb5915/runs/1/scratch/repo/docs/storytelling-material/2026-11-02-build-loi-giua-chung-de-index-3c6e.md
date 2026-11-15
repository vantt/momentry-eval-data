---
id: 2026-11-02-build-loi-giua-chung-de-index-3c6e
code: M-S2R6
aliases: [M-S2R6]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1045", "claude:2dfb5915#L1046", "claude:2dfb5915#L1091"]
hook: "Build lỗi giữa chừng, index sai mãi mà test vẫn xanh"
tension: tuong_ma_hoa_ra
sides: ["Bộ so khớp với Python khớp nghĩa là đúng", "Python sai y hệt nên không ai bắt được"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust để kết quả khớp với bản Python. Người làm tin rằng test so khớp với Python là đủ để chứng minh build đúng. Review phát hiện: nếu build lỗi giữa chừng, lần build sau không tính lại edges và index sai mãi, còn bản Python cũng sai y như vậy nên test không bắt được. Ai viết lại code và dựa vào test so khớp với bản gốc nên nhớ: giống bản gốc không có nghĩa là đúng."
audience: dev viết lại công cụ bằng test so khớp với bản gốc
spine_context: "Một công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust để kết quả khớp với bản Python."
spine_context_lines: [profile]
spine_want: "Hoàn tất plan viết lại lõi Rust, với kết quả khớp bản Python trên cùng một vault."
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Build lỗi giữa chừng để lại index sai, và test so khớp không bắt được."
spine_obstacle_lines: ["claude:2dfb5915#L1038"]
spine_turn: "Tưởng test so khớp với Python là đủ để tin build đúng; hoá ra Python có cùng lỗi hai transaction tách rời, nên test không phát hiện."
spine_turn_lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1091"]
spine_action: "Thêm cờ dirty trong meta để buộc tính lại edges sau build lỗi, kèm test mô phỏng lỗi."
spine_action_lines: ["claude:2dfb5915#L1091"]
spine_outcome: Test mô phỏng lỗi đã có; parity vẫn 0 lệch chưa có tên.
spine_outcome_lines: ["claude:2dfb5915#L1091", "claude:2dfb5915#L1094"]
spine_takeaway: "Test so khớp với bản gốc chỉ chứng minh giống bản gốc, không chứng minh bản gốc đúng."
spine_takeaway_lines: ["claude:2dfb5915#L1038"]
completeness: 7
---

# Build lỗi giữa chừng để index sai mãi, và Python cũng sai y như vậy

**Góc kể:** Dự án là một công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust để kết quả khớp với bản Python. Người làm tin rằng test so khớp với Python là đủ để chứng minh build đúng. Review phát hiện: nếu build lỗi giữa chừng, lần build sau không tính lại edges và index sai mãi, còn bản Python cũng sai y như vậy nên test không bắt được. Ai viết lại code và dựa vào test so khớp với bản gốc nên nhớ: giống bản gốc không có nghĩa là đúng.
**Bối cảnh:** Quá trình build ghi note và edges bằng hai transaction tách rời.
**Chuyện gì xảy ra:** Review phát hiện nếu build lỗi sau transaction đầu, lần build sau thấy không đổi nên không tính lại edges. Python có đúng cấu trúc hai transaction nên bộ so khớp không bắt được. Sửa bằng cờ dirty trong meta để buộc tính lại, có test mô phỏng lỗi.
**Bài học:** Parity test chỉ chứng minh giống bản gốc, không chứng minh bản gốc đúng.
