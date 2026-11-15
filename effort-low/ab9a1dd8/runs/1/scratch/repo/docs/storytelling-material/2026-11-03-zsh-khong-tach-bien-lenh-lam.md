---
id: 2026-11-03-zsh-khong-tach-bien-lenh-lam
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L105", "claude:ab9a1dd8#L109", "claude:ab9a1dd8#L1199", "claude:ab9a1dd8#L1226", "claude:ab9a1dd8#L1235", "claude:ab9a1dd8#L3770", "claude:ab9a1dd8#L3884", "claude:ab9a1dd8#L3891"]
hook: "Cùng một lệnh, zsh lỗi năm lần, bash chạy được"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh không tách biến lệnh làm lỗi kiểm thử; phải chạy lại bằng bash

**Bối cảnh:** Shell mặc định của agent là zsh, còn các script kiểm thử đều viết theo bash, dùng for và biến.
**Chuyện gì xảy ra:** Ít nhất năm lần lệnh zsh lỗi: không tách biến, glob không khớp, hoặc hàm shell bọc pi và omp làm lệnh thật bị đổi nghĩa. Mỗi lần agent chuyển sang bash -c hoặc tìm đường dẫn thật bằng type -P trước khi chạy lại.
**Bài học:** Khi script có cú pháp bash, luôn gọi bash -c rõ ràng; và tìm đường dẫn thật của lệnh vì các hàm bọc trong shell có thể làm sai kết quả.
**Artefact:** Output lỗi zsh và lệnh bash -c đã sửa, đặt cạnh nhau. Không cần che gì.
