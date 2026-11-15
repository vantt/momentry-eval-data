---
id: 2026-11-02-artifact-ci-khong-tai-an-danh-3c6e
code: M-6E8E
aliases: [M-6E8E]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L1178"]
hook: "Repo công khai mà tải artifact vẫn đòi đăng nhập"
tension: tuong_ma_hoa_ra
sides: ["Repo công khai thì ai cũng tải được artifact", "GitHub vẫn bắt đăng nhập, phải chuyển sang Release"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh cho vault Obsidian, đang viết lại bằng Rust, cần cài được mà không cần Python. Người làm nghĩ repo phụ thuộc OHS là private nên mới phải đăng nhập GitHub. Kiểm lại thì fork đang public, nhưng GitHub vẫn đòi đăng nhập để tải artifact từ Actions. Ai phát hành công cụ kèm gói tải từ CI nên kiểm đường tải có cần đăng nhập không, đừng chỉ nhìn repo public hay private."
audience: dev phát hành công cụ kèm gói tải từ CI
spine_context: "Một công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust để cho kết quả khớp với bản Python."
spine_context_lines: [profile]
spine_want: Muốn phần đóng gói và phân phối được kiểm tra kỹ.
spine_want_lines: ["claude:2dfb5915#L1017"]
spine_obstacle: "Gói OHS lấy từ artifact GitHub Actions của fork, và fork chưa có Release vì bước smoke đang hỏng."
spine_obstacle_lines: ["claude:2dfb5915#L1148"]
spine_turn: "Nghĩ repo OHS là private nên mới cần đăng nhập; kiểm lại thì fork đang public, nhưng artifact vẫn đòi đăng nhập."
spine_turn_lines: ["claude:2dfb5915#L1140", "claude:2dfb5915#L1143", "claude:2dfb5915#L1148"]
spine_action: "Kiểm lại visibility của fork OHS và repo pkm, rồi cho script cài thử tải công khai trước, không được thì dùng gh."
spine_action_lines: ["claude:2dfb5915#L1142", "claude:2dfb5915#L1169"]
spine_outcome: "Khách có gh phải gh auth login; máy không có gh cài OHS bằng tay qua file zip. Khi fork có Release, OHS không cần đăng nhập."
spine_outcome_lines: ["claude:2dfb5915#L1178"]
spine_takeaway: "Trước khi hứa cài một lệnh, kiểm xem đường tải có cần đăng nhập không, kể cả khi repo đã public."
spine_takeaway_lines: ["claude:2dfb5915#L1148"]
completeness: 7
---

# Artifact CI không tải ẩn danh được, nên bộ cài dùng gh rồi chuyển sang Release

**Góc kể:** Một công cụ dòng lệnh cho vault Obsidian, đang viết lại bằng Rust, cần cài được mà không cần Python. Người làm nghĩ repo phụ thuộc OHS là private nên mới phải đăng nhập GitHub. Kiểm lại thì fork đang public, nhưng GitHub vẫn đòi đăng nhập để tải artifact từ Actions. Ai phát hành công cụ kèm gói tải từ CI nên kiểm đường tải có cần đăng nhập không, đừng chỉ nhìn repo public hay private.
**Bối cảnh:** Gói OHS lấy từ artifact GitHub Actions của fork, và fork chưa có Release vì smoke test trên hai nền đang đỏ.
**Chuyện gì xảy ra:** GitHub yêu cầu đăng nhập để tải artifact dù repo công khai, nên máy khách không có gh không tải được. Chủ dự án chọn giữ repo private và installer thử URL công khai trước, dự phòng bằng gh. Sau đó fork đăng Release, nên OHS tải được không cần đăng nhập.
**Bài học:** Đường tải không cần đăng nhập đáng được ưu tiên sớm, không để artifact CI làm nguồn chính.
