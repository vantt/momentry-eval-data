---
id: 2026-11-02-tu-dien-tu-ghep-bo-pyvi
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672"]
hook: "Bỏ từ điển GPL, học từ 20.523 cặp âm tiết, điểm vẫn tăng"
tension: giup_ma_hai
sides: ["Bỏ từ điển vì trùng nguồn GPL", "Từ điển tự học làm nDCG tăng từ 0,79 lên 0,86"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép: bỏ pyvi, học từ thống kê trên dữ liệu CC BY

**Bối cảnh:** Danh sách từ ghép ban đầu lấy từ một repo có giấy phép MIT nhưng không rõ nguồn gốc các mục.
**Chuyện gì xảy ra:** Tách từ đưa nDCG@5 của hạng mục tách từ tăng 0,909 lên 0,932. Khi kiểm nguồn, phần lớn danh sách trùng một từ điển GPL nên chủ dự án quyết định bỏ. Từ điển mới học từ 20.523 cặp âm tiết trên ba bộ dữ liệu CC BY, và trên bộ câu khó hơn nDCG tăng từ 0,79 lên 0,86.
**Bài học:** Giấy phép của repo chưa đủ để chứng minh nguồn của từng mục; hãy kiểm nguồn trước khi phát hành dữ liệu.
**Artefact:** So sánh tỷ lệ trùng với từ điển GPL và bảng nDCG theo bộ. Không cần che.
