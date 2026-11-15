---
id: 2026-11-02-bo-cai-va-phat-hanh-windows
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, artefact]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1073", "claude:2dfb5915#L1148", "claude:2dfb5915#L1163", "claude:2dfb5915#L1257"]
hook: "Bản cài chạy ngon trên máy tôi, máy sạch thiếu một file DLL là chết"
tension: tuong_ma_hoa_ra
sides: ["Chạy được trên máy dev nghĩa là phát hành được", "Máy sạch thiếu vcruntime140.dll, script cài không kiểm sha"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ cài và phát hành Windows: vcruntime140.dll và script cài không kiểm sha

**Bối cảnh:** Audit đóng gói trước bản phát hành đầu tiên trên Windows.
**Chuyện gì xảy ra:** Audit (chạy bằng skill đóng gói) tìm ba chặn: `pkm.exe` cần `vcruntime140.dll` mà máy sạch có thể thiếu, không có chỗ cài cố định, và README thiếu hướng dẫn. Agent sửa bằng CRT tĩnh, script cài kiểm sha256 trước khi thay, và bước CI fail nếu còn phụ thuộc DLL. Repo private buộc script cài có đường dự phòng qua `gh`.
**Bài học:** Với binary Windows, kiểm phụ thuộc DLL trong CI thay vì hy vọng máy đích có sẵn runtime.
**Artefact:** Danh sách DLL import của pkm.exe trước và sau khi build CRT tĩnh.
**Góc người ngoài:** cách làm phổ biến là Gắn tag rồi mới biết pipeline phát hành có chạy không. Lỗi đóng gói lộ ra lúc đã có Release công khai; ở đây khác ở Có thể diễn tập phát hành mà không phát hành. Cùng lúc có một bước audit đóng gói theo checklist tìm ra lỗi như DLL runtime và thiếu script cài từ trước khi có người dùng. Người đọc muốn có đường 'dry run' này cho dự án của mình.
