# Thử góc kể (riêng tư, không commit)

- `haiku/<phiên>/runs/1/capture.json`: danh sách xếp hạng có góc kể của `haiku` (mặc định), dạng bản chụp để trang duyệt đọc. Thêm `angleRun` (đầu ra `momentry angle --json`, có evidence và lý do `none`) và `angleCalls` (USD, token từng lời gọi).
- `sonnet/<phiên>/runs/1/capture.json`: như trên với `sonnet`.
- `sonnet-vs-haiku.md`: hai góc kể cạnh nhau cho từng chuyện; `numbers.json`: số đo.
- `replay/`: hai bản chụp `new-defaults` chép sang, chạy lại bằng `--fake-llm` với `--keep`; `replay/<phiên>/runs/1/replay/` là repo nháp mà `momentry angle` đã ghi (đang mang góc kể `haiku`). `manifest.json` là manifest của lần chạy lại.

Xem và chấm trên trang duyệt:

```sh
node scripts/eval/review.mjs --data docs/_private/eval/angle-trial/haiku
```

Kiểm góc kể lưu vào `docs/_private/eval/angle-trial/haiku/angle-labels/<phiên>.json`.

## Xương chuyện (spine)

- `spine/<phiên>/runs/1/capture.json`: lần chạy cuối của góc kể có xương chuyện, hồ sơ dự án và yêu cầu của chủ phiên (`haiku`, `momentry angle --force --top 10` trên bản chép của `replay/<phiên>/runs/1/replay`, nằm ở `spine/<phiên>/runs/1/scratch/`). Mỗi chuyện có `spine`, `completeness`, và `prevAngle`/`prevAudience` là góc kể `haiku` cũ để xem cạnh nhau. Thêm `angleRun`, `angleCalls`, `profiles` (hồ sơ đã dùng cho góc kể).
- `spine/<phiên>/runs/1/profile-used-by-angles.md`: hồ sơ mà các góc kể đã dùng; hồ sơ trong `scratch/cache/profiles/` là bản viết lại bằng prompt cuối (bỏ câu "tài liệu không nói mục tiêu").
- `spine-v1/`: lần chạy đầu (trước hai chỉnh prompt), 6 none.

```sh
node scripts/eval/review.mjs --data docs/_private/eval/angle-trial/spine
```
