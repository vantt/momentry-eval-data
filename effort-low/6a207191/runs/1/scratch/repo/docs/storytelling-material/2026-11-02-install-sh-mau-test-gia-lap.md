---
id: 2026-11-02-install-sh-mau-test-gia-lap
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L293", "claude:6a207191#L296", "claude:6a207191#L298", "claude:6a207191#L299", "claude:6a207191#L861", "claude:6a207191#L871", "claude:6a207191#L878", "claude:6a207191#L880"]
hook: "Đọc code không thấy, test giả lập tìm ra 2 lỗi"
tension: tuong_ma_hoa_ra
sides: ["Script trông đúng khi đọc code", "Chạy thử không có terminal thì script crash"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# install.sh mẫu: test giả lập lộ 2 lỗi mà đọc code không thấy

**Bối cảnh:** Viết installer POSIX mẫu rồi test với một bản release giả lập qua file://.
**Chuyện gì xảy ra:** Lần test đầu, lệnh uninstall bị chặn bởi kiểm tra 'unstamped version' dù uninstall không cần version, nên agent di chuyển kiểm tra đó. Lần test thứ hai chạy bằng dash để chắc là POSIX thật. Khi không có terminal, /dev/tty vẫn tồn tại nhưng không mở được, và script crash thay vì yêu cầu thêm --yes. Sửa bằng cách thử mở /dev/tty thật, rồi kiểm lại cả hai trường hợp.
**Bài học:** Kiểm tra [ -r /dev/tty ] không chứng minh có terminal. Chỉ thử mở thật mới biết. Hãy test installer bằng dash, không chỉ bash.
**Artefact:** Terminal output hai lỗi trước và sau khi sửa.
