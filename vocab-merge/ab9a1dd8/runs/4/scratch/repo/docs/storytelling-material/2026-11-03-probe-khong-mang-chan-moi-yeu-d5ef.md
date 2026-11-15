---
id: 2026-11-03-probe-khong-mang-chan-moi-yeu-d5ef
code: M-PQ9S
aliases: [M-PQ9S]
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3932"]
hook: "Khoá giả vẫn bị báo sai: công cụ lén gọi mạng"
tension: tuong_ma_hoa_ra
sides: ["tưởng probe chạy offline với khoá giả", "lỗi 'Incorrect API key' chứng tỏ nó vẫn gọi mạng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe không mạng: chặn mọi yêu cầu bằng namespace mạng rỗng

**Bối cảnh:** Agent cần chạy thử các CLI bên thứ ba (pi, omp, agy) để đo hook, nhưng không muốn lệnh nào gửi yêu cầu ra ngoài.
**Chuyện gì xảy ra:** Lần đầu omp in lỗi 'Incorrect API key' với khoá giả, cho thấy nó vẫn gọi mạng. Agent chuyển sang chạy trong namespace mạng rỗng bằng unshare, rồi chạy probe agy trong đó.
**Bài học:** Khi thử công cụ bên thứ ba bằng khoá giả, hãy chặn mạng ở tầng hệ điều hành, đừng tin vào cấu hình của công cụ.
**Artefact:** Dòng lệnh unshare và đầu ra lỗi đã che khoá.
