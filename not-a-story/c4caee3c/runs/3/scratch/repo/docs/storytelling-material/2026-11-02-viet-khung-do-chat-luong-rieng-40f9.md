---
id: 2026-11-02-viet-khung-do-chat-luong-rieng-40f9
code: M-BB1F
aliases: [M-BB1F]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L3596", "claude:c4caee3c#L3615", "claude:c4caee3c#L3623", "claude:c4caee3c#L3633", "claude:c4caee3c#L3645", "claude:c4caee3c#L3809", "claude:c4caee3c#L3822"]
hook: "Đo chất lượng trên vault thật mà không đưa chữ nào ra repo"
tension: khac
sides: ["Muốn đo bằng dữ liệu cá nhân thật", "Không được để nội dung đó ra khỏi máy hay vào repo"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết khung đo chất lượng riêng cho từng người dùng (eval trên vault thật) mà không đưa nội dung cá nhân ra ngoài repo.

**Chuyện gì xảy ra:** Viết khung đo chất lượng riêng cho từng người dùng (eval trên vault thật) mà không đưa nội dung cá nhân ra ngoài repo.
**Góc người ngoài:** cách làm phổ biến là Người ta thường đưa dữ liệu thật vào repo hoặc CI để dễ chia sẻ, hoặc không đo gì cả; ở đây khác ở Golden set và chi tiết từng câu nằm trên máy người dùng, chỉ in số tổng hợp, và script từ chối ghi nếu đường dẫn nằm trong repo. Người đọc muốn có cách đo chất lượng trên dữ liệu thật mà vẫn giữ riêng tư.
