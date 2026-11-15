---
id: 2026-10-09-nguoi-duyet-bat-regression-ma-fixture-4257
code: M-2QJV
aliases: [M-2QJV]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1725", "omp:cd4449ab#L1831", "omp:cd4449ab#L1833", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Mô tả skill thành '>-' vì fixture chỉ kiểm trust"
tension: nho_ma_to
sides: ["Fixture xanh, tưởng migration đúng", "Mô tả thành '>-', tên 'test-audit' thành 'Test Audit'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một skill hub cho AI agent, đang chuyển dữ liệu sang schema phiên bản 3 ở phase 4. Bộ test fixture chỉ kiểm trust nên báo xanh, trong khi khi người duyệt so sánh đầu ra thật thì mô tả skill thành '>-' và tên bị đổi. Người nghe nên quan tâm vì mô tả là thứ agent dùng để định tuyến, nên một bài test chỉ kiểm một phần có thể xanh mà vẫn làm hỏng việc chọn skill."
audience: dev viết công cụ hoặc test migration dữ liệu cho AI agent
spine_context: "Dự án là một skill hub cho AI agent, đang chuyển dữ liệu sang schema phiên bản 3 ở phase 4."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Migration phải giữ nguyên những gì agent nhìn thấy: mô tả, tên và định tuyến."
spine_want_lines: ["omp:cd4449ab#L1713"]
spine_obstacle: Fixture test chỉ kiểm trust nên bỏ sót regression ở mô tả và tên.
spine_obstacle_lines: ["omp:cd4449ab#L1713"]
spine_turn: Fixture báo xanh nên tưởng migration đúng; hoá ra mô tả skill thành '>-' và tên 'test-audit' bị đổi thành 'Test Audit'.
spine_turn_lines: ["omp:cd4449ab#L1713"]
spine_action: "Đọc frontmatter bằng YAML parser thật, đổi thứ tự ưu tiên tên, chỉ ghi khóa repo, và mở rộng test so sánh name, description, status, routing trên đầu ra thật."
spine_action_lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713"]
spine_outcome: Tên 'test-audit' giữ nguyên sau migration trong lần kiểm trên bản sao.
spine_outcome_lines: ["omp:cd4449ab#L1890"]
spine_takeaway: "Trước khi báo xanh, kiểm tên, mô tả, trạng thái và định tuyến trên đầu ra thật; chỉ kiểm trust là chưa đủ."
spine_takeaway_lines: ["omp:cd4449ab#L1713"]
completeness: 7
---

# Người duyệt bắt regression mà fixture bỏ sót: mô tả thành '>-'

**Góc kể:** Dự án là một skill hub cho AI agent, đang chuyển dữ liệu sang schema phiên bản 3 ở phase 4. Bộ test fixture chỉ kiểm trust nên báo xanh, trong khi khi người duyệt so sánh đầu ra thật thì mô tả skill thành '>-' và tên bị đổi. Người nghe nên quan tâm vì mô tả là thứ agent dùng để định tuyến, nên một bài test chỉ kiểm một phần có thể xanh mà vẫn làm hỏng việc chọn skill.
**Bối cảnh:** Sau migration, lead so sánh skill show --json trước và sau, phát hiện mô tả và tên đổi.
**Chuyện gì xảy ra:** Frontmatter của một skill dùng block scalar (>-) nên sau migration mô tả thành '>-', đây là lỗi định tuyến. Tên 'test-audit' thành 'Test Audit'. Fixture ban đầu chỉ kiểm trust nên không bắt được. Agent đổi sang YAML parser thật và đặt thứ tự ưu tiên tên. Sau sửa, tên giữ 'test-audit' (L1890).
**Bài học:** Kiểm tra name, description, status và routing trên output thật trước khi báo xanh; chỉ kiểm trust là không đủ.
**Artefact:** Bảng JSON trước và sau migration cho ba skill; che tên người và đường dẫn.
