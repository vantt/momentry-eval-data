---
id: 2026-10-21-doi-ten-tai-khoan-cho-thong-fd46
code: M-YSBE
aliases: [M-YSBE]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L2982", "claude:9514b261#L3027", "claude:9514b261#L3070", "claude:9514b261#L3118", "claude:9514b261#L3127", "claude:9514b261#L3153", "claude:9514b261#L3202", "claude:9514b261#L3579", "claude:9514b261#L3600"]
hook: "Đổi tên profile: đếm bảng auth trước, chuyển chỗ tạm thay vì xoá"
tension: khac
sides: ["Muốn tên tài khoản thống nhất theo nhà cung cấp", "Không được mất đăng nhập, nên kiểm trước và không xoá"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Forgent (fgOS) là nền tảng chạy ứng dụng agent. Người làm đang cấu hình các tài khoản LLM qua CLI pi và omp trên máy này.
spine_context_lines: [profile, "claude:9514b261#L3609"]
spine_want: Cài provider TheHive cho pi và omp theo hướng dẫn.
spine_want_lines: ["claude:9514b261#L3609"]
spine_obstacle: "Hướng dẫn được viết cho máy mới, còn máy này đã có tài khoản pi thehive sẵn."
spine_obstacle_lines: ["claude:9514b261#L3620"]
spine_action: Kiểm hiện trạng pi so với hướng dẫn trước khi chạy các bước.
spine_action_lines: ["claude:9514b261#L3620"]
completeness: 4
---

# Đổi tên tài khoản cho thống nhất: đặt tên theo nhà cung cấp, kiểm đăng nhập trước khi di chuyển

**Bối cảnh:** Profile và alias của hai CLI đặt tên lộn xộn, chủ muốn một tên chung theo nhà cung cấp.
**Chuyện gì xảy ra:** Agent tạo rồi bỏ một profile trùng tên. Trước khi đổi tên một profile vừa tạo, agent đếm bảng auth để chắc chưa có đăng nhập, rồi chuyển thư mục đó sang chỗ tạm thay vì xoá. Thư mục tài khoản pi, alias zsh và config được đổi theo. Agent cũng phát hiện bốn alias trỏ tới profile chưa tồn tại và tạo khung cho chúng. Kết quả: 8 tài khoản trong 5 pool.
**Bài học:** Đặt quy tắc tên một lần. Trước khi di chuyển thông tin xác thực, kiểm nó có đăng nhập không, và chuyển sang chỗ tạm thay vì xoá.
**Artefact:** Bảng alias theo CLI, không chứa giá trị khoá. Không cần ảnh.
