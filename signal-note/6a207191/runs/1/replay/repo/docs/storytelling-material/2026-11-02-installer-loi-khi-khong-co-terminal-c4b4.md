---
id: 2026-11-02-installer-loi-khi-khong-co-terminal-c4b4
code: M-6ADF
aliases: [M-6ADF]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L870", "claude:6a207191#L890"]
hook: "/dev/tty có đó nhưng không mở được, installer crash thay vì báo"
tension: nho_ma_to
sides: ["Script kiểm tra thấy /dev/tty tồn tại", "Không có terminal thật, ghi vào là crash"]
strength: 2
stakes: 2
hits: 1
runs: 1
unverified: [agent_only]
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ hướng dẫn đóng gói và cài đặt cho các công cụ dòng lệnh, đúc kết từ nhiều repo, và có một installer mẫu phải chạy được cả khi không có terminal. Người làm tin rằng chỉ cần kiểm tra /dev/tty có tồn tại và đọc/ghi được là đủ để biết có hỏi người dùng được không. Hoá ra khi không có terminal, thiết bị vẫn hiện diện nhưng không mở được, nên installer crash thay vì báo cần xác nhận. Ai viết script cài đặt chạy trong CI hay do agent gọi nên chú ý: phải thử mở thiết bị, đừng chỉ kiểm tra nó có đó."
audience: dev viết script cài đặt chạy trong CI hoặc do agent gọi
spine_context: "Dự án là bộ hướng dẫn đóng gói và cài đặt cho các công cụ dòng lệnh, đúc kết từ nhiều repo, có một installer mẫu."
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L701"]
spine_want: "Installer mẫu phải chạy được cả trong dash và khi không có terminal, ví dụ khi agent gọi."
spine_want_lines: ["claude:6a207191#L870"]
spine_obstacle: /dev/tty tồn tại nhưng không mở được khi không có terminal.
spine_obstacle_lines: ["claude:6a207191#L879"]
spine_turn: Tưởng kiểm tra /dev/tty có tồn tại và đọc/ghi được là đủ để biết có hỏi người dùng được không; hoá ra phải thử mở thiết bị mới biết.
spine_turn_lines: ["claude:6a207191#L879", "claude:6a207191#L880"]
spine_action: "Thay kiểm tra bằng cách thử mở /dev/tty thật; không có terminal thì báo cần --yes, có terminal thì hỏi và huỷ khi người dùng gõ n."
spine_action_lines: ["claude:6a207191#L879"]
spine_outcome: "Không có terminal, installer báo cần xác nhận thay vì crash; có terminal thì hỏi và huỷ đúng khi gõ n."
spine_outcome_lines: ["claude:6a207191#L880", "claude:6a207191#L890"]
spine_takeaway: Kiểm tra thiết bị tồn tại hay có quyền đọc/ghi chưa đủ; phải thử mở nó.
spine_takeaway_lines: ["claude:6a207191#L879"]
completeness: 7
---

# Installer lỗi khi không có terminal: /dev/tty tồn tại nhưng không mở được

**Góc kể:** Dự án là bộ hướng dẫn đóng gói và cài đặt cho các công cụ dòng lệnh, đúc kết từ nhiều repo, và có một installer mẫu phải chạy được cả khi không có terminal. Người làm tin rằng chỉ cần kiểm tra /dev/tty có tồn tại và đọc/ghi được là đủ để biết có hỏi người dùng được không. Hoá ra khi không có terminal, thiết bị vẫn hiện diện nhưng không mở được, nên installer crash thay vì báo cần xác nhận. Ai viết script cài đặt chạy trong CI hay do agent gọi nên chú ý: phải thử mở thiết bị, đừng chỉ kiểm tra nó có đó.
**Bối cảnh:** Installer mẫu phải chạy được trong dash và cả khi không có terminal, ví dụ khi agent gọi.
**Chuyện gì xảy ra:** Test bằng dash trên một release giả lập. Lỗi: /dev/tty tồn tại nhưng không ghi được khi không có terminal, nên script crash thay vì báo cần --yes. Sửa bằng cách thử mở /dev/tty thật. Sau sửa, không có terminal thì báo cần xác nhận; có terminal thì hỏi và huỷ khi người dùng gõ n.
**Bài học:** Kiểm tra thiết bị tồn tại chưa đủ. Phải thử mở nó mới biết dùng được hay không.
**Artefact:** Log hai đường chạy, có terminal và không có terminal. Cần che đường dẫn tạm.
