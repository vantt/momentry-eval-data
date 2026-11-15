---
id: 2026-10-29-zsh-bien-ky-tu-va-thanh
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L290", "claude:0faf0bb2#L304", "claude:0faf0bb2#L862", "claude:0faf0bb2#L1531", "claude:0faf0bb2#L3229", "claude:0faf0bb2#L3231", "claude:0faf0bb2#L3994"]
hook: "Lệnh đúng cú pháp, nhưng zsh chặn từ ngoài cửa vì dấu ? và ="
tension: nho_ma_to
sides: ["Một dấu ? hoặc = trong lệnh", "zsh báo no matches found, ít nhất 6 lệnh hỏng; thêm ngoặc kép là chạy"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh biến ký tự ? và = thành glob, làm hỏng gh api và grep --include

**Bối cảnh:** Chạy gh api và grep với URL hoặc pattern có ký tự đặc biệt trong shell zsh của máy.
**Chuyện gì xảy ra:** Các lệnh như grep --include=*.tsx và gh api repos/.../commits?per_page=2 báo 'no matches found' hoặc '= not found' ngay từ shell, không tới được công cụ. Lỗi lặp lại ở ít nhất 6 lệnh trong phiên. Mỗi lần chỉ cần đặt tham số trong dấu ngoặc kép là chạy được.
**Bài học:** Trong zsh, luôn đặt trong ngoặc kép các tham số có ?, * hoặc =; lỗi 'no matches found' là lỗi shell, không phải lỗi API.
**Artefact:** Không có.
