---
id: 2026-11-02-dry-run-release-bang-workflow-dispatch
date: 2026-11-02
repo: repo
status: raw
signals: [artefact, quy trình]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L251", "claude:2dfb5915#L2098", "claude:2dfb5915#L2536", "claude:2dfb5915#L3550"]
hook: "Dry-run qua cả 3 bản rc, vẫn trượt vì máy macOS chờ quá 15 phút"
tension: tuong_ma_hoa_ra
sides: ["Dry-run xanh, mọi sha256 đúng", "Job macOS bị huỷ vì chờ máy runner"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dry-run release bằng workflow_dispatch trước khi gắn tag

**Bối cảnh:** Release workflow có bước kiểm sha256 và build bốn nền tảng.
**Chuyện gì xảy ra:** Trước khi tag, dry-run ra 4 binary, install.ps1, install.sh và checksums; mọi sha256 đúng, không tạo Release. Sau rc.1, rc.2, rc.3 đều tải về kiểm 6 file trong checksums. Lỗi thật: job macOS bị GitHub huỷ vì chờ máy runner quá 15 phút; chạy lại đúng job lỗi thì qua.
**Bài học:** Dry-run trước khi tag; job bị huỷ vì runner không phải lỗi code, chỉ cần chạy lại đúng job.
**Artefact:** Bảng 7 file và kết quả sha256, che đường dẫn.
