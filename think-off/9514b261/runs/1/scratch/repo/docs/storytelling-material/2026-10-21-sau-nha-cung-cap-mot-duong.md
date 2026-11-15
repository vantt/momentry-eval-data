---
id: 2026-10-21-sau-nha-cung-cap-mot-duong
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1994", "claude:9514b261#L2148", "claude:9514b261#L2284", "claude:9514b261#L2516", "claude:9514b261#L2825", "claude:9514b261#L3219"]
hook: "Sáu nhà cung cấp, lần probe đầu chỉ chạy được 1 trên 6"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sáu nhà cung cấp, một đường dây: probe từ 1/6 lên 6/6 sau nhiều lần chỉnh

**Bối cảnh:** Hội đồng cần nhiều family độc lập, nhưng ban đầu chỉ một family chạy được qua CLI thật.
**Chuyện gì xảy ra:** Lần probe đầu chỉ claude chạy (1/6); các family khác lỗi đăng nhập hoặc không có tài khoản. Sau khi copy session và khai kho tài khoản, deepseek và glm chạy được. Khi openai chuyển sang đường pi và xai chạy qua profile omp đã đăng nhập, cả sáu đều có lượt chạy thành công với exit 0; riêng gemini bị gắn inconclusive vì agent không trả đúng định dạng có cấu trúc.
**Bài học:** Kho tài khoản rỗng nghĩa là fgOS không quản lý tài khoản đó, không phải tài khoản hỏng; đếm bằng probe thật, không đoán từ cấu hình.
**Artefact:** Bảng sáu family: trạng thái lần đầu, lần giữa và lần cuối. Không ghi tên tài khoản.
