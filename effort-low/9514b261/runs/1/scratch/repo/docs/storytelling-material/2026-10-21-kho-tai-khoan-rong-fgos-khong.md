---
id: 2026-10-21-kho-tai-khoan-rong-fgos-khong
date: 2026-10-21
repo: repo
status: raw
signals: [số trước/sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1999", "claude:9514b261#L2284", "claude:9514b261#L2630", "claude:9514b261#L2825"]
hook: "6 tài khoản AI, chỉ 1 chạy được, 1 treo 300 giây"
tension: tuong_ma_hoa_ra
sides: ["Có sáu family tài khoản, tưởng dùng được hết", "Ban đầu chỉ 1 chạy; xai treo 200–300 giây vì profile chưa đăng nhập"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kho tài khoản rỗng: fgOS không quản quota, probe là cách duy nhất biết

**Bối cảnh:** Dàn tài khoản LLM cho hội đồng kiến trúc. Lệnh xem kho tài khoản trả rỗng, nên fgOS không biết còn quota hay không.
**Chuyện gì xảy ra:** Ban đầu chỉ 1 trong 6 family chạy được (claude). Sau khi đồng bộ phiên đăng nhập, deepseek và glm chạy được, lên 4/6. Openai chặn ở hộp thoại Trust của Codex, còn xai treo 200 đến 300 giây khi profile omp không có đăng nhập. Sau khi vô hiệu hoá tài khoản treo, probe xai qua đúng profile đã đăng nhập pass trong 23 giây.
**Bài học:** Probe thật là bằng chứng duy nhất khi hệ không quản quota. Tài khoản chưa đăng nhập nên bị loại ngay, đừng để nó treo cả ghế.
**Artefact:** Bảng family, đường gọi, kết quả probe qua các vòng (tên tài khoản che thành nhãn chung).
