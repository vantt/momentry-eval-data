---
id: 2026-11-02-subagent-bao-update-ghi-de-binary
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L96", "claude:6a207191#L957"]
hook: "Subagent báo update ghi đè binary, nhưng chưa ai chạy thử"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo nói update ghi file tar.gz đè lên binary", "Chỉ là suy luận từ đọc code, chưa chạy thử"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Subagent báo update ghi đè binary: chỉ là suy luận từ đọc code, chưa chạy thử

**Bối cảnh:** Các subagent nghiên cứu packaging chạy song song trên bốn repo. Một báo cáo chỉ ra lỗi thật trong herdr-go.
**Chuyện gì xảy ra:** Báo cáo nói lệnh update ghi file .tar.gz tải về đè lên chính binary đang chạy thay vì giải nén. Nó cũng nói lệnh gỡ cài đặt in ra trong installer macOS trỏ tới một file không được publish. Agent ghi hai điểm này vào danh sách việc còn lại và nói rõ đây là kết luận từ đọc code, chưa chạy thử.
**Bài học:** Ghi mức kiểm chứng (đã chạy hay chỉ đọc code) ngay bên cạnh mỗi phát hiện, để người đọc sau không coi nó là đã xác nhận.
**Artefact:** Đoạn báo cáo tóm tắt hai lỗi, đã bỏ tên repo nếu không muốn công khai.
