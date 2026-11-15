---
id: 2026-11-02-tieu-chi-agent-native-mot-agent
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L636", "claude:6a207191#L639", "claude:6a207191#L657", "claude:6a207191#L1561"]
hook: "Không cho đọc README, chỉ có --help: agent mới có tự cài xong được không?"
tension: khac
sides: ["agent mới không biết gì về công cụ", "chỉ một màn --help phải đủ để cài xong"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tiêu chí agent-native: một agent mới chỉ đọc --help có cài xong được không

**Bối cảnh:** Người dùng muốn chỉ cần nói 'cài X giúp tôi' là agent tự làm được, chỉ bằng cách đọc init --help và doctor --help.
**Chuyện gì xảy ra:** Agent biến ý này thành tiêu chí đo: không cho đọc README, chỉ có --help, và phải tự đưa doctor về trạng thái ổn. Agent thêm nhóm rule CMD-13 đến CMD-19: help đủ dùng, không hỏi đáp khi không có terminal, dòng Next trong kết quả, trường fix trong JSON chạy được, và lệnh an toàn khi chạy lại. Bước 12 trong Verify chính là bài kiểm tra này.
**Bài học:** Đo chất lượng tài liệu bằng cách xem một agent sạch có làm xong việc không. Đây là thước đo khác với việc đọc README.
**Artefact:** Mẫu đoạn --help có ví dụ copy được và bảng exit code.
