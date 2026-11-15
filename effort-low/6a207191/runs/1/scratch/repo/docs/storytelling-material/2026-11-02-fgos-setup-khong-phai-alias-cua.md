---
id: 2026-11-02-fgos-setup-khong-phai-alias-cua
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L720", "claude:6a207191#L727", "claude:6a207191#L732"]
hook: "Lệnh 'setup' tưởng chỉ là tên khác của doctor, hoá ra làm thêm 5 việc"
tension: tuong_ma_hoa_ra
sides: ["setup trông như alias của doctor --fix", "setup còn ghi rc, tạo config, cài hook và copy skills"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# fgos: 'setup' không phải alias của doctor, nên chuẩn hoá từ hiện trạng

**Bối cảnh:** User tin rằng init và setup chỉ là alias trỏ về doctor. Agent đọc code thực tế trước khi chuẩn hoá.
**Chuyện gì xảy ra:** Lệnh setup thực ra chạy các fix của doctor --fix, rồi làm thêm: ghi dòng source vào rc, tạo file config, cài git hook, cài Claude hook và copy skills. Lệnh fgctl init chạy ba bước nối tiếp. Chính code ghi nhận rằng doctor --fix không làm những việc kia. Thiết kế đích: doctor là máy duy nhất, init bằng doctor --fix cộng thêm quyền tạo mới, setup bỏ đi và chỉ giữ alias ẩn.
**Bài học:** Giả định về ý định có thể đúng, nhưng hiện trạng thường khác. Hãy đọc code trước khi viết quy chuẩn.
**Artefact:** Bảng lệnh và việc thực tế mà mỗi lệnh làm. Ẩn tên repo nếu cần.
