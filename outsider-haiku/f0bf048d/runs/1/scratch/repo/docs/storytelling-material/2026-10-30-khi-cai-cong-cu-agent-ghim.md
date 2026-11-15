---
id: 2026-10-30-khi-cai-cong-cu-agent-ghim
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L698", "claude:f0bf048d#L701", "claude:f0bf048d#L702", "claude:f0bf048d#L709", "claude:f0bf048d#L1288", "claude:f0bf048d#L1296", "claude:f0bf048d#L2975"]
hook: "Cài bản mới nhất thì tiện, ghim bản 14 ngày tuổi mới an toàn"
tension: tuong_ma_hoa_ra
sides: ["bản mới nhất là bản tốt nhất", "bản chưa qua 14 ngày chưa ai kiểm, nên phải ghim và đối chiếu checksum"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi cài công cụ, agent ghim phiên bản đã phát hành ít nhất 14 ngày, và đối chiếu checksum (md5 hoặc sha256) với metadata chính thức trước khi dùng. Với công cụ bên thứ ba, nó đọc mã nguồn hoặc kiểm tra trên thư mục nháp trước khi đưa vào hệ thống.

**Chuyện gì xảy ra:** Khi cài công cụ, agent ghim phiên bản đã phát hành ít nhất 14 ngày, và đối chiếu checksum (md5 hoặc sha256) với metadata chính thức trước khi dùng. Với công cụ bên thứ ba, nó đọc mã nguồn hoặc kiểm tra trên thư mục nháp trước khi đưa vào hệ thống.
**Góc người ngoài:** cách làm phổ biến là Cài bản mới nhất bằng lệnh install, không kiểm checksum, và không ghim phiên bản; ở đây khác ở Đây là một chuỗi kiểm tra chuỗi cung ứng thực hiện tự động, chạy trước khi cài lên máy chạy agent. Người đọc muốn biết cách làm vì sao chuyện 'cài nhầm bản vừa phát hành có lỗi' được chặn từ đầu.
