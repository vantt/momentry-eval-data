---
session: ab9a1dd8
host: claude
path: ~/.claude/projects/-home-vantt-projects-momentry/ab9a1dd8-2e8c-4156-8f2c-4736da941413.jsonl
window: 1-4000
language: vi
domain: đóng gói, phát hành và thêm host cho momentry
status: reviewed
---
| # | slug | tiêu đề | dòng | keywords | t | lý do |
|---|---|---|---|---|---|---|
| 1 | phan-phoi-gan-nhu-chua-co | Audit packaging: lõi ổn nhưng người mới hay agent chỉ đọc --help không tự cài được | 42-300 | packaging, phân phối, audit, --help, cs-packaging-distribution | x | Mở đầu plan, nêu khoảng trống lớn. |
| 2 | tu-cai-hook | Chọn để momentry tự cài hook thay vì chỉ in ra (ước 200–300 dòng) | 251-340 | hook, tự cài, init, quyết định |  | Trade-off sản phẩm, user chốt. |
| 3 | review-windows-installer | Reviewer tìm 4 lỗi nặng, phần lớn ở nhánh Windows và --home tuỳ chỉnh | 2026-2180 | reviewer, PowerShell 5.1, --home, install-dir, Windows |  | Review bắt lỗi trước khi push. |
| 4 | ci-lan-dau-macos-windows | Push đầu lộ lỗi Linux không thấy: macOS /var symlink, Windows RUNNER~1, 38 lỗi | 2305-2800 | macOS, /private/var, symlink, RUNNER~1, Windows, CI |  | Lỗi chỉ lộ trên hệ điều hành khác. |
| 5 | commit-nham-file-phien-khac | Commit kèm việc đổi tên README do phiên khác stage sẵn; main mất README.md, CI đỏ 9/9 | 2708-2777 | README.md, stage, phiên khác, CI đỏ, package-release |  | Nhiều phiên song song gây lỗi; bài học chỉ stage file của mình. |
| 6 | cat-v010 | Stop hook đòi "tốt đẹp" dẫn tới cắt v0.1.0 và thử lệnh cài một dòng thật | 2948-3042 | v0.1.0, release, tag, Stop hook |  | Phát hành công khai đầu tiên. |
| 7 | ten-su-kien-hook-codex | Đọc mã nguồn Codex: tên sự kiện hook pre_compact sai, cần trusted_hash hoặc bypass | 3052-3213 | Codex, pre_compact, PreCompact, trusted_hash, bypass-hook-trust |  | Lỗi tích hợp chỉ thấy khi đọc nguồn Codex. |
| 8 | host-moi-pi-omp-agy | Thêm host pi, omp, agy và tự tìm profile (4 Codex, 9 pi, 10 omp, 4 agy) | 3306-3985 | pi, omp, agy, Antigravity, profile |  | Mở rộng tính năng, ít giằng xé. |
| 9 | 205-205-test-xanh-nhung-nguoi | 205/205 test xanh nhưng người mới không cài nổi | 170-236, 653 | 205/205, người mới, không cài nổi |  | thêm từ danh sách momentry tìm ra |
| 10 | zsh-va-ham-boc-lam-agent | zsh và hàm bọc làm agent vấp nhiều lần | 109, 1226-1235, 3891 | zsh, hàm bọc, binary, pi |  | thêm từ danh sách momentry tìm ra |
