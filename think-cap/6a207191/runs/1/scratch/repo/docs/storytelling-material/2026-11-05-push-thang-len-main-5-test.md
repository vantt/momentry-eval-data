---
id: 2026-11-05-push-thang-len-main-5-test
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2049", "claude:6a207191#L2053", "claude:6a207191#L2060", "claude:6a207191#L2063", "claude:6a207191#L2073", "claude:6a207191#L2080", "claude:6a207191#L2103", "claude:6a207191#L2152", "claude:6a207191#L2158", "claude:6a207191#L2179", "claude:6a207191#L2221", "claude:6a207191#L2246"]
hook: "5 test đỏ chỉ trên máy tôi, CI xanh vì runner không có cấu hình"
tension: cam_ma_van_lot
sides: ["CI GitHub xanh, test có vẻ ổn", "Test đọc cấu hình thật của người dùng, đỏ trên máy dev"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Push thẳng lên main: 5 test Go đỏ chỉ trên máy tôi vì test đọc cấu hình thật của người dùng

**Bối cảnh:** Người dùng bảo merge và push. Repo yêu cầu make check trước khi commit, và thay đổi chỉ nằm ở phần web.
**Chuyện gì xảy ra:** make check có 5 test Go trong package cli đỏ. Agent stash thay đổi để chạy baseline trên main và thấy đúng 5 lỗi đó. Gốc rễ: TestMain đổi HOME và XDG nhưng không đổi thư mục làm việc. status và doctor đi ngược cây thư mục từ cwd lên tới thư mục home, gặp cấu hình Codex và Gemini được ghi lúc connect --global cùng hôm đó, rồi coi home là một project. Đường dẫn binary đăng ký khác với binary test nên báo FAILED, làm 5 assertion đỏ. Agent đẩy thẳng lên main bằng fast-forward, không qua PR, vì lỗi đã có sẵn trên main. CI GitHub xanh vì runner không có các file cấu hình đó.
**Bài học:** Test phải cách ly cả thư mục làm việc, không chỉ HOME. Cấu hình agent ghi ra home có thể làm lệch test trên máy dev.
**Artefact:** Bảng 5 test gồm tên, kỳ vọng và lý do đỏ. Không kèm đường dẫn cá nhân.
**Góc người ngoài:** cách làm phổ biến là Dev thường bỏ qua test lỗi có vẻ không liên quan, hoặc tắt test đó, hoặc chỉ nói 'lỗi có sẵn'; ở đây khác ở Agent kiểm chứng được lỗi có sẵn, giải thích cơ chế cụ thể, và báo rõ bằng chứng. Người đọc sẽ muốn biết vì sao môi trường cá nhân làm test đỏ mà CI thì xanh.
