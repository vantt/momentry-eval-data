---
id: 2026-11-01-cai-pi-va-omp-bang-script-f60d
code: M-5D6Y
aliases: [M-5D6Y]
date: 2026-11-01
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2965", "claude:f0bf048d#L2968", "claude:f0bf048d#L3007", "claude:f0bf048d#L3011", "claude:f0bf048d#L3031", "claude:f0bf048d#L3053"]
hook: "Nâng omp lên 18.14.2 rồi quay về 18.12.6 chỉ mất vài giây"
tension: it_ma_nhieu
sides: ["ghim phiên bản, mỗi bản một thư mục", "nâng cấp hay lùi đều trong vài giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một đội chạy các runtime AI (pi và omp) cho hệ thống agent multica trên máy chủ, mỗi tài khoản đã đăng nhập."
spine_context_lines: ["claude:f0bf048d#L2890", "claude:f0bf048d#L2955"]
spine_want: Cho System Operator tự cài và nâng cấp pi/omp mà không cần sudo.
spine_want_lines: ["claude:f0bf048d#L2955"]
spine_obstacle: Ghi vào thư mục cài đặt chung cần sudo.
spine_obstacle_lines: ["claude:f0bf048d#L3031"]
spine_action: "Thêm lệnh status và tools vào script ghim phiên bản, deploy skill, chạy tools-owner.sh một lần, rồi chạy lại tools."
spine_action_lines: ["claude:f0bf048d#L3001", "claude:f0bf048d#L3043"]
spine_outcome: Lệnh --version của pi đúng bản ghim; runtime Pi đã online với pi 1.4.0 trong kết quả kiểm tra.
spine_outcome_lines: ["claude:f0bf048d#L3052"]
completeness: 5
---

# Cài pi và omp bằng script ghim phiên bản, kiểm checksum, cho System Operator tự nâng cấp

**Bối cảnh:** Runtime cần pi và omp cài dưới user daemon, agent không có sudo.
**Chuyện gì xảy ra:** Script ghim phiên bản: pi cài từ npm, omp tải từ release và kiểm SHA256 khớp checksum chính thức (18.12.6). Mỗi phiên bản nằm trong thư mục riêng nên quay về bản cũ chỉ mất vài giây. Agent thử nâng omp lên 18.14.2 rồi quay lại 18.12.6, cả hai đều chạy đúng. Không dùng 'pi update' hay 'omp update' vì chúng tự nâng cấp ngoài bản ghim.
**Bài học:** Đừng dùng cơ chế update tích hợp của công cụ khi bạn cần kiểm soát phiên bản. Ghim phiên bản và tự cài, có đường quay lại.
**Artefact:** Kết quả lệnh status (không có secret).
