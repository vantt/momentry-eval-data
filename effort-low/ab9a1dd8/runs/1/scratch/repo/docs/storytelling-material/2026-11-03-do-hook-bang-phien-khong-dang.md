---
id: 2026-11-03-do-hook-bang-phien-khong-dang
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3091", "claude:ab9a1dd8#L3233", "claude:ab9a1dd8#L3239", "claude:ab9a1dd8#L3910", "claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3932"]
hook: "Khoá API giả mà omp vẫn gọi mạng thật, phải cô lập bằng namespace"
tension: cam_ma_van_lot
sides: ["dùng khoá giả để phiên không gọi được ra ngoài", "omp vẫn gửi yêu cầu tới API thật"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo hook bằng phiên không đăng nhập: omp vẫn gọi mạng thật, phải chặn mạng bằng namespace

**Bối cảnh:** Để biết hook có được gọi trước khi phiên báo lỗi đăng nhập, agent chạy các CLI thật với khoá giả trong HOME tạm.
**Chuyện gì xảy ra:** Phiên Codex trên Windows không gọi hook dù đã bỏ bước duyệt tin cậy. Khi thử omp trên Linux, phiên vẫn gửi yêu cầu tới API thật và nhận lỗi khoá sai, nghĩa là khoá giả không chặn được mạng. Agent chuyển sang unshare -rn để chạy trong namespace mạng rỗng, bảo đảm không có yêu cầu nào ra ngoài.
**Bài học:** Khoá giả không đảm bảo phiên không gọi mạng; chặn mạng bằng namespace khi thử công cụ thật.
**Artefact:** Dòng lỗi API omp (khoá giả) và lệnh unshare. Che khoá và địa chỉ API nếu có.
**Góc người ngoài:** cách làm phổ biến là Người ta thường thử với khoá thật hoặc chỉ tin rằng tool sẽ không gọi mạng; ít ai tự chặn mạng khi đo thử; ở đây khác ở Agent dựng môi trường cô lập ở mức hệ điều hành để đo hook mà không tốn tiền và không gửi dữ liệu đi, một kỹ thuật ít người biết tới.
