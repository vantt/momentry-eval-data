---
id: 2026-10-09-diff-skill-show-json-truoc-sau-4257
code: M-64AG
aliases: [M-64AG]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, artefact_nhin_duoc]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1728", "omp:cd4449ab#L1729", "omp:cd4449ab#L1731", "omp:cd4449ab#L1831", "omp:cd4449ab#L1833", "omp:cd4449ab#L1872", "omp:cd4449ab#L1873", "omp:cd4449ab#L1875", "omp:cd4449ab#L1876", "omp:cd4449ab#L1878", "omp:cd4449ab#L1879", "omp:cd4449ab#L1881", "omp:cd4449ab#L1882", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Migrate xong, tên 'test-audit' thành 'Test Audit' mà không ai báo"
tension: tuong_ma_hoa_ra
sides: ["migrate trông êm, không lỗi nào", "diff trước/sau lộ tên đã bị đổi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ quản lý skill cho agent đang chuyển dữ liệu của một hub thật sang schema 3. Bộ test trên fixture đã xanh, nên người làm tin migrate giữ nguyên mô tả skill. Trên dữ liệu thật, một skill có mô tả viết kiểu YAML nhiều dòng (>-) nên sau migrate mô tả thành đúng chuỗi \">-\", và resolver dùng mô tả này nên agent bị ảnh hưởng ngay. Ai viết test trên fixture cần so output với dữ liệu thật."
audience: dev viết test và migration cho dữ liệu thật
spine_context: "Một công cụ quản lý skill cho agent (skillhub), đang đưa hub thật lên schema 3."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1462"]
spine_want: Migrate dữ liệu hub thật mà không làm hỏng thứ agent nhìn thấy.
spine_want_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713"]
spine_obstacle: Bộ test trên fixture không bắt được mô tả bị hỏng trên dữ liệu thật.
spine_obstacle_lines: ["omp:cd4449ab#L1713"]
spine_turn: "Tưởng: test fixture xanh nghĩa là migrate giữ nguyên mô tả skill. Hoá ra: một skill dùng YAML nhiều dòng (>-), và sau migrate mô tả thành đúng chuỗi \">-\"."
spine_turn_lines: ["omp:cd4449ab#L1713"]
spine_action: So sánh output skill show --json trước và sau migrate trên bản sao hub thật.
spine_action_lines: ["omp:cd4449ab#L1888"]
spine_outcome: "Diff của test-audit: tên vẫn 'test-audit' sau migrate. Kết quả cho mô tả của skill có YAML nhiều dòng không có trong trích đoạn."
spine_outcome_lines: ["omp:cd4449ab#L1890"]
spine_takeaway: Test trên fixture không thay được việc so output trước và sau trên dữ liệu thật.
spine_takeaway_lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1890"]
completeness: 7
---

# Diff skill show --json trước/sau: tên đổi thành Test Audit

**Góc kể:** Một công cụ quản lý skill cho agent đang chuyển dữ liệu của một hub thật sang schema 3. Bộ test trên fixture đã xanh, nên người làm tin migrate giữ nguyên mô tả skill. Trên dữ liệu thật, một skill có mô tả viết kiểu YAML nhiều dòng (>-) nên sau migrate mô tả thành đúng chuỗi ">-", và resolver dùng mô tả này nên agent bị ảnh hưởng ngay. Ai viết test trên fixture cần so output với dữ liệu thật.
**Bối cảnh:** Lead yêu cầu diff output JSON của ba skill trước và sau migrate, dùng binary bản main làm mốc.
**Chuyện gì xảy ra:** Lần chạy đầu, binary main báo lỗi vì bản clone chưa có runtime/catalog/pointer.json. Phải migrate ngược về v2 và rebuild để có mốc trước. Diff lộ ra tên đổi: test-audit thành 'Test Audit', vì tên lấy từ H1 thay vì id. Sau khi sửa thứ tự ưu tiên tên (meta name khác frontmatter, rồi frontmatter, rồi H1, rồi id), tên trở lại 'test-audit'.
**Bài học:** Mốc trước phải lấy từ binary cũ trên cùng dữ liệu; diff JSON nhìn thấy thứ mà test assert không thấy.
**Artefact:** Bảng diff hai cột trước/sau cho các trường name, description, status; che đường dẫn.
