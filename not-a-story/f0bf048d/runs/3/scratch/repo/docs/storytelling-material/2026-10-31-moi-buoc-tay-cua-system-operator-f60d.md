---
id: 2026-10-31-moi-buoc-tay-cua-system-operator-f60d
code: M-2CS8
aliases: [M-2CS8]
date: 2026-10-31
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1759", "claude:f0bf048d#L3204", "claude:f0bf048d#L3221", "claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3305", "claude:f0bf048d#L3370", "claude:f0bf048d#L3382", "claude:f0bf048d#L3410", "claude:f0bf048d#L3441"]
hook: "Gặp ba lỗi khi tách user, mỗi bước đều chép lại vào skill"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi bước tay của System Operator phải dạy lại vào skill

**Bối cảnh:** Daemon ops đã tắt từ giai đoạn 0. Người vận hành yêu cầu mọi bước làm bằng tay cũng phải dạy lại cho System Operator.
**Chuyện gì xảy ra:** Agent lưu quy tắc vào memory, viết kế hoạch tách System Operator khỏi user vantt thành 7 bước. Khi làm bước 2.1 và 2.2, agent gặp lỗi kiểm tra user opc-ops chưa tồn tại, syntax check báo lỗi dù đã ok, và kiểm vai trò qua CLI thất bại. Mỗi bước đều có phần dạy lại trong skill, gồm tài liệu về opc-priv và các lệnh sudo phải soạn sẵn cho chủ chạy.
**Bài học:** Nếu agent vận hành có quyền riêng, mọi thao tác tay phải được đưa vào skill của nó, nếu không lần sau nó sẽ không biết làm.
**Artefact:** Bảng 7 bước của kế hoạch tách user, đã che tên user.
