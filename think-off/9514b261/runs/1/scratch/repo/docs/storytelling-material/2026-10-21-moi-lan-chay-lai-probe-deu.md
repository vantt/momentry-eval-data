---
id: 2026-10-21-moi-lan-chay-lai-probe-deu
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2213", "claude:9514b261#L2470", "claude:9514b261#L2772", "claude:9514b261#L2954", "claude:9514b261#L3338"]
hook: "Mỗi lần chạy lại probe: cất kết quả cũ, rồi kiểm không sót tiến trình"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mỗi lần chạy lại probe đều chuyển kết quả cũ sang một thư mục prev riêng trước, chạy nền, rồi sau đó kiểm tra không còn pane hay tiến trình nào sót và không có file git nào bị bẩn.

**Chuyện gì xảy ra:** Mỗi lần chạy lại probe đều chuyển kết quả cũ sang một thư mục prev riêng trước, chạy nền, rồi sau đó kiểm tra không còn pane hay tiến trình nào sót và không có file git nào bị bẩn.
**Góc người ngoài:** cách làm phổ biến là Ghi đè file kết quả cũ, không kiểm dọn tiến trình sau khi chạy, và tin rằng lần chạy đó đã sạch; ở đây khác ở Người đọc sẽ muốn biết vì sao so sánh được giữa các lần chạy và làm sao không để lại rác. Cách làm này giữ được lịch sử kết quả và xác nhận môi trường sạch sau mỗi lần.
