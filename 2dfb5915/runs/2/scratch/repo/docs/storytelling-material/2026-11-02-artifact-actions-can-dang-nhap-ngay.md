---
id: 2026-11-02-artifact-actions-can-dang-nhap-ngay
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L2297"]
hook: "Repo public mà tải artifact vẫn bắt đăng nhập"
tension: tuong_ma_hoa_ra
sides: ["repo public thì ai cũng tải được", "artifact vẫn đòi đăng nhập"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Artifact Actions cần đăng nhập ngay cả khi repo public

**Bối cảnh:** Bộ cài phải lấy gói OHS đã build sẵn từ fork.
**Chuyện gì xảy ra:** Artifact của GitHub Actions bắt đăng nhập khi tải, dù repo fork là public. Máy khách chỉ tải được nếu có gh đã đăng nhập. Khi fork đưa gói lên Release, bộ cài tải thẳng không cần đăng nhập. Gói được chuyển sang Release, và đường dẫn --ohs vẫn giữ cho ai đã có gói.
**Bài học:** Đừng dùng artifact CI làm nguồn phân phối cho người dùng. Hãy dùng Release.
**Artefact:** Không.
