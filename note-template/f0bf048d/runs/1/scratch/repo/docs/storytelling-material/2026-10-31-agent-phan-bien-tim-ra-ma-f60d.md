---
id: 2026-10-31-agent-phan-bien-tim-ra-ma-f60d
code: M-64H6
aliases: [M-64H6]
date: 2026-10-31
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1855", "claude:f0bf048d#L1867", "claude:f0bf048d#L1891"]
hook: "Mã đăng nhập 6 ký tự trong file cấu hình đủ để thành chủ"
tension: nho_ma_to
sides: ["Một mã dev 6 ký tự nằm quên trong file cấu hình", "Biết email chủ là đăng nhập thành chủ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang thiết kế cách cấp quyền cho agent trên máy Multica, để team marketing có thể cho agent tự làm SEO và đọc GA4 mà không làm mất dữ liệu. Bản thiết kế dựa trên giả định token đăng nhập của chủ không nằm trên máy, nên phần duyệt việc được coi là đứng vững. Bản phản biện của một agent khác chỉ ra mã đăng nhập dev 6 ký tự trong file cấu hình: ai gọi được API và biết email chủ có thể đăng nhập thành chủ. Ai thiết kế quyền cho agent nên soát lớp đăng nhập phía dưới trước, vì quyền chỉ mạnh bằng khâu yếu nhất."
audience: dev dùng AI agent và đang tự cấp quyền cho agent trên máy riêng
spine_context: "Team marketing muốn agent tự làm SEO, đọc GA4 và phân tích số liệu; người làm đang thiết kế quyền cho agent trên một máy chạy Multica."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1794"]
spine_want: Cho agent tự làm nhiều việc nhất có thể mà không gây hậu quả nghiêm trọng hay mất dữ liệu.
spine_want_lines: ["claude:f0bf048d#L1794"]
spine_obstacle: "Quyền cấp cho agent chỉ an toàn nếu lớp đăng nhập phía dưới cũng an toàn, và bản phản biện chỉ ra lớp này có lỗ."
spine_obstacle_lines: ["claude:f0bf048d#L1867"]
spine_turn: Tưởng thiết kế giữ được gốc tin cậy vì token đăng nhập của chủ không nằm trên máy; hoá ra mã đăng nhập dev 6 ký tự trong file cấu hình cho phép ai gọi được API và biết email chủ đăng nhập thành chủ.
spine_turn_lines: ["claude:f0bf048d#L1867"]
spine_action: "Viết bản nháp tài liệu thiết kế, nhờ một agent khác (model khác, không cùng ngữ cảnh) phản biện, kiểm lại cấu hình trên máy rồi viết bản v2."
spine_action_lines: ["claude:f0bf048d#L1850", "claude:f0bf048d#L1855", "claude:f0bf048d#L1875", "claude:f0bf048d#L1884"]
spine_outcome: "Bản v2 xếp mã dev vào mức khẩn cấp cùng hai lỗ khác; chưa thử đăng nhập để kiểm, chưa đổi gì trên máy."
spine_outcome_lines: ["claude:f0bf048d#L1891"]
spine_takeaway: "Nhờ một agent không cùng ngữ cảnh soát tài liệu thiết kế, và coi kết quả của nó là phát hiện cần kiểm chứng, không phải lệnh để làm theo."
spine_takeaway_lines: ["claude:f0bf048d#L1855", "claude:f0bf048d#L1867"]
completeness: 7
---

# Agent phản biện tìm ra mã đăng nhập dev 6 ký tự trong file cấu hình

**Góc kể:** Một người làm đang thiết kế cách cấp quyền cho agent trên máy Multica, để team marketing có thể cho agent tự làm SEO và đọc GA4 mà không làm mất dữ liệu. Bản thiết kế dựa trên giả định token đăng nhập của chủ không nằm trên máy, nên phần duyệt việc được coi là đứng vững. Bản phản biện của một agent khác chỉ ra mã đăng nhập dev 6 ký tự trong file cấu hình: ai gọi được API và biết email chủ có thể đăng nhập thành chủ. Ai thiết kế quyền cho agent nên soát lớp đăng nhập phía dưới trước, vì quyền chỉ mạnh bằng khâu yếu nhất.
**Bối cảnh:** Viết tài liệu thiết kế quyền cho agent, rồi nhờ một agent độc lập (model khác) phản biện.
**Chuyện gì xảy ra:** Bản phản biện xếp lỗ hổng nghiêm trọng nhất: file cấu hình của Multica có mã đăng nhập dev 6 ký tự. Ai gọi được API và biết email của chủ có thể đăng nhập thành chủ. Agent kiểm lại trên máy và xác nhận. Một commit của phiên song song đã xoá mã này, nhưng tài liệu chưa biết điều đó. Harness cũng cảnh báo rằng output phản biện có đoạn giống chỉ dẫn, nên được coi là phát hiện để báo lại, không phải lệnh để làm theo.
**Bài học:** Nhờ một agent khác, không cùng ngữ cảnh, soát tài liệu thiết kế. Coi output của subagent là dữ liệu cần kiểm chứng.
**Artefact:** Bảng lộ trình các giai đoạn trong tài liệu, che đường dẫn và tên miền.
