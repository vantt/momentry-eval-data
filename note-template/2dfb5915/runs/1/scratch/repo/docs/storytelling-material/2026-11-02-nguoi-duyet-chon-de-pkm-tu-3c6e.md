---
id: 2026-11-02-nguoi-duyet-chon-de-pkm-tu-3c6e
code: M-RHCF
aliases: [M-RHCF]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3088", "claude:2dfb5915#L3098", "claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "Hai agent cãi lại plan, người duyệt đứng về phía họ"
tension: nguoi_dung_may_sai
sides: ["Plan ghi chuyển tool read sang OHS", "Hai agent chỉ ra OHS chỉ đọc được note đã index"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người duyệt chọn để pkm tự đọc file thay vì chuyển sang OHS

**Bối cảnh:** Thiết kế bộ tool MCP một cửa cho phase 17. Hai agent làm độc lập, rồi phản biện chéo.
**Chuyện gì xảy ra:** Hai agent cùng đề xuất 13 tool và cùng bác code mode. Plan ghi tool read chuyển sang OHS, nhưng cả hai phản đối vì OHS chỉ đọc được note đã index. Ước lượng token theo ký tự: từ khoảng 6,0 nghìn xuống 4,4 nghìn; bản phản biện đo danh sách golden được 13.381 ký tự, cao gấp đôi ước tính ban đầu. Người duyệt chọn read do pkm tự đọc.
**Bài học:** Ước lượng bằng độ dài chuỗi dễ sai một nửa; đo lại trước khi chốt ngưỡng.
**Artefact:** Bảng so phương án: số tool, token định nghĩa ước lượng, số lượt gọi cho nhóm câu hỏi D.
