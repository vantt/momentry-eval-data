---
id: 2026-11-03-codex-khong-bao-gio-chay-hook
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228"]
hook: "Hook Codex không chạy lần nào, nhưng CI vẫn xanh"
tension: cam_ma_van_lot
sides: ["CI xanh, test qua hết", "hook sai tên sự kiện nên Codex bỏ qua, không báo lỗi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Codex không bao giờ chạy hook: tên sự kiện sai kiểu chữ, CI vẫn xanh

**Bối cảnh:** momentry ghi hook Codex với tên pre_compact và session_start. hooks.json của Codex đòi PreCompact, SessionEnd, SessionStart. Test của dự án chỉ kiểm chuỗi trong file, không kiểm Codex có thực sự gọi hook.
**Chuyện gì xảy ra:** Agent đọc mã nguồn Codex trên GitHub để kiểm tên sự kiện và cách tính trusted_hash. Các hook sai tên bị bỏ qua mà không báo lỗi. Sau khi sửa và thêm SessionEnd, test vẫn xanh vì chưa có bài kiểm chạy thật. Hook Codex chưa được chứng minh chạy trong phiên thật.
**Bài học:** Test kiểm chuỗi cấu hình không thay thế được việc chạy thật; với công cụ bên thứ ba, đối chiếu tên sự kiện với mã nguồn hoặc tài liệu của chính họ.
**Artefact:** Bảng tên sự kiện: cột momentry, cột Codex, cột trạng thái. Không cần che gì.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường chỉ đọc tài liệu chính thức hoặc thử lại bằng tay; ít người tìm tới mã nguồn để xem cơ chế nội bộ; ở đây khác ở Khi tài liệu không nói rõ, agent đọc thẳng mã nguồn qua API để biết tên sự kiện đúng, cờ bỏ qua tin cậy và cách hash, nên sửa được lỗi mà người khác có thể bỏ qua.
