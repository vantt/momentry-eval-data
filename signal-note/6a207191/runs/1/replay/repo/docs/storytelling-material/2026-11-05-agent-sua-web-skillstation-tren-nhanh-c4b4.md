---
id: 2026-11-05-agent-sua-web-skillstation-tren-nhanh-c4b4
code: M-XYK0
aliases: [M-XYK0]
date: 2026-11-05
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1520", "claude:6a207191#L1573", "claude:6a207191#L1604", "claude:6a207191#L1611", "claude:6a207191#L1745", "claude:6a207191#L1906", "claude:6a207191#L1917", "claude:6a207191#L1984", "claude:6a207191#L2008", "claude:6a207191#L2029", "claude:6a207191#L2038", "claude:6a207191#L2103"]
hook: "229 test qua, agent vẫn dừng trước commit và chờ chủ dự án"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent sửa web skillstation trên nhánh riêng, merge thẳng vào main khi được bảo

**Bối cảnh:** Chủ dự án yêu cầu làm phần UI bằng skill ak-frontend-development, nhưng skill này không được nạp vào phiên.
**Chuyện gì xảy ra:** Agent tìm thấy file SKILL.md trong thư mục dự án và làm theo. Viết hai component và thêm test, 229 test web đều qua, typecheck, lint và build sạch. Agent dừng trước commit để chờ. Chủ dự án bảo merge và push, agent gộp fast-forward vào main mà không mở PR. CI trên GitHub qua hết.
**Bài học:** Khi skill không nạp được, đọc thẳng file hướng dẫn là đường dự phòng. Nhưng repo có quy trình PR thì vẫn nên đi qua PR.
**Artefact:** Chưa chụp. Nên chụp banner và nhãn trong danh sách trước khi công bố, và che địa chỉ hub.
