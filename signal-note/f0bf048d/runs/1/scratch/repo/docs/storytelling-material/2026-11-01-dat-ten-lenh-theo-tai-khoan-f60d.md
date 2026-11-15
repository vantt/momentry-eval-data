---
id: 2026-11-01-dat-ten-lenh-theo-tai-khoan-f60d
code: M-F603
aliases: [M-F603]
date: 2026-11-01
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2862", "claude:f0bf048d#L2870", "claude:f0bf048d#L2880", "claude:f0bf048d#L2885"]
hook: "Chủ nói tetnu là tài khoản, không phải nhà cung cấp"
tension: nguoi_dung_may_sai
sides: ["agent đặt tên theo nhà cung cấp", "chủ chỉ ra tetnu là tài khoản"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đặt tên lệnh theo tài khoản, không theo nhà cung cấp

**Bối cảnh:** Lệnh pi-openai-codex gắn tên nhà cung cấp, nhưng máy có nhiều tài khoản OpenAI và sau này sẽ thêm nữa.
**Chuyện gì xảy ra:** Chủ nói tetnu là tài khoản, không phải nhà cung cấp. Agent đổi tên sang dạng công cụ-nhà cung cấp-tài khoản, sửa profile, skill và tài liệu, rồi deploy lại skill. Thư mục đăng nhập giữ nguyên nên không phải login lại.
**Bài học:** Đặt tên theo đơn vị sẽ được nhân lên (tài khoản) để sau này khỏi trùng khi thêm.
**Artefact:** Bảng tên lệnh cũ và mới.
