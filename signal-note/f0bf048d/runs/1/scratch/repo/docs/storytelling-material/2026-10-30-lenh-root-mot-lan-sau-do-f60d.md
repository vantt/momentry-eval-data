---
id: 2026-10-30-lenh-root-mot-lan-sau-do-f60d
code: M-KGT3
aliases: [M-KGT3]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L479", "claude:f0bf048d#L480", "claude:f0bf048d#L482", "claude:f0bf048d#L1659", "claude:f0bf048d#L3031", "claude:f0bf048d#L3040", "claude:f0bf048d#L3053"]
hook: "Một lệnh root duy nhất, sau đó agent tự cài không cần sudo"
tension: it_ma_nhieu
sides: ["chạy một lệnh root một lần", "agent tự cài mãi về sau không cần sudo"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh root một lần, sau đó agent cài không cần sudo

**Bối cảnh:** Agent không có sudo, nên mọi lệnh cài phải chờ chủ chạy bằng tay.
**Chuyện gì xảy ra:** Lệnh sudo yêu cầu mật khẩu nên agent không tự chạy được. Chủ hỏi có tổ chức để System Operator tự cài được không. Script tools-owner chạy một lần để giao thư mục cài cho chủ sở hữu hợp lý, sau đó lệnh cài chạy dưới user thường. Ba runtime được chuyển sang cách cài mới mà không gián đoạn phiên đăng nhập.
**Bài học:** Gom quyền root thành một thao tác một lần để phần còn lại chạy được dưới user thường.
**Artefact:** Kết quả ls -ld cho thấy chủ sở hữu thư mục (che đường dẫn nếu cần).
