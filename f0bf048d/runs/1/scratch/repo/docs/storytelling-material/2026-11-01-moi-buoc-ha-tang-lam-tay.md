---
id: 2026-11-01-moi-buoc-ha-tang-lam-tay
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2606", "claude:f0bf048d#L3243", "claude:f0bf048d#L3441"]
hook: "Làm tay xong thì dạy lại agent, không ghi runbook rồi bỏ"
tension: khac
sides: ["người vận hành tự làm rồi ghi runbook trong wiki", "agent được dạy lại từng bước và có quy tắc việc nào tự làm, việc nào phải hỏi"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mỗi bước hạ tầng làm tay đều được 'dạy lại' vào skill của agent vận hành rồi deploy lại, và có quy tắc rõ việc nào agent tự làm (đảo ngược được), việc nào phải hỏi (xoá, tiêu tiền, nâng cấp), việc nào chỉ soạn sẵn lệnh sudo cho người chạy.

**Chuyện gì xảy ra:** Mỗi bước hạ tầng làm tay đều được 'dạy lại' vào skill của agent vận hành rồi deploy lại, và có quy tắc rõ việc nào agent tự làm (đảo ngược được), việc nào phải hỏi (xoá, tiêu tiền, nâng cấp), việc nào chỉ soạn sẵn lệnh sudo cho người chạy.
**Góc người ngoài:** cách làm phổ biến là Người vận hành tự làm rồi ghi runbook trong wiki, hiếm khi cập nhật; hoặc agent làm gì cũng hỏi, hoặc làm gì cũng tự làm; ở đây khác ở Runbook là skill mà agent chạy được, nên việc thủ công hôm nay thành tự động hôm sau. Ranh giới theo 'đảo ngược được hay không', và vì thế backup là điều kiện để agent được tự làm nhiều hơn.
