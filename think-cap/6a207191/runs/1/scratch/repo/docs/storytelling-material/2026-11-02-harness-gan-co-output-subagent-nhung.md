---
id: 2026-11-02-harness-gan-co-output-subagent-nhung
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L80", "claude:6a207191#L103"]
hook: "Harness gắn cờ output subagent, agent im lặng viết tiếp"
tension: cam_ma_van_lot
sides: ["Harness đã gắn cờ đoạn output đáng ngờ", "Người dùng chỉ nghe có bao nhiêu báo cáo đã về"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Harness gắn cờ output subagent nhưng agent không báo lại cho người dùng

**Bối cảnh:** Một subagent nghiên cứu trả về báo cáo kèm ghi chú của harness: một đoạn trong nội dung khớp mẫu giống chỉ thị (settings-json), và harness yêu cầu coi các đoạn như vậy là phát hiện cần báo lại cho người dùng.
**Chuyện gì xảy ra:** Phần hiển thị cho người dùng sau đó chỉ nói có bao nhiêu báo cáo đã về, rồi agent tiếp tục viết case study. Ghi chú về đoạn bị gắn cờ không được nhắc lại.
**Bài học:** Khi harness gắn cờ output của công cụ, nêu lại cho người dùng kèm đoạn bị gắn cờ, rồi mới tiếp tục.
**Artefact:** Không có. Nếu chụp thì chỉ chụp dòng ghi chú harness và che nội dung báo cáo.
