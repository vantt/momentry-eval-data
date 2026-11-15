---
id: 2026-11-02-lint-bao-ok-nhung-thoat-ma-c4b4
code: M-HXBH
aliases: [M-HXBH]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L290", "claude:6a207191#L292"]
hook: "Lint in OK, nhưng thoát mã 1 vì thiếu shellcheck"
tension: tuong_ma_hoa_ra
sides: ["output báo OK, 183 rule hợp lệ", "exit code 1 do máy thiếu một công cụ"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lint báo OK nhưng thoát mã 1 vì máy thiếu shellcheck

**Bối cảnh:** Lần đầu chạy lint-guides và kiểm tra cú pháp install.sh.
**Chuyện gì xảy ra:** Script in 'OK: 183 rules, structure valid | install.sh syntax ok' nhưng exit code là 1. Nguyên nhân là shellcheck chưa được cài trên máy, trong khi output vẫn báo OK. Agent xác nhận lỗi do thiếu công cụ, không phải do cấu trúc skill.
**Bài học:** Script kiểm tra nên in rõ lý do exit khác 0 ở dòng cuối, không in OK rồi thoát 1 một cách âm thầm.
**Artefact:** Hai dòng output trên. Không cần che.
