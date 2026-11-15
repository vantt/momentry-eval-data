---
id: 2026-10-21-probe-sau-nha-cung-cap-kho-fd46
code: M-XBYQ
aliases: [M-XBYQ]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:9514b261#L1949", "claude:9514b261#L1999", "claude:9514b261#L2129", "claude:9514b261#L2148", "claude:9514b261#L2206", "claude:9514b261#L2284", "claude:9514b261#L2630"]
hook: "Kho tài khoản rỗng không có nghĩa là hết tài khoản"
tension: tuong_ma_hoa_ra
sides: ["Provider-capacity trả rỗng, tưởng chỉ claude chạy được", "Chủ copy lại session thì deepseek, glm cũng chạy; ba nhà còn lại lỗi vì lý do khác"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe sáu nhà cung cấp: 'kho tài khoản rỗng' nghĩa là fgOS không quản lý tài khoản nào

**Bối cảnh:** Chủ hỏi các tài khoản còn quota không, và nếu grok hết thì chuyển sang đâu. Hệ thống có lệnh probe-account nhưng kho tài khoản trống.
**Chuyện gì xảy ra:** Lệnh provider-capacity trả về providers rỗng, nên fgOS không biết quota của ai. Lần probe đầu chỉ claude chạy được. Sau khi chủ copy lại session, kho có hai nhà cung cấp, deepseek và glm chạy được; openai, gemini và xai vẫn lỗi vì hết đăng nhập, hiện no-model, hoặc treo ở khâu giao lệnh. Agent chỉ đọc tên file và ngày sửa, không đọc nội dung credential.
**Bài học:** Đừng đổ lỗi quota khi kho tài khoản rỗng. Kiểm kho và trạng thái đăng nhập trước, rồi mới chạy probe nhỏ.
**Artefact:** Bảng kết quả probe theo family, không kèm tài khoản thật. Không cần ảnh.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường thử thủ công từng cái, nhớ kết quả trong đầu, hoặc không lưu kết quả để so sánh; ở đây khác ở Mỗi vòng probe được lưu vào thư mục tạm riêng, có bảng so sánh 'lần trước / lần này', nên thấy ngay cái gì đã đổi sau khi user copy session hay khai thêm tài khoản. Người đọc muốn có cách kiểm trạng thái nhiều dịch vụ mà không mất dấu lịch sử.
