---
id: 2026-11-02-kiem-tra-installer-shell-bang-cach-c4b4
code: M-FCHC
aliases: [M-FCHC]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L871", "claude:6a207191#L878", "claude:6a207191#L879", "claude:6a207191#L880"]
hook: "Shellcheck sạch chưa đủ: chạy installer bằng dash mới biết"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm tra installer shell bằng cách chạy bằng dash để chắc đó là POSIX thật, dựng một bản release giả qua file:// rồi thử cài, cài lại, gỡ cài và checksum sai. Mọi thứ đều chạy trong thư mục tạm.

**Chuyện gì xảy ra:** Kiểm tra installer shell bằng cách chạy bằng dash để chắc đó là POSIX thật, dựng một bản release giả qua file:// rồi thử cài, cài lại, gỡ cài và checksum sai. Mọi thứ đều chạy trong thư mục tạm.
**Góc người ngoài:** cách làm phổ biến là Chỉ chạy shellcheck hoặc đọc lại bằng mắt, ít khi thử trên shell tối giản như dash hay trên một bản cài cục bộ không cần mạng; ở đây khác ở Cách này bắt được lỗi thật mà đọc mắt bỏ sót, ví dụ việc kiểm tra terminal thất bại khi không có tty. Người đọc muốn biết cách dựng môi trường thử an toàn, không đụng máy thật.
