---
id: 2026-11-02-fgos-co-ba-lenh-init-setup
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định, ràng buộc định hình thiết kế]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L727", "claude:6a207191#L897"]
hook: "Ba lệnh init, setup, doctor chồng nhau: gộp lại còn một, bớt 18 rule"
tension: hop_ma_tan
sides: ["ba lệnh cùng làm một việc", "gộp thành doctor, 230 rule còn 212"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# fgos có ba lệnh init/setup/doctor chồng nhau; chốt doctor là máy duy nhất

**Bối cảnh:** fgos là hệ lớn, phân phối qua bộ cài fgctl chứ không phải một binary. Người dùng nghĩ init và setup chỉ là alias của doctor, nên agent đọc code để kiểm chứng.
**Chuyện gì xảy ra:** Thực tế: fgctl init gọi fgos init, rồi doctor --fix, rồi doctor. Lệnh setup cũ gọi cùng các fix của doctor nhưng thêm việc ghi dòng source vào rc, tạo file config, cài git hook và Claude hook, copy skill. Chính mô tả trong code thừa nhận doctor --fix chỉ chạy các fix đã đăng ký. Đề xuất: doctor là bộ máy duy nhất, init = doctor --fix cộng quyền tạo mới, setup bỏ. Khi viết lại, số rule giảm từ 230 xuống 212 nhờ gom các chỗ nói cùng một việc.
**Bài học:** Khi một lệnh được gọi là alias, hãy đọc code trước: alias thường đã thành một bản sao có thêm việc riêng. Đặt một bộ máy duy nhất và coi các lệnh khác là cách gọi vào đó.
**Artefact:** Bảng bốn dòng: tên lệnh và việc thật nó làm.
