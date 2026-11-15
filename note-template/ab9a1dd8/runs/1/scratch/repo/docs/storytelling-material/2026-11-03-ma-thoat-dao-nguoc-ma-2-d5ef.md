---
id: 2026-11-03-ma-thoat-dao-nguoc-ma-2-d5ef
code: M-7K9E
aliases: [M-7K9E]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L735", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L1797"]
hook: "Đổi mã thoát có thể làm script đọc nhầm đúng chỗ kiểm riêng tư"
tension: chon_mot_mat_mot
sides: ["Giữ bảng mã cũ để script không đọc sai", "Theo chuẩn: 0, 1, 2, chấp nhận thay đổi gây vỡ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "momentry là công cụ đọc transcript phiên làm việc với coding agent, nhặt chuyện đáng kể để kể ra ngoài. Đang chuẩn bị phần đóng gói để người mới cài và chạy được."
spine_context_lines: [profile]
spine_want: "Muốn người dùng cài và chạy được từ đầu trên Windows, WSL, Linux và macOS."
spine_want_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L264"]
spine_obstacle: Người mới không tự đi từ số 0 tới lần chạy đầu thành công; hook có thể hỏng im lặng.
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_action: Đổi mã thoát theo chuẩn trong test và ghi các mục đóng gói vào checklist.
spine_action_lines: ["claude:ab9a1dd8#L300", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908"]
spine_outcome: "Bộ test còn 204 qua, 1 hỏng."
spine_outcome_lines: ["claude:ab9a1dd8#L911"]
completeness: 5
---

# Mã thoát đảo ngược: mã 2 từ 'vi phạm riêng tư' thành 'sai cú pháp'

**Bối cảnh:** CLI đã công bố bảng mã thoát, và script pre-commit có thể đang dựa vào mã 2 để chặn vi phạm riêng tư.
**Chuyện gì xảy ra:** Agent đề xuất giữ bảng cũ vì đổi mã có thể làm script đọc sai đúng ở chỗ kiểm riêng tư, loại sai nguy hiểm nhất. Chủ chọn chuẩn: 0 xong, 1 có lỗi kể cả khi check thấy vi phạm, 2 sai cú pháp. Hai test đổi từ mã 2 sang mã 1, và thay đổi được ghi là Breaking trong CHANGELOG.
**Bài học:** Đổi mã thoát là đổi hợp đồng với script bên ngoài; ghi Breaking trong CHANGELOG và đổi test trong cùng một commit.
**Artefact:** Bảng mã thoát trước và sau, mã 0 đến 5.
