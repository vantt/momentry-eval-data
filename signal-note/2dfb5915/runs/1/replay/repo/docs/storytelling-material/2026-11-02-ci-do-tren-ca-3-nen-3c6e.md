---
id: 2026-11-02-ci-do-tren-ca-3-nen-3c6e
code: M-N10S
aliases: [M-N10S]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1364"]
hook: "CI đỏ cả 3 nền vì cache xoá thư mục rỗng, máy cục bộ vẫn xanh"
tension: nho_ma_to
sides: ["Chạy cục bộ luôn đúng", "Cache chỉ để lại thư mục rỗng, CI đỏ trên cả 3 nền"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ giúp hỏi Claude Desktop về graph vault Obsidian đang viết lại lõi bằng Rust để khớp với bản Python cũ, và CI đỏ sau nhiều lần merge. Người làm tin thư mục target/ trên CI cũng giữ nguyên như trên máy; hoá ra cache chỉ giữ thư mục build, xoá hết file khác và để lại thư mục rỗng, khiến bước so khớp từ chối ghi đè. Ai ghi file tạm vào cache chia sẻ đều có thể dính, và chạy cục bộ xanh không chứng minh CI xanh."
audience: dev viết CI và công cụ build bằng Rust
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph vault Obsidian, đang viết lại lõi bằng Rust để cho kết quả khớp với bản Python cũ."
spine_context_lines: [profile]
spine_want: Muốn CI xanh trở lại trên các nền sau khi merge.
spine_want_lines: ["claude:2dfb5915#L1263"]
spine_obstacle: "CI đỏ ở ubuntu và macos sau hai lần merge, rồi đỏ trên cả 3 nền."
spine_obstacle_lines: ["claude:2dfb5915#L1265", "claude:2dfb5915#L1364"]
spine_turn: "Tưởng thư mục target/ trên CI giữ nguyên như trên máy; hoá ra cache chỉ giữ target/ nhưng xoá mọi file khác, chỉ để lại thư mục rỗng nên bước so khớp từ chối ghi đè. Chạy cục bộ vẫn xanh vì không ai dọn target/ của máy."
spine_turn_lines: ["claude:2dfb5915#L1364"]
spine_action: "Ghi dump ra $RUNNER_TEMP/rust-dump bằng --dump-out, và thêm --no-fail-fast cho bước test trong CI."
spine_action_lines: ["claude:2dfb5915#L1364", "claude:2dfb5915#L1373"]
spine_outcome: "Các fix đã commit trên main nhưng chưa push, nên chưa biết CI có xanh không; fix cho Windows chưa chạy trên máy Windows."
spine_outcome_lines: ["claude:2dfb5915#L1364"]
spine_takeaway: "Cache CI chỉ giữ thư mục build; đừng ghi đầu ra tạm vào đó, hãy ghi ra thư mục tạm riêng. Chạy cục bộ xanh không chứng minh CI xanh."
spine_takeaway_lines: ["claude:2dfb5915#L1364"]
completeness: 7
---

# CI đỏ trên cả 3 nền vì cache Rust xoá thư mục rỗng: dump không ghi ra ngoài cache thì hết

**Góc kể:** Một công cụ giúp hỏi Claude Desktop về graph vault Obsidian đang viết lại lõi bằng Rust để khớp với bản Python cũ, và CI đỏ sau nhiều lần merge. Người làm tin thư mục target/ trên CI cũng giữ nguyên như trên máy; hoá ra cache chỉ giữ thư mục build, xoá hết file khác và để lại thư mục rỗng, khiến bước so khớp từ chối ghi đè. Ai ghi file tạm vào cache chia sẻ đều có thể dính, và chạy cục bộ xanh không chứng minh CI xanh.
**Bối cảnh:** Bước so khớp mới được thêm vào CI, và từ run sau đó mọi lần chạy đều hỏng dù code không đổi.
**Chuyện gì xảy ra:** Action cache chỉ giữ target và xoá mọi file ngoài thư mục build, chỉ để lại các thư mục rỗng. Run đầu tiên lưu cache trong trạng thái đó, các run sau khôi phục lại đúng trạng thái rỗng và bộ so khớp từ chối ghi đè thư mục không phải dump. Chạy cục bộ thì luôn đúng vì không ai xoá target của máy.
**Bài học:** Đừng ghi đầu ra tạm vào thư mục mà cache chia sẻ quản lý; nếu có thì ghi ra thư mục tạm riêng.
**Artefact:** Trích đoạn lỗi 'exit code 2' và cách sửa bằng --dump-out ra RUNNER_TEMP. Không đưa log đầy đủ.
