---
id: 2026-11-02-fuzz-so-khop-voi-ban-goc
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L340", "claude:2dfb5915#L692", "claude:2dfb5915#L1650"]
hook: "Chọn thư viện YAML bằng 40.400 ca ngẫu nhiên: lệch từ 0 đến 21.317"
tension: tuong_ma_hoa_ra
sides: ["5 thư viện YAML trông đều đáng tin, đủ sao và tài liệu", "đo bằng dữ liệu ngẫu nhiên thì lệch từ 0 đến 21.317 ca"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fuzz so khớp với bản gốc: sinh 25.000 note YAML ngẫu nhiên, 15.000 note link ngẫu nhiên và 400 lời gọi tool ngẫu nhiên, chạy qua cả Python lẫn Rust, rồi đếm số lệch. Dùng kết quả này để chọn thư viện YAML (5 ứng viên, số lệch từ 0 đến 21.317).

**Chuyện gì xảy ra:** Fuzz so khớp với bản gốc: sinh 25.000 note YAML ngẫu nhiên, 15.000 note link ngẫu nhiên và 400 lời gọi tool ngẫu nhiên, chạy qua cả Python lẫn Rust, rồi đếm số lệch. Dùng kết quả này để chọn thư viện YAML (5 ứng viên, số lệch từ 0 đến 21.317).
**Góc người ngoài:** cách làm phổ biến là Chọn thư viện theo số sao, tài liệu hoặc thử vài ví dụ. Hiếm ai đo mức tương thích bằng dữ liệu ngẫu nhiên trên cả hai phía; ở đây khác ở Quyết định chọn crate có số liệu, không dựa cảm tính. Probe còn phát hiện thư viện panic với block scalar ở cuối frontmatter, một dạng rất thường gặp mà test vài ví dụ sẽ bỏ sót.
