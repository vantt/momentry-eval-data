---
id: 2026-11-01-khong-dung-pi-update-vi-tu
date: 2026-11-01
repo: repo
status: raw
signals: ["5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2965", "claude:f0bf048d#L3031"]
hook: "Lệnh update của pi tự nâng cấp vượt qua bản đã ghim"
tension: giup_ma_hai
sides: ["Lệnh update sinh ra để giữ công cụ mới", "Nó phá bản ghim, nên phải bỏ và tự viết status"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Không dùng pi update vì tự nâng cấp ngoài bản ghim

**Bối cảnh:** Công cụ pi và omp có lệnh update tự cập nhật.
**Chuyện gì xảy ra:** Lệnh update của pi và omp tự nâng cấp ra ngoài phiên bản đã ghim trong script. Thay vào đó, script có lệnh status so bản ghim với bản mới nhất, và tools cài đúng bản ghim, giữ bản cũ để quay lại trong vài giây.
**Bài học:** Tắt cơ chế tự cập nhật của công cụ agent; nâng cấp phải qua bản ghim có kiểm checksum.
