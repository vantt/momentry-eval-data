---
id: 2026-10-30-mo-hinh-mot-khach-mot-workspace-f60d
code: M-5TZN
aliases: [M-5TZN]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1122", "claude:f0bf048d#L1125", "claude:f0bf048d#L1174", "claude:f0bf048d#L1183", "claude:f0bf048d#L1277"]
hook: "Một khách một workspace: mua bộ nào cài bộ đó"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô hình một khách một workspace, mua bộ nào cài bộ đó

**Bối cảnh:** Gói được cài mặc định vào một workspace chung và gộp nhiều bộ nghiệp vụ vào đó.
**Chuyện gì xảy ra:** Chủ đưa ra mô hình: workspace là đơn vị, khách mua bộ nào thì chỉ có team của bộ đó. Gói nội dung đổi tên thành opc-content và bỏ deploy mặc định. Agent nhận ra lớp hạ tầng của khách (workspace, thành viên, daemon, secret) đang bị ngầm gộp vào bộ, nên đề xuất một manifest cho mỗi khách. Chủ đồng ý, và manifest của khách đầu tiên chạy plan sạch.
**Bài học:** Tách lớp hạ tầng của khách (workspace, người, daemon, secret) khỏi lớp bộ nghiệp vụ. Bộ không được tự tạo workspace.
**Artefact:** Sơ đồ hai lớp: workspace khách ở dưới, các bộ gắn lên trên.
