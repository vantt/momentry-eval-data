---
id: 2026-10-09-bao-cao-da-verify-van-sai
date: 2026-10-09
repo: repo
status: raw
signals: ["2"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713", "omp:cd4449ab#L1833", "omp:cd4449ab#L1890"]
hook: "Báo cáo 'đã verify', nhưng description thành chuỗi '>-'"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo ghi đã verify", "Description thành '>-', name đổi thành 'Test Audit'"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Báo cáo 'đã verify' vẫn sai: description thành '>-' và thứ tự name bị đảo

**Bối cảnh:** Sau khi migration đã chạy được, lead so sánh skill show --json trước và sau migration.
**Chuyện gì xảy ra:** Description của herdr-cook-plan thành chuỗi '>-' vì frontmatter dùng block scalar và parser đọc theo dòng. Name của test-audit đổi thành 'Test Audit' vì ưu tiên H1 thay vì frontmatter. Báo cáo trước đó ghi là đã verify, nhưng fixture test không khoá các trường này. Sau khi sửa bằng YAML parser thật và đúng thứ tự name, diff của 3 skill chỉ còn khác ở các trường đã cố ý đổi.
**Bài học:** Test kiểu 'trust không đổi' không đủ; hãy diff đúng output mà agent và người dùng thật sự đọc, trước và sau thay đổi.
**Artefact:** Bảng diff skill show --json trước/sau cho 3 skill, chỉ hiện trường đổi. Che nội dung skill nội bộ.
