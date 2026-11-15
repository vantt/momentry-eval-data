---
id: 2026-10-31-moi-thao-tac-tay-phai-duoc-f60d
code: M-E6XC
aliases: [M-E6XC]
date: 2026-10-31
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguoi_duyet_may_soan]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1659", "claude:f0bf048d#L2955", "claude:f0bf048d#L3204", "claude:f0bf048d#L3243", "claude:f0bf048d#L3292", "claude:f0bf048d#L3441"]
hook: "Mọi bước làm tay đều phải dạy lại cho System Operator"
tension: it_ma_nhieu
sides: ["Một lệnh root chạy đúng một lần", "Các lần cài sau không cần sudo nữa"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi thao tác tay phải được dạy lại cho System Operator

**Bối cảnh:** System Operator là agent vận hành chạy trên máy. Mỗi việc làm tay trên máy đều có nguy cơ không được ghi lại.
**Chuyện gì xảy ra:** Chủ yêu cầu System Operator tự cài và nâng cấp pi và omp. Sau đó lệnh root chỉ cần chạy một lần để cấp quyền ghi cho thư mục runtime, và các lần cài sau không cần sudo. Khi daemon ops đang tắt, agent đề xuất bật lại, nhưng chủ yêu cầu liệt kê các bước còn lại trước. Chủ yêu cầu rõ mọi bước làm tay đều phải dạy lại cho System Operator, nên agent ghi vào memory và viết tài liệu quy trình riêng.
**Bài học:** Sau mỗi thao tác tay trên máy, cập nhật đúng skill của agent vận hành rồi deploy lại. Nếu không, lần sau nó không biết cách làm.
**Artefact:** Trích một đoạn skill đã cập nhật, che đường dẫn và tên người.
