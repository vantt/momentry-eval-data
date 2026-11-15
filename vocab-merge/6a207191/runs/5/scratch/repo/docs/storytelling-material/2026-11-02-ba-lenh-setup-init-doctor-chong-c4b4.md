---
id: 2026-11-02-ba-lenh-setup-init-doctor-chong-c4b4
code: M-YQFZ
aliases: [M-YQFZ]
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định, ràng buộc thiết kế, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L727", "claude:6a207191#L732", "claude:6a207191#L897"]
hook: "Ba lệnh setup, init, doctor chồng chéo nhau, nên gộp còn một"
tension: hop_ma_tan
sides: ["ba lệnh cùng làm việc có ích", "chúng chồng chéo, rule giảm từ 230 xuống 212"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba lệnh setup/init/doctor chồng chéo, và 'doctor là bộ máy duy nhất'

**Bối cảnh:** fgos là hệ lớn: fgctl là bộ cài và nâng cấp, không phải một binary đơn. Người dùng nói init và setup chỉ nên là alias của doctor.
**Chuyện gì xảy ra:** Agent đọc mã fgos và thấy setup không phải alias: nó gọi các fix của doctor rồi thêm việc ghi dòng source vào rc, tạo file config, cài git hook, cài Claude hook và copy skills. Lệnh init chạy fgos init, rồi doctor --fix, rồi doctor. Thiết kế đích là doctor làm máy duy nhất, init bằng doctor --fix cộng quyền tạo mới, còn setup bị bỏ. Sau khi gộp phần trùng, số rule của skill giảm từ 230 xuống 212.
**Bài học:** Mọi trạng thái cần thiết lập nên là một kiểm tra có cách sửa của doctor; lệnh nào tự ghi file ngoài đó sẽ tạo ra lệnh chồng chéo.
**Artefact:** Bảng 4 dòng: lệnh và việc thực tế nó làm (từ kết quả đọc mã). Không có đường dẫn cần che.
