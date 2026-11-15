---
id: 2026-11-03-commit-keo-theo-doi-ten-readme-d5ef
code: M-3HSD
aliases: [M-3HSD]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, dao_quyet_dinh]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L2282", "claude:ab9a1dd8#L2289", "claude:ab9a1dd8#L2300", "claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2769"]
hook: "Một commit lỡ kéo theo đổi tên README, main mất README, CI đỏ hết"
tension: nho_ma_to
sides: ["Commit nhỏ chỉ muốn đẩy phần của mình", "Kéo theo việc đổi tên của phiên khác, main mất README, CI đỏ"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Repo momentry, công cụ đọc phiên làm việc với coding agent, đang đẩy code lên GitHub để CI chạy lần đầu. Người làm tin commit của mình chỉ mang phần việc của nó, nhưng commit đó lại kéo theo việc đổi tên README.md do một phiên khác đã stage sẵn, làm main mất README và CI đỏ. Ai làm nhiều phiên agent trên cùng một repo đều có thể dính cái bẫy index dùng chung này."
audience: dev chạy nhiều phiên coding agent trên cùng repo
spine_context: "Repo momentry, công cụ đọc phiên làm việc với coding agent để nhặt chuyện đáng kể. Người làm đang đẩy code lên GitHub để CI chạy lần đầu."
spine_context_lines: [profile, "claude:ab9a1dd8#L2233"]
spine_want: Đẩy được main lên GitHub để CI chạy lần đầu.
spine_want_lines: ["claude:ab9a1dd8#L2233"]
spine_obstacle: Push bị từ chối vì main trên GitHub có commit mới; sau đó main thiếu README.md nên CI đỏ toàn bộ.
spine_obstacle_lines: ["claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2749"]
spine_turn: Tưởng commit chỉ đẩy phần của mình; hoá ra nó kéo theo việc đổi tên README.md thành README.vi.md do một phiên khác đã stage sẵn.
spine_turn_lines: ["claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2749"]
spine_action: "Rebase lên origin/main, không force; đối chiếu README, hỏi người dùng rồi commit README song ngữ đang có, chỉ đúng 4 file."
spine_action_lines: ["claude:ab9a1dd8#L2290", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766"]
spine_outcome: "Test cục bộ 232 pass, 0 fail; commit README song ngữ đã tạo. Kết quả CI chưa có trong trích đoạn."
spine_outcome_lines: ["claude:ab9a1dd8#L2762", "claude:ab9a1dd8#L2766"]
spine_takeaway: "Index git dùng chung giữa các phiên: chạy git diff --cached trước khi commit và stage đúng từng file."
spine_takeaway_lines: ["claude:ab9a1dd8#L2759", "claude:ab9a1dd8#L2765"]
completeness: 7
---

# Commit kéo theo đổi tên README từ phiên khác, main mất README.md và CI đỏ toàn bộ

**Góc kể:** Repo momentry, công cụ đọc phiên làm việc với coding agent, đang đẩy code lên GitHub để CI chạy lần đầu. Người làm tin commit của mình chỉ mang phần việc của nó, nhưng commit đó lại kéo theo việc đổi tên README.md do một phiên khác đã stage sẵn, làm main mất README và CI đỏ. Ai làm nhiều phiên agent trên cùng một repo đều có thể dính cái bẫy index dùng chung này.
**Bối cảnh:** Hai phiên làm việc cùng một repo. Push bị từ chối vì main có hai commit tài liệu đặt tên từ bên kia.
**Chuyện gì xảy ra:** Agent rebase ba commit lên origin/main, không force, rồi push được. Sau đó commit e78f3ab vô tình đẩy việc đổi tên README.md thành README.vi.md mà phiên khác đã stage sẵn trong index chung. README.md tiếng Anh chưa commit nên main thiếu file này và CI đỏ. User chọn commit README song ngữ đang có; CI xanh lại.
**Bài học:** Index git dùng chung giữa các phiên: luôn git diff --cached trước khi commit và stage đúng từng file.
**Artefact:** Kết quả git diff --cached --stat trước commit (README 115 dòng, README.vi.md 2 dòng).
