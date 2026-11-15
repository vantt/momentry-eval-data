---
id: 2026-11-02-nguoi-dung-dat-lai-thu-tu
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L319", "claude:6a207191#L578", "claude:6a207191#L586", "claude:6a207191#L633"]
hook: "Mất người dùng ở bất kỳ bước nào là mất hẳn, nên UX đứng trước an toàn"
tension: khac
sides: ["An toàn và đúng đắn là nền tảng", "Người dùng bỏ đi ở bước đầu thì chẳng còn gì để bảo vệ"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người dùng đặt lại thứ tự ưu tiên: UX trước, rồi an toàn, đúng đắn, nhanh gọn

**Bối cảnh:** Ban đầu skill coi mọi phần như nhau. Người dùng nói điểm quyết định là chặng đầu: giới thiệu, cài đặt và quick start.
**Chuyện gì xảy ra:** Agent mô tả hành trình người dùng mới gồm đọc giới thiệu, cài, quick start, rồi thấy chạy được; mất người dùng ở bất kỳ bước nào cũng là mất hẳn. Skill có thêm file 03-first-contact với 16 rule, gồm tagline, GIF dưới 40 giây, quick start chạy trong CI và tối đa 3 lệnh sau khi cài. Thứ tự 4 tầng được ghi ở đầu SKILL.md: UX, an toàn, đúng đắn, nhanh gọn. Một rule tầng dưới chỉ được vượt UX khi sắp vi phạm MUST của chính nó.
**Bài học:** Lấy câu hỏi 'người mới mất ở bước nào' làm tiêu chí ưu tiên đầu tiên cho tài liệu hướng dẫn cho agent.
**Artefact:** Sơ đồ 4 bước hành trình người dùng mới và sơ đồ 4 tầng ưu tiên.
