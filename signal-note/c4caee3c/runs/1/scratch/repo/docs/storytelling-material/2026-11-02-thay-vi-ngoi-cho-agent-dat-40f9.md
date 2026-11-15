---
id: 2026-11-02-thay-vi-ngoi-cho-agent-dat-40f9
code: M-NYGV
aliases: [M-NYGV]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:c4caee3c#L119", "claude:c4caee3c#L120", "claude:c4caee3c#L488", "claude:c4caee3c#L492", "claude:c4caee3c#L733", "claude:c4caee3c#L734", "claude:c4caee3c#L763", "claude:c4caee3c#L764", "claude:c4caee3c#L2155", "claude:c4caee3c#L2156"]
hook: "Thay vì ngồi chờ, agent hẹn giờ và ghi trạng thái ra file"
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

# Thay vì ngồi chờ, agent đặt lịch đánh thức (wakeup) để kiểm tiến độ các agent nền, rồi ghi trạng thái ra file ngoài repo để sống sót qua việc nén ngữ cảnh

**Chuyện gì xảy ra:** Thay vì ngồi chờ, agent đặt lịch đánh thức (wakeup) để kiểm tiến độ các agent nền, rồi ghi trạng thái ra file ngoài repo để sống sót qua việc nén ngữ cảnh
**Góc người ngoài:** cách làm phổ biến là Dev thường để một phiên làm việc chạy liên tục, theo dõi bằng cách tự mở terminal xem log; ít người lưu trạng thái điều phối ra file để tiếp tục sau khi ngữ cảnh bị cắt; ở đây khác ở Người đọc muốn biết cách một phiên dài không mất mạch: lịch đánh thức và file trạng thái giúp tiếp tục đúng việc dù AI quên hết ngữ cảnh cũ.
