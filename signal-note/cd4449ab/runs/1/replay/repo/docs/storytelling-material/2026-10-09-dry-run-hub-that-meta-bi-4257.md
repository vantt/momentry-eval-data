---
id: 2026-10-09-dry-run-hub-that-meta-bi-4257
code: M-8R5J
aliases: [M-8R5J]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1481", "omp:cd4449ab#L1490", "omp:cd4449ab#L1523", "omp:cd4449ab#L1529", "omp:cd4449ab#L1592", "omp:cd4449ab#L1594", "omp:cd4449ab#L1657", "omp:cd4449ab#L1673", "omp:cd4449ab#L1675", "omp:cd4449ab#L1679", "omp:cd4449ab#L1690", "omp:cd4449ab#L1712"]
hook: "Migrate chạy ổn trên test, gãy ngay trên bản clone hub thật"
tension: tuong_ma_hoa_ra
sides: ["test xanh, migrate tưởng ổn", "hub thật có .meta/ bị coi là entity"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một hub lưu skill cho AI agent đang chuyển dữ liệu sang schema mới bằng lệnh migrate. Phần migrate đã qua test trên fixture tự viết nên được coi là ổn. Khi chạy thử trên bản sao hub thật, lệnh gãy vì validator coi file .meta/ là entity, trong khi ở schema cũ đó chỉ là metadata. Bài học: test trên dữ liệu tự viết không bảo đảm gì về dữ liệu thật, nên chạy thử trên bản sao thật trước khi báo xong."
audience: dev viết công cụ migrate hoặc quản lý dữ liệu cho AI agent
spine_context: "Một hub lưu skill cho AI agent, đang chuyển dữ liệu của hub sang schema mới bằng lệnh migrate."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Lệnh migrate đưa hub thật lên schema 3 mà không làm hỏng skill nào.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: "Validator coi mọi file trong .meta/ là entity, nhưng ở schema cũ .meta/ là metadata của hub; fixture tự viết lại không chứa dữ liệu thật."
spine_obstacle_lines: ["omp:cd4449ab#L1462"]
spine_turn: Tưởng migrate đã ổn vì chạy đúng trên fixture tự viết; hoá ra bản sao hub thật có .meta/skill.yaml khiến migrate v1→v2 báo lỗi thiếu ID.
spine_turn_lines: ["omp:cd4449ab#L1462"]
spine_action: "Bỏ qua .meta/ khi schema dưới 3 trong canonical, rồi thay fixture tự viết bằng bản sao byte-for-byte của file thật và test cả đường v1→v2→v3."
spine_action_lines: ["omp:cd4449ab#L1529", "omp:cd4449ab#L1655"]
spine_outcome: "Migrate hub thật chạy được lên schema 3, validate qua và trust không đổi."
spine_outcome_lines: ["omp:cd4449ab#L1713"]
spine_takeaway: Fixture tự viết không khớp dữ liệu thật; chạy thử trên bản sao dữ liệu thật trước khi báo xong.
spine_takeaway_lines: ["omp:cd4449ab#L1462"]
completeness: 7
---

# Dry run hub thật: .meta/ bị coi là entity, migrate v1→v2 gãy

**Góc kể:** Một hub lưu skill cho AI agent đang chuyển dữ liệu sang schema mới bằng lệnh migrate. Phần migrate đã qua test trên fixture tự viết nên được coi là ổn. Khi chạy thử trên bản sao hub thật, lệnh gãy vì validator coi file .meta/ là entity, trong khi ở schema cũ đó chỉ là metadata. Bài học: test trên dữ liệu tự viết không bảo đảm gì về dữ liệu thật, nên chạy thử trên bản sao thật trước khi báo xong.
**Bối cảnh:** Hub thật có file .meta/skill.yaml dưới schema v1/v2. Migration được kiểm trên fixture tự viết nên không bắt được lỗi này.
**Chuyện gì xảy ra:** Lead chạy migrate trên bản clone của hub thật và báo lỗi 'canonical entity is missing an ID' ở skills/default/test-audit/.meta/skill.yaml. Gốc là validator coi mọi thứ trong .meta/ là entity canonical, trong khi ở v1/v2 .meta/ là metadata của hub. Sửa: canonical và catalog bỏ qua .meta/skill.yaml khi schema < 3. Sau khi sửa, migrate lên schema 3 và validate qua.
**Bài học:** Fixture tự viết không bao giờ khớp dữ liệu thật; chạy dry run trên bản clone thật trước khi báo xong.
**Artefact:** Bảng trước/sau của lệnh migrate preview trên bản clone, che tên skill và đường dẫn máy.
