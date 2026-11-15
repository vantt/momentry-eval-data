---
id: 2026-10-21-tu-mot-ho-model-chay-duoc-fd46
code: M-ME4M
aliases: [M-ME4M]
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L2148", "claude:9514b261#L2284", "claude:9514b261#L2516", "claude:9514b261#L2577", "claude:9514b261#L2630", "claude:9514b261#L2825", "claude:9514b261#L2913", "claude:9514b261#L3219"]
hook: "Một họ model chạy được lên bốn; một tài khoản treo 300 giây vì thiếu một file"
tension: nho_ma_to
sides: ["Tài khoản treo 200 đến 300 giây, tưởng lỗi nặng", "Nguyên nhân chỉ là profile thiếu agent.db, stderr chỉ ghi skipped missing-file"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ một họ model chạy được lên bốn, và một tài khoản treo 300 giây vì kho đăng nhập thiếu file

**Bối cảnh:** Dự án gọi nhiều CLI model qua nhiều tài khoản. Ban đầu kho tài khoản của fgOS rỗng nên không biết quota.
**Chuyện gì xảy ra:** Lần probe đầu chỉ claude chạy được. Sau khi người dùng copy session và khai pool, deepseek và glm chạy được. Openai thất bại vì codex đứng trước pi trong thứ tự invocation và chiếm lượt, rồi bị hộp thoại đăng nhập hoặc Trust this folder chặn. Xai treo 200 đến 300 giây vì profile omp thiếu agent.db, và stderr chỉ ghi skipped missing-file. Sau khi sửa thứ tự và kho, openai qua pi-herdr exit 0 trong 26 giây, xai exit 0 trong 23 giây. Gemini có một run bị gắn inconclusive dù agent đã trả OK.
**Bài học:** Thứ tự invocation quyết định tài khoản nào được dùng. Kho đăng nhập thiếu file thì gây treo chứ không báo lỗi nhanh.
**Artefact:** Bảng họ model, đường dùng và kết quả qua từng vòng probe. Không kèm tên tài khoản hay email.
**Góc người ngoài:** cách làm phổ biến là Tin vào trạng thái cấu hình hoặc kết quả của lệnh kiểm tra tổng hợp, ví dụ thấy doctor báo pass là coi như xong; ở đây khác ở Cấu hình pass không có nghĩa tài khoản dùng được. Các lần chạy thật phát hiện lỗi đăng nhập và tình trạng treo mà cấu hình không thể hiện.
