---
id: 2026-10-09-migration-v4-nuot-loi-duyet-cay-4257
code: M-J18G
aliases: [M-J18G]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3989", "omp:cd4449ab#L3999"]
hook: "Một dòng _ = WalkDir nuốt mọi lỗi đọc thư mục khi migrate"
tension: nho_ma_to
sides: ["Một dòng code gọn, bỏ qua lỗi", "Migration lặng lẽ nuốt lỗi, workspace có thể hỏng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án công cụ MCP cho kho skill đang gom mô hình dữ liệu về bản tối giản, và người làm đang chuyển dữ liệu từ v3 sang v4. Người làm tưởng bước migration đã xong sau khi commit, nhưng vòng đọc thư mục vẫn bỏ qua mọi lỗi, nên migrate có thể chạy xong mà thiếu dữ liệu không ai hay. Dev viết migration hay công cụ đọc dữ liệu hàng loạt sẽ muốn biết cách đảm bảo hoặc xong hết, hoặc không đổi gì."
audience: dev viết migration hoặc công cụ đọc dữ liệu hàng loạt
spine_context: "Một dự án công cụ MCP cho kho skill đang gom mô hình dữ liệu về bản tối giản, người làm chuyển dữ liệu từ bản v3 sang v4 theo từng phase."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: "Muốn migration v3→v4 hoặc xong hết, hoặc không đổi gì trong workspace."
spine_want_lines: ["omp:cd4449ab#L3656"]
spine_obstacle: Vòng đọc cây thư mục insight bỏ qua mọi lỗi bằng dấu gạch dưới.
spine_obstacle_lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3962"]
spine_turn: "Tưởng migration đã xong sau khi commit; hoá ra lỗi đọc vẫn bị nuốt, và lead phải chỉ ra."
spine_turn_lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3957"]
spine_action: "Thay mọi lỗi đọc hoặc parse bị bỏ trong v4 bằng lỗi có tên file, rồi viết test với một file insight hỏng."
spine_action_lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3987"]
spine_outcome: Test riêng lúc đầu fail; sau đó toàn bộ package internal/migration chạy xanh.
spine_outcome_lines: ["omp:cd4449ab#L3989", "omp:cd4449ab#L4001"]
spine_takeaway: "Trước khi báo xong, grep các chỗ bỏ qua lỗi (_ =); lỗi bị nuốt không hiện ra trong test xanh."
spine_takeaway_lines: ["omp:cd4449ab#L3962"]
completeness: 7
---

# Migration v4 nuốt lỗi duyệt cây thư mục

**Góc kể:** Một dự án công cụ MCP cho kho skill đang gom mô hình dữ liệu về bản tối giản, và người làm đang chuyển dữ liệu từ v3 sang v4. Người làm tưởng bước migration đã xong sau khi commit, nhưng vòng đọc thư mục vẫn bỏ qua mọi lỗi, nên migrate có thể chạy xong mà thiếu dữ liệu không ai hay. Dev viết migration hay công cụ đọc dữ liệu hàng loạt sẽ muốn biết cách đảm bảo hoặc xong hết, hoặc không đổi gì.
**Bối cảnh:** Migration v4 đọc cây thư mục insight để sinh distill; lỗi đọc bị bỏ qua.
**Chuyện gì xảy ra:** Code có dòng _ = filepath.WalkDir(...), bỏ lỗi đọc. Lead yêu cầu fail-closed: mỗi lỗi đọc hoặc parse phải trả về lỗi có tên file, và khi preview lỗi thì workspace không đổi (L3656). Agent viết test với một file insight bị hỏng.
**Bài học:** Lỗi bị bỏ bằng _ = không lộ ra trong test xanh; quét _ = trước khi báo xong.
**Artefact:** Output grep các chỗ _ = trước khi sửa; che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Bỏ qua file lỗi, ghi cảnh báo rồi đi tiếp, vì như vậy migration không bị dừng giữa chừng; ở đây khác ở Lỗi bị nuốt sẽ làm migrate trên dữ liệu thật xong nhưng thiếu một phần mà không ai biết. Người đọc sẽ hỏi cách đảm bảo 'hoặc xong hết, hoặc không đổi gì' và cách test điều đó.
