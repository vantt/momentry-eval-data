---
id: 2026-11-02-probe-ohs-kill-9-van-khong
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L307"]
hook: "kill -9 giữa lúc index, OHS vẫn tự thoát dưới 1 giây"
tension: tuong_ma_hoa_ra
sides: ["kill -9 tưởng sẽ để lại tiến trình mồ côi", "OHS thấy stdin đóng và thoát, không còn node nào"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe OHS: kill -9 vẫn không để lại tiến trình node

**Bối cảnh:** Thử kết nối OHS qua stdio từ Rust với 6 truy vấn gửi cùng lúc.
**Chuyện gì xảy ra:** 6 trên 6 truy vấn trả về cùng bộ note và cùng thứ tự với CLI của OHS. Khi kill -9 lúc đang index, OHS thấy stdin đóng và thoát trong dưới 1 giây, không còn tiến trình node nào.
**Bài học:** Dùng việc stdin đóng làm tín hiệu thoát cho tiến trình con, và kiểm bằng kill -9.
**Artefact:** Không có.
