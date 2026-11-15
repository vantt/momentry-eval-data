---
id: 2026-10-29-don-ten-chien-dich-utm-4-87d9
code: M-ZMWS
aliases: [M-ZMWS]
date: 2026-10-29
repo: repo
status: raw
signals: [số trước-sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c04#L8", "claude:5a1e7c04#L9", "claude:5a1e7c04#L10", "claude:5a1e7c04#L11", "claude:5a1e7c04#L12", "claude:5a1e7c04#L13"]
hook: "Script dọn 15 link ghi đè file gốc, không sao lưu, chỉ đếm dòng"
tension: giup_ma_hai
sides: ["dọn tên chiến dịch cho gọn, thống nhất", "ghi đè không sao lưu, kiểm chứng chỉ đếm 15 dòng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Người làm đang chuẩn bị tuần ra mắt serum vitamin C, gồm banner, sheet link UTM và kế hoạch ngân sách."
spine_context_lines: ["claude:5a1e7c04#L1"]
spine_want: "Sheet link UTM gọn, tên chiến dịch thống nhất."
spine_want_lines: ["claude:5a1e7c04#L8"]
spine_obstacle: "Tên chiến dịch viết hoa lẫn thường: 4 link 'VitC_Launch' và 6 link 'vitc-launch'."
spine_obstacle_lines: ["claude:5a1e7c04#L10"]
spine_action: "Đổi cả 15 dòng CSV sang chữ thường, gạch ngang, bằng script Python ghi đè thẳng links.csv, không sao lưu."
spine_action_lines: ["claude:5a1e7c04#L7", "claude:5a1e7c04#L11"]
spine_outcome: "Bước kiểm chỉ in số dòng 15. Agent báo cả 15 link đã thống nhất, nhưng đoạn này không đếm lại giá trị sau khi sửa."
spine_outcome_lines: ["claude:5a1e7c04#L12", "claude:5a1e7c04#L13"]
spine_takeaway: "Trước khi ghi đè CSV, hãy sao lưu và đếm lại giá trị sau khi sửa, đừng chỉ đếm số dòng."
spine_takeaway_lines: ["claude:5a1e7c04#L11", "claude:5a1e7c04#L12"]
completeness: 6
---

# Dọn tên chiến dịch UTM: 4 tên viết hoa lẫn 6 tên thường, và script ghi đè thẳng file gốc

**Bối cảnh:** Sheet link UTM của chiến dịch launch lộn xộn. GA4 tách chiến dịch theo chữ hoa và chữ thường, nên báo cáo bị chia nhỏ ra nhiều tên.
**Chuyện gì xảy ra:** Đếm được 4 link đặt tên 'VitC_Launch' và 6 link đặt tên 'vitc-launch'. Một script Python chuẩn hoá cả 15 dòng: source, medium và campaign về chữ thường, gạch dưới đổi thành gạch ngang. Script ghi đè thẳng vào file, không sao lưu. Bước kiểm chứng chỉ in số dòng là 15 và không đếm lại giá trị sau khi sửa.
**Bài học:** Đặt tên tham số UTM theo một quy ước chữ thường. Trước khi ghi đè file CSV, hãy sao lưu và đếm lại giá trị sau khi sửa, đừng chỉ đếm số dòng.
**Artefact:** Hai bảng đếm campaign trước và sau khi sửa, không kèm đường link.
