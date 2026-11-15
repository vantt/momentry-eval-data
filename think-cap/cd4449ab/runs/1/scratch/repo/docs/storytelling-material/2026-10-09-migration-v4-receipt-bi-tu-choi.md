---
id: 2026-10-09-migration-v4-receipt-bi-tu-choi
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2557", "omp:cd4449ab#L2584", "omp:cd4449ab#L2593", "omp:cd4449ab#L2602", "omp:cd4449ab#L2608", "omp:cd4449ab#L2653", "omp:cd4449ab#L2656", "omp:cd4449ab#L2677", "omp:cd4449ab#L2689", "omp:cd4449ab#L2708", "omp:cd4449ab#L2713", "omp:cd4449ab#L2750", "omp:cd4449ab#L2770", "omp:cd4449ab#L2800"]
hook: "8 lượt test đỏ, rồi nới kiểm tra để migration đi qua"
tension: giup_ma_hai
sides: ["Validator chặn receipt sai hình dạng", "Agent nới luôn check để đi đường tương thích"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v4: receipt bị từ chối vì shape check của distill/

**Bối cảnh:** Test migration v3→v4 tạo receipt rồi gọi mutation.ConfirmMutation.
**Chuyện gì xảy ra:** Test đỏ khoảng 8 lượt với 'proposed mutation is invalid' và 'Canonical schema version is incompatible'. Validator canonical kiểm shape của file distill/ mà migration ghi, còn receipt có before_content nhiều dòng. Agent nới check shape cho file distill/ và xoá schema-version trong test receipt để đi đường tương thích.
**Bài học:** Validator canonical và migration phải dùng chung một định nghĩa shape; khi lệch thì sửa định nghĩa chung, không nới ở một bên.
**Artefact:** Thông báo 'proposed mutation is invalid', che đường dẫn.
