---
id: 2026-11-02-chi-muc-dang-build-thi-loi-3c6e
code: M-EVNG
aliases: [M-EVNG]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1091"]
hook: "Chỉ mục lỗi giữa chừng giữ cạnh cũ mãi, parity test không thấy"
tension: tuong_ma_hoa_ra
sides: ["Bộ so khớp xanh nên tưởng Rust giống Python", "Python cũng có lỗi này nên giống nhau vẫn là sai"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để cho kết quả giống bản Python cũ. Người làm tin rằng test so khớp với Python xanh nghĩa là Rust đúng, nhưng khi build lỗi giữa chừng thì cạnh cũ vẫn còn mãi, và bản Python cũng làm vậy nên test không bắt được. Ai port code có bản tham chiếu nên biết: so khớp với bản cũ không chứng minh được trạng thái sau lỗi giữa chừng."
audience: dev port code hoặc viết lại công cụ có bản tham chiếu
spine_context: "Một công cụ hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust để cho kết quả giống bản Python cũ."
spine_context_lines: [profile]
spine_want: "Muốn Rust cho kết quả giống bản Python, được kiểm bằng parity test."
spine_want_lines: ["claude:2dfb5915#L1038"]
spine_obstacle: "Build lỗi giữa chừng để lại cạnh cũ, và bản Python có cùng cấu trúc ba transaction nên test so khớp không bắt được."
spine_obstacle_lines: ["claude:2dfb5915#L1038"]
spine_turn: Tưởng test so khớp xanh nghĩa là Rust đúng; hoá ra cả Python cũng có lỗi này nên giống Python vẫn là sai.
spine_turn_lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1094"]
spine_action: Thêm cờ dirty vào meta để buộc tính lại cạnh khi cờ còn; thêm khoá file và IMMEDIATE transaction cho build đồng thời.
spine_action_lines: ["claude:2dfb5915#L1091"]
spine_outcome: "Parity vẫn khớp: 64 mục, 0 lệch chưa có tên; test mới failed_build_is_rederived_next_time kiểm việc tính lại sau lỗi."
spine_outcome_lines: ["claude:2dfb5915#L1091", "claude:2dfb5915#L1094"]
spine_takeaway: "Khi test chỉ so với một bản tham chiếu có cùng lỗi, phải tự hỏi trạng thái sau lỗi giữa chừng."
spine_takeaway_lines: ["claude:2dfb5915#L1038"]
completeness: 7
---

# Chỉ mục đang build thì lỗi giữa chừng để lại cạnh cũ mãi: lỗi này cả bản Python cũng có và bộ so khớp không bắt được

**Góc kể:** Một công cụ hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để cho kết quả giống bản Python cũ. Người làm tin rằng test so khớp với Python xanh nghĩa là Rust đúng, nhưng khi build lỗi giữa chừng thì cạnh cũ vẫn còn mãi, và bản Python cũng làm vậy nên test không bắt được. Ai port code có bản tham chiếu nên biết: so khớp với bản cũ không chứng minh được trạng thái sau lỗi giữa chừng.
**Bối cảnh:** Quá trình build ghi note, cạnh và meta trong ba transaction riêng biệt.
**Chuyện gì xảy ra:** Nếu adapter lỗi sau transaction đầu tiên, lần build sau không thấy note nào đổi nên cạnh cũ được giữ. Bản Python có đúng cấu trúc này nên parity test không phát hiện. Fix thêm cờ dirty vào meta, buộc tính lại cạnh khi cờ còn; thêm khoá file và IMMEDIATE transaction cho build đồng thời.
**Bài học:** Khi test chỉ so với một bản tham chiếu có cùng lỗi, phải tự đặt câu hỏi về trạng thái sau lỗi giữa chừng.
**Artefact:** Sơ đồ ba transaction trước và sau khi thêm cờ dirty.
