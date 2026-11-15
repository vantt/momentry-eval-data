---
id: 2026-11-03-clone-sach-qua-205-205-test
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L146", "claude:ab9a1dd8#L156", "claude:ab9a1dd8#L167", "claude:ab9a1dd8#L170", "claude:ab9a1dd8#L236"]
hook: "Clone sạch qua 205/205, máy tác giả chỉ 202/203"
tension: tuong_ma_hoa_ra
sides: ["test xanh trên máy tác giả", "file ngoài git làm test hỏng, clone sạch mới lộ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Clone sạch qua 205/205 test, bản làm việc chỉ 202/203 vì thư mục chưa đưa vào git

**Bối cảnh:** Test imports quét mọi file .mjs, kể cả thư mục .claude và .agentkit chưa được git theo dõi. Chạy trên bản làm việc thì test này hỏng.
**Chuyện gì xảy ra:** Bản clone sạch qua 205/205. Bản làm việc chỉ qua 202/203, lỗi nằm ở test quét thư mục không track. Lỗi chỉ lộ khi so với clone sạch, vì máy của tác giả có nhiều file ngoài git hơn.
**Bài học:** Chạy test trên một clone sạch từ git, không chỉ trên thư mục làm việc; test quét tự động dễ bắt cả file không thuộc dự án.
**Artefact:** Hai dòng kết quả test: 205/205 trên clone và 202/203 trên bản làm việc, đặt cạnh nhau.
