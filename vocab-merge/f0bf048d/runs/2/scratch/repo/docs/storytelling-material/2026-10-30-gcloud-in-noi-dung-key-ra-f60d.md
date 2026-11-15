---
id: 2026-10-30-gcloud-in-noi-dung-key-ra-f60d
code: M-Q9H3
aliases: [M-Q9H3]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L742", "claude:f0bf048d#L1566", "claude:f0bf048d#L1571"]
hook: "Lệnh tạo key in luôn key ra log, log thành chỗ chứa bí mật"
tension: giup_ma_hai
sides: ["Lệnh tạo key đúng yêu cầu", "Key lộ trong log phiên"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# gcloud in nội dung key ra terminal khi tạo key: phải coi log phiên là nhạy cảm

**Bối cảnh:** Tạo key service account cho GA4 và Search Console, rồi tạo key PageSpeed dùng chung.
**Chuyện gì xảy ra:** Lệnh gcloud in nội dung key ra output của phiên, nên log có bí mật. Đã cảnh báo người dùng không chia sẻ log. Key PageSpeed (chỉ dùng cho PSI và CrUX, không gắn billing) gọi thử được, điểm performance mobile là 0,31.
**Bài học:** Đọc output của lệnh tạo credential trước khi chạy trong phiên có log; dùng cờ không in hoặc ghi ra file.
**Artefact:** Không đăng (dữ liệu nhạy cảm).
