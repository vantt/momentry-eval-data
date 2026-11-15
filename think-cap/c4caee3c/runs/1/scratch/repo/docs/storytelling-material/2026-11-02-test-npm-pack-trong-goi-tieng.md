---
id: 2026-11-02-test-npm-pack-trong-goi-tieng
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3474", "claude:c4caee3c#L3486", "claude:c4caee3c#L3545", "claude:c4caee3c#L3712", "claude:c4caee3c#L3745"]
hook: "Test npm pack xanh ở máy mình, đỏ trên CI vì npm 12"
tension: tuong_ma_hoa_ra
sides: ["Test đọc đầu ra npm tưởng luôn là mảng", "npm 12 trả dạng khác nên CI hỏng"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test npm pack trong gói tiếng Việt đọc sai đầu ra npm 12

**Bối cảnh:** Catchup chạy npm 12 đầu tiên trên PATH; npm 12 trả object thay vì mảng.
**Chuyện gì xảy ra:** Test chỉ đọc được mảng nên hỏng trên CI; sửa để đọc cả hai dạng, 23/23 xanh. Sau đó một lần khác đòi build/index.js khi gói chưa compile, sửa thành chỉ kiểm package.json khai đúng thư mục.
**Bài học:** Khi CI dùng phiên bản công cụ khác máy dev, test đọc đầu ra công cụ phải chịu được cả hai dạng.
**Artefact:** Không cần.
