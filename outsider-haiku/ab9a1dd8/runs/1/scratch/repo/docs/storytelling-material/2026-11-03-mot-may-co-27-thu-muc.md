---
id: 2026-11-03-mot-may-co-27-thu-muc
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, số trước/sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3434", "claude:ab9a1dd8#L3437", "claude:ab9a1dd8#L3450", "claude:ab9a1dd8#L3454", "claude:ab9a1dd8#L3574"]
hook: "Một máy, 27 thư mục profile: giả định một thư mục mặc định là sai"
tension: tuong_ma_hoa_ra
sides: ["mỗi công cụ một thư mục mặc định", "thực tế 27 thư mục profile"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một máy có 27 thư mục profile: quét nào cũng phải tìm đủ

**Bối cảnh:** Trên máy này user có nhiều tài khoản Codex, pi, omp và agy, mỗi tài khoản một thư mục home riêng.
**Chuyện gì xảy ra:** Thay vì giả định một thư mục mặc định, momentry liệt kê mọi profile: 4 thư mục Codex, 9 của pi, 10 của omp và 4 của agy, tổng 27. Hook và quét đều dùng chung hàm hostRoots.
**Bài học:** Với công cụ đọc dữ liệu của agent, hãy hỏi có bao nhiêu profile trước khi viết đường dẫn mặc định.
**Artefact:** Bảng host và số profile tìm được, không nêu tên profile.
