---
id: 2026-10-30-dung-goi-cai-dat-co-ghim-f60d
code: M-ATKN
aliases: [M-ATKN]
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L698", "claude:f0bf048d#L711", "claude:f0bf048d#L1647", "claude:f0bf048d#L1651", "claude:f0bf048d#L2738", "claude:f0bf048d#L2745", "claude:f0bf048d#L3002", "claude:f0bf048d#L3013"]
hook: "Cài công cụ: ghim phiên bản, bản đủ hai tuần, kiểm checksum"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng gói cài đặt có ghim phiên bản, kiểm bản phát hành đã có ít nhất hai tuần, và kiểm checksum trước khi cài công cụ trên máy (gcloud, uv, omp, MCP server).

**Chuyện gì xảy ra:** Dùng gói cài đặt có ghim phiên bản, kiểm bản phát hành đã có ít nhất hai tuần, và kiểm checksum trước khi cài công cụ trên máy (gcloud, uv, omp, MCP server).
**Góc người ngoài:** cách làm phổ biến là Thường người ta chạy lệnh curl | bash hoặc cài bản mới nhất, không kiểm checksum hay tuổi bản phát hành; ở đây khác ở Mỗi công cụ được đối chiếu md5/sha256 với metadata chính thức và chỉ dùng bản đã phát hành đủ lâu. Người đọc muốn biết cách làm này để tránh cài nhầm bản lỗi hoặc bị thay thế trên đường tải.
