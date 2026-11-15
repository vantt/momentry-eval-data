---
id: 2026-11-02-push-merge-khi-test-con-do-40f9
code: M-D5SK
aliases: [M-D5SK]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L2790", "claude:c4caee3c#L2796", "claude:c4caee3c#L2811", "claude:c4caee3c#L2818"]
hook: "Đẩy merge khi còn test đỏ, chạy lại ba lần đều xanh"
tension: tuong_ma_hoa_ra
sides: ["Tưởng test hỏng thật", "Ba lần chạy lại đều xanh 459/459 vì máy tải nặng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Push merge khi test còn đỏ, rồi chạy lại ba lần mới thấy xanh

**Bối cảnh:** Merge nhánh của một agent vào master kèm gói tiếng Việt. Test fail đúng sau merge, nhưng lead đã push trước khi kiểm.
**Chuyện gì xảy ra:** Merge được đẩy khi gói vẫn còn một test hỏng. Chạy lại ba lần đều 459/459 xanh, nên lead kết luận test chạy chậm lúc máy tải nặng. Lead thừa nhận đáng lẽ phải dừng trước khi push.
**Bài học:** Test flaky vẫn là lỗi. Chạy xanh ba lần không chứng minh được gì. Ghi lại, sửa, rồi mới push.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường push ngay khi local xanh, và bỏ qua hook hoặc test chưa qua; ở đây khác ở Phiên này có lúc push merge khi test còn đỏ và phải sửa sau, nên bước kiểm chéo có ích. Người đọc sẽ hỏi cách làm để không lặp lại lỗi đó.
