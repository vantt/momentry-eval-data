---
id: 2026-11-02-dia-tmp-het-han-muc-moi
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508", "claude:c4caee3c#L632", "claude:c4caee3c#L680", "claude:c4caee3c#L3972"]
hook: "/tmp hết hạn mức, 11 agent cùng hỏng cả lệnh chẩn đoán"
tension: nho_ma_to
sides: ["một thư mục tạm đầy hạn mức", "mọi lệnh shell của mọi agent lỗi, kể cả chẩn đoán"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đĩa /tmp hết hạn mức: mọi agent hỏng lệnh shell cùng lúc

**Bối cảnh:** Worktree và node_modules của 11 agent nằm trong /tmp, một tmpfs 16G có hạn mức. Mỗi worktree tốn khoảng 1,3G cho thư viện phụ thuộc.
**Chuyện gì xảy ra:** Khi hạn mức đầy, mọi lệnh shell của mọi agent đều lỗi EDQUOT, kể cả lệnh chẩn đoán. Cách xử lý: dừng toàn bộ agent, chuyển worktree sang ổ đĩa lớn rồi chạy git worktree repair, sau đó cho từng agent chạy lại. /tmp còn 26 phần trăm. Đĩa làm việc giảm từ 21G còn khoảng 6,4G sau khi dọn.
**Bài học:** Đặt worktree và bản dựng trên ổ có dung lượng lớn; /tmp là nơi hết hạn mức sớm nhất.
**Artefact:** Kết quả du -sh trước và sau khi dọn, không kèm đường dẫn cá nhân.
