---
id: 2026-11-03-release-v0-1-0-lenh-cai-d5ef
code: M-B9KX
aliases: [M-B9KX]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2968", "claude:ab9a1dd8#L2980", "claude:ab9a1dd8#L2984", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
hook: "Lệnh cài một dòng trong README không chạy được cho đến khi có tag"
tension: tuong_ma_hoa_ra
sides: ["README đã ghi lệnh cài một dòng", "Chưa có tag nên lệnh đó chưa chạy được"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Dự án momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent. Người làm đang cắt bản phát hành công khai v0.1.0.
spine_context_lines: [profile, "claude:ab9a1dd8#L2962"]
spine_want: Cắt v0.1.0 công khai để lệnh cài một dòng trong README dùng được.
spine_want_lines: ["claude:ab9a1dd8#L2962"]
spine_obstacle: Chưa có máy Windows với Claude Code đã đăng nhập để kiểm hook thật.
spine_obstacle_lines: ["claude:ab9a1dd8#L3052"]
spine_action: "Tạo tag v0.1.0, chờ release.yml chạy xong, rồi chạy đúng lệnh cài trong README ở HOME tạm."
spine_action_lines: ["claude:ab9a1dd8#L2981", "claude:ab9a1dd8#L3022"]
spine_outcome: "Release đã công bố, CI xanh; lệnh cài cho ra momentry 0.1.0."
spine_outcome_lines: ["claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3025"]
completeness: 5
---

# Release v0.1.0: lệnh cài một dòng trong README không chạy được cho đến khi có tag

**Bối cảnh:** Chủ dự án đã chọn cắt bản phát hành công khai. Workflow release có bước cài thử trước khi công bố.
**Chuyện gì xảy ra:** Điều kiện tag: HEAD trùng origin/main, CI xanh trên commit đó, chưa có tag, VERSION và CHANGELOG khớp. Workflow release chạy CI 9/9, tạo bản nháp, cài thử trên Linux, macOS và Windows, rồi mới công bố. Sau đó chạy đúng lệnh curl trong README trong HOME tạm: cài được 0.1.0, init báo sẵn sàng, update báo đã mới nhất.
**Bài học:** Hướng dẫn cài một dòng chỉ đáng tin sau khi chạy đúng lệnh đó từ internet trên máy trống, chứ không phải sau bước đóng gói nội bộ.
**Artefact:** Trang release v0.1.0 trên GitHub với danh sách file: tarball, install.sh, install.ps1, checksums.txt.
