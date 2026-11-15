---
id: 2026-11-03-quet-lich-su-git-tim-khoa
date: 2026-11-03
repo: repo
status: raw
signals: [người duyệt, ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3829", "claude:2dfb5915#L3835", "claude:2dfb5915#L3847"]
hook: "Quét khoá trước khi mở repo public, chỉ có grep và kết quả 0"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quét lịch sử git tìm khoá trước khi chuyển repo sang public

**Bối cảnh:** Repo sắp chuyển public, nên lịch sử git có thể lộ bí mật.
**Chuyện gì xảy ra:** Agent tìm các mẫu token GitHub, khoá Anthropic, khoá AWS và private key trong toàn bộ lịch sử. Lệnh đầu bị từ chối quyền đọc một tệp; lệnh thứ hai dùng mẫu chính xác và cho kết quả 0. Không có gitleaks trên máy, nên chỉ quét bằng grep.
**Bài học:** Quét bí mật trước khi đổi visibility; ghi rõ công cụ và mẫu đã dùng để người khác biết giới hạn của lần quét.
**Artefact:** Không có.
