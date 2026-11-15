---
id: 2026-11-02-review-ohs-tim-ra-treo-may-3c6e
code: M-GYW9
aliases: [M-GYW9]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L607", "claude:2dfb5915#L631"]
hook: "Một byte stderr không phải UTF-8 đủ làm treo cả supervisor"
tension: nho_ma_to
sides: ["Một byte lỗi trong stderr", "Reader thoát, pipe đầy, close() và Drop treo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ hỏi Claude Desktop về graph của vault Obsidian, và lõi đang được viết lại bằng Rust. Người làm tin module giữ tiến trình chạy lâu qua pipe đã xong, chỉ chờ review. Review lại tìm ra hai lỗi: stderr có byte không phải UTF-8 làm luồng đọc thoát, rồi pipe đầy làm cả tiến trình đứng; và ghi stdin giữ khoá không giới hạn khiến pkm không thoát được. Ai viết tiến trình con qua pipe nên quan tâm, vì cả hai lỗi đều liên quan tới việc đọc không chạy tới EOF và ghi không có thời hạn."
audience: dev Rust viết tiến trình con qua pipe
spine_context: "Dự án là một công cụ hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust."
spine_context_lines: [profile]
spine_want: Muốn đưa bản cài được hoàn tất theo plan.
spine_want_lines: ["claude:2dfb5915#L571"]
spine_obstacle: "Review chỉ ra hai lỗi nghiêm trọng: stderr của tiến trình con làm luồng đọc thoát, và ghi stdin giữ khoá không giới hạn thời gian."
spine_obstacle_lines: ["claude:2dfb5915#L607"]
spine_turn: "Tưởng module đã xong, chỉ chờ review; hoá ra có hai lỗi mức High."
spine_turn_lines: ["claude:2dfb5915#L598", "claude:2dfb5915#L607"]
spine_action: Gửi kết quả review về cho chính agent đã viết module để sửa trên nhánh của nó.
spine_action_lines: ["claude:2dfb5915#L615"]
spine_outcome: "Bản sửa đã được gộp và đẩy lên main; test mới chỉ chạy trên Linux, Windows và macOS chưa kiểm tra."
spine_outcome_lines: ["claude:2dfb5915#L631", "claude:2dfb5915#L640"]
spine_takeaway: "Đọc tiến trình con qua pipe phải chạy tới EOF bất kể dữ liệu, và mọi thao tác ghi phải có thời hạn."
spine_takeaway_lines: ["claude:2dfb5915#L607"]
completeness: 7
---

# Review OHS tìm ra treo máy: stderr có byte không phải UTF-8 làm reader thoát, còn stdin đầy thì khoá cả supervisor

**Góc kể:** Dự án là công cụ hỏi Claude Desktop về graph của vault Obsidian, và lõi đang được viết lại bằng Rust. Người làm tin module giữ tiến trình chạy lâu qua pipe đã xong, chỉ chờ review. Review lại tìm ra hai lỗi: stderr có byte không phải UTF-8 làm luồng đọc thoát, rồi pipe đầy làm cả tiến trình đứng; và ghi stdin giữ khoá không giới hạn khiến pkm không thoát được. Ai viết tiến trình con qua pipe nên quan tâm, vì cả hai lỗi đều liên quan tới việc đọc không chạy tới EOF và ghi không có thời hạn.
**Bối cảnh:** Module giữ một tiến trình OHS chạy lâu bằng pipe. Phần này được viết xong trước khi review.
**Chuyện gì xảy ra:** Review chỉ ra hai lỗi nghiêm trọng: đọc stderr dừng khi gặp UTF-8 lỗi, pipe đầy 4 KB trên Windows thì console.error của OHS chặn luôn event loop; ghi stdin giữ mutex không có giới hạn thời gian nên close() và Drop bị treo. Agent sửa bằng một luồng ghi riêng, đọc tới EOF, và kill process khi quá hạn.
**Bài học:** Với tiến trình con qua pipe, đọc phải chạy tới EOF không phụ thuộc dữ liệu, và mọi thao tác ghi phải có thời hạn.
**Artefact:** Sơ đồ luồng đọc và ghi có thể vẽ lại. Không có log.
