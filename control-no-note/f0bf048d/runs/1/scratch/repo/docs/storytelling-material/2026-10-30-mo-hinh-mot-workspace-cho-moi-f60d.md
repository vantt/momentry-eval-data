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
hook: "Gói tên trùng workspace của chính mình, suýt cài nhầm lần nữa"
tension: nho_ma_to
sides: ["Chỉ là một cái tên gói", "Trùng tên workspace nên từng cài nhầm, phải đổi tên"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang đóng gói bộ agent AI để triển khai cho từng khách trên Multica, mỗi khách một workspace và mua bộ nào cài bộ đó. Gói đầu tiên lại mang tên workspace của chính họ và mặc định cài vào đó, nên quên một tham số là cài nhầm, như sự cố trước. Đổi tên theo bộ nghiệp vụ và bắt buộc chỉ định workspace đích giúp công cụ tự chặn lỗi này, điều đáng biết với ai triển khai nhiều khách trên cùng một nền tảng."
audience: người triển khai agent AI cho nhiều khách trên cùng nền tảng
spine_context: "Người làm đóng gói bộ agent AI để triển khai cho từng khách trên Multica, đang chuẩn bị cài cho khách đầu tiên."
spine_context_lines: ["claude:f0bf048d#L968"]
spine_want: "Mỗi khách có một workspace riêng, mua bộ nào thì cài bộ đó."
spine_want_lines: ["claude:f0bf048d#L1122"]
spine_obstacle: "Gói đầu tiên mang tên workspace nội bộ và mặc định cài vào đó, nên dễ cài nhầm."
spine_obstacle_lines: ["claude:f0bf048d#L1125"]
spine_turn: Tưởng gói là đơn vị cài cho khách mà vẫn cài đúng chỗ khi quên tham số đích; hoá ra gói mặc định cài vào workspace của chính mình.
spine_turn_lines: ["claude:f0bf048d#L1125"]
spine_action: "Đổi tên gói thành opc-content, bỏ deploy mặc định và bắt buộc truyền file env của khách."
spine_action_lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1126"]
spine_outcome: "Commit 237d250, chưa push; plan bộ Content chỉ đổi đúng phần Content, bộ coding báo 0 change."
spine_outcome_lines: ["claude:f0bf048d#L1165"]
spine_takeaway: "Đặt tên đơn vị triển khai theo bộ nghiệp vụ, không theo tên workspace; để công cụ từ chối chạy khi thiếu đích."
spine_takeaway_lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1165"]
completeness: 7
---

# Mô hình một workspace cho mỗi khách: đổi tên gói vì gói mang tên workspace

**Góc kể:** Người làm đang đóng gói bộ agent AI để triển khai cho từng khách trên Multica, mỗi khách một workspace và mua bộ nào cài bộ đó. Gói đầu tiên lại mang tên workspace của chính họ và mặc định cài vào đó, nên quên một tham số là cài nhầm, như sự cố trước. Đổi tên theo bộ nghiệp vụ và bắt buộc chỉ định workspace đích giúp công cụ tự chặn lỗi này, điều đáng biết với ai triển khai nhiều khách trên cùng một nền tảng.
**Bối cảnh:** Người vận hành mô tả mô hình: mỗi khách một workspace, khách mua bộ nào thì gắn bộ đó vào.
**Chuyện gì xảy ra:** Gói tên opc-studio gây nhầm với workspace của chính mình, nên đổi thành opc-content. Bỏ mặc định deploy vào workspace opc-studio để không cài nhầm như sự cố trước. Hai lớp được tách: workspace khách dựng một lần, các bộ nghiệp vụ gắn vào sau. Người vận hành đồng ý làm manifest cho một khách mẫu, plan sạch cho cả hai manifest.
**Bài học:** Đặt tên đơn vị triển khai theo bộ nghiệp vụ, không theo tên workspace. Thiếu tham số đích thì công cụ phải từ chối chạy.
**Artefact:** Mẫu manifest khách đã che email và id.
