---
id: 2026-11-02-lead-tu-truot-push-merge-khi-40f9
code: M-2J38
aliases: [M-2J38]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L800", "claude:c4caee3c#L2796", "claude:c4caee3c#L2811", "claude:c4caee3c#L2819", "claude:c4caee3c#L2929"]
hook: "Lead push khi test đỏ, rồi chạy lại ba lần đều xanh"
tension: tuong_ma_hoa_ra
sides: ["Người điều phối tưởng đã kiểm kỹ", "Push trước khi kiểm, test đỏ do máy tải"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lead tự trượt: push merge khi test còn đỏ, và merge khi cây còn thay đổi chưa commit

**Bối cảnh:** Lead merge nhánh V13b rồi push ngay, dù gói có một test đỏ.
**Chuyện gì xảy ra:** Sau khi merge, một test đỏ nhưng lead đã push trước khi kiểm. Ba lần chạy lại đều xanh (459/459), nên nhiều khả năng là test tốc độ chạy khi máy tải nặng. Trước đó có lần pull --rebase và merge bị từ chối vì cây còn thay đổi chưa commit.
**Bài học:** Chạy test xong rồi mới push, kể cả khi merge trông nhỏ; và commit hoặc lưu trữ thay đổi trước khi merge.
**Artefact:** Thông báo lỗi git và số test trước và sau khi chạy lại.
