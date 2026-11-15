---
id: 2026-10-30-mo-hinh-mot-workspace-cho-moi-f60d
code: M-0YPE
aliases: [M-0YPE]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1122", "claude:f0bf048d#L1125", "claude:f0bf048d#L1174", "claude:f0bf048d#L1178", "claude:f0bf048d#L1183", "claude:f0bf048d#L1211", "claude:f0bf048d#L1277"]
hook: "Đổi tên gói vì trùng tên workspace, tránh cài nhầm lần nữa"
tension: nho_ma_to
sides: ["Chỉ là một cái tên gói opc-studio", "Trùng tên workspace gây sự cố cài nhầm trước đó"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô hình một workspace cho mỗi khách: đổi tên gói vì gói mang tên workspace

**Bối cảnh:** Người vận hành mô tả mô hình: mỗi khách một workspace, khách mua bộ nào thì gắn bộ đó vào.
**Chuyện gì xảy ra:** Gói tên opc-studio gây nhầm với workspace của chính mình, nên đổi thành opc-content. Bỏ mặc định deploy vào workspace opc-studio để không cài nhầm như sự cố trước. Hai lớp được tách: workspace khách dựng một lần, các bộ nghiệp vụ gắn vào sau. Người vận hành đồng ý làm manifest cho một khách mẫu, plan sạch cho cả hai manifest.
**Bài học:** Đặt tên đơn vị triển khai theo bộ nghiệp vụ, không theo tên workspace. Thiếu tham số đích thì công cụ phải từ chối chạy.
**Artefact:** Mẫu manifest khách đã che email và id.
