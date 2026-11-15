---
id: 2026-11-02-build-loi-giua-chung-de-edges
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1094"]
hook: "Build lỗi một lần, edges cũ nằm lại mãi không ai sửa"
tension: nho_ma_to
sides: ["một lần derive lỗi giữa chừng", "edges sai mãi vì build sau tưởng không có gì đổi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Build lỗi giữa chừng để edges cũ mãi

**Bối cảnh:** Review phase 09 tìm ra lỗi ở đường build thất bại.
**Chuyện gì xảy ra:** Note được lưu trong transaction đầu, derive lỗi sau đó. Lần build sau không thấy file đổi nên không bao giờ sửa lại edges. Python có cùng lỗi. Sửa bằng cờ dirty trong meta, xoá khi build xong. Thêm lock file để hai build không ghi cùng lúc, chờ tối đa 5 phút.
**Bài học:** Đánh dấu trạng thái dở dang trước transaction đầu, và xoá dấu khi xong.
**Artefact:** Không.
