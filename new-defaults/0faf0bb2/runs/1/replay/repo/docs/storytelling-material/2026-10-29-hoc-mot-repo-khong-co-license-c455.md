---
id: 2026-10-29-hoc-mot-repo-khong-co-license-c455
code: M-0J8R
aliases: [M-0J8R]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L403", "claude:0faf0bb2#L413", "claude:0faf0bb2#L417"]
hook: "Repo không license: học được thiết kế, nhưng không được chép một dòng UI"
tension: khac
sides: ["Repo hợp tầm nhìn nhất", "Không license nên chỉ được học thiết kế, UI phải viết lại"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Học một repo không có license: chỉ học thiết kế, UI phải viết lại

**Bối cảnh:** Distill gr8r-studio: repo chỉ có 3 commit, 1 tác giả, không có license.
**Chuyện gì xảy ra:** Không có license nghĩa là chỉ được học thiết kế, không được copy code. Người dùng hỏi vì sao phải viết lại UI khi viết lại rất tốn công. Agent tìm các project có license dùng được và thấy đã có sẵn ứng viên gần đúng với tầm nhìn.
**Bài học:** Repo không có license là nguồn để học, không phải để fork. Hãy kiểm tra license trước khi đề xuất viết lại hay tái dùng.
**Artefact:** Bảng tổng quan repo: số commit, số tác giả, license.
