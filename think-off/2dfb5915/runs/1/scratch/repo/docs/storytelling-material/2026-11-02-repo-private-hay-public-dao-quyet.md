---
id: 2026-11-02-repo-private-hay-public-dao-quyet
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1142", "claude:2dfb5915#L1162", "claude:2dfb5915#L3785", "claude:2dfb5915#L3804"]
hook: "Giữ repo private, rồi GitHub dừng mọi job vì thanh toán"
tension: tuong_ma_hoa_ra
sides: ["quyết định giữ private đã chốt", "lỗi thanh toán buộc chuyển public, khách tải khỏi đăng nhập"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo private hay public: đảo quyết định vì Actions ngừng chạy

**Bối cảnh:** Repo giữ private nên cài phải qua gh đăng nhập. Artifact OHS cũng cần đăng nhập để tải.
**Chuyện gì xảy ra:** Quyết định giữ private được chốt ở bước chọn phương án. Khi rc.3 chạy, GitHub từ chối mọi job vì tài khoản có vấn đề thanh toán, không phải lỗi code. Người dùng chuyển repo sang public, CI chạy lại. Từ đó khách tải OHS từ Release không cần đăng nhập.
**Bài học:** Quyết định về visibility phụ thuộc chi phí CI. Ghi rõ điều kiện để có thể đảo quyết định khi điều kiện đổi.
**Artefact:** Không có.
