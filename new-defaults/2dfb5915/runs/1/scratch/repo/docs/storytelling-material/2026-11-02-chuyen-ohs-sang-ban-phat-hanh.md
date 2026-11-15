---
id: 2026-11-02-chuyen-ohs-sang-ban-phat-hanh
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L1178", "claude:2dfb5915#L2296", "claude:2dfb5915#L3804"]
hook: "Tôi giữ repo private để an toàn, rồi cài đặt chỉ cần một dòng"
tension: tuong_ma_hoa_ra
sides: ["Giữ private và dựng đường dự phòng bằng gh cho chắc", "Công khai xong, cài chỉ cần irm | iex, không cần gh"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuyển OHS sang bản phát hành công khai: từ đăng nhập gh sang tải thẳng

**Bối cảnh:** Gói OHS ban đầu lấy từ artifact CI, GitHub bắt đăng nhập để tải, nên máy khách phải có gh và đăng nhập. Repo pkm cũng đang private.
**Chuyện gì xảy ra:** Ban đầu chọn giữ private và dùng gh làm đường dự phòng. Sau khi fork OHS có Release công khai (vantt.3, rồi vantt.4), chuyển nguồn sang Release. Khi người dùng chuyển repo sang public, cài đặt chỉ cần irm | iex, không cần gh.
**Bài học:** Artifact CI không phải nguồn phân phối; đưa gói lên Release công khai để máy khách không cần tài khoản.
**Artefact:** Hai lệnh cài (gh cũ và irm mới) để so sánh; che tên người dùng.
**Góc người ngoài:** cách làm phổ biến là Dùng gói từ artifact tạm thời hoặc yêu cầu người dùng tự tải và cài bằng tay; ở đây khác ở Installer thử URL công khai trước, không được thì rơi về gh; đổi nguồn cũng không cần sửa script. Người đọc muốn biết cách thiết kế installer có đường lui mà không cần đổi code khi chuyển public.
