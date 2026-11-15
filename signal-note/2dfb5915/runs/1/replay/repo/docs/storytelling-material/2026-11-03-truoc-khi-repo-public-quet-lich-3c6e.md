---
id: 2026-11-03-truoc-khi-repo-public-quet-lich-3c6e
code: M-K7NX
aliases: [M-K7NX]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3829", "claude:2dfb5915#L3835", "claude:2dfb5915#L3847"]
hook: "Quét toàn bộ lịch sử git tìm khoá và private key: 0 khớp"
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

# Trước khi repo public: quét lịch sử git tìm khoá và private key, không thấy khớp nào

**Bối cảnh:** Người dùng đổi repo sang public. Lịch sử git trước đó chưa từng được rà.
**Chuyện gì xảy ra:** Agent thử công cụ quét bí mật chuyên dụng nhưng không có sẵn, nên quét bằng regex trên toàn bộ lịch sử: mẫu token GitHub, khoá Anthropic, khoá AWS và private key. Kết quả 0 khớp. Một lệnh liệt kê file nhạy cảm bị chặn bởi hook truy cập file.
**Bài học:** Trước khi đổi repo sang public, quét lịch sử git chứ không chỉ commit mới nhất; và ghi kết quả quét là 0 khớp với mẫu nào.
**Artefact:** Số lượng khớp 0 và danh sách mẫu đã quét. Không đưa nội dung lịch sử.
