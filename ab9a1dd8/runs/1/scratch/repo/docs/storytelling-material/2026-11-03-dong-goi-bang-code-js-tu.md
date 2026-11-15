---
id: 2026-11-03-dong-goi-bang-code-js-tu
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, artefact]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L1112", "claude:ab9a1dd8#L1380", "claude:ab9a1dd8#L1384", "claude:ab9a1dd8#L1409"]
hook: "Tự viết đóng gói tar, đóng lại vẫn ra cùng sha256"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đóng gói bằng code JS tự viết: đóng lại vẫn ra cùng sha256

**Bối cảnh:** Update cần giải nén mà không phụ thuộc lệnh tar của hệ thống, vì Windows không có sẵn đúng dạng.
**Chuyện gì xảy ra:** Agent tự viết đọc và ghi ustar. Đóng gói lặp lại cho cùng phiên bản thì sha256 y hệt. Installer cài, cài lại không đổi gì, update báo mã 10 khi có bản mới và cập nhật vẫn giữ cấu hình.
**Bài học:** Đặt mục tiêu tái lập được từ đầu; nó giúp kiểm checksum và cài lại mà không phải đoán.
**Artefact:** Dòng checksums.txt trong bản phát hành.
**Góc người ngoài:** cách làm phổ biến là Dev chạy `tar czf` hoặc dùng bộ công cụ release sẵn; kết quả đổi theo thời gian và thứ tự file nên hash không lặp lại; ở đây khác ở Archive tái lập được giúp checksum có ý nghĩa và cài lại thì không đổi gì. Người làm một mình muốn release đáng tin mà không dựng hạ tầng ký số.
