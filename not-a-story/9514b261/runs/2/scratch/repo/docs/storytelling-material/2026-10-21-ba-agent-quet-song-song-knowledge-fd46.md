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
hook: "Registry đã có 479 tài liệu, suýt đề xuất làm lại từ đầu"
tension: tuong_ma_hoa_ra
sides: ["Đề xuất mới coi như chưa có gì sẵn", "Registry chạy rồi, lỗi gốc chỉ là so chuỗi ngày ra NaN"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là tầng nền tảng để xây và chạy các app agent, và người làm đang bàn một đề xuất Knowledge and Documentation Engine. Đề xuất này được viết như một component mới, nhưng ba agent quét song song cho thấy Knowledge Registry đã chạy thật trên 479 tài liệu, nên phần lớn đã có sẵn. Điều đáng chú ý là một check trong registry không bao giờ bắn vì so chuỗi ngày ra NaN, nên lỗi này đã nằm đó khoảng 47–55 ngày. Ai đang xây công cụ tương tự nên đếm thứ đã có trước khi đề xuất component mới."
audience: dev xây nền tảng agent hoặc đề xuất component mới
spine_context: Forgent (fgOS) là tầng nền tảng để xây và chạy app agent. Người làm đang bàn một đề xuất Knowledge and Documentation Engine.
spine_context_lines: [profile, "claude:9514b261#L1325"]
spine_want: Chủ muốn biết KDE có trùng với thứ đã xây trước đó không.
spine_want_lines: ["claude:9514b261#L1325"]
spine_obstacle: "Đề xuất KDE trông như component mới, nhưng đã có Knowledge Registry chạy trên tài liệu end-user, và có ba chỉ mục song song (492, 479 và 0 mục)."
spine_obstacle_lines: ["claude:9514b261#L1417"]
spine_turn: "Đề xuất được viết như một component mới; hoá ra phần lớn đã có ở Knowledge Registry, chỉ phủ tài liệu end-user và chưa phủ platform, architect hay specs."
spine_turn_lines: ["claude:9514b261#L1572"]
spine_action: "Bật ba agent quét song song (plans/reports, history/journals, work items/mã/specs), rồi kiểm lại các con số trước khi gộp tổng hợp."
spine_action_lines: ["claude:9514b261#L1384", "claude:9514b261#L1476"]
spine_outcome: "Registry có 479 doc, khoảng 15% trong 3146 file .md; 332 doc provisional và 147 active. Check doc-provisional-aged không bao giờ bắn vì so chuỗi ISO ra NaN, nên lỗi đã nằm đó khoảng 47–55 ngày. KDE thật sự mới chỉ còn sáu phần chưa có mã."
spine_outcome_lines: ["claude:9514b261#L1448", "claude:9514b261#L1572"]
spine_takeaway: "Trước khi đề xuất component mới, đếm xem thứ tương tự đã chạy chưa. Một check không bao giờ bắn cũng là lỗi cần bắt."
spine_takeaway_lines: ["claude:9514b261#L1572"]
completeness: 7
---

# Ba agent quét song song: Knowledge Registry đã chạy trên 479 tài liệu, đề xuất mới suýt trùng

**Góc kể:** Forgent (fgOS) là tầng nền tảng để xây và chạy các app agent, và người làm đang bàn một đề xuất Knowledge and Documentation Engine. Đề xuất này được viết như một component mới, nhưng ba agent quét song song cho thấy Knowledge Registry đã chạy thật trên 479 tài liệu, nên phần lớn đã có sẵn. Điều đáng chú ý là một check trong registry không bao giờ bắn vì so chuỗi ngày ra NaN, nên lỗi này đã nằm đó khoảng 47–55 ngày. Ai đang xây công cụ tương tự nên đếm thứ đã có trước khi đề xuất component mới.
**Bối cảnh:** Chủ nghi kho quản lý tài liệu trong đề xuất Knowledge and Documentation Engine đã có một hệ tương tự xây trước đó. Agent chạy ba researcher song song, mỗi người quét một mảng.
**Chuyện gì xảy ra:** Registry có 479 topic và 479 doc, chỉ phủ tài liệu end-user, khoảng 15% trong 3146 file .md. Có ba index song song với 492, 479 và 0 mục. Trong 479 doc có 332 provisional và 147 active, với 365 role khác nhau. Lỗi gốc nhỏ: check doc-provisional-aged không bao giờ bắn, vì so updatedAt là chuỗi ISO nên ra NaN. Agent kiểm lại từng con số trước khi gộp rồi ghi 25 dòng ghi chú vào proposal.
**Bài học:** Trước khi đề xuất component mới, hãy đếm xem thứ tương tự đã chạy chưa. Một check trả NaN im lặng còn nguy hiểm hơn việc không có check.
**Artefact:** Bản tổng hợp ba báo cáo và bảng số liệu các index. Không cần ảnh.
