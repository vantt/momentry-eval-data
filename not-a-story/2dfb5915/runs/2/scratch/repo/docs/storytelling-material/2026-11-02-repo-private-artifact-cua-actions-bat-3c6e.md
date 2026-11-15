---
id: 2026-11-02-repo-private-artifact-cua-actions-bat-3c6e
code: M-3JCR
aliases: [M-3JCR]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L1178", "claude:2dfb5915#L3804", "claude:2dfb5915#L3929"]
hook: "Repo public mà artifact vẫn bắt đăng nhập mới tải được"
tension: tuong_ma_hoa_ra
sides: ["Fork public thì ai cũng tải được artifact", "GitHub bắt đăng nhập mới cho tải, bộ cài phải dự phòng bằng gh"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, người làm đang cố đưa bản Rust ra để khách cài bằng một lệnh. Người làm tin repo đã public thì gói tải từ CI ai cũng lấy được, nhưng artifact của GitHub Actions vẫn bắt đăng nhập; chỉ Release mới tải công khai được. Ai làm bộ cài cho người khác nên chọn nguồn theo quyền của người dùng cuối, không theo CI."
audience: dev làm bộ cài và phát hành công cụ CLI
spine_context: "Công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, đang chuyển sang lõi Rust và cần gói OHS cho bộ cài."
spine_context_lines: [profile]
spine_want: "Hoàn tất bản Rust để cài được trên Windows, macOS và Linux."
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Artifact CI của fork OHS vẫn cần đăng nhập GitHub để tải, máy khách không có gh thì không tải tự động được."
spine_obstacle_lines: ["claude:2dfb5915#L1148"]
spine_turn: "Tưởng repo public thì artifact CI ai cũng tải được; hoá ra artifact vẫn cần đăng nhập GitHub, chỉ Release mới tải công khai."
spine_turn_lines: ["claude:2dfb5915#L1143", "claude:2dfb5915#L1148"]
spine_action: Bộ cài tải gói OHS qua artifact CI đã ghim; sau đó repo pkm và release được chuyển sang public.
spine_action_lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L3804", "claude:2dfb5915#L3808"]
spine_outcome: "Release v0.1.0-rc.3 đã phát hành, cài không cần gh đăng nhập nữa."
spine_outcome_lines: ["claude:2dfb5915#L3929"]
spine_takeaway: "Artifact CI và Release khác nhau về quyền tải; với bộ cài cho người dùng cuối, nên dùng Release."
spine_takeaway_lines: ["claude:2dfb5915#L1148"]
completeness: 7
---

# Repo private: artifact của Actions bắt đăng nhập, đến rc.3 đổi sang public

**Góc kể:** Dự án là công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, người làm đang cố đưa bản Rust ra để khách cài bằng một lệnh. Người làm tin repo đã public thì gói tải từ CI ai cũng lấy được, nhưng artifact của GitHub Actions vẫn bắt đăng nhập; chỉ Release mới tải công khai được. Ai làm bộ cài cho người khác nên chọn nguồn theo quyền của người dùng cuối, không theo CI.
**Bối cảnh:** Bộ cài cần tải gói OHS từ artifact CI của fork, còn bản pkm thì nằm trong repo private.
**Chuyện gì xảy ra:** GitHub chỉ cho tải artifact của Actions khi đã đăng nhập, dù fork là public. Người dùng chọn giữ repo private, và bộ cài thử tải công khai trước rồi dự phòng bằng gh. Khi OHS có Release public, nguồn đổi sang Release. Đến rc.3 người dùng chuyển repo sang public, bộ cài không còn cần gh.
**Bài học:** Artifact CI và Release là hai nguồn tải khác nhau về quyền truy cập. Chọn nguồn phát hành theo quyền của người dùng cuối, không theo CI.
**Artefact:** Hai lệnh cài trước và sau khi public (không có tên người).
