---
id: 2026-11-01-kiem-tra-bang-chay-that-khong
date: 2026-11-01
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, "số trước, số sau"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1971", "claude:f0bf048d#L2950", "claude:f0bf048d#L3049", "claude:f0bf048d#L3079", "claude:f0bf048d#L3139", "claude:f0bf048d#L3193", "claude:f0bf048d#L3199"]
hook: "Tôi báo xong nhờ --version, trong khi 3 lượt chạy đã diễn ra"
tension: tuong_ma_hoa_ra
sides: ["kiểm bằng --version và trạng thái online, báo đã xong", "log cho thấy 3 lượt chạy thật đã có từ 17:40, tôi chưa thấy"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm tra bằng chạy thật, không bằng --version

**Bối cảnh:** Sau khi cài xong runtime, agent (tôi) báo 'online' nhưng chưa có lượt chạy nào; người dùng hỏi lại và yêu cầu kiểm chạy thật.
**Chuyện gì xảy ra:** Tôi đã kiểm bằng --version và trạng thái online rồi báo xong, nhưng người dùng nhắc 'anh thấy chạy rồi đấy'; khi đối chiếu log thì đúng là Pi OpenAI và Grok đã có 3 lượt chạy lúc 17:40 mà tôi chưa nhìn thấy. Sau đó tạo agent spike-gemini và giao STU-15, hoàn thành trong khoảng 30 giây, không lỗi, đúng model gemini-3.8-flash.
**Bài học:** Đừng báo 'hoạt động' khi mới kiểm được trạng thái; kiểm một lượt chạy thật, và đối chiếu nhật ký trước khi kết luận chưa chạy.
**Artefact:** Bảng STU-10…14 với kết quả từng issue (đã che đường dẫn và nội dung).
**Góc người ngoài:** cách làm phổ biến là Dev thử agent bằng prompt demo hoặc xem agent chạy vài lệnh rồi tin là ổn. Ít ai thiết kế bài kiểm tra có đáp án giấu sẵn; ở đây khác ở Đây là bài test đầu-cuối có 'đáp án ẩn': biết trước lỗi nhưng không gợi ý, xem agent có tự tìm ra không. Cho kết quả tin cậy hơn nhiều so với hỏi agent 'bạn dùng được tool chưa'. Agent chặn đúng chỗ còn giúp lộ lỗ hổng đóng gói (file key chưa tới).
