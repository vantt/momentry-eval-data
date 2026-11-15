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
hook: "205/205 test qua, người mới vẫn không chạy được lần đầu"
tension: tuong_ma_hoa_ra
sides: ["205/205 test qua trên clone sạch", "init --yes báo Unknown option, list và check thoát 1 ngay sau quick start"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là CLI Node nhặt chuyện từ phiên làm việc với coding agent, và đang chuẩn bị phát hành lần đầu. Người làm tưởng 205/205 test xanh là gần đủ. Khi thử đúng đường người mới đi, trong HOME trống, lệnh init --yes đầu tiên đã báo Unknown option và list, check thoát 1 sau quick start. Test xanh chỉ chứng minh lõi chạy, còn cài đặt và lần chạy đầu mới là chỗ người mới rớt."
audience: "dev làm CLI hoặc công cụ cho dev, sắp phát hành bản đầu tiên"
spine_context: "Momentry là CLI Node nhặt những chuyện đáng kể từ phiên làm việc với coding agent, đang chuẩn bị đóng gói phân phối lần đầu."
spine_context_lines: [profile, "claude:ab9a1dd8#L42"]
spine_want: Người mới cài xong phải chạy được từ con số 0 trước khi phát hành.
spine_want_lines: ["claude:ab9a1dd8#L42", "claude:ab9a1dd8#L236"]
spine_obstacle: Lệnh init --yes báo Unknown option; list và check thoát 1 ngay sau quick start.
spine_obstacle_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_turn: Tưởng 205/205 test xanh là gần đủ để phát hành; hoá ra đường đi thật của người mới hỏng ở khâu cài đặt và lần chạy đầu.
spine_turn_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_action: "Chạy các bước kiểm trong HOME tạm, đi từ con số 0, rồi ghi báo cáo audit."
spine_action_lines: ["claude:ab9a1dd8#L223", "claude:ab9a1dd8#L229"]
spine_outcome: "Báo cáo liệt kê thiếu sót: không có install, update, uninstall, doctor, --version; --help mỏng; hook có thể hỏng im lặng. Bốn điểm cần quyết được đưa cho chủ phiên."
spine_outcome_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L256"]
spine_takeaway: Test xanh chỉ chứng minh lõi chạy; phải thử đường cài đặt từ HOME trống mới biết người mới có dùng được không.
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 7
---

# Cài từ con số 0 hỏng: 205/205 test qua nhưng người mới không chạy được lần đầu

**Góc kể:** Momentry là CLI Node nhặt chuyện từ phiên làm việc với coding agent, và đang chuẩn bị phát hành lần đầu. Người làm tưởng 205/205 test xanh là gần đủ. Khi thử đúng đường người mới đi, trong HOME trống, lệnh init --yes đầu tiên đã báo Unknown option và list, check thoát 1 sau quick start. Test xanh chỉ chứng minh lõi chạy, còn cài đặt và lần chạy đầu mới là chỗ người mới rớt.
**Bối cảnh:** momentry là CLI Node không phụ thuộc gói ngoài, đang chuẩn bị đóng gói phân phối lần đầu. Audit theo skill cs-packaging-distribution.
**Chuyện gì xảy ra:** Audit chạy các bước verify trong HOME tạm: 205/205 test qua trên clone sạch, nhưng 'init --yes' báo Unknown option. init chỉ tạo file cấu hình, chưa có hộp chuyện, nên 'list' và 'check' thoát 1 ngay sau quick start. Kết luận: phần lõi ổn, nhưng install, update, uninstall, doctor và --version gần như chưa có.
**Bài học:** Test xanh chỉ chứng minh lõi chạy. Phải thử đường đi từ con số 0 trong HOME trống mới biết cài đặt có tồn tại không.
**Artefact:** Bảng 'có gì / thiếu gì' của audit, hoặc log terminal của 'init --yes' báo lỗi. Che đường dẫn HOME.
