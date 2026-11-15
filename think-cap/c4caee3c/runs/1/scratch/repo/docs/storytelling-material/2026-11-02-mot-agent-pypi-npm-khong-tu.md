---
id: 2026-11-02-mot-agent-pypi-npm-khong-tu
date: 2026-11-02
repo: repo
status: raw
signals: ["Số trước, số sau", Nguyên nhân bất ngờ, Ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3288", "claude:c4caee3c#L3312", "claude:c4caee3c#L3349", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "CI đỏ vì 0,728 so với 0,735: khác CPU, không phải khác code"
tension: tuong_ma_hoa_ra
sides: ["Tụt 0,007 điểm trông như lỗi code", "Baseline ghi trên máy dev khác loại CPU với runner"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một agent PyPI/npm không tự nhận 'xong': cổng chất lượng đỏ vì baseline ghi trên máy khác CPU

**Bối cảnh:** Dự án fork một search engine (OHS) có gói tiếng Việt, mỗi bản phát hành chạy cổng chất lượng trên CI. Cổng so điểm eval với baseline đã ghi trên một máy khác.
**Chuyện gì xảy ra:** CI báo QUALITY_FAILED ở đúng một mục: nDCG@5 eval tiếng Anh không có gói đo được 0,728 trên runner GitHub, nhưng baseline ghi trên máy dev là 0,735, vượt ngưỡng 0,005. Nguyên nhân: ONNX lượng tử cho số hơi khác theo loại CPU (AMD EPYC khác các loại khác). Cùng lỗi kiểu này cũng làm bước kiểm mức lệch của gói Mac Intel hỏng ở vài lần chạy. Sửa bằng cách so với upstream đo ngay trong cùng lần chạy, baseline ghi chỉ còn dùng báo trôi; CI xanh ở run 41410567165.
**Bài học:** Đừng so điểm đo trên máy này với điểm đo trên máy khác khi mô hình lượng tử phụ thuộc CPU; đo đối chứng trong cùng một lần chạy.
**Artefact:** Bảng hai mục ndcg_5 (0.735 baseline vs 0.728 runner) trong báo cáo catchup; che nội dung câu hỏi nếu có.
