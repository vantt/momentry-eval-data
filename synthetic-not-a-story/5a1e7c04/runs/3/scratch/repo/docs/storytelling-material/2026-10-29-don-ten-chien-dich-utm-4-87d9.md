---
id: 2026-10-29-don-ten-chien-dich-utm-4-87d9
code: M-ZMWS
aliases: [M-ZMWS]
date: 2026-10-29
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c04#L8", "claude:5a1e7c04#L9", "claude:5a1e7c04#L10", "claude:5a1e7c04#L11", "claude:5a1e7c04#L12", "claude:5a1e7c04#L13"]
hook: "Script chuẩn hoá 15 link, ghi đè file gốc, không sao lưu"
tension: nho_ma_to
sides: ["Chỉ là dọn tên chiến dịch 4 hoa 6 thường", "Ghi đè không sao lưu, kiểm chứng chỉ đếm 15 dòng"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn tên chiến dịch UTM: 4 tên viết hoa lẫn 6 tên thường, và script ghi đè thẳng file gốc

**Bối cảnh:** Sheet link UTM của chiến dịch launch lộn xộn. GA4 tách chiến dịch theo chữ hoa và chữ thường, nên báo cáo bị chia nhỏ ra nhiều tên.
**Chuyện gì xảy ra:** Đếm được 4 link đặt tên 'VitC_Launch' và 6 link đặt tên 'vitc-launch'. Một script Python chuẩn hoá cả 15 dòng: source, medium và campaign về chữ thường, gạch dưới đổi thành gạch ngang. Script ghi đè thẳng vào file, không sao lưu. Bước kiểm chứng chỉ in số dòng là 15 và không đếm lại giá trị sau khi sửa.
**Bài học:** Đặt tên tham số UTM theo một quy ước chữ thường. Trước khi ghi đè file CSV, hãy sao lưu và đếm lại giá trị sau khi sửa, đừng chỉ đếm số dòng.
**Artefact:** Hai bảng đếm campaign trước và sau khi sửa, không kèm đường link.
