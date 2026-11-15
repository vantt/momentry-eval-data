---
id: 2026-10-21-he-thong-can-xay-moi-hoa
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định, người duyệt, số trước sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L542", "claude:9514b261#L1325", "claude:9514b261#L1417", "claude:9514b261#L1457", "claude:9514b261#L1523", "claude:9514b261#L1572"]
hook: "Tưởng phải xây mới, hóa ra 479 tài liệu đã chạy thật"
tension: tuong_ma_hoa_ra
sides: ["Đề xuất coi hệ thống là còn thiếu", "Registry đã chạy thật với 479 tài liệu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hệ thống 'cần xây mới' hoá ra đã chạy một nửa

**Bối cảnh:** Đề xuất kiến trúc mô tả một engine tài liệu mới. Câu hỏi đặt ra là phần nào đã có sẵn.
**Chuyện gì xảy ra:** Ba agent nghiên cứu song song các mảng plans và reports, history, work items và mã. Registry tài liệu end-user đang chạy thật: 479 doc, khoảng 15% trong 3146 file md, trong đó 332 provisional và 147 active. Một work item quyết định đã xong đúng ở phần đề xuất coi là còn thiếu. Kết luận: engine mới chỉ là bước hoàn thiện, còn ba nhóm chưa có mã.
**Bài học:** Trước khi thiết kế component mới, quét work item đã xong và báo cáo cũ. Chữ 'chưa có' thường nghĩa là 'chưa tìm thấy'.
**Artefact:** Bảng: component đề xuất | đã có | chưa có. Không ghi tên note.
