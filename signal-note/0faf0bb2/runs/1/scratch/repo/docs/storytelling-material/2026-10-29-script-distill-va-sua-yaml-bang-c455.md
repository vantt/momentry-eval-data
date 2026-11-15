---
id: 2026-10-29-script-distill-va-sua-yaml-bang-c455
code: M-98C6
aliases: [M-98C6]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L197", "claude:0faf0bb2#L204", "claude:0faf0bb2#L216", "claude:0faf0bb2#L227", "claude:0faf0bb2#L242", "claude:0faf0bb2#L590", "claude:0faf0bb2#L602", "claude:0faf0bb2#L606", "claude:0faf0bb2#L613", "claude:0faf0bb2#L1903"]
hook: "Một dấu hai chấm trong dòng why làm hỏng cả file YAML"
tension: nho_ma_to
sides: ["Chỉ một dấu hai chấm trong dòng why", "YAML hỏng, lệnh thay chuỗi khớp nhầm, phải sửa nhiều vòng"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Script distill và sửa YAML bằng thay chuỗi: đổi goal làm vỡ domains, sed và node lỗi

**Bối cảnh:** Learning area của fgOPC ghi lesson bằng script distill, mỗi lần đổi goal phải chấm lại.
**Chuyện gì xảy ra:** Có nhiều lỗi lặp lại: dòng why chứa dấu hai chấm làm YAML không hợp lệ, một lệnh Python thay goal khớp nhầm chuỗi 'domains:' trong core_domains, một lệnh sed sai cú pháp, và một lần script Node lỗi khi load ESM. Mỗi lần sửa xong đều chạy lại format, và cuối cùng 30 lesson được ghi đúng.
**Bài học:** Khi sửa YAML bằng thay chuỗi, khớp cả dòng đầy đủ thay vì khớp chuỗi con.
**Artefact:** Không có.
