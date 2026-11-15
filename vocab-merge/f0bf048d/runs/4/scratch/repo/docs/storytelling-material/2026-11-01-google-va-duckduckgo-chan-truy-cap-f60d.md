---
id: 2026-11-01-google-va-duckduckgo-chan-truy-cap-f60d
code: M-D6QG
aliases: [M-D6QG]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, artefact]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3165"]
hook: "Google và DuckDuckGo chặn server, chỉ Bing trả đúng 3 kết quả"
tension: cam_ma_van_lot
sides: ["Agent SEO cần dữ liệu tìm kiếm Google", "Google trả 429, DuckDuckGo đòi CAPTCHA, chỉ Bing cho 3 kết quả"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Google và DuckDuckGo chặn truy cập từ server, chỉ Bing trả kết quả

**Bối cảnh:** Agent thử tìm kiếm web qua Playwright trên server để đọc tin và so sánh model loa.
**Chuyện gì xảy ra:** DuckDuckGo đòi CAPTCHA; Google trả lỗi 429 và chuyển sang trang sorry; Bing trả được 3 kết quả đầu. Agent SEO cần SERP nên không được cào Google từ server.
**Bài học:** Agent cần SERP thì đi qua API có khoá, đừng dùng trình duyệt cào trang tìm kiếm.
**Artefact:** Bảng so sánh công cụ tìm kiếm và trạng thái bị chặn.
