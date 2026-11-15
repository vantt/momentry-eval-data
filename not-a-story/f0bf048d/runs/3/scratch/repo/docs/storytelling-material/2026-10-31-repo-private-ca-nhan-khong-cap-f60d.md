---
id: 2026-10-31-repo-private-ca-nhan-khong-cap-f60d
code: M-HMER
aliases: [M-HMER]
date: 2026-10-31
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2289", "claude:f0bf048d#L2354", "claude:f0bf048d#L2367", "claude:f0bf048d#L2373"]
hook: "Agent đề xuất quyền chỉ đọc, kiểm tài liệu thì repo cá nhân không có"
tension: nguoi_dung_may_sai
sides: ["Agent đề xuất cấp quyền chỉ đọc cho bot trên repo private cá nhân", "Tài liệu GitHub chỉ cho quyền ghi, agent tự nhận sai khi kiểm lại"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo private cá nhân không cấp quyền chỉ đọc: đề xuất sai rồi đính chính

**Bối cảnh:** Cần bot đọc repo GitHub để chạy, nhưng không muốn bot ghi được vào main.
**Chuyện gì xảy ra:** Agent đề xuất cấp quyền chỉ đọc cho bot trên repo private của tài khoản cá nhân. Khi kiểm tài liệu GitHub, không làm được: repo private cá nhân chỉ cấp được quyền ghi. Agent nhận sai và xin lỗi. Hai đường còn lại: chuyển sang organization miễn phí (chưa chắc có cài đặt fork) hoặc GitHub Pro khoảng $4 mỗi tháng. Chủ chọn để như hiện tại và ghi nhận phương án hoãn.
**Bài học:** Kiểm tài liệu của nền tảng trước khi đề xuất cấu hình quyền. Ghi rõ đường nào chưa xác nhận được.
**Artefact:** Bảng ba phương án và điều kiện của từng phương án.
