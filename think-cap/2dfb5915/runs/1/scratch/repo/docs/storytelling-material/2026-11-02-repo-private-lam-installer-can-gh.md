---
id: 2026-11-02-repo-private-lam-installer-can-gh
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, người duyệt, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L3785", "claude:2dfb5915#L3804"]
hook: "Giữ repo private, rồi GitHub từ chối chạy CI vì billing và phải chuyển public"
tension: giup_ma_hai
sides: ["Giữ repo private cho an toàn", "CI bị chặn billing, buộc chuyển public"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo private làm installer cần gh; rồi chuyển public vì CI bị chặn billing

**Bối cảnh:** Artifact OHS trên GitHub Actions chỉ tải được khi đã đăng nhập, kể cả với repo public.
**Chuyện gì xảy ra:** Installer thử URL công khai trước, không được thì dùng gh release download. User chọn giữ private. Sau đó GitHub Actions từ chối chạy mọi job với thông báo lỗi thanh toán hoặc hết hạn mức. User tự chuyển repo sang public; Actions miễn phí, CI chạy lại, rc.3 được phát hành.
**Bài học:** Kiểm billing và visibility trước khi lên lịch release; artifact cần đăng nhập không phải kênh phát hành công khai.
**Artefact:** Ảnh thông báo billing của Actions, che tên tài khoản.
