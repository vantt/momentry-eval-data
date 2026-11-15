---
id: 2026-11-03-vong-agent-native-hoi-tu-khi
date: 2026-11-03
repo: repo
status: raw
signals: [số trước/sau, artefact]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968", "claude:ab9a1dd8#L1984", "claude:ab9a1dd8#L2230"]
hook: "Lỗi chỉ gợi ý sửa file thì agent kẹt hai vòng; có lệnh chạy được thì xong ngay"
tension: it_ma_nhieu
sides: ["thêm một lệnh privacy-add", "vòng lặp agent hội tụ ngay lần đầu"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng agent-native hội tụ khi lỗi có lệnh chạy được

**Bối cảnh:** momentry được thiết kế để agent tự cài và tự sửa lỗi chỉ bằng --help và --json.
**Chuyện gì xảy ra:** Ở vòng thử đầu, agent mới vướng vì lỗi nguồn riêng tư chỉ có câu gợi ý chỉnh file cấu hình, không chạy được. Vòng lặp hội tụ sau hai vòng. Sau khi thêm `momentry config privacy-add`, vòng sau hội tụ ngay lần đầu, và test thông báo lỗi được cập nhật.
**Bài học:** Thông báo lỗi nên kèm lệnh chạy được nguyên văn; một agent mới là bài test UX tốt nhất.
**Artefact:** Dòng agent runs trong output script vòng agent.
**Góc người ngoài:** cách làm phổ biến là Người dùng đọc README, làm theo tay; khi lỗi thì hỏi người viết hoặc tự tra cứu, không có vòng thử nghiệm bằng agent; ở đây khác ở Công cụ được thiết kế để agent đọc thông báo lỗi có sẵn lệnh sửa, rồi chạy thử và đo số vòng đến khi hội tụ. Đây là cách biến 'agent cài được không' thành phép đo.
