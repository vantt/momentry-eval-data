---
id: 2026-10-29-token-gateway-khong-co-trong-moi
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:0faf0bb2#L891", "claude:0faf0bb2#L894", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1123"]
hook: "Lấy token thật từ tiến trình đang chạy, không in ra dòng nào"
tension: khac
sides: ["Cần token thật để chạy script", "Không để lộ token ở màn hình, dòng lệnh hay repo"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Token gateway không có trong môi trường của lệnh: đọc từ tiến trình đang chạy và không in ra

**Bối cảnh:** Script tạo agent cho Paperclip cần token của gateway OpenClaw. Lệnh chạy lại trong shell mới không có biến môi trường đó nên KeyError.
**Chuyện gì xảy ra:** Token thật nằm trong môi trường của tiến trình gateway đang chạy. Mình đọc nó từ /proc của tiến trình đó, không in ra màn hình và không đưa vào dòng lệnh. Cách này cũng được dùng cho các script sau, và các script được chép vào repo không chứa bí mật.
**Bài học:** Lấy secret từ tiến trình đang chạy thay vì truyền qua dòng lệnh, để không lộ trong lịch sử shell hay log.
**Artefact:** Đoạn lệnh đọc /proc đã che PID và tên biến.
**Góc người ngoài:** cách làm phổ biến là Dev thường copy token vào file .env hoặc dán thẳng vào lệnh/chat, hoặc hard-code tạm trong script rồi quên xoá. Ít ai nghĩ tới việc lấy từ tiến trình đang chạy; ở đây khác ở Người đọc làm một mình, hay nhờ AI chạy lệnh, dễ để lộ token trong lịch sử shell, log hoặc commit. Cách này cho thấy AI chạy được việc cần bí mật mà không phải nhìn thấy bí mật, và có bước quét secret trước khi commit.
