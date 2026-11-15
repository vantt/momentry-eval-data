---
id: 2026-10-09-test-fixture-la-ban-sao-byte
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1613", "omp:cd4449ab#L1774", "omp:cd4449ab#L2384", "omp:cd4449ab#L2492"]
hook: "Fixture là bản sao 1184 dòng của file thật, không phải mẫu rút gọn"
tension: giup_ma_hai
sides: ["Dữ liệu mẫu rút gọn cho test gọn nhẹ", "Chỉ assert chạy qua, bỏ sót các bất biến nghiệp vụ"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test fixture là bản sao byte-for-byte của file thật (distill.yaml 1184 dòng, skill.meta.yaml) đặt trong testdata, kèm kiểm tra trust verdict, upstream status, digest không đổi sau migration

**Chuyện gì xảy ra:** Test fixture là bản sao byte-for-byte của file thật (distill.yaml 1184 dòng, skill.meta.yaml) đặt trong testdata, kèm kiểm tra trust verdict, upstream status, digest không đổi sau migration
**Góc người ngoài:** cách làm phổ biến là Test dùng dữ liệu mẫu rút gọn, chỉ assert test chạy qua, không assert các bất biến nghiệp vụ; ở đây khác ở Assert bất biến (trust, digest, name, description, routing, danh sách tài nguyên) trước/sau thay cho assert 'không lỗi' bắt được regression im lặng khi đổi định dạng lưu trữ.
