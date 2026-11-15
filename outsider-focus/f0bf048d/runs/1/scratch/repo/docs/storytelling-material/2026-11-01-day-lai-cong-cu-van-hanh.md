---
id: 2026-11-01-day-lai-cong-cu-van-hanh
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2813", "claude:f0bf048d#L2827", "claude:f0bf048d#L2846", "claude:f0bf048d#L2948", "claude:f0bf048d#L3022", "claude:f0bf048d#L3027", "claude:f0bf048d#L3292", "claude:f0bf048d#L3294"]
hook: "Làm tay một lần, rồi ép cả hệ thống học lại cho plan ra 0"
tension: khac
sides: ["Làm tay cho nhanh rồi ghi wiki", "Ghi vào skill, deploy lại, plan phải ra 0 thay đổi"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dạy lại công cụ vận hành: mọi bước làm tay đều được ghi vào skill của agent System Operator rồi deploy lại, và plan phải ra 0 thay đổi sau khi deploy

**Chuyện gì xảy ra:** Dạy lại công cụ vận hành: mọi bước làm tay đều được ghi vào skill của agent System Operator rồi deploy lại, và plan phải ra 0 thay đổi sau khi deploy
**Góc người ngoài:** cách làm phổ biến là Làm tay rồi ghi vào wiki hoặc quên; tài liệu và hệ thống lệch nhau; ở đây khác ở Skill vừa là tài liệu vừa là thứ agent chạy, kèm quy tắc đặt thành memory để các phiên sau giữ. Người đọc muốn có vòng 'làm một lần, agent tự làm lần sau' và kiểm bằng plan idempotent.
