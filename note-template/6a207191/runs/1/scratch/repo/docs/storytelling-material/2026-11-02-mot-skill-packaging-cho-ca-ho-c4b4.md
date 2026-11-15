---
id: 2026-11-02-mot-skill-packaging-cho-ca-ho-c4b4
code: M-V1P9
aliases: [M-V1P9]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L319", "claude:6a207191#L339", "claude:6a207191#L545", "claude:6a207191#L578", "claude:6a207191#L661", "claude:6a207191#L701", "claude:6a207191#L897"]
hook: "Cắt skill từ 11.900 xuống 6.400 từ, rồi review vẫn bắt được 2 lệnh mâu thuẫn"
tension: giup_ma_hai
sides: ["Rút gọn 46% cho gọn và đỡ dư thừa", "Vẫn còn hai lệnh tự mâu thuẫn nhau, phải thêm rule lên 212"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một skill packaging cho cả họ dự án: từ 46% dư thừa đến bộ lệnh init/doctor chung

**Bối cảnh:** Người làm dự án đã distill packaging từ 4 repo (mdview, skillstation, herdr-go, forgent) thành một skill dùng lại cho các dự án sau. Ban đầu skill quá dài và có mâu thuẫn về lệnh.
**Chuyện gì xảy ra:** Lần đầu skill có khoảng 11.900 từ, sau khi người dùng chê dư thừa, rút xuống khoảng 6.400 từ (−46%). Một agent review độc lập chỉ ra 2 lệnh mâu thuẫn (INS-13 dùng `setup`, CMD-04 cấm `setup`) và install.sh mẫu in ra `Next: doctor --fix` thay vì `init`. Sau khi sửa, số rule từ 183 lên 212 và mô hình init/doctor được chốt: doctor là bộ máy duy nhất, init = doctor --fix + được phép tạo mới, setup bỏ đi.
**Bài học:** Khi viết bộ quy tắc cho agent, hãy chốt một đích duy nhất cho mỗi việc (ví dụ init/doctor) và để agent review độc lập tìm mâu thuẫn trước khi dùng thật.
**Artefact:** Bảng so sánh số từ trước/sau và sơ đồ init/doctor trong common/07-command-surface.md; che tên hub, IP và đường dẫn máy.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người ta viết hướng dẫn theo cảm tính hoặc sao chép từ một nguồn, rồi tự đánh giá là ổn; ở đây khác ở Phiên này đọc đối chiếu từng dự án, đo số từ, rút gọn 46%, rồi giao một agent khác review và kiểm chứng bằng cách thử 'cài X giúp tôi' chỉ với --help. Người đọc sẽ muốn biết cách tự kiểm chứng một bộ hướng dẫn có vẻ hợp lý.
