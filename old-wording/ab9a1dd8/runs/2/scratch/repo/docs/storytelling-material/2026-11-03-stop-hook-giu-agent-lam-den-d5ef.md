---
id: 2026-11-03-stop-hook-giu-agent-lam-den-d5ef
code: M-Y5HN
aliases: [M-Y5HN]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3047"]
hook: "Stop hook đẩy agent quay lại ba lần, mỗi lần một thiếu sót"
tension: gap_ma_phai_chon
sides: ["Agent tưởng đã xong 43/45, rồi 45/45", "Hook chặn vì còn push, tag và đo Windows"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ agent làm đến khi xong: ba lần bị đẩy lại, mỗi lần một điều kiện chưa đạt

**Bối cảnh:** Điều kiện phiên: dùng /ak-cook --auto trên plan cho tới khi hoàn tất tốt đẹp. Stop hook chặn dừng cho tới khi điều kiện đạt.
**Chuyện gì xảy ra:** Lần 1: 43/45 việc, hai việc cần push. Agent hỏi, chủ chọn push lên main. Lần 2: 45/45 và CI xanh, nhưng v0.1.0 chưa cắt và hook Windows chưa đo. Agent hỏi, chủ chọn cắt tag. Lần 3: hook Windows vẫn chưa đo trên phiên thật, agent thêm workflow probe. Mỗi lần hook chặn, agent không kết thúc được lượt.
**Bài học:** Điều kiện 'làm đến khi xong' sẽ đẩy agent tới những việc ra ngoài mà nó phải hỏi. Nên nêu trước những việc ra ngoài nào được phép.
**Artefact:** Chuỗi ba thông báo của Stop hook. Không có dữ liệu nhạy cảm.
**Góc người ngoài:** cách làm phổ biến là Người dùng nhắc lại bằng tay sau mỗi lượt, hoặc chấp nhận kết quả nửa vời rồi tự kiểm tra; ở đây khác ở Việc dừng được quyết định bởi một điều kiện đo được, không phải bởi cảm giác 'xong rồi' của agent. Người đọc sẽ muốn biết cách đặt điều kiện này và cách chặn agent dừng sớm.
