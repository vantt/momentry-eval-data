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
hook: "Lệnh cài một dòng trong README chưa chạy được cho đến khi có tag"
tension: tuong_ma_hoa_ra
sides: ["README ghi lệnh cài một dòng, tưởng dùng được", "Chưa có tag v0.1.0 nên lệnh không chạy"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang cắt bản phát hành công khai đầu tiên, v0.1.0. README đã ghi sẵn lệnh cài một dòng như thể nó dùng được, nhưng lệnh đó trỏ tới một bản phát hành chưa tồn tại, nên chỉ chạy được sau khi có tag. Sau khi cắt tag và chạy đúng lệnh curl từ internet trong một HOME trống, lệnh cài mới thật sự cài được bản 0.1.0. Ai viết hướng dẫn cài một dòng nên thử đúng lệnh đó từ internet, đừng chỉ tin bước đóng gói nội bộ."
audience: dev làm công cụ CLI và viết hướng dẫn cài đặt
spine_context: "momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang cắt bản phát hành công khai đầu tiên, v0.1.0."
spine_context_lines: [profile, "claude:ab9a1dd8#L2963"]
spine_want: Muốn lệnh cài một dòng trong README dùng được cho người khác.
spine_want_lines: ["claude:ab9a1dd8#L2962"]
spine_obstacle: Khối cài trong checklist bị đánh dấu partial vì trỏ tới một bản phát hành chưa có.
spine_obstacle_lines: ["claude:ab9a1dd8#L3030"]
spine_turn: README đã ghi sẵn lệnh cài một dòng như thể nó dùng được; hoá ra nó chỉ chạy được sau khi có tag.
spine_turn_lines: ["claude:ab9a1dd8#L2962", "claude:ab9a1dd8#L3030"]
spine_action: "Cắt tag v0.1.0 sau khi kiểm điều kiện, để workflow release chạy và công bố."
spine_action_lines: ["claude:ab9a1dd8#L2981"]
spine_outcome: "Release công khai, CI 9/9 xanh; lệnh curl trong README cài được 0.1.0 trong HOME tạm."
spine_outcome_lines: ["claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
spine_takeaway: Hướng dẫn cài một dòng chỉ đáng tin sau khi chạy đúng lệnh đó từ internet trên máy trống.
spine_takeaway_lines: ["claude:ab9a1dd8#L3042"]
completeness: 7
---

# Release v0.1.0: lệnh cài một dòng trong README không chạy được cho đến khi có tag

**Góc kể:** momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang cắt bản phát hành công khai đầu tiên, v0.1.0. README đã ghi sẵn lệnh cài một dòng như thể nó dùng được, nhưng lệnh đó trỏ tới một bản phát hành chưa tồn tại, nên chỉ chạy được sau khi có tag. Sau khi cắt tag và chạy đúng lệnh curl từ internet trong một HOME trống, lệnh cài mới thật sự cài được bản 0.1.0. Ai viết hướng dẫn cài một dòng nên thử đúng lệnh đó từ internet, đừng chỉ tin bước đóng gói nội bộ.
**Bối cảnh:** Chủ dự án đã chọn cắt bản phát hành công khai. Workflow release có bước cài thử trước khi công bố.
**Chuyện gì xảy ra:** Điều kiện tag: HEAD trùng origin/main, CI xanh trên commit đó, chưa có tag, VERSION và CHANGELOG khớp. Workflow release chạy CI 9/9, tạo bản nháp, cài thử trên Linux, macOS và Windows, rồi mới công bố. Sau đó chạy đúng lệnh curl trong README trong HOME tạm: cài được 0.1.0, init báo sẵn sàng, update báo đã mới nhất.
**Bài học:** Hướng dẫn cài một dòng chỉ đáng tin sau khi chạy đúng lệnh đó từ internet trên máy trống, chứ không phải sau bước đóng gói nội bộ.
**Artefact:** Trang release v0.1.0 trên GitHub với danh sách file: tarball, install.sh, install.ps1, checksums.txt.
