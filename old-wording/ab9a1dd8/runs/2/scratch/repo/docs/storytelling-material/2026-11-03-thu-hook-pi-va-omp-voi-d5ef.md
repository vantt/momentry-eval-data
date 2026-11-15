---
id: 2026-11-03-thu-hook-pi-va-omp-voi-d5ef
code: M-7YK2
aliases: [M-7YK2]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3935"]
hook: "Báo sai khoá API, nhưng chưa chứng minh được hook đã chạy"
tension: tuong_ma_hoa_ra
sides: ["Lỗi xác thực trông như hook đã chạy trước đó", "Phải đọc hook.log mới biết thật sự"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử hook pi và omp với khoá giả, và cô lập mạng bằng unshare: lỗi xác thực không chứng minh được hook đã chạy

**Bối cảnh:** Muốn đo hook của pi, omp, agy mà không có khoá API thật và không để yêu cầu nào ra ngoài.
**Chuyện gì xảy ra:** Probe pi và omp chạy trong HOME tạm với khoá giả fake-local. omp báo Incorrect API key khi hook đã được cài, nhưng chưa đủ để kết luận hook chạy trước lỗi, cần đọc hook.log. Probe agy chạy trong namespace mạng rỗng bằng unshare -rn. Hook cài thành công và in đường dẫn cấu hình.
**Bài học:** Để đo hook của công cụ có API mà không có khoá thật, dùng khoá giả và namespace mạng rỗng. Lỗi xác thực chỉ là tín hiệu gián tiếp, cần log để xác nhận.
**Artefact:** Dòng 'Incorrect API key provided: fake-local' và output của lệnh unshare. Che token nếu có.
