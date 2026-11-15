---
id: 2026-11-02-hai-tinh-nang-ranh-gioi-duoc
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L819", "claude:2dfb5915#L1045", "claude:2dfb5915#L1957", "claude:2dfb5915#L2056", "claude:2dfb5915#L2057", "claude:2dfb5915#L2063"]
hook: "Bản mới sửa lỗi của bản gốc rồi quên ghi, hoặc chép nguyên lỗi"
tension: khac
sides: ["sửa lỗi bản gốc nhưng không ghi lại", "sao chép cả lỗi vì sợ khác hành vi"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai tính năng ranh giới được ghi thẳng vào `docs/DECISIONS.md` và `spec/PORTING.md` thành 'lệch có chủ ý so với Python': ngân sách bộ nhớ cho YAML độc hại, giới hạn độ sâu và thời gian cho truy vấn đường đi, khoá file khi hai lần build chạy cùng lúc. Mỗi mục có tên ngoại lệ và bộ so khớp liệt kê ngoại lệ chưa dùng.

**Chuyện gì xảy ra:** Hai tính năng ranh giới được ghi thẳng vào `docs/DECISIONS.md` và `spec/PORTING.md` thành 'lệch có chủ ý so với Python': ngân sách bộ nhớ cho YAML độc hại, giới hạn độ sâu và thời gian cho truy vấn đường đi, khoá file khi hai lần build chạy cùng lúc. Mỗi mục có tên ngoại lệ và bộ so khớp liệt kê ngoại lệ chưa dùng.
**Góc người ngoài:** cách làm phổ biến là Người ta sửa lỗi của bản gốc trong bản mới rồi quên ghi lại, hoặc sao chép nguyên cả lỗi vì sợ khác hành vi; ở đây khác ở Khi coi bản gốc là đặc tả mà vẫn muốn sửa lỗi an toàn, cần một sổ ghi và cơ chế cho phép lệch có tên. Nhờ đó bộ so khớp không bị nới lỏng chung chung, và người đọc sau này biết lệch nào cố ý.
