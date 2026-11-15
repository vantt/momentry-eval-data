---
id: 2026-10-21-tu-khang-dinh-khong-thuoc-component
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L383", "claude:9514b261#L542"]
hook: "AI nói 'không thuộc dòng việc nào', rồi tự tìm ra nó thuộc"
tension: tuong_ma_hoa_ra
sides: ["AI khẳng định thành phần này không có chỗ", "Tìm lại thì có việc đã xong và hai máy kiểm"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tự khẳng định 'không thuộc component nào' rồi tự sửa

**Bối cảnh:** Agent đã nói ba máy kiểm không có chủ trong bản đồ kiến trúc.
**Chuyện gì xảy ra:** Người dùng nói có một component nhằm làm tươi các luật còn hiệu lực. Agent tìm lại và thấy một work item quyết định đã xong, cùng hai máy kiểm thuộc dòng việc đó. Agent đính chính: 'không có chủ trong bản đồ' là đúng, còn 'không thuộc dòng nào' là sai.
**Bài học:** Chỉ nói 'không có' sau khi tìm trong cả lịch sử work item, không chỉ trong bản đồ kiến trúc.
**Artefact:** Đoạn đính chính đặt cạnh câu sai ban đầu.
