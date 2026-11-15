---
id: 2026-11-02-reviewer-doc-lap-bat-mau-thuan
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L673", "claude:6a207191#L675", "claude:6a207191#L681", "claude:6a207191#L690", "claude:6a207191#L695", "claude:6a207191#L897"]
hook: "Bộ quy tắc dạy agent tự cài, nhưng chính nó làm agent kẹt"
tension: giup_ma_hai
sides: ["Bộ rule được viết để agent tự cài chỉ bằng --help", "Rule mâu thuẫn nhau, installer mẫu vi phạm rule, agent không đăng ký được MCP"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập bắt mâu thuẫn trong chính bộ lệnh skill

**Bối cảnh:** Sau khi skill chạy được, agent được giao review độc lập ở mức suy nghĩ cao. Reviewer đóng vai người đang dùng skill để làm một Go CLI có MCP server, và chỉ được đọc, không sửa file.
**Chuyện gì xảy ra:** Reviewer thấy một rule yêu cầu lệnh setup trong khi rule khác nói không có lệnh đó. Installer mẫu in gợi ý sai. Chuỗi lệnh agent chạy không bao giờ đăng ký MCP server, nên tiêu chí agent tự cài chỉ bằng --help bị trượt. Installer mẫu cũng vi phạm chính các rule của skill. Sau khi gộp các rule trùng, số rule giảm từ 230 xuống 212.
**Bài học:** Đừng hỏi reviewer 'có ổn không'. Hãy giao một kịch bản dùng thật, ví dụ một Go CLI có MCP, để nó tự đi qua quy trình. Cách này bắt được mâu thuẫn mà người viết đọc lại không thấy.
**Artefact:** Bảng các phát hiện đã đánh số và mức độ ưu tiên. Ẩn đường dẫn máy.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường tự đọc lại tài liệu của mình, thấy ổn là chốt, và chỉ phát hiện lỗi khi người khác dùng thật; ở đây khác ở Dùng một reviewer độc lập có mục tiêu rõ (ưu tiên UX, agent-native) để bắt lỗi chính bản thân tạo ra. Người đọc sẽ hỏi: làm sao biết nên giao cho reviewer cái gì, và vì sao nó bắt được lỗi mà người viết không thấy?.
