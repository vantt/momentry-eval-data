---
id: 2026-11-02-commit-python-223c9c3-thieu-goi-ngon
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L2247", "claude:2dfb5915#L2282"]
hook: "Hai bên chung index nhưng khác cấu hình nên OHS dựng lại mãi"
tension: nho_ma_to
sides: ["Một biến môi trường bị thiếu", "OHS dựng lại index liên tục"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit Python 223c9c3: thiếu gói ngôn ngữ thì OHS dựng lại index liên tục

**Bối cảnh:** pkm và MCP ohs của user dùng chung một index nhưng cấu hình gói ngôn ngữ có thể khác nhau.
**Chuyện gì xảy ra:** Bản Python thêm biến OHS_LANGUAGE_PACK trỏ tới gói tiếng Việt trong bundle. Nếu pkm không đặt biến này, hai bên đọc chung index nhưng khác cấu hình nên OHS dựng lại view liên tục. Port vào mọi lần khởi OHS trong pkm: MCP, related và doctor --deep. Chạy thật trên bundle báo language_pack loaded là true.
**Bài học:** Hai tiến trình dùng chung cache phải đồng bộ cấu hình, không chỉ đường dẫn.
**Artefact:** Không có.
