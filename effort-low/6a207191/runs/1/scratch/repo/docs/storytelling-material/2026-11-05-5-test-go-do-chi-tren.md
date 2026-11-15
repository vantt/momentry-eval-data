---
id: 2026-11-05-5-test-go-do-chi-tren
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2053", "claude:6a207191#L2063", "claude:6a207191#L2073", "claude:6a207191#L2129", "claude:6a207191#L2152", "claude:6a207191#L2158", "claude:6a207191#L2179", "claude:6a207191#L2190", "claude:6a207191#L2221", "claude:6a207191#L2246"]
hook: "5 test đỏ chỉ trên máy tôi, vì test đọc cấu hình agent thật"
tension: nho_ma_to
sides: ["CI xanh, test đã đổi HOME sang thư mục giả", "Không đổi thư mục làm việc nên test đọc file cấu hình thật, 5 test đỏ"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 5 test Go đỏ chỉ trên máy tôi: test đọc cấu hình agent thật

**Bối cảnh:** make check trên main báo 5 test lỗi trong package cli. Ban đầu agent nghi do môi trường.
**Chuyện gì xảy ra:** Chạy lại với HOME tạm vẫn lỗi. Nguyên nhân: TestMain đổi HOME nhưng không đổi thư mục làm việc. Lệnh status và doctor đi ngược lên các thư mục cha tìm cấu hình dự án, và tới thư mục nhà thì gặp file cấu hình Codex và Gemini vừa được ghi lúc connect toàn cục. Vì HOME giả, code coi thư mục nhà là một dự án, so đường dẫn binary và báo FAILED. CI không có các file đó nên vẫn xanh. Cả 5 test cùng một gốc.
**Bài học:** Test đọc cấu hình người dùng thật sẽ đỏ khi máy có kết nối thật. Hãy cách ly cả thư mục làm việc, không chỉ HOME. CI xanh không chứng minh máy dev sạch.
**Artefact:** Bảng 5 test với kỳ vọng và kết quả thực tế. Che đường dẫn và địa chỉ hub.
**Góc người ngoài:** cách làm phổ biến là Người làm thường bỏ qua test lỗi vì nghĩ là do môi trường, hoặc sửa test để xanh lại mà không rõ nguyên nhân; ở đây khác ở Chứng minh lỗi có trước commit của mình, rồi chỉ ra cơ chế (test đọc cấu hình agent thật ở thư mục cha). Người đọc sẽ hỏi: làm sao phân biệt lỗi do môi trường với lỗi thật?.
