---
id: 2026-10-30-mo-hinh-mot-workspace-cho-moi-f60d
code: M-0YPE
aliases: [M-0YPE]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1122", "claude:f0bf048d#L1125", "claude:f0bf048d#L1138", "claude:f0bf048d#L1146", "claude:f0bf048d#L1158", "claude:f0bf048d#L1174", "claude:f0bf048d#L1178", "claude:f0bf048d#L1183", "claude:f0bf048d#L1185", "claude:f0bf048d#L1211", "claude:f0bf048d#L1257", "claude:f0bf048d#L1277", "claude:f0bf048d#L1759"]
hook: "Mỗi khách một workspace, nhưng không ai ghi khách đã mua gì"
tension: tuong_ma_hoa_ra
sides: ["mô hình một workspace cho mỗi khách", "workspace tạo ngầm, thiếu danh sách bộ đã mua"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ agent AI cho marketing và coding, đóng gói để cài lên Multica cho từng khách; người làm muốn mỗi khách có đúng các bộ họ mua. Ban đầu gói mặc định cài vào workspace của chính mình, và workspace được tạo ngầm khi cài, nên không ai ghi khách đã mua bộ nào. Hoá ra cài một bộ không đủ để dựng khách: workspace phải là lớp riêng, có danh sách bộ, và deploy thiếu đích phải bị từ chối. Sau khi đổi, manifest của khách đầu tiên và workspace của mình đều plan sạch."
audience: dev đóng gói agent AI để bán cho nhiều khách
spine_context: "Dự án là bộ agent AI cho marketing và coding, đóng gói để cài lên Multica cho từng khách."
spine_context_lines: ["claude:f0bf048d#L968", "claude:f0bf048d#L1122"]
spine_want: Mỗi khách có đúng các bộ agent và tool mà họ đã mua.
spine_want_lines: ["claude:f0bf048d#L968", "claude:f0bf048d#L1122"]
spine_obstacle: "Gói mặc định cài vào workspace của chính mình, và workspace được tạo ngầm khi cài nên không ai ghi khách đã mua bộ nào."
spine_obstacle_lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1178"]
spine_turn: "Tưởng cài một bộ là đủ để dựng khách; hoá ra workspace là lớp riêng bị gộp ngầm, còn danh sách bộ khách mua không được ghi lại."
spine_turn_lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1178"]
spine_action: "Đổi tên gói thành opc-content, bỏ deploy mặc định, và viết manifest client.yaml cho từng khách."
spine_action_lines: ["claude:f0bf048d#L1126", "claude:f0bf048d#L1211"]
spine_outcome: "Manifest của khách đầu tiên và workspace của mình đều plan sạch; commit 3519382, chưa push."
spine_outcome_lines: ["claude:f0bf048d#L1277"]
spine_takeaway: "Mỗi khách một workspace, ghi danh sách bộ đã mua trong manifest, và từ chối deploy khi thiếu đích."
spine_takeaway_lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1178"]
completeness: 7
---

# Mô hình một workspace cho mỗi khách, mỗi bộ là một gói

**Góc kể:** Dự án là bộ agent AI cho marketing và coding, đóng gói để cài lên Multica cho từng khách; người làm muốn mỗi khách có đúng các bộ họ mua. Ban đầu gói mặc định cài vào workspace của chính mình, và workspace được tạo ngầm khi cài, nên không ai ghi khách đã mua bộ nào. Hoá ra cài một bộ không đủ để dựng khách: workspace phải là lớp riêng, có danh sách bộ, và deploy thiếu đích phải bị từ chối. Sau khi đổi, manifest của khách đầu tiên và workspace của mình đều plan sạch.
**Bối cảnh:** Chủ giải thích: khách mua bộ nào thì có team đó trong workspace của khách.
**Chuyện gì xảy ra:** Gói opc-studio được đổi tên thành opc-content, bỏ deploy mặc định, bắt buộc có file env của khách. Chủ chốt mô hình: một workspace cho mỗi khách, cài thêm bộ khi khách mua. Agent phát hiện thiếu một lớp: workspace được tạo ngầm, không có danh sách bộ khách đã mua. Viết manifest client.yaml, plan xác nhận 0 thay đổi trên workspace hiện có.
**Bài học:** Gắn mỗi khách một workspace và bắt buộc tham số đích. Thiếu tham số thì từ chối deploy thay vì cài nhầm.
**Artefact:** Mẫu manifest (cấu trúc, không có giá trị).
