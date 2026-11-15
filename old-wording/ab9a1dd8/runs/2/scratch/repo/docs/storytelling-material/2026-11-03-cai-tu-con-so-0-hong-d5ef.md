---
id: 2026-11-03-cai-tu-con-so-0-hong-d5ef
code: M-X7VT
aliases: [M-X7VT]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
hook: "205/205 test qua, nhưng người mới chạy init --yes là lỗi"
tension: tuong_ma_hoa_ra
sides: ["205/205 test qua trên clone sạch", "init --yes báo Unknown option, list và check thoát 1"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry là một CLI Node nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị phát hành lần đầu cho người khác cài. Người làm tin rằng 205/205 test xanh là đủ để phát hành, nhưng khi chạy thử từ một HOME trống, init --yes báo lỗi và list, check đều thoát 1. Ai tin test xanh là sẵn sàng phân phối nên thử đường đi của người mới trước khi đóng gói."
audience: dev làm công cụ CLI chuẩn bị phát hành lần đầu
spine_context: "momentry là CLI Node không phụ thuộc gói ngoài, nhặt chuyện từ phiên làm việc với coding agent, đang chuẩn bị đóng gói phân phối lần đầu."
spine_context_lines: [profile]
spine_want: Người mới cài từ con số 0 và chạy được lần đầu thành công trước khi phát hành.
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: init --yes báo Unknown option; init chỉ tạo file cấu hình nên list và check thoát 1 ngay sau quick start.
spine_obstacle_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_turn: Tưởng 205/205 test xanh nghĩa là sẵn sàng phân phối; hoá ra người mới chạy lần đầu vẫn hỏng vì phần cài đặt gần như chưa có.
spine_turn_lines: ["claude:ab9a1dd8#L229", "claude:ab9a1dd8#L236"]
spine_action: "Chạy các bước verify của skill trong HOME tạm, rồi lập bảng có/thiếu và ghi kết luận vào báo cáo audit."
spine_action_lines: ["claude:ab9a1dd8#L223", "claude:ab9a1dd8#L229", "claude:ab9a1dd8#L236"]
spine_outcome: "Phần lõi ổn (205/205 test qua trên clone sạch), nhưng thiếu install, update, uninstall, doctor và --version."
spine_outcome_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_takeaway: Test xanh chỉ chứng minh lõi chạy; phải thử đường đi từ HOME trống mới biết cài đặt có tồn tại không.
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 7
---

# Cài từ con số 0 hỏng: 205/205 test qua nhưng người mới không chạy được lần đầu

**Góc kể:** Dự án momentry là một CLI Node nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị phát hành lần đầu cho người khác cài. Người làm tin rằng 205/205 test xanh là đủ để phát hành, nhưng khi chạy thử từ một HOME trống, init --yes báo lỗi và list, check đều thoát 1. Ai tin test xanh là sẵn sàng phân phối nên thử đường đi của người mới trước khi đóng gói.
**Bối cảnh:** momentry là CLI Node không phụ thuộc gói ngoài, đang chuẩn bị đóng gói phân phối lần đầu. Audit theo skill cs-packaging-distribution.
**Chuyện gì xảy ra:** Audit chạy các bước verify trong HOME tạm: 205/205 test qua trên clone sạch, nhưng 'init --yes' báo Unknown option. init chỉ tạo file cấu hình, chưa có hộp chuyện, nên 'list' và 'check' thoát 1 ngay sau quick start. Kết luận: phần lõi ổn, nhưng install, update, uninstall, doctor và --version gần như chưa có.
**Bài học:** Test xanh chỉ chứng minh lõi chạy. Phải thử đường đi từ con số 0 trong HOME trống mới biết cài đặt có tồn tại không.
**Artefact:** Bảng 'có gì / thiếu gì' của audit, hoặc log terminal của 'init --yes' báo lỗi. Che đường dẫn HOME.
