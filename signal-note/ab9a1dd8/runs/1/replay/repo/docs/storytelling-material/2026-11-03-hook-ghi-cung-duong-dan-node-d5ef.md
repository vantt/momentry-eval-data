---
id: 2026-11-03-hook-ghi-cung-duong-dan-node-d5ef
code: M-8ZGC
aliases: [M-8ZGC]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L332", "claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L2230"]
hook: "Nâng phiên bản Node, hook im lặng chết mà không ai biết"
tension: nho_ma_to
sides: ["Hook luôn thoát 0 nên trông như vẫn chạy", "Đổi Node hay thư mục là hook vô hiệu, không báo gì"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang đóng gói nó thành bản cài một lệnh. Cấu hình hook được in ra với đường dẫn Node tuyệt đối, người làm coi như vẫn đúng khi dán vào. Hoá ra nâng Node hoặc chuyển thư mục là hook chết mà lệnh vẫn thoát 0, nên không ai biết. Ai viết hook cho công cụ CLI nên tránh đúng bẫy này."
audience: dev viết hook hoặc công cụ CLI có cấu hình trên máy người dùng
spine_context: momentry là công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể; người làm đang đóng gói nó thành bản cài một lệnh.
spine_context_lines: [profile]
spine_want: "Muốn cài và cập nhật chỉ bằng một lệnh, ưu tiên trải nghiệm người dùng."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Cấu hình hook và mẫu /bip in đường dẫn Node tuyệt đối, nên hỏng khi đổi Node hoặc chuyển thư mục."
spine_obstacle_lines: ["claude:ab9a1dd8#L332"]
spine_turn: Coi đường dẫn tuyệt đối in sẵn là vẫn đúng khi dán vào; hoá ra lệnh hook luôn thoát 0 nên hỏng mà không ai biết.
spine_turn_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L322"]
spine_action: "Đổi hook gọi qua lệnh momentry đã cài trên PATH, thay vì đường dẫn Node cố định."
spine_action_lines: ["claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L2230"]
spine_outcome: Hook gọi qua lệnh đã cài; 232 test qua trên Linux. Báo cáo chưa ghi việc nâng Node thật.
spine_outcome_lines: ["claude:ab9a1dd8#L2230"]
spine_takeaway: Hook thất bại im lặng là lỗi tệ nhất; gọi qua một lệnh ổn định trên PATH và có doctor kiểm hook còn chạy.
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 7
---

# Hook ghi cứng đường dẫn Node tuyệt đối: nâng Node là hook chết im lặng

**Góc kể:** momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang đóng gói nó thành bản cài một lệnh. Cấu hình hook được in ra với đường dẫn Node tuyệt đối, người làm coi như vẫn đúng khi dán vào. Hoá ra nâng Node hoặc chuyển thư mục là hook chết mà lệnh vẫn thoát 0, nên không ai biết. Ai viết hook cho công cụ CLI nên tránh đúng bẫy này.
**Bối cảnh:** Cấu hình hook và mẫu /bip đều in đường dẫn node và bin tuyệt đối.
**Chuyện gì xảy ra:** Lệnh hook luôn thoát 0 nên không ai biết nó hỏng. Nâng Node qua nvm hoặc fnm, hay chuyển thư mục clone, làm hook vô hiệu mà không có gì báo. Sửa: installer đặt một shim momentry, hook gọi shim, shim tìm node lúc chạy.
**Bài học:** Hook thất bại im lặng là lỗi tệ nhất. Hook nên gọi qua một lệnh ổn định trên PATH, và có doctor kiểm hook còn chạy được.
**Artefact:** Cấu hình hook trước (đường dẫn tuyệt đối) và sau (lệnh momentry hook). Che đường dẫn home.
