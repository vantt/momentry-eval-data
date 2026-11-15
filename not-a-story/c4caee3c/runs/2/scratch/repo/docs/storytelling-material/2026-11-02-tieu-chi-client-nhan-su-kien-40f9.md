---
id: 2026-11-02-tieu-chi-client-nhan-su-kien-40f9
code: M-X0KF
aliases: [M-X0KF]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1614", "claude:c4caee3c#L1615", "claude:c4caee3c#L1622", "claude:c4caee3c#L1923"]
hook: "Chưa đạt 1 giây thì sửa debounce, không hạ tiêu chí"
tension: chon_mot_mat_mot
sides: ["Nới tiêu chí là cách nhanh nhất để báo xong", "Giữ tiêu chí, đổi debounce 5000 ms xuống 250 ms mới đạt dưới 1 giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tiêu chí client nhận sự kiện trong 1 giây không được hạ, phải đổi debounce

**Bối cảnh:** Watcher của upstream chờ 5 giây sau khi file đổi mới index, nên sự kiện index chậm hơn tiêu chí 1 giây.
**Chuyện gì xảy ra:** Agent báo chưa đạt và đề nghị nới tiêu chí. Lead từ chối hạ tiêu chí và giao đổi debounce thành biến môi trường, mặc định vẫn 5000 ms. Với 250 ms, test thấy sự kiện đến trong dưới 1 giây. Probe cho 1 trên upstream và 0 trên fork.
**Bài học:** Khi một tiêu chí không đạt vì mặc định của upstream, thêm tuỳ chọn có mặc định giữ hành vi cũ. Đừng nới tiêu chí.
