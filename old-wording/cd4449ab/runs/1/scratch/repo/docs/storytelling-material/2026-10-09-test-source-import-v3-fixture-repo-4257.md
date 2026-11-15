---
id: 2026-10-09-test-source-import-v3-fixture-repo-4257
code: M-1SWK
aliases: [M-1SWK]
date: 2026-10-09
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2202", "omp:cd4449ab#L2244", "omp:cd4449ab#L2252", "omp:cd4449ab#L2261", "omp:cd4449ab#L2264", "omp:cd4449ab#L2267", "omp:cd4449ab#L2271", "omp:cd4449ab#L2306"]
hook: "Test xanh khi chạy riêng, đỏ khi chạy chung"
tension: tuong_ma_hoa_ra
sides: ["TestGitRevisionAt xanh khi chạy một mình", "make check vẫn đỏ ở một test không liên quan"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test source_import v3: fixture repo file:// phải khớp kiểu Revision và Record

**Bối cảnh:** Test mới kiểm tra source_import trong workspace v3 tạo .meta/skill.yaml giống skill_add. Fixture dùng git repo cục bộ và test đỏ nhiều lần vì kiểu dữ liệu không khớp.
**Chuyện gì xảy ra:** Lỗi xuất hiện lần lượt: URL phải có dạng file://, Revision phải đúng cấu trúc, Record thiếu trường. Có lúc make check đỏ ở một test không liên quan, nhưng TestGitRevisionAt lại xanh khi chạy riêng. Sau khi sửa, các test TestSourceImport xanh.
**Bài học:** Khi test chỉ đỏ trong make check mà xanh khi chạy riêng, hãy kiểm thứ tự chạy và trạng thái dùng chung trước khi sửa code.
**Artefact:** Không có.
