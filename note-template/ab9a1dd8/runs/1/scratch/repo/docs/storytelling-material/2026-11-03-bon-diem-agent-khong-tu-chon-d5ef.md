---
id: 2026-11-03-bon-diem-agent-khong-tu-chon-d5ef
code: M-9Z78
aliases: [M-9Z78]
date: 2026-11-03
repo: repo
status: raw
signals: [nguoi_duyet_may_soan]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:ab9a1dd8#L251", "claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300"]
hook: "Agent có đề xuất, nhưng bốn điểm đánh đổi vẫn để chủ quyết"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bốn điểm agent không tự chọn, đưa đánh đổi cho chủ quyết

**Bối cảnh:** Skill đóng gói chuẩn và PRD của dự án mâu thuẫn ở bốn điểm, và việc chọn là quyết định sản phẩm.
**Chuyện gì xảy ra:** Agent liệt kê từng điểm (hook chỉ in hay tự cài, mã thoát giữ hay theo chuẩn, hỗ trợ nền tảng nào, thứ tự làm) kèm đánh đổi và một đề xuất. Chủ chọn tự cài hook, mã thoát theo chuẩn, hỗ trợ Linux, macOS, Windows và WSL, và chọn phương án A cho điểm thứ tư. Agent ghi ba quyết định vào checklist ngay sau khi có câu trả lời.
**Bài học:** Khi chuẩn bên ngoài và văn bản dự án lệch nhau, đưa đánh đổi và đề xuất để người quyết, rồi ghi quyết định vào tài liệu ngay.
**Artefact:** Bảng bốn quyết định với cột chuẩn skill, PRD và lựa chọn.
**Góc người ngoài:** cách làm phổ biến là Agent tự chọn phương án rồi báo sau, hoặc hỏi quá nhiều câu nhỏ; ở đây khác ở Người đọc sẽ thấy một kiểu làm việc khác: agent chia việc có thể đảo ngược và việc không đảo được, và chỉ dừng ở việc thứ hai.
