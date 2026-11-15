---
id: 2026-11-02-ci-do-vi-rust-cache-xoa
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1364"]
hook: "Cache tăng tốc CI lại làm CI đỏ vì xoá file ngoài thư mục build"
tension: giup_ma_hai
sides: ["cache để CI chạy nhanh", "cache xoá file nên CI đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đỏ vì rust-cache xoá file ngoài thư mục build

**Bối cảnh:** Sau một push, bước so khớp parity lỗi trên cả ba hệ điều hành, và các lần sau cũng lỗi dù code không đổi.
**Chuyện gì xảy ra:** Swatinem/rust-cache chỉ lưu target và xoá mọi file ngoài thư mục build, nhưng giữ lại thư mục rỗng. Lần chạy có dump đầu tiên đã lưu cache với thư mục dump rỗng và không có manifest. Từ lần sau cache khớp đúng, và bước kiểm từ chối ghi đè thư mục không phải dump. Sửa: ghi dump ra ngoài cache. Tái hiện được bằng cách tạo đúng thư mục rỗng và thấy đúng thông điệp lỗi.
**Bài học:** Cache CI có thể giữ trạng thái nửa vời. Đừng để dữ liệu sinh ra nằm bên trong thư mục cache.
**Artefact:** Sơ đồ thư mục target trước và sau khi cache được khôi phục.
