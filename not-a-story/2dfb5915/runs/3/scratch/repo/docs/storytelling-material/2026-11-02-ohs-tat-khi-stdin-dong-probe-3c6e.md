---
id: 2026-11-02-ohs-tat-khi-stdin-dong-probe-3c6e
code: M-70WC
aliases: [M-70WC]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L307", "claude:2dfb5915#L315"]
hook: "Kill -9 probe, OHS tự thoát trong chưa tới 1 giây"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# OHS tắt khi stdin đóng, probe 6 truy vấn đồng thời khớp 6 trên 6 với CLI

**Bối cảnh:** Probe Rust điều khiển một tiến trình OHS serve --stdio.
**Chuyện gì xảy ra:** Probe gửi 6 truy vấn search cùng lúc, ghép trả lời theo id, và kết quả khớp 6 trên 6 với CLI của OHS trên cùng DB. Sau khi probe bị kill -9, OHS thấy stdin đóng và thoát trong dưới 1 giây, không còn tiến trình node sót lại.
**Bài học:** Đóng stdin là tín hiệu tắt đáng tin cậy cho tiến trình con, dễ hơn tín hiệu kill.
