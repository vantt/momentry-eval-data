---
id: 2026-11-02-ban-sua-ohs-ha-cap-goi-3c6e
code: M-2NBH
aliases: [M-2NBH]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3293"]
hook: "Bản sửa lặng lẽ hạ gói vantt.4 về vantt.3"
tension: giup_ma_hai
sides: ["Bản sửa nhằm giữ đúng phiên bản ghim", "Nó hạ cấp gói mới hơn về bản cũ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Công cụ pkm cài gói OHS vào thư mục riêng theo bản ghim, và nhánh đưa bản ghim mới vào main đang chờ review. Nhánh gốc tin rằng gói khác bản ghim là gói cũ cần thay, nên gói vantt.4 đang có sẵn sẽ bị hạ về vantt.3. Lỗi bị bắt trước khi phát hành và được sửa để chỉ nâng khi gói cũ hơn hoặc không đọc được phiên bản. Ai viết trình cài đặt có ghim phiên bản nên so phiên bản theo thứ tự, không theo việc khác nhau."
audience: dev viết trình cài đặt có ghim phiên bản
spine_context: Công cụ pkm cài gói OHS vào thư mục riêng theo một bản ghim trong main. Nhánh ohs-release-pin đưa bản ghim mới vào main.
spine_context_lines: ["claude:2dfb5915#L3286"]
spine_want: "Đưa nhánh ohs-release-pin vào main cùng bản ghim OHS v0.17.2-vantt.4, và giữ CI xanh."
spine_want_lines: ["claude:2dfb5915#L3286"]
spine_obstacle: "Nhánh gốc thay gói bất cứ khi nào phiên bản khác bản ghim, nên gói vantt.4 đang có sẵn sẽ bị đổi thành vantt.3."
spine_obstacle_lines: ["claude:2dfb5915#L3286"]
spine_turn: Tưởng khác bản ghim nghĩa là gói cũ và thay được; hoá ra gói mới hơn bị hạ xuống bản ghim cũ.
spine_turn_lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3299"]
spine_action: "Thêm hàm so sánh phiên bản theo thứ tự X.Y.Z[-vantt.N]: chỉ nâng khi gói cũ hơn hoặc không đọc được phiên bản; gói đưa vào bằng --ohs không bao giờ bị ghi đè, có test cho việc này."
spine_action_lines: ["claude:2dfb5915#L3286"]
spine_outcome: Main ghim vantt.4. CI trên commit đó xanh trên cả ba hệ điều hành và bốn bản build.
spine_outcome_lines: ["claude:2dfb5915#L3286"]
spine_takeaway: "Khi so phiên bản của gói đã cài, hãy so theo thứ tự, không chỉ xem có khác bản ghim hay không, để không hạ cấp gói mới hơn."
spine_takeaway_lines: ["claude:2dfb5915#L3299"]
completeness: 7
---

# Bản sửa OHS hạ cấp gói mới hơn về bản ghim cũ

**Góc kể:** Công cụ pkm cài gói OHS vào thư mục riêng theo bản ghim, và nhánh đưa bản ghim mới vào main đang chờ review. Nhánh gốc tin rằng gói khác bản ghim là gói cũ cần thay, nên gói vantt.4 đang có sẵn sẽ bị hạ về vantt.3. Lỗi bị bắt trước khi phát hành và được sửa để chỉ nâng khi gói cũ hơn hoặc không đọc được phiên bản. Ai viết trình cài đặt có ghim phiên bản nên so phiên bản theo thứ tự, không theo việc khác nhau.
**Bối cảnh:** Installer thay gói OHS khi phiên bản khác bản ghim.
**Chuyện gì xảy ra:** Gói vantt.4 trong thư mục của pkm bị thay bằng vantt.3 vì ghim là vantt.3, tức là hạ cấp. Review bắt được trước khi phát hành. Sửa: chỉ nâng khi gói cũ hơn hoặc không đọc được phiên bản, và có test cho gói đưa vào bằng cờ.
**Bài học:** So sánh phiên bản theo thứ tự, không theo việc khác nhau.
