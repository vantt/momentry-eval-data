---
id: 2026-10-29-ngan-sach-0-dong-am-tham
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1160", "claude:0faf0bb2#L1169", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1175", "claude:0faf0bb2#L1338"]
hook: "Đặt ngân sách 0 đồng để khỏi tốn tiền, agent kẹt hơn 10 phút không ai báo"
tension: giup_ma_hai
sides: ["Đặt ngân sách 0 đồng để kiểm soát chi phí", "Comment của chủ không đánh thức được agent, lỗi không hiện trên giao diện"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ngân sách 0 đồng âm thầm chặn agent: comment của chủ không đánh thức được ai

**Bối cảnh:** Paperclip cho đặt budget tháng cho từng agent, nhưng mô hình thuê bao không có giá theo token để tính chi phí.
**Chuyện gì xảy ra:** Sau khi đặt budget, lượt đánh thức trả 409 'recorded usage has no reliable price'. Comment của chủ trên issue không tạo run mới, và agent vẫn in_progress sau hơn 10 phút. Lỗi không hiện rõ trên giao diện. Đặt budget về 0 cho 3 agent, resume agent bị paused (lý do budget), và run mới bắt đầu trong vài giây.
**Bài học:** Ràng buộc tài chính viết cho mô hình tính theo token có thể chặn cả mô hình thuê bao; khi comment không kích hoạt gì, kiểm tra điều kiện chặn trước khi nghi tín hiệu.
**Artefact:** Dòng lỗi 409 và bảng budget trước/sau của 3 agent (0 sau khi sửa).
