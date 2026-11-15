---
id: 2026-11-05-5-test-go-chi-hong-tren-c4b4
code: M-91Q7
aliases: [M-91Q7]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2063", "claude:6a207191#L2073", "claude:6a207191#L2129", "claude:6a207191#L2152", "claude:6a207191#L2221", "claude:6a207191#L2246"]
hook: "5 test chỉ đỏ trên máy tôi, CI thì xanh"
tension: tuong_ma_hoa_ra
sides: ["CI pass, test tưởng ổn", "Máy làm việc có sẵn 2 file config ở thư mục cha làm test hỏng"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 5 test Go chỉ hỏng trên máy làm việc: test đổi HOME nhưng không đổi thư mục làm việc

**Bối cảnh:** make check chạy toàn bộ test Go. Năm test về doctor và status fail trên máy làm việc nhưng pass trên CI.
**Chuyện gì xảy ra:** Các test đổi HOME sang thư mục tạm nhưng không đổi cwd, nên status và doctor đi ngược lên thư mục cha và gặp ~/.codex/config.toml cùng ~/.gemini/settings.json. Hai file này vừa được ghi bởi lệnh connect --global vài phút trước. Code coi thư mục home là một dự án, so đường dẫn binary đã đăng ký với binary test, thấy khác nhau và báo Connection files FAILED. CI không có hai file này nên pass.
**Bài học:** Test cách ly phải đổi cả thư mục làm việc và chặn việc đi ngược cây thư mục; nếu không, cấu hình thật trên máy dev sẽ lọt vào test.
**Artefact:** Bảng 5 test với kỳ vọng và lý do fail (L2221). Không cần che.
