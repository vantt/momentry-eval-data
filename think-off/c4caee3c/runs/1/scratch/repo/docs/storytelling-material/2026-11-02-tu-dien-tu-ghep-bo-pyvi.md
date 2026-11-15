---
id: 2026-11-02-tu-dien-tu-ghep-bo-pyvi
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Từ điển trùng 95% với nguồn GPL, phải học lại từ đầu bằng dữ liệu CC BY"
tension: tuong_ma_hoa_ra
sides: ["Tưởng pyvi là nguồn dùng tự do", "95% danh sách trùng nguồn GPL, nên phải thay hẳn"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép: bỏ pyvi vì trùng 95% với nguồn GPL, học lại từ dữ liệu CC BY

**Bối cảnh:** Gói tiếng Việt cần từ điển ghép để tách từ. Danh sách ban đầu lấy từ pyvi, có giấy phép MIT nhưng không ghi nguồn gốc.
**Chuyện gì xảy ra:** Phân tích cho thấy 95% danh sách pyvi trùng với Viet74K (GPL), nên người duyệt yêu cầu thay nguồn. Agent học 20.523 từ ghép từ thống kê cặp âm tiết trên ba bộ dữ liệu CC BY 4.0, rồi kiểm chứng script dựng lại cho ra file giống hệt từng byte. Với segment bật mặc định, nDCG@5 tổng tăng từ 0,909 lên 0,932; vi-compound khó hơn tăng từ 0,632 lên 0,983.
**Bài học:** Với dữ liệu sinh ra từ nguồn không rõ, ghi rõ nguồn và chứng minh giấy phép trước khi đưa vào sản phẩm.
**Artefact:** Bảng so sánh số từ, giấy phép và điểm vi-compound. Không ghi tên văn bản pháp luật hay nội dung mẫu.
