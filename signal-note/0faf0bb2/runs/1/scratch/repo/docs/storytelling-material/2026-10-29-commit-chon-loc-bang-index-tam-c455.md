---
id: 2026-10-29-commit-chon-loc-bang-index-tam-c455
code: M-PVXT
aliases: [M-PVXT]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2166", "claude:0faf0bb2#L2172", "claude:0faf0bb2#L2176", "claude:0faf0bb2#L2184", "claude:0faf0bb2#L2188", "claude:0faf0bb2#L2191", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3924"]
hook: "Commit 20 file tài liệu mà không đụng phần đang stage dở của người khác"
tension: giup_ma_hai
sides: ["Cần commit ngay phần tài liệu của mình", "Không reset, không stash, giữ nguyên thay đổi dở của người khác"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit chọn lọc bằng index tạm để không đụng thay đổi đang dở của người khác

**Bối cảnh:** Repo có sẵn thay đổi đang stage trong company/ và README chưa commit.
**Chuyện gì xảy ra:** Mình tạo nhánh docs/opc-research và dùng GIT_INDEX_FILE tạm để commit đúng các file tài liệu của mình, 20 file trong lần đầu. Phần company/ đã stage được giữ nguyên, không reset và không stash. Lần sau (152f378) làm tương tự và quét regex tìm token trước khi commit.
**Bài học:** Khi cây làm việc đang bẩn, commit qua index riêng để giữ nguyên thay đổi của người khác, không reset hay stash.
**Artefact:** Đầu ra git log --stat đã rút gọn.
