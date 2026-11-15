---
id: 2026-10-30-skillstation-hub-chon-loc-skill-qua-f60d
code: M-XRPA
aliases: [M-XRPA]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L571", "claude:f0bf048d#L586", "claude:f0bf048d#L594", "claude:f0bf048d#L606", "claude:f0bf048d#L615", "claude:f0bf048d#L623"]
hook: "Hub skill phải đi vòng proxy vì daemon không thấy home"
tension: cam_ma_van_lot
sides: ["Nối thẳng HTTP trả về đường dẫn trong home chủ", "Daemon bị cắt home nên phải kéo skill về cache qua proxy"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# skillstation: hub chọn lọc skill qua tailnet, phải dùng proxy vì daemon bị cắt home

**Bối cảnh:** Người vận hành hỏi có thể dùng skillstation làm hub chung cho cả hạ tầng Multica không.
**Chuyện gì xảy ra:** skillstation hub chọn lọc một bộ skill và phục vụ qua MCP. Agent nối thẳng qua HTTP sẽ nhận đường dẫn trong home chủ, nhưng daemon chạy với ProtectHome=tmpfs nên không thấy home đó. Vì vậy phải dùng mcp proxy, kéo skill về cache của user daemon. Trên tailnet, hub chỉ nghe trên IP Tailscale, mã mời dùng một lần và hết hạn sau 10 phút. Người vận hành để việc này sau.
**Bài học:** Kiến trúc hub từ xa phải tính tới sandbox của daemon, không chỉ tới mạng. Lỗi đường dẫn có thể là dấu hiệu của sandbox.
**Artefact:** Sơ đồ hub, proxy, cache và daemon.
