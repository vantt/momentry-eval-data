---
id: 2026-10-30-dong-goi-theo-khach-mot-workspace
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915", "claude:f0bf048d#L968", "claude:f0bf048d#L1122", "claude:f0bf048d#L1174", "claude:f0bf048d#L1178"]
hook: "Deploy một gói đã gỡ 3 agent khỏi team của phiên khác"
tension: giup_ma_hai
sides: ["đóng gói gọn để triển khai cho khách", "ghi đè team Coding, 3 agent bị gỡ khỏi squad"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đóng gói theo khách: một workspace, nhiều bộ, và sự cố ghi đè team Coding

**Bối cảnh:** Gói agent của OPC được deploy vào cùng workspace Multica, và hai gói khác nhau cùng ghi lên một workspace.
**Chuyện gì xảy ra:** Gói opc-studio ban đầu chứa cả team Coding; deploy nó ghi đè instructions và squad của gói opc-coding do phiên khác đang làm, khiến 3 agent bị gỡ khỏi squad. Lỗi gốc là plan chỉ đọc phần thay đổi của gói mình, bỏ qua dòng thay đổi ngoài Marketing. Sau đó tách thành 3 gói theo bộ (content, seo-analytics, coding) và mỗi khách một file manifest; deploy không bao giờ xoá nên không gỡ được bộ đã cài.
**Bài học:** Đọc toàn bộ kết quả plan trước khi deploy, không chỉ các dòng thuộc gói mình; và gắn mỗi gói vào một đơn vị triển khai rõ ràng (workspace theo khách) từ đầu.
**Artefact:** Bảng 'Bộ khách mua → gói → agent' và đoạn ví dụ lệnh deploy với --env; che tên khách thật.
