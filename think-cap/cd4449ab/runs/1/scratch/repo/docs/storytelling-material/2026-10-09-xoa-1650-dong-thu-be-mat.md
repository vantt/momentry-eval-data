---
id: 2026-10-09-xoa-1650-dong-thu-be-mat
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3433", "omp:cd4449ab#L3473", "omp:cd4449ab#L3485", "omp:cd4449ab#L3487", "omp:cd4449ab#L3499", "omp:cd4449ab#L3553", "omp:cd4449ab#L3622", "omp:cd4449ab#L3672", "omp:cd4449ab#L3680", "omp:cd4449ab#L3683", "omp:cd4449ab#L3689", "omp:cd4449ab#L3695", "omp:cd4449ab#L3701", "omp:cd4449ab#L3956", "omp:cd4449ab#L3957"]
hook: "Xoá 1650 dòng, 17 tool biến mất, test vẫn đỏ nhiều lượt"
tension: giup_ma_hai
sides: ["Dọn gọn bề mặt, bỏ 17 tool cũ", "Test contract đỏ nhiều lượt, phải sửa cả test"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá 1650 dòng: thu bề mặt MCP/web về bảng contract

**Bối cảnh:** Đưa bề mặt MCP và web về bảng contract của model distill tối giản.
**Chuyện gì xảy ra:** Commit đổi 19 file, +350 và -1650 dòng; commit message ghi 17 tool legacy bị bỏ. Riêng curation_tools.go mất 113 dòng. Sau đó make web-check vẫn thoát 2 và các test contract MCP đỏ nhiều lượt, agent sửa cả test expectedToolAnnotations để khớp bề mặt mới.
**Bài học:** Khi cắt bề mặt, test contract là danh sách việc; phải phân biệt sửa code cho đúng contract với sửa test cho khớp code.
**Artefact:** git diff --stat của commit, không cần nội dung tool.
