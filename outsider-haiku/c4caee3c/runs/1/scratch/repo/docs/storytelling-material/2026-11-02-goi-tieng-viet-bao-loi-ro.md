---
id: 2026-11-02-goi-tieng-viet-bao-loi-ro
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2755", "claude:c4caee3c#L2771", "claude:c4caee3c#L2863"]
hook: "Thiếu dữ liệu từ điển, gói tiếng Việt báo lỗi thay vì im lặng"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Việt báo lỗi rõ khi thiếu dữ liệu, thay vì im lặng chạy như không có gói

**Bối cảnh:** Một lần đo trên bản gói cũ cho thấy OHS chạy như không có gói khi thiếu thư mục data.
**Chuyện gì xảy ra:** Phát hiện cho thấy gói không khai báo thư mục data trong danh sách file, nên khi cài sẽ thiếu từ điển và OHS im lặng bỏ qua gói. Thư mục data thực ra đã có trong gói từ trước, phát hiện đến từ việc đo trên bản cũ. Sửa: gói báo lỗi rõ khi thiếu dữ liệu.
**Bài học:** Chỉ đo trên bản đã đóng gói thật; bản chạy trong repo có thể che mất lỗi đóng gói.
**Artefact:** Thông báo lỗi khi thiếu dữ liệu.
