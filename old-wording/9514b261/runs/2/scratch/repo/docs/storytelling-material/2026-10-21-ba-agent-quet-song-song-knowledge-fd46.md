---
id: 2026-10-21-ba-agent-quet-song-song-knowledge-fd46
code: M-04ZP
aliases: [M-04ZP]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo, nguoi_duyet_may_soan]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1325", "claude:9514b261#L1384", "claude:9514b261#L1398", "claude:9514b261#L1417", "claude:9514b261#L1457", "claude:9514b261#L1476", "claude:9514b261#L1572", "claude:9514b261#L1582"]
hook: "Registry đã có 479 tài liệu, đề xuất mới suýt làm trùng"
tension: nho_ma_to
sides: ["Một lỗi nhỏ: so chuỗi ISO ra NaN", "Check doc-provisional-aged không bao giờ bắn, 332 doc vẫn provisional"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là nền tảng để xây app agent, và người làm đang rà đề xuất Knowledge and Documentation Engine xem có trùng với hệ thống đã có không. Đề xuất coi đây là component mới cần xây, nhưng khi quét ba mảng song song thì Knowledge Registry đã chạy trên main với 479 tài liệu, chỉ phủ phần end-user. Ai đề xuất hệ thống mới nên đếm trước xem thứ tương tự đã có chưa, vì một check bị lỗi im lặng còn tệ hơn không có check."
audience: dev đề xuất component mới cho nền tảng agent
spine_context: Forgent (fgOS) là nền tảng để xây app agent. Người làm đang rà đề xuất Knowledge and Documentation Engine xem có trùng với hệ thống đã có hay không.
spine_context_lines: [profile, "claude:9514b261#L1325"]
spine_want: "Muốn biết KDE có trùng với Knowledge Registry đã xây không, và có sơ khai nào bị quên không."
spine_want_lines: ["claude:9514b261#L1325"]
spine_obstacle: "Tài liệu có ba chỉ mục song song (492, 479 và 0 mục). Registry chưa phủ docs/platform, docs/architect và docs/specs."
spine_obstacle_lines: ["claude:9514b261#L1572"]
spine_turn: "Đề xuất coi KDE là component mới cần xây. Hoá ra Knowledge Registry đã chạy trên main với 479 tài liệu, chỉ phủ phần end-user."
spine_turn_lines: ["claude:9514b261#L1325", "claude:9514b261#L1572"]
spine_action: "Bật ba researcher chạy song song, mỗi người quét một mảng và ghi một báo cáo riêng. Sau đó gộp kết quả và kiểm lại các con số."
spine_action_lines: ["claude:9514b261#L1384", "claude:9514b261#L1572"]
spine_outcome: "KDE chuyển thành bước hoàn thiện Knowledge Registry bằng profile. Check doc-provisional-aged không bao giờ bắn vì so chuỗi ISO ra NaN, nên 332 doc provisional đã nằm 47–55 ngày mà không ai biết."
spine_outcome_lines: ["claude:9514b261#L1448", "claude:9514b261#L1572"]
spine_takeaway: "Trước khi đề xuất component mới, hãy đếm xem thứ tương tự đã chạy chưa. Một check trả NaN im lặng còn nguy hiểm hơn việc không có check."
spine_takeaway_lines: ["claude:9514b261#L1572"]
completeness: 7
---

# Ba agent quét song song: Knowledge Registry đã chạy trên 479 tài liệu, đề xuất mới suýt trùng

**Góc kể:** Forgent (fgOS) là nền tảng để xây app agent, và người làm đang rà đề xuất Knowledge and Documentation Engine xem có trùng với hệ thống đã có không. Đề xuất coi đây là component mới cần xây, nhưng khi quét ba mảng song song thì Knowledge Registry đã chạy trên main với 479 tài liệu, chỉ phủ phần end-user. Ai đề xuất hệ thống mới nên đếm trước xem thứ tương tự đã có chưa, vì một check bị lỗi im lặng còn tệ hơn không có check.
**Bối cảnh:** Chủ nghi kho quản lý tài liệu trong đề xuất Knowledge and Documentation Engine đã có một hệ tương tự xây trước đó. Agent chạy ba researcher song song, mỗi người quét một mảng.
**Chuyện gì xảy ra:** Registry có 479 topic và 479 doc, chỉ phủ tài liệu end-user, khoảng 15% trong 3146 file .md. Có ba index song song với 492, 479 và 0 mục. Trong 479 doc có 332 provisional và 147 active, với 365 role khác nhau. Lỗi gốc nhỏ: check doc-provisional-aged không bao giờ bắn, vì so updatedAt là chuỗi ISO nên ra NaN. Agent kiểm lại từng con số trước khi gộp rồi ghi 25 dòng ghi chú vào proposal.
**Bài học:** Trước khi đề xuất component mới, hãy đếm xem thứ tương tự đã chạy chưa. Một check trả NaN im lặng còn nguy hiểm hơn việc không có check.
**Artefact:** Bản tổng hợp ba báo cáo và bảng số liệu các index. Không cần ảnh.
