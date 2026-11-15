---
id: 2026-10-30-mot-lenh-root-de-system-operator-f60d
code: M-HTFG
aliases: [M-HTFG]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L478", "claude:f0bf048d#L480", "claude:f0bf048d#L482", "claude:f0bf048d#L1659", "claude:f0bf048d#L2955", "claude:f0bf048d#L2965", "claude:f0bf048d#L2970", "claude:f0bf048d#L3031", "claude:f0bf048d#L3040", "claude:f0bf048d#L3043", "claude:f0bf048d#L3053"]
hook: "Chạy đúng một lệnh root, agent tự cài công cụ không cần sudo nữa"
tension: it_ma_nhieu
sides: ["chủ chạy đúng một lệnh root", "agent tự cài công cụ mãi về sau"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một lệnh root để System Operator tự cài pi/omp không cần sudo

**Bối cảnh:** Máy không có sudo không cần mật khẩu. System Operator cần cài và nâng cấp pi và omp mà không gọi sudo.
**Chuyện gì xảy ra:** Agent kiểm sudo, thấy yêu cầu mật khẩu nên phải đưa lệnh cho chủ chạy. Thay vì phụ thuộc sudo mỗi lần, agent viết stack/tools-owner.sh để chủ chạy đúng một lần: giao /opt/opc-agent/bin và lib cho user vantt. Sau đó agent chạy pi-runtime.sh tools không cần sudo, ba lệnh bọc trỏ tới thư mục theo phiên bản. Bản cũ được giữ để quay lại.
**Bài học:** Đổi một lệnh root lấy nhiều thao tác không cần root, và kiểm lại quyền sau khi đổi.
**Artefact:** Kết quả ls -ld quyền thư mục trước và sau khi chạy.
