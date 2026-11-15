---
id: 2026-11-02-chu-bo-khoi-danh-sach-lam-40f9
code: M-4XTE
aliases: [M-4XTE]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2586", "claude:c4caee3c#L2590", "claude:c4caee3c#L2592"]
hook: "Chữ 'bỏ khỏi danh sách' làm người dùng hiểu ngược"
tension: tuong_ma_hoa_ra
sides: ["Người dùng tưởng agent đang đề xuất lại phương án đã bị bác", "Thực ra đó là đề nghị khác hẳn"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chữ 'bỏ khỏi danh sách' làm người dùng hiểu ngược

**Bối cảnh:** Agent viết đề xuất có nhiều thuật ngữ nội bộ như nền bắt buộc và dòng dựng gói tuỳ chọn, đồng thời ám chỉ một phương án người dùng chưa chọn.
**Chuyện gì xảy ra:** Người dùng ngắt agent đang giao việc, rồi nói chưa hiểu câu 'tôi đề nghị bỏ khỏi danh sách nền bắt buộc', vì trông như đang đề xuất phương án đã bị bác. Agent giải thích từng phần bằng ngôn ngữ thường, rồi chỉ giao việc sau khi người dùng xác nhận.
**Bài học:** Khi viết đề xuất cho người duyệt, nêu rõ lựa chọn đang chờ quyết, tránh câu phủ định nhiều lớp. Khi bị ngắt, hỏi lại chứ đừng đoán.
