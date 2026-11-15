---
id: 2026-11-02-watcher-debounce-5-giay-khong-ha
date: 2026-11-02
repo: repo
status: raw
signals: [Đảo quyết định có lý do, Người duyệt thứ máy soạn]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L1614", "claude:c4caee3c#L1615", "claude:c4caee3c#L1622", "claude:c4caee3c#L1923", "claude:c4caee3c#L1926"]
hook: "Không hạ tiêu chí 5 giây: thêm một biến môi trường, còn dưới 1 giây"
tension: it_ma_nhieu
sides: ["Chỉ thêm một biến môi trường", "Độ trễ từ 5 giây xuống dưới 1 giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Watcher debounce 5 giây: không hạ ngưỡng mà thêm biến môi trường

**Bối cảnh:** Tiêu chí: client nhận sự kiện index trong 1 giây sau khi ghi file. Watcher upstream chờ cố định 5 giây.
**Chuyện gì xảy ra:** Agent đề xuất hạ tiêu chí hoặc chấp nhận 5 giây. Người duyệt không hạ tiêu chí: thêm biến OBSIDIAN_WATCH_DEBOUNCE_MS với mặc định 5000 để không đổi hành vi upstream, khuyến nghị 250 cho client. Test chứng minh sự kiện đến trong dưới 1 giây khi đặt 250 ms.
**Bài học:** Thêm núm cấu hình giữ được ngưỡng; hạ ngưỡng để qua test là thương lượng sai.
**Artefact:** Bảng thời gian từ lúc ghi file đến lúc nhận sự kiện.
**Góc người ngoài:** cách làm phổ biến là Khi tiêu chí không đạt, dev thường nới ngưỡng, skip test, hoặc ghi 'known issue' để qua việc; ở đây khác ở Có quy tắc cứng 'không hạ ngưỡng' được truyền xuống mọi sub-agent; sửa bằng cách làm ngưỡng cấu hình được nhưng mặc định giữ đúng giá trị gốc, nên bất biến vẫn đúng ở bản mặc định. Người đọc muốn có cách để AI không âm thầm lách chuẩn.
