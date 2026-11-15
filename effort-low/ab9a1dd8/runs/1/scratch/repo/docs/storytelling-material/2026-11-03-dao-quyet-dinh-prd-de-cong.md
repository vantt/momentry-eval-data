---
id: 2026-11-03-dao-quyet-dinh-prd-de-cong
date: 2026-11-03
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L1718"]
hook: "Từ in đoạn cấu hình sang tự ghi file người dùng: 300 dòng"
tension: khac
sides: ["chỉ in đoạn cấu hình thì rẻ và an toàn", "người dùng chọn tự cài, tốn 200-300 dòng và phải sửa PRD"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đảo quyết định PRD: để công cụ tự ghi file cấu hình của người dùng

**Bối cảnh:** PRD ghi rằng công cụ không bao giờ tự sửa settings.json của Claude Code hay file của Codex; người dùng chỉ dán đoạn cấu hình in ra. Hook hỏng im lặng vì đường dẫn Node ghi cứng.
**Chuyện gì xảy ra:** Agent đề xuất hai phương án: chỉ in đoạn cấu hình, hoặc tự cài. Tự cài đòi hỏi sao lưu, từ chối file hỏng, ghi qua file tạm, kiểm lại nếu file bị đổi giữa chừng, ước 200 đến 300 dòng. Người dùng chọn tự cài và yêu cầu sửa PRD mục 3.2, 6.4 và 12 cho khớp.
**Bài học:** Khi đảo một quyết định đã chốt trong tài liệu, đổi tài liệu ngay trong cùng lượt làm việc, kèm lý do đảo; nếu không, tài liệu và code sẽ nói hai điều khác nhau.
**Artefact:** Bảng so sánh hai phương án chỉ in và tự cài, với cột rủi ro và chi phí. Che đường dẫn file cấu hình thật.
