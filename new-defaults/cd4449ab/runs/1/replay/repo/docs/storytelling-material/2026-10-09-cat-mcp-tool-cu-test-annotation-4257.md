---
id: 2026-10-09-cat-mcp-tool-cu-test-annotation-4257
code: M-6XRQ
aliases: [M-6XRQ]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3433", "omp:cd4449ab#L3457", "omp:cd4449ab#L3490", "omp:cd4449ab#L3493", "omp:cd4449ab#L3502", "omp:cd4449ab#L3505", "omp:cd4449ab#L3520", "omp:cd4449ab#L3553", "omp:cd4449ab#L3622", "omp:cd4449ab#L3672", "omp:cd4449ab#L3683", "omp:cd4449ab#L3695", "omp:cd4449ab#L3701", "omp:cd4449ab#L3708", "omp:cd4449ab#L3710"]
hook: "Xoá 17 tool cũ, mỗi lần xoá lại có test báo thiếu hoặc thừa"
tension: giup_ma_hai
sides: ["Dọn bớt 17 tool để gọn hơn", "Mỗi lần xoá, test contract và web-check đỏ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cắt MCP tool cũ: test annotation và web-check đòi khớp contract

**Bối cảnh:** Contract table định nghĩa các tool MCP và route web được giữ. Test annotation và boundary đếm từng tool.
**Chuyện gì xảy ra:** Bỏ 17 tool cũ như inbox_list, insight_* và curation_run_*, đồng thời thêm source_list. Mỗi lần xoá, test expectedToolAnnotations hoặc boundary báo tool thiếu hoặc thừa. make web-check cũng fail khi route insights và runs bị xoá, nên phải viết lại routes_distill. Agent phải đọc lại skill_update_preview và routing_evaluate ở origin/main để giữ annotation đúng.
**Bài học:** Viết contract tool thành test liệt kê danh sách. Khi bỏ tool, test sẽ chỉ ra ngay tool nào còn thiếu annotation.
**Artefact:** Bảng tool trước và sau (tên tool, có hoặc không). Đây là artefact tốt để chụp.
