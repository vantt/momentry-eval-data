---
id: 2026-11-02-loi-ci-do-tu-cache-rust-3c6e
code: M-1XXV
aliases: [M-1XXV]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1272", "claude:2dfb5915#L1372", "claude:2dfb5915#L1452"]
hook: "Cache CI xoá hết file nhưng giữ lại thư mục rỗng, và thế là đủ làm hỏng"
tension: nho_ma_to
sides: ["Thư mục rỗng chẳng chứa gì", "Nó làm cache hỏng và cả các lần chạy sau đều đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi CI đỏ từ cache: rust-cache xoá file ngoài target nhưng giữ thư mục rỗng

**Bối cảnh:** CI đỏ trên cả ba nền sau một lần merge, bước so khớp parity lỗi vì thư mục dump không có manifest.
**Chuyện gì xảy ra:** Swatinem/rust-cache lưu target/ nhưng xoá mọi file ngoài thư mục build, giữ lại thư mục rỗng. Lần chạy đầu ghi thư mục con vào target/parity rồi lưu cache hỏng; các lần sau khôi phục đúng cache đó và bị từ chối ghi đè. Sửa bằng cách ghi dump ra RUNNER_TEMP, ngoài cache.
**Bài học:** Đừng ghi kết quả sinh ra vào thư mục mà cache của CI sẽ dọn; ghi ra thư mục tạm.
**Artefact:** Sơ đồ hai lần chạy CI (cache hỏng → lần sau lỗi); không có dữ liệu nhạy cảm.
**Góc người ngoài:** cách làm phổ biến là Xoá cache thủ công hoặc chạy lại CI đến khi xanh; khi bị từ chối vì billing thường tưởng code lỗi; ở đây khác ở Agent đọc thông báo lỗi của GitHub, tách lỗi hạ tầng khỏi lỗi code, và đề xuất đúng hành động cho người dùng. Người đọc muốn biết cách phân biệt để khỏi sửa nhầm code.
