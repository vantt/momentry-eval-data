---
id: 2026-11-02-may-windows-that-tim-ra-loi-3c6e
code: M-AZKR
aliases: [M-AZKR]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1873", "claude:2dfb5915#L3233", "claude:2dfb5915#L3242", "claude:2dfb5915#L3275"]
hook: "Máy Windows thật lòi ra lỗi mà máy Linux không thấy"
tension: tuong_ma_hoa_ra
sides: ["Local xanh nên tưởng đã ổn", "Windows thật lộ gạch chéo, tiếng Việt và cờ Python lỗi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy Windows thật tìm ra lỗi mà máy Linux không thấy

**Bối cảnh:** Chạy bộ so khớp và installer trên Windows với Python và vault thử.
**Chuyện gì xảy ra:** Đường dẫn Windows có gạch chéo ngược khi escape trong JSON lọt qua bộ che, gây 2 lệch ở CLI. Tiếng Việt in qua pipe làm sập script Python. Cờ -I của Python ẩn user site nên không thấy PyYAML cài bằng --user; đổi sang -E -P. Các sửa đưa vào main và CI xanh cả ba nền.
**Bài học:** Cờ -I của Python không chỉ cô lập mà còn tắt site-packages của user; cần biết khi đổi.
