---
id: 2026-11-03-ci-lan-dau-do-9-to
date: 2026-11-03
repo: repo
status: raw
signals: [số trước số sau, nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2347", "claude:ab9a1dd8#L2356", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2497", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2548", "claude:ab9a1dd8#L2595", "claude:ab9a1dd8#L2658", "claude:ab9a1dd8#L2810"]
hook: "Linux xanh hết, nhưng macOS và Windows đỏ 9 tổ hợp"
tension: tuong_ma_hoa_ra
sides: ["CI Linux xanh nên tưởng code ổn", "macOS và Windows đỏ 9 tổ hợp, Windows hỏng 38 test"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI lần đầu đỏ 9 tổ hợp: macOS và Windows lộ lỗi mà Linux không thấy

**Bối cảnh:** Ma trận CI gồm ubuntu, macos và windows, mỗi hệ với Node 20, 22 và 24. Linux xanh hoàn toàn trên máy làm việc.
**Chuyện gì xảy ra:** Lần đầu Windows có 38 test hỏng, chủ yếu do test giả định POSIX như chèn đường dẫn thô vào JSON, kiểm quyền 0600 và tách bằng dấu hai chấm. Sau khi sửa, còn 4 hỏng. macOS hỏng vì repo nằm sau symlink /var sang /private/var. Đến lần chạy cuối, Windows còn lỗi ở bước installer vì PowerShell 5.1 làm hỏng đối số JSON khi truyền cho chương trình ngoài và runner chạy quyền Administrator.
**Bài học:** Đưa CI đa nền tảng lên sớm, trước khi viết nhiều code; test viết cho POSIX sẽ hỏng hàng loạt trên Windows và symlink của macOS là bẫy khác.
**Artefact:** Bảng số test hỏng qua từng lần chạy CI: 38, 4, 0. Che tên runner nếu có thông tin cục bộ.
**Góc người ngoài:** cách làm phổ biến là Thường dev sửa một lỗi, đẩy lên, rồi nếu còn đỏ thì mới xem tiếp; ít người đọc log theo từng job song song; ở đây khác ở Agent đếm số lỗi theo từng tổ hợp, theo dõi tiến độ (38 xuống 4) và kiểm lại cả job đã có vẻ chạy xong, nên việc đó có kết quả rõ ràng và không đoán mò.
