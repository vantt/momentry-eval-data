---
id: 2026-10-30-deploy-goi-thu-hai-ghi-de
date: 2026-10-30
repo: repo
status: raw
signals: ["2", "3"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L896", "claude:f0bf048d#L902", "claude:f0bf048d#L915"]
hook: "Deploy gói Marketing xong, 3 agent Coding bị đưa về bản cũ"
tension: nho_ma_to
sides: ["Chỉ đọc phần Marketing trong plan", "Ghi đè team của phiên song song, gỡ 3 agent khỏi squad"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Deploy gói thứ hai ghi đè team của phiên song song

**Bối cảnh:** Hai gói (opc-studio và opc-coding) deploy vào cùng một workspace; gói opc-studio còn giữ bản cũ của team Coding.
**Chuyện gì xảy ra:** Lần deploy đầu của opc-studio đưa instructions, model và skill của 3 agent Coding về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow cho một project. Agent đã bỏ qua các dòng ngoài phần Marketing khi đọc plan. Khôi phục bằng cách deploy lại opc-coding từ file của phiên kia; plan sau đó báo 0 thay đổi. Sau đó xoá phần Coding khỏi gói opc-studio.
**Bài học:** Khi nhiều gói cùng deploy vào một workspace, đọc toàn bộ diff của plan, không chỉ phần mình sửa.
**Artefact:** Kết quả plan trước và sau khôi phục (0 change).
