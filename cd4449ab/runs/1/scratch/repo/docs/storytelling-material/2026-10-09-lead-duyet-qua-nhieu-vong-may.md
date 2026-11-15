---
id: 2026-10-09-lead-duyet-qua-nhieu-vong-may
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L1364", "omp:cd4449ab#L1462", "omp:cd4449ab#L1713", "omp:cd4449ab#L2025", "omp:cd4449ab#L2123", "omp:cd4449ab#L2345", "omp:cd4449ab#L2352", "omp:cd4449ab#L2358", "omp:cd4449ab#L2363", "omp:cd4449ab#L2373", "omp:cd4449ab#L2374", "omp:cd4449ab#L3656"]
hook: "Agent code xong rồi tự dừng 3 lần chờ người merge"
tension: khac
sides: ["Máy làm nhanh, tự chạy được", "Mỗi checkpoint vẫn dừng để người duyệt và merge"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lead duyệt qua nhiều vòng: máy dừng ở mỗi checkpoint, người merge fast-forward

**Bối cảnh:** Quy trình duyệt của lead cho Phase 4, rồi Phase 3.
**Chuyện gì xảy ra:** Phase 4 qua ba vòng review: dry run fail, before/after diff, và claim sai. Mỗi vòng agent dừng sau commit, báo hash, và lead merge. Rebase 11 commit lên main mới cho 0 xung đột, tip mới là b01eaa3. Phase 3 được chia thành các checkpoint a, b, c.
**Bài học:** Dừng sau mỗi checkpoint và báo hash giúp người duyệt merge từng phần. Mỗi vòng cũng cho biết lỗi nằm ở đâu và đã đi bao xa.
**Artefact:** Sơ đồ chuỗi commit theo checkpoint, gồm hash và tiêu đề. Không chứa dữ liệu nội bộ.
**Góc người ngoài:** cách làm phổ biến là Dev dùng AI thường chỉ một phiên, một thư mục, một nhánh; hoặc nhiều phiên cùng sửa chung một checkout rồi tự gỡ xung đột; ở đây khác ở Worktree tách biệt cho phép 3-4 agent làm song song mà không giẫm file nhau. Guard pre-commit và điểm dừng cho người merge giúp người dùng vẫn nắm quyền kiểm soát. Dev một mình muốn nhân năng suất sẽ hỏi cách dựng quy trình này.
