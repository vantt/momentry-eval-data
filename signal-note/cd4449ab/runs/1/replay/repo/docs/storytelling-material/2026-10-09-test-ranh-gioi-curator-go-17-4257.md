---
id: 2026-10-09-test-ranh-gioi-curator-go-17-4257
code: M-X0VY
aliases: [M-X0VY]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, dao_quyet_dinh, nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1928", "omp:cd4449ab#L1931", "omp:cd4449ab#L1945", "omp:cd4449ab#L1958", "omp:cd4449ab#L1960", "omp:cd4449ab#L3374", "omp:cd4449ab#L3377", "omp:cd4449ab#L3449", "omp:cd4449ab#L3457", "omp:cd4449ab#L3473", "omp:cd4449ab#L3485", "omp:cd4449ab#L3488", "omp:cd4449ab#L3490", "omp:cd4449ab#L3493", "omp:cd4449ab#L3500", "omp:cd4449ab#L3502", "omp:cd4449ab#L3518", "omp:cd4449ab#L3520", "omp:cd4449ab#L3596", "omp:cd4449ab#L3617", "omp:cd4449ab#L3620", "omp:cd4449ab#L3622", "omp:cd4449ab#L3678", "omp:cd4449ab#L3683", "omp:cd4449ab#L3695", "omp:cd4449ab#L3699", "omp:cd4449ab#L3701", "omp:cd4449ab#L3711", "omp:cd4449ab#L3713", "omp:cd4449ab#L3956"]
hook: "Gỡ 17 tool cũ: xoá 1650 dòng, thêm 350"
tension: it_ma_nhieu
sides: ["thêm 350 dòng mới", "xoá 1650 dòng, 17 tool biến mất"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án MCP skill hub, làm trong một worktree riêng để hoàn thành phase 4 của đợt tái cấu trúc."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Căn các tool MCP theo bảng contract và gỡ các tool cũ.
spine_want_lines: ["omp:cd4449ab#L3957"]
spine_obstacle: Test ranh giới được viết trước và đỏ ngay.
spine_obstacle_lines: ["omp:cd4449ab#L1933"]
spine_action: "Gỡ curation_tools.go và 17 tool legacy, đăng ký source_list, rồi đồng bộ hai bản SKILL.md."
spine_action_lines: ["omp:cd4449ab#L3485", "omp:cd4449ab#L3956"]
spine_outcome: "Commit gồm 19 file, +350 và -1650 dòng."
spine_outcome_lines: ["omp:cd4449ab#L3956"]
completeness: 5
---

# Test ranh giới curator: gỡ 17 tool, đồng bộ SKILL.md

**Bối cảnh:** Test ranh giới curator khẳng định curator chỉ dùng tool được phép, và hai bản SKILL.md phải giống hệt nhau.
**Chuyện gì xảy ra:** Test viết trước đỏ ngay vì mcpserver vẫn đăng ký tool cũ. Gỡ curation_tools (113 dòng) và 17 tool legacy, đăng ký source_list, rồi đồng bộ hai bản SKILL.md. Test contract SDK đỏ thêm vì bảng annotation vẫn liệt kê tool đã xoá. Commit tổng: 19 file, +350 và -1650 dòng.
**Bài học:** Test ranh giới viết trước cho biết chính xác có bao nhiêu chỗ phụ thuộc vào tool cũ; mỗi tool xoá kéo theo bảng contract và tài liệu.
**Artefact:** Diff stat của commit (19 file, +350/-1650), không kèm tên nhánh.
