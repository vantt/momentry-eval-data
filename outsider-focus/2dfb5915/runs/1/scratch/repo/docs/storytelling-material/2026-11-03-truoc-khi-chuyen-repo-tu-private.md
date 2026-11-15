---
id: 2026-11-03-truoc-khi-chuyen-repo-tu-private
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L3804", "claude:2dfb5915#L3829", "claude:2dfb5915#L3835", "claude:2dfb5915#L3836", "claude:2dfb5915#L3847"]
hook: "Quét sạch mọi nhánh git trước khi public repo: 0 chỗ lộ khóa"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi chuyển repo từ private sang public, agent tự quét toàn bộ lịch sử git (mọi nhánh) tìm mẫu token GitHub, khoá Anthropic, khoá AWS, private key và tên file nhạy cảm. Kết quả là 0 chỗ khớp.

**Chuyện gì xảy ra:** Trước khi chuyển repo từ private sang public, agent tự quét toàn bộ lịch sử git (mọi nhánh) tìm mẫu token GitHub, khoá Anthropic, khoá AWS, private key và tên file nhạy cảm. Kết quả là 0 chỗ khớp.
**Góc người ngoài:** cách làm phổ biến là Chuyển public luôn rồi mới nhớ ra, hoặc chỉ nhìn file hiện tại. Lịch sử git vẫn giữ lại mọi thứ đã từng commit; ở đây khác ở Đổi visibility là việc khó đảo ngược vì lịch sử đã bị người khác clone. Việc quét `git log --all -p` bằng regex chỉ mất vài giây, và nó nên làm trước khi mở repo. Dev làm một mình thường bỏ qua bước này.
