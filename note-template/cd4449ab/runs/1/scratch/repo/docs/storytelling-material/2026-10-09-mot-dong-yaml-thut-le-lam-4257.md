---
id: 2026-10-09-mot-dong-yaml-thut-le-lam-4257
code: M-2JES
aliases: [M-2JES]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2741", "omp:cd4449ab#L2743", "omp:cd4449ab#L2746"]
hook: "Một dòng thụt lề sai khiến cả receipt không đọc được"
tension: nho_ma_to
sides: ["Chỉ một dòng YAML thụt lề sai", "Cả receipt không đọc được: 'did not find expected key'"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một dự án hub kỹ năng cho agent (MCP), đang được đơn giản hoá trong worktree riêng."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: Viết test migration v3 sang v4 với fixture trước Phase 3.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: Test migration đỏ; decoder YAML báo lỗi khi đọc receipt.
spine_obstacle_lines: ["omp:cd4449ab#L2713", "omp:cd4449ab#L2743"]
spine_action: Thử lại chuỗi YAML với block scalar đã sửa và qua decoder thật.
spine_action_lines: ["omp:cd4449ab#L2741", "omp:cd4449ab#L2744"]
spine_outcome: Decode thành công sau khi sửa chỉ báo thụt lề của block scalar.
spine_outcome_lines: ["omp:cd4449ab#L2746"]
completeness: 5
---

# Một dòng YAML thụt lề làm receipt không đọc được

**Bối cảnh:** Test migration v4 ghi receipt WAL chứa nội dung file dạng YAML nhiều dòng.
**Chuyện gì xảy ra:** Test lỗi ở bước đọc receipt. Decoder báo 'did not find expected key' ở dòng 1 (L2743). Gốc là block scalar before_content thiếu thụt lề đúng. Sau khi sửa thành block scalar hợp lệ, decode thành công (L2746). Một dòng thụt lề làm cả receipt không đọc được.
**Bài học:** Đưa chuỗi YAML nhiều dòng qua decoder thật trong test, đừng tin lần dump đầu tiên.
**Artefact:** Hai đoạn YAML lỗi và đúng cạnh nhau; che nội dung nhạy cảm.
