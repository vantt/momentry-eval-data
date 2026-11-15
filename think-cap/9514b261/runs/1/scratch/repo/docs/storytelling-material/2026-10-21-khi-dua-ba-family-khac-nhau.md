---
id: 2026-10-21-khi-dua-ba-family-khac-nhau
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1871", "claude:9514b261#L1876", "claude:9514b261#L2795", "claude:9514b261#L2805", "claude:9514b261#L2966"]
hook: "Mã có chế độ chia đều ghế, nhưng chỉ là ưu tiên mềm"
tension: tuong_ma_hoa_ra
sides: ["Tưởng chế độ spread bảo đảm mỗi ghế một family khác nhau", "Thật ra chỉ ưu tiên mềm, family hỏng là thiếu ghế"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi đưa ba family khác nhau vào mỗi ghế, mã có sẵn chỉ là ưu tiên mềm

**Bối cảnh:** Hội đồng cần các ghế đến từ family khác nhau để giảm thiên lệch chung của một model.
**Chuyện gì xảy ra:** Mã gán vai có chế độ spread, nhưng chỉ là ưu tiên mềm: family ít được dùng nhất được chọn trước. Khi một family hỏng, walk phải có dự phòng để đủ ghế. Mô phỏng sau cùng cho 11/11 ghế với bốn family.
**Bài học:** Ràng buộc đa dạng nguồn phải được kiểm bằng cách mô phỏng khi bớt từng family, không chỉ dựa vào tham số có sẵn.
**Artefact:** Bảng ghế với family và kết quả khi loại từng family.
