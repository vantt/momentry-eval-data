---
id: 2026-11-02-reviewer-doc-lap-bat-skill-tu
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt, "số trước, số sau"]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L681", "claude:6a207191#L690", "claude:6a207191#L897"]
hook: "Skill dạy luật đóng gói, nhưng installer mẫu vi phạm chính luật đó"
tension: giup_ma_hai
sides: ["Skill đặt ra luật cho installer", "Installer mẫu thiếu --help, gỡ không hỏi, hỏng trên Alpine"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập bắt skill tự mâu thuẫn: 'setup' vs 'init', installer mẫu vi phạm luật của chính nó

**Bối cảnh:** Sau nhiều vòng, skill có 230 rule. Người dùng nhờ một agent mạnh review và giao mục tiêu: UX trước, agent-native, dễ hiểu.
**Chuyện gì xảy ra:** Reviewer đóng vai một agent phân phối cho Go CLI có MCP server rồi đi theo quy trình của skill. Nó tìm ra ba lỗi phải sửa: INS-13 bảo dùng setup trong khi CMD-04 nói không có setup; installer mẫu in lệnh Next sai; chuỗi init --yes rồi doctor --fix không bao giờ chạy connect, nên agent chỉ đọc --help sẽ không đăng ký MCP. Installer mẫu cũng vi phạm luật: thiếu --help, gỡ cài đặt không hỏi, hỏng trên Alpine, crash khi --version không có giá trị. Sau khi sửa, số rule là 212.
**Bài học:** Đưa reviewer một kịch bản người dùng cụ thể và cho nó chạy đầu đến cuối. Cách này bắt được lỗi mà đọc từng file không thấy.
**Artefact:** Bảng phát hiện gồm ID rule, điểm mâu thuẫn và cách sửa.
