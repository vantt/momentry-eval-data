---
id: 2026-11-02-upstream-khong-tu-duoi-nua-chot
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2663", "claude:c4caee3c#L2685"]
hook: "Bỏ cron 6 giờ, ghim tag thủ công, và gh vẫn trả 404"
tension: khac
sides: ["Chuyển sang đuổi upstream thủ công, ghim tag cho chắc", "Lệnh gh resolve sang repo cha nên trả 404 nếu thiếu GH_REPO"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Upstream không tự đuổi nữa: chốt ghim tag thay cho cron 6 giờ

**Bối cảnh:** Ban đầu catchup chạy theo lịch 6 giờ và tự đẩy tag khi upstream ra bản mới.
**Chuyện gì xảy ra:** Người dùng chọn đuổi theo thủ công. Workflow bỏ lịch, luôn đọc tag ghim trong vantt/upstream.pin, và đồng bộ master chỉ chạy khi được yêu cầu. Lệnh gh workflow run cần GH_REPO, nếu không sẽ resolve sang repo cha và trả 404. Hai lần dry_run đầu đỏ vì một test trong patch.
**Bài học:** Với repo fork, luôn đặt GH_REPO rõ ràng; ghim phiên bản upstream thay vì tự đuổi nếu chưa cần.
**Artefact:** Nội dung file ghim tag, một dòng.
