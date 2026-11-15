---
id: 2026-11-03-truoc-khi-cong-khai-repo-quet-3c6e
code: M-YZX0
aliases: [M-YZX0]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3829", "claude:2dfb5915#L3835", "claude:2dfb5915#L3836", "claude:2dfb5915#L3847"]
hook: "Quét sạch lịch sử git tìm khoá: 0 kết quả"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi công khai repo, quét lịch sử git tìm khoá

**Bối cảnh:** Repo chuyển từ private sang public, lịch sử git sẽ lộ ra ngoài.
**Chuyện gì xảy ra:** Agent quét toàn bộ lịch sử git bằng các mẫu token GitHub, khoá Anthropic, khoá AWS và private key: 0 kết quả khớp. Trong quá trình này có một lần đọc file bị hook chặn, agent không đi vòng qua.
**Bài học:** Quét lịch sử git theo mẫu bí mật trước khi lật công tắc public, không chỉ quét file hiện tại.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ kiểm tra file hiện tại, hoặc không kiểm gì trước khi đổi sang public; ở đây khác ở Agent quét mọi commit trên mọi nhánh theo các mẫu token GitHub, khoá Anthropic, khoá AWS và private key trước khi ghi nhận việc đổi sang public. Người đọc muốn biết bước kiểm này trông như thế nào.
