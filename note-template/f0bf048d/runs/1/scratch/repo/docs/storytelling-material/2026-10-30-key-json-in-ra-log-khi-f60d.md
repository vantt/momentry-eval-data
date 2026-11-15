---
id: 2026-10-30-key-json-in-ra-log-khi-f60d
code: M-2EBE
aliases: [M-2EBE]
date: 2026-10-30
repo: repo
status: raw
signals: [khac]
signal_note: "Rò rỉ nhỏ trong log, nhưng đáng kể vì log thường được chia sẻ hoặc lưu lại."
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L742", "claude:f0bf048d#L1654"]
hook: "Tạo key bằng gcloud là key nằm luôn trong log phiên"
tension: nho_ma_to
sides: ["Một lệnh tạo key rất bình thường", "Nội dung key bị in ra và nằm trong log"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Key JSON in ra log khi tạo bằng gcloud

**Bối cảnh:** Tạo key cho service account bằng gcloud trong phiên làm việc.
**Chuyện gì xảy ra:** Lệnh tạo key in nội dung key ra terminal, nên nội dung key nằm trong log của phiên. Agent đã cảnh báo chủ không chia sẻ log. Key được chuyển vào thư mục tạm có quyền 600 và sau đó được đưa sang nơi lưu cố định.
**Bài học:** Khi tạo secret bằng CLI, kiểm xem công cụ có in nội dung ra stdout không, rồi redirect hoặc dùng cờ ghi thẳng vào file.
**Artefact:** Không chụp. Chỉ mô tả cơ chế.
