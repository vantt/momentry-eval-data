# Nhãn bộ test chất lượng (Q.1), bản nháp

Nhãn cho [plan story-quality](../../../../plans/261104-story-quality/plan.md), mục Q.1. Agent soạn nháp ngày 2026-11-05; anh duyệt. Thư mục này nằm trong `docs/_private/` (gitignore), không commit.

## Các phiên

| id | domain | ngôn ngữ | host | cửa sổ | đáp án | `t` |
|---|---|---|---|---|---|---|
| 9514b261 | quản lý luật/decision và tài khoản LLM (fgOS) | vi | claude | 1-4000 | 7 | 4 |
| 6a207191 | skill chuẩn đóng gói CLI, hub skillstation | mixed | claude | 1-2412 | 8 | 5 |
| ab9a1dd8 | đóng gói, phát hành, thêm host cho momentry | vi | claude | 1-4000 | 8 | 3 |
| 2dfb5915 | điều phối agent port Python sang Rust (pkm) | mixed | claude | 1-4000 | 8 | 4 |
| c4caee3c | fork tìm kiếm Obsidian, gói tiếng Việt | vi | claude | 1-4000 | 8 | 4 |
| 0faf0bb2 | nghiên cứu nền tảng điều phối agent (OPC) | vi | claude | 1-4000 | 8 | 4 |
| f0bf048d | đội agent marketing/SEO, phân quyền máy | vi | claude | 1-3520 | 8 | 4 |
| cd4449ab | migration schema Go, agent thợ do agent lead review | en | omp | 1-4000 | 5 | 2 |

Tổng: 8 phiên, 60 đáp án, 30 nhãn `t`.

- **Codex:** rollout duy nhất trong `~/.codex/sessions` (`01a12e1c`, 15 dòng) chỉ là "Reply with the single word ok", không dùng được. Các profile `~/.codex-*` cũng chỉ có rollout 3–38 dòng. Bộ này **chưa có phiên Codex nào**.
- **Tiếng Anh:** mọi phiên Claude trên máy đều do anh gõ tiếng Việt. Phiên tiếng Anh duy nhất là `cd4449ab` (host omp, model Gemini): người giao việc là một agent lead, nên đây là phiên bán tự động.
- `mixed`: anh gõ tiếng Việt, agent ghi tiến độ bằng tiếng Anh ở nhiều đoạn.
- `cd4449ab` lấy 8 hex cuối của uuid theo quy ước của momentry cho host omp; các phiên khác lấy 8 ký tự đầu.

## Định dạng file

Frontmatter (`session`, `host`, `path`, `window`, `language`, `domain`, `status`) rồi một bảng: `#`, `slug`, `tiêu đề`, `dòng` (khoảng dòng jsonl, gần đúng), `keywords` (3–6 từ, cách nhau dấu phẩy, để so khớp với tiêu đề và tóm tắt máy sinh), `t`, `lý do`.

## Cách duyệt

1. Mở từng file `<id>.md`, đọc tiêu đề và lý do. Cần thì mở transcript ở `path`, đúng khoảng `dòng`.
2. Sửa cột `t`: `x` là chuyện anh thấy thật sự đáng kể, để trống là không.
3. Xoá dòng không phải chuyện; thêm dòng cho chuyện agent bỏ sót (slug kebab-case ASCII, `dòng` gần đúng là được).
4. Sửa `keywords` nếu chưa đúng chữ mà một tiêu đề hay tóm tắt sẽ dùng.
5. Duyệt xong thì đổi `status: draft` thành `status: reviewed`.
