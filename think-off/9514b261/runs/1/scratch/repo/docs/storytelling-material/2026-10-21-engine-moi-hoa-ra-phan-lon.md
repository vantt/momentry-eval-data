---
id: 2026-10-21-engine-moi-hoa-ra-phan-lon
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1511", "claude:9514b261#L1523", "claude:9514b261#L1572", "claude:9514b261#L1622"]
hook: "Tưởng phải xây engine mới, hoá ra 479 tài liệu đã chạy sẵn"
tension: tuong_ma_hoa_ra
sides: ["định xây engine tri thức mới từ đầu", "registry đã chạy với 479 tài liệu, chỉ thiếu sáu mảnh"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Engine mới hoá ra phần lớn đã có: Knowledge Registry phủ khoảng 15% tài liệu và đang chạy

**Bối cảnh:** Đề xuất có một Knowledge and Documentation Engine mới, nghi ngờ trùng với hệ thống đã có.
**Chuyện gì xảy ra:** Ba agent quét plans, history và work items song song. Registry có 479 tài liệu, khoảng 15% trong 3146 file .md, và chỉ phủ tài liệu người dùng cuối. Có 332 provisional và 147 active, cùng 365 role khác nhau trên 479 doc. Phần thật sự mới của engine chỉ là sáu thứ chưa có mã. Proposal được sửa thành điểm xuất phát chứ không phải xây mới.
**Bài học:** Trước khi thiết kế engine mới, đếm xem cái đang chạy phủ bao nhiêu phần; phần mới thường nhỏ hơn bản thiết kế.
**Artefact:** Bảng so sánh: phần có sẵn đang chạy và phần mới chưa có mã.
