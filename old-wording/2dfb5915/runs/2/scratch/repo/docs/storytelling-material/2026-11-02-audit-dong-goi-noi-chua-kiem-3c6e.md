---
id: 2026-11-02-audit-dong-goi-noi-chua-kiem-3c6e
code: M-8NYX
aliases: [M-8NYX]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1063", "claude:2dfb5915#L1078", "claude:2dfb5915#L1132"]
hook: "Báo cáo audit nói chưa kiểm được, nhưng workflow đã chạy xong"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo viết chưa có bằng chứng về action phát hành", "Workflow trước đó đã chạy và kiểm sha256 cả bốn binary"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Audit đóng gói nói chưa kiểm được, hoá ra đã chạy thử được bằng workflow

**Bối cảnh:** Agent audit theo skill đóng gói, chạy chỉ đọc và không dựng được binary vì hook chặn thư mục target.
**Chuyện gì xảy ra:** Audit liệt kê 3 lỗi chặn bản cài đầu tiên trên Windows: pkm.exe cần vcruntime140.dll, không có script cài, và không có hướng dẫn cho người dùng. Khi tổng hợp, agent phát hiện mình đã viết sai: báo cáo nói chưa có bằng chứng về các action trong release, nhưng thực tế workflow_dispatch trước đó đã chạy thành công và kiểm sha256 cả bốn binary.
**Bài học:** Trước khi báo cáo một thứ là chưa kiểm, hãy tra lại lịch sử lần chạy của chính mình.
**Artefact:** Báo cáo audit có bảng theo mức độ (không có đường dẫn máy).
