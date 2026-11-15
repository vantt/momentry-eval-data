---
id: 2026-10-21-lenh-nhap-khoa-dau-tien-da-fd46
code: M-16KD
aliases: [M-16KD]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
signal_note: "Sự cố vặt: dọn một file sao lưu chứa khoá hỏng, agent hỏi owner trước khi xoá vì file đó là thông tin xác thực."
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3930", "claude:9514b261#L3958", "claude:9514b261#L3962"]
hook: "Bản sao lưu đã cứu khoá cũ, nhưng bản hỏng 25 ký tự vẫn nằm trên đĩa"
tension: khac
sides: ["Lệnh nhập khoá có bản sao lưu", "Bản sao chứa khoá hỏng bị từ chối vẫn còn trên đĩa"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh nhập khoá đầu tiên đã có bản sao lưu nhưng bản sao hỏng vẫn còn trên đĩa

**Bối cảnh:** Sau khi khoá mới được nhận, lệnh có sao lưu đã để lại auth.json.bak chứa khoá bị từ chối.
**Chuyện gì xảy ra:** Agent xác nhận file .bak chứa khoá 25 ký tự bị từ chối và đề nghị xoá. Owner yêu cầu dọn dẹp, agent kiểm độ dài rồi xoá. Một lệnh python đọc JSON lỗi vì trường không phải dict, và agent đọc lại đúng cấu trúc.
**Bài học:** Sao lưu thông tin xác thực để khôi phục là đúng, nhưng phải dọn bản sao khi không còn cần, vì nó là bí mật.
**Artefact:** Không có. Chỉ mô tả: 'đã xoá một file sao lưu khoá hỏng'.
