# Góc kể: sonnet và haiku, cạnh nhau

Riêng tư (chứa nội dung phiên). Cùng 10 chuyện đầu bảng mỗi phiên, cùng trích đoạn, cùng prompt.

| | sonnet | haiku |
|---|---|---|
| stories | 20 | 20 |
| angles | 20 | 19 |
| none | 0 | 1 |
| failed | 0 | 0 |
| usdPerSession | 0.2102 | 0.0166 |
| usdPerCall | 0.0210 | 0.0017 |
| retries | 0 | 0 |
| tokInPerCall | 8925 | 9749 |
| tokOutPerCall | 317 | 1366 |
| secsPerCall | 3.6000 | 7.6000 |
| meanChars | 344 | 328 |
| over3Sentences | 6 | 3 |
| meanEvidence | 3 | 2.5000 |

## c4caee3c

### Corpus tiếng Việt quá dễ: baseline 0,93 không đo được gì

- **sonnet:** Điểm tìm kiếm 0,93 trông như hệ thống đã tìm tốt tiếng Việt không dấu. Thật ra tiêu đề note trùng đúng câu hỏi nên tìm theo tiêu đề và vector đã đủ, còn chỗ bỏ dấu của công cụ tìm gần như không được thử. Làm bộ test khó hơn thì điểm tụt còn 0,27 (không dấu) và 0,40 (chữ đ). Ai đang tin một con số benchmark đẹp nên kiểm tra xem bộ test có để lộ đáp án không.
  - *cho:* dev tự xây hoặc đánh giá công cụ tìm kiếm, đặc biệt cho tiếng không phải tiếng Anh · dòng 315, 1044, 1114
- **haiku:** Bộ test tiếng Việt cho kết quả Hit@5 0,93 nên trông tìm kiếm đã tốt. Thật ra mỗi câu tìm đều là tiêu đề của chính ghi chú đó, nên hệ thống tìm được nhờ tiêu đề chứ không nhờ bộ tìm kiếm xử lý được dấu. Khi làm corpus khó hơn, điểm giảm còn 0,27 với chữ không dấu và 0,40 với chữ đ. Benchmark có đáp án lộ ra ngoài sẽ che mất lỗi tìm kiếm, nên cần đo lại với nhiều kiểu gõ.
  - *cho:* dev làm tìm kiếm hoặc đo chất lượng tìm kiếm cho ứng dụng tiếng Việt · dòng 315, 1034, 1044

### Gói tiếng Việt: nDCG@5 0,666 lên 0,932 qua nhiều lớp, và một lớp làm hỏng lớp trước

- **sonnet:** Thêm lớp sửa gõ sai để tìm tốt hơn, tưởng chỉ có lợi. Hoá ra nó âm thầm viết lại những từ đã nằm trong từ điển đồng nghĩa (ví dụ "phone" bị đổi thành một từ gần giống trong vault), nên từ đồng nghĩa không còn khớp và một kết quả tụt từ hạng 4 xuống 7, Hit@5 của vi-synonym rơi xuống 0,73. Ai xếp nhiều lớp xử lý lên cùng một câu tìm kiếm đều có thể dính: lớp sau phải thấy được dạng người dùng gõ gốc.
  - *cho:* dev xây tìm kiếm hoặc pipeline nhiều lớp xử lý văn bản · dòng 1470
- **haiku:** Người làm tin rằng thêm lớp sửa gõ sai sẽ giúp tìm tốt hơn. Nhưng lớp này viết lại truy vấn trước khi lớp từ đồng nghĩa kịp đọc, nên một từ đồng nghĩa người dùng gõ bị đổi thành từ khác trong kho ghi chú, và ghi chú đúng tụt từ hạng 4 xuống hạng 7. Ai xếp nhiều lớp xử lý truy vấn cần kiểm tra lớp sau có thấy dạng gốc mà người dùng gõ hay không.
  - *cho:* dev làm tìm kiếm cho ghi chú tiếng Việt hoặc xếp nhiều lớp xử lý truy vấn · dòng 1470, 1478

### Cùng model ONNX, CPU khác, điểm khác: cổng chất lượng đỏ vì baseline ghi trên máy khác

- **sonnet:** Cổng chất lượng đỏ vì điểm eval 0,735 ghi trên máy agent lệch 0,728 đo trên runner CI, vượt ngưỡng 0,005. Cứ tưởng cùng model thì cùng điểm, nhưng model lượng tử ONNX cho số khác nhau theo loại CPU. Số lặp lại y hệt trên cùng loại CPU, nên chỉ so điểm trong cùng một lần chạy mới đáng tin. Ai dùng eval làm cổng CI đều có thể dính.
  - *cho:* dev đặt cổng chất lượng/eval trong CI cho tính năng dùng model ONNX hoặc AI · dòng 3312, 3370, 3415
- **haiku:** Cổng chất lượng so điểm eval với baseline ghi trên một máy khác và coi đó là chuẩn chung. Hoá ra cùng một model ONNX lượng tử int8 cho điểm khác nhau theo loại CPU: 0,735 trên máy đã ghi, 0,728 trên runner CI, nên lệch quá ngưỡng 0,005 dù code không đổi. Cách sửa là đo bản upstream ngay trong cùng lần chạy, trên cùng máy, rồi so với nó; baseline ghi sẵn chỉ còn dùng để báo độ trôi.
  - *cho:* dev dùng model AI cục bộ và viết test đánh giá chất lượng · dòng 3312, 3349, 3370

### Eval vault thật: tổng tăng 0,600 lên 0,698 nhưng cổng hạng mục đỏ, người dùng quyết

- **sonnet:** Gói tiếng Việt làm điểm tìm kiếm chung tăng từ 0,600 lên 0,698, nên tưởng là tốt hơn hẳn. Nhưng cổng kiểm tra theo từng hạng mục vẫn đỏ: mỗi hạng mục chỉ có 2–6 câu, nên một câu rơi khỏi top 5 đã kéo vi-iy tụt 0,26. Với bộ test nhỏ, điểm theo hạng mục có thể báo hỏng dù bản thân gói không tệ đi.
  - *cho:* dev tự làm eval cho tìm kiếm hoặc RAG trên bộ dữ liệu nhỏ · dòng 3653, 3680, 3682
- **haiku:** Cổng chất lượng theo từng hạng mục được thiết kế để bắt hồi quy, nên tưởng là đọc được kết quả từng mục. Trên vault thật, tổng điểm tăng 0,600 lên 0,698 nhưng cổng vẫn đỏ, vì một câu rơi khỏi top 5 kéo hạng mục vi-iy tụt 0,26. Mỗi hạng mục chỉ có 2 đến 6 câu nên một câu có thể quyết định kết quả cả mục. Ai dùng cổng theo hạng mục cho bộ test nhỏ cần biết điều này.
  - *cho:* dev dùng cổng chất lượng hoặc bộ eval nhỏ cho công cụ tìm kiếm · dòng 3653, 3680

### Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi: nDCG@5 0,57 lên 0,97

- **sonnet:** Người ta hay nghĩ thêm một ngôn ngữ mới thì phải đục vào lõi hệ thống tìm kiếm. Gói tiếng Đức chạy qua điểm cắm P01 mà không sửa lõi, và điểm nDCG@5 trên bộ eval tiếng Đức tăng từ 0,57 lên 0,97, không hạng mục nào tụt. Ai định làm công cụ có plug-in đáng để biết: viết gói ngôn ngữ thứ hai là cách thử thật xem hợp đồng plug-in đã đủ tổng quát chưa.
  - *cho:* dev xây công cụ có hệ plug-in hoặc gói ngôn ngữ · dòng 789, 816, 1114
- **haiku:** **none**: Trích đoạn chỉ ghi kết quả và tiến độ: gói tiếng Đức chạy qua P01 không sửa lõi, nDCG@5 tăng 0,57 lên 0,97. Không có chỗ nào ghi ai tin một điều sai rồi bị bác bỏ. Điểm 'không cần sửa lõi' chỉ là điều kiện trong bài học của chuyện, chưa phải niềm tin bị đảo ngược.

### Phục hồi dấu biến một từ không dấu thành từ khác trong câu có dấu một phần

- **sonnet:** Ngưỡng 50% đúng theo spec nên ai cũng tưởng lỗi nằm ở ngưỡng. Hoá ra ngưỡng không sai: câu "Hội An" chỉ có một nửa âm tiết có dấu nên đi vào nhánh phục hồi, và chữ "An" bị đổi thành "ăn" vì từ này phổ biến hơn trong vault. Lỗi nằm ở cách dựng câu gửi cho model nhúng, và sau khi sửa, nDCG@5 tổng tăng từ 0,932 lên 0,954. Ai làm tìm kiếm có tự động sửa dấu nên cẩn thận với tên riêng.
  - *cho:* dev làm tìm kiếm hoặc nhúng văn bản cho tiếng có dấu · dòng 2776, 2789
- **haiku:** Nhóm nghi ngờ ngưỡng 50% âm tiết có dấu là lỗi khiến từ đã gõ dấu bị đổi. Hoá ra ngưỡng đúng theo quy tắc; lỗi nằm ở cách dựng câu gửi đi: "Hội An" thành "hội ăn", vì chữ "An" bị đổi sang "ăn" là dạng hay gặp hơn. Đổi đúng theo quy tắc vẫn có thể làm sai nghĩa, nên phải chứng minh bằng test trước khi đổi quy tắc.
  - *cho:* dev làm tìm kiếm tiếng Việt · dòng 2776, 2787, 2789

### Cờ restoreForEmbedding giải quyết vi-snippet mà không cần sửa mã

- **sonnet:** Câu tìm kiếm tiếng Việt không dấu làm note đích mất khỏi nhánh tìm theo nghĩa, nên tưởng thuật toán xếp hạng có lỗi. Hoá ra không: bộ khôi phục dấu đã đúng, chỉ là bộ nhúng nhận câu không dấu. Một cờ bật mặc định đưa note đích lên hạng 1, không sửa dòng mã nào. Ai tìm kiếm đa ngôn ngữ nên kiểm xem nhánh nào thiếu ứng viên trước khi sửa thuật toán.
  - *cho:* dev làm tìm kiếm lai (từ khoá + vector) hoặc xử lý văn bản tiếng Việt · dòng 2900, 2927
- **haiku:** Người làm tưởng một câu tìm tiếng Việt không dấu bị xếp sai vì thuật toán, nên định sửa mã. Hoá ra một cờ mặc định đã bật khi gộp nhánh chính: câu được khôi phục dấu thành "quen ngủ", và note đích lên hạng 1 mà không sửa dòng nào. Người dùng AI hằng ngày nên biết: trước khi viết lại logic, hãy kiểm tra xem tuỳ chọn có sẵn đã đủ chưa.
  - *cho:* dev dùng AI, làm công cụ tìm kiếm ghi chú tiếng Việt · dòng 2919, 2927

### Tách từ bật mặc định: vi-compound đã đạt trước nhưng bộ khó cho thấy tác dụng

- **sonnet:** Tổng điểm tìm kiếm tiếng Việt đã đạt 1,00 ở hạng mục từ ghép nên tưởng thêm tách từ cũng chẳng thấy gì. Hoá ra bộ câu từ ghép khó hơn mới lộ tác dụng: điểm tăng từ 0,52–0,79 lên 0,86–1,00, không hạng mục nào tụt. Bộ khó này do agent tự dựng, nên ai đo chất lượng bằng bộ test đã bão hoà nên dựng thêm bộ khó và ghi rõ nguồn gốc của nó.
  - *cho:* dev đo chất lượng tìm kiếm hoặc eval cho tính năng AI · dòng 1672
- **haiku:** Người làm eval tin rằng vi-compound đã đạt 1,00 trước khi tách từ nên tách từ không thể cho thấy thêm gì, và điểm tổng tăng là đủ bằng chứng. Hoá ra bộ đã bão hoà không đo được tác dụng: trên bộ câu từ ghép khó do agent tự dựng, nDCG@5 tăng từ 0,52–0,79 lên 0,86–1,00. Người nghe nên để ý vì một hạng mục đã đạt tối đa có thể che mất hiệu quả thật, nên cần bộ khó riêng.
  - *cho:* dev xây bộ eval cho tìm kiếm và công cụ AI · dòng 1640, 1672

### Từ điển từ ghép: danh sách MIT có thể mang nguồn GPL, đổi sang thống kê dữ liệu CC BY

- **sonnet:** Danh sách từ ghép có giấy phép MIT trông an toàn để dùng. Nhưng repo đó không nói danh sách lấy từ đâu, và 95% trùng với một danh sách GPL, nên giấy phép của bản chép không nói lên nguồn gốc. Agent học lại từ ba bộ dữ liệu CC BY 4.0, không chép mục nào từ danh sách cũ, và kết quả còn tốt hơn: vi-compound trên bộ câu khó tăng từ 0,632 lên 0,983.
  - *cho:* dev dùng dữ liệu hoặc danh sách bên thứ ba trong sản phẩm và lo về giấy phép · dòng 1672, 2862, 2875
- **haiku:** Ai dùng danh sách từ ghép trong một repo MIT đều nghĩ dữ liệu đó đã sạch giấy phép. Hoá ra khoảng 95% danh sách trùng với bộ Viet74K mang giấy phép GPL, nên giấy phép của bản chép không nói được nguồn gốc thật. Agent đã học lại danh sách từ dữ liệu CC BY, không chép mục nào, và kết quả vẫn tốt hơn: 0,983 so với 0,632 của bản gốc. Với ai làm dữ liệu mở, nên kiểm nguồn gốc chứ không chỉ đọc file giấy phép.
  - *cho:* dev làm dữ liệu hoặc thư viện mở cho tiếng Việt · dòng 1672, 2875

### Worktree trong /tmp làm đầy hạn mức, 11 agent cùng hỏng shell

- **sonnet:** Cả 11 agent đang chạy song song thì mọi lệnh shell đều hỏng cùng lúc, nhìn như hỏng cả hệ thống. Thật ra chỉ là /tmp có hạn mức nhỏ, mà mỗi worktree kéo theo khoảng 1,3 GB thư viện nên đầy. Dừng agent, chuyển worktree sang ổ /home rồi cho chạy lại thì việc dở vẫn còn. Ai chạy nhiều agent song song nên đặt worktree trên ổ thật ngay từ đầu.
  - *cho:* dev chạy nhiều agent AI song song, mỗi agent một worktree · dòng 487, 492, 506, 740
- **haiku:** Tưởng thư mục tạm /tmp đủ chỗ cho 11 bản làm việc song song. Hoá ra /tmp có hạn mức, mỗi bản kéo theo khoảng 1,3 GB thư viện nên đầy nhanh; khi đầy, mọi lệnh shell của cả 11 agent cùng hỏng. Ai chạy nhiều agent song song nên kiểm tra chỗ chứa trước khi bắt đầu.
  - *cho:* dev chạy nhiều agent AI song song trên máy cá nhân · dòng 506, 508


## ab9a1dd8

### 205/205 test xanh nhưng người mới không cài nổi

- **sonnet:** 205/205 test đều xanh trên bản clone sạch nên cứ tưởng dự án sẵn sàng cho người mới. Hoá ra README không có bước lấy code, không có version hay install, và `init --yes --json` báo 'Unknown option'. Test xanh chỉ chứng minh lõi chạy đúng, không chứng minh người mới cài được, nên dev nào có bộ test đẹp cũng nên chạy thử quick start từ đầu.
  - *cho:* dev làm CLI hoặc công cụ có bộ test tốt, sắp đưa cho người khác dùng · dòng 170, 232, 236
- **haiku:** Mọi người tin rằng bộ test xanh 205/205 nghĩa là công cụ đã sẵn sàng cho người dùng. Thực tế, trên một bản clone sạch test đúng là qua hết, nhưng README thiếu bước lấy code, và lệnh `init --yes --json` báo lỗi 'Unknown option'. Ai đang phát hành công cụ CLI nên biết test xanh không chứng minh người mới cài được.
  - *cho:* dev phát hành công cụ dòng lệnh · dòng 170, 232

### Reviewer độc lập: hai lỗi làm install và uninstall Windows hỏng

- **sonnet:** 230 test và kiểm thử installer đều xanh nên tưởng cài và gỡ trên Windows ổn. Thực ra test chạy trên Linux, không đụng tới cách PowerShell 5.1 và cmd.exe xử lý dấu nháy: installer báo 'Node quá cũ' cho mọi người, còn uninstall báo thành công mà không xoá được gì. Ai viết công cụ chạy đa nền tảng mà chỉ test trên Linux đều có thể dính.
  - *cho:* dev viết installer hoặc công cụ dòng lệnh chạy cả Windows và Linux · dòng 2010, 2017, 2026
- **haiku:** Agent tưởng đã xong: 230 test xanh và installer chạy trơn trên Linux. Reviewer độc lập đọc code theo hành vi Windows thì thấy cài trên Windows luôn báo 'Node quá cũ' dù máy có Node, còn gỡ cài báo thành công nhưng không xoá được file nào. Test chạy trên Linux không bắt được lỗi kiểu quoting này, nên ai viết công cụ đa nền tảng cần đọc code theo từng nền tảng.
  - *cho:* dev viết công cụ dòng lệnh có installer đa nền tảng · dòng 2017, 2026

### Codex không bao giờ chạy hook: tên sự kiện sai, bị bỏ không báo

- **sonnet:** Momentry ghi cấu hình hook cho Codex xong là coi như hook đã cài, nhưng Codex không chạy hook nào. Tên sự kiện momentry ghi là snake_case (pre_compact, session_start), trong khi Codex dùng hooks.json kiểu Claude và đòi PascalCase (PreCompact, SessionStart). Codex bỏ qua im lặng, không báo lỗi, nên ai tự động cài hook cho nhiều agent cũng có thể tưởng hook đang chạy trong khi nó chưa từng chạy.
  - *cho:* dev viết hook hoặc tích hợp cho nhiều coding agent (Claude Code, Codex) · dòng 3187, 3195, 3205
- **haiku:** Ghi cấu hình hook cho Codex tưởng là đã cài xong. Nhưng Codex yêu cầu tên sự kiện viết kiểu PascalCase, còn code ghi snake_case, nên Codex bỏ qua hook mà không báo lỗi gì. Ai tự cấu hình hook cho công cụ AI có thể đang có hook không bao giờ chạy mà không biết; cách kiểm tra là xem log do chính hook ghi, không chỉ xem file cấu hình đã được ghi.
  - *cho:* dev tự cấu hình hook hoặc plugin cho công cụ AI coding · dòng 3184, 3195, 3228

### Hook chết im lặng vì ghi cứng đường dẫn Node

- **sonnet:** tưởng nâng Node chỉ là việc vặt, hook vẫn chạy. Thật ra cấu hình hook ghi cứng đường dẫn Node tuyệt đối, và lệnh hook luôn thoát 0 nên khi hỏng không ai thấy, cũng không có công cụ nào báo. Ai dùng hook với agent đều có thể mất một lớp kiểm tra (ở đây là kiểm riêng tư) mà không hay biết.
  - *cho:* dev dùng hook của Claude Code hoặc công cụ dòng lệnh tự động hoá · dòng 236, 2230
- **haiku:** Ai dán hook vào ~/.claude/settings.json thường tin rằng nó sẽ chạy mãi. Thực tế, cấu hình ghi cứng đường dẫn Node tuyệt đối, nên khi nâng Node qua nvm/fnm hoặc chuyển thư mục clone, hook chết mà lệnh hook vẫn thoát 0, không ai biết. Bản sửa để hook gọi qua lệnh momentry đã cài, nên nâng Node không làm hook chết nữa.
  - *cho:* dev dùng Claude Code hằng ngày và tự cài hook · dòng 236, 2230

### Mã thoát đảo nghĩa: 2 từ 'vi phạm riêng tư' thành 'sai cú pháp'

- **sonnet:** Tưởng đổi mã thoát cho đúng chuẩn chỉ là chỉnh cho gọn. Thật ra mã 2 đang nghĩa là 'có vi phạm riêng tư', ai dùng `momentry check` làm pre-commit hook hay viết script đọc mã 2 sẽ hiểu sai mà không có lỗi nào báo. Sai đúng ở chỗ kiểm riêng tư là loại sai nguy hiểm nhất, nên đổi mã thoát thực chất là đổi hợp đồng công khai.
  - *cho:* dev viết CLI hoặc script/hook dựa vào mã thoát của công cụ khác · dòng 256, 264, 616
- **haiku:** Script hoặc pre-commit hook dùng mã thoát 2 của `momentry check` để biết có vi phạm riêng tư. Theo chuẩn mới, 2 lại nghĩa là gõ sai cú pháp, còn vi phạm chuyển sang 1. Script cũ không báo lỗi gì mà hiểu sai đúng chỗ kiểm riêng tư.
  - *cho:* dev viết script hoặc git hook gọi công cụ dòng lệnh · dòng 256, 264, 616

### Plan 45/45 chưa đủ: release thật mới đóng được việc

- **sonnet:** Plan đã đánh dấu xong 45/45 việc, nên cứ tưởng là xong. Nhưng stop hook không chịu: CI thật trên máy Windows/macOS lộ ra lỗi mà máy Linux không thấy (symlink trên macOS, tên thư mục ngắn và PowerShell 5.1 trên Windows, 38 test chỉ chạy được trên Linux), và lệnh cài một dòng trong README chỉ chạy được sau khi cắt release v0.1.0 thật. Ai tin 'plan xong, test local xanh' là xong đều có thể dính chuyện này.
  - *cho:* dev dùng AI agent để làm và phát hành công cụ dòng lệnh chạy trên nhiều hệ điều hành · dòng 2230, 2233, 2945, 3042
- **haiku:** Agent báo đã xong 45/45 việc trong plan và CI xanh, nên tưởng là đóng được việc. Hoá ra hook dừng việc lại vì chưa có bản phát hành thật: cài thử từ GitHub mới là bằng chứng. Dev dùng AI agent nên cần nhớ: tick 'xong' trong plan chưa chứng minh được hệ thống chạy được, và trong chuyện này phần hook trên Windows vẫn chưa đo trong phiên thật.
  - *cho:* dev dùng AI agent để viết code và muốn biết khi nào agent thật sự xong việc · dòng 2945, 2948, 3042, 3047

### CI lần đầu: macOS đỏ 2 test, Windows đỏ 38 test

- **sonnet:** Linux xanh cả ba bản Node, nên tưởng code chạy được mọi nơi. Chạy CI thật thì macOS đỏ 2 test vì /var là symlink tới /private/var, Windows đỏ 38 test vì test viết theo kiểu POSIX. Ai chỉ thử trên Linux đều có thể dính, vì test mang theo giả định của hệ điều hành nơi nó được viết.
  - *cho:* dev viết công cụ dòng lệnh trên Linux rồi mới nghĩ tới macOS và Windows · dòng 2318, 2338, 2362, 2513
- **haiku:** Linux xanh cả ba bản Node nên tưởng code chạy được mọi nơi. CI thật trên macOS và Windows cho thấy test viết theo giả định của một hệ điều hành: Windows đỏ 38 test, còn macOS không tìm thấy phiên vì /var là đường dẫn tắt tới /private/var. Ai viết test cho công cụ chạy đa nền tảng đều có thể dính lỗi này.
  - *cho:* dev viết test cho công cụ dòng lệnh chạy đa nền tảng · dòng 2318, 2338, 2362, 2544

### Push bị từ chối, và commit kéo theo việc đổi tên README của phiên khác

- **sonnet:** Agent push lên main một commit trông bình thường, sau khi rebase vì bị từ chối. Nó tưởng chỉ đẩy file của mình, nhưng index dùng chung với một phiên khác đã stage sẵn việc đổi tên README.md thành README.vi.md, nên commit mang theo luôn. Kết quả: main mất README.md và CI đỏ toàn bộ. Ai chạy nhiều phiên agent trên cùng một repo đều có thể dính.
  - *cho:* dev chạy nhiều phiên AI agent song song trên cùng một repo · dòng 2260, 2266, 2269, 2289, 2724, 2733, 2749, 2765
- **haiku:** Agent tưởng commit đẩy lên main chỉ chứa việc của mình, nhưng nó đã kéo theo việc đổi tên README.md thành README.vi.md mà một phiên khác đã stage sẵn. Hậu quả là main mất README.md và CI đỏ toàn bộ. Ai chạy nhiều phiên AI trên cùng một repo cần biết index dùng chung có thể làm commit của mình chứa thay đổi không phải của mình.
  - *cho:* dev chạy nhiều phiên AI trên cùng một repo git · dòng 2733, 2749

### Antigravity không có sự kiện kết thúc: gom chuyện khi mở phiên sau

- **sonnet:** Định gom chuyện lúc phiên kết thúc như với Claude Code, nhưng Antigravity chỉ có SessionStart và Stop, không có sự kiện kết thúc. Stop lại chạy sau mỗi lượt và chặn agent đang chạy, nên không dùng để gom được; cách còn lại là gom ở lúc mở phiên sau. Ai viết công cụ chạy trên nhiều agent khác nhau đừng mặc định host nào cũng có SessionEnd.
  - *cho:* dev làm công cụ/hook chạy trên nhiều AI coding agent · dòng 3427, 3433
- **haiku:** Dễ tưởng công cụ AI nào cũng có sự kiện báo khi phiên kết thúc để gom chuyện đúng lúc. Antigravity thì không: chỉ có sự kiện mở phiên và Stop, mà Stop chạy sau mỗi lượt và chặn agent trong lúc chạy, nên phải gom khi mở phiên sau. Ai viết hook cho nhiều công cụ nên kiểm tra sự kiện có sẵn trước khi chọn thời điểm gom.
  - *cho:* dev viết hook hoặc extension cho công cụ AI dòng lệnh · dòng 3410, 3427, 3433

### Ba host mới: một người có nhiều profile, số lượng tìm được

- **sonnet:** Công cụ gom chuyện từ các agent AI mặc định mỗi agent chỉ có một thư mục dữ liệu. Quét thử trên một máy thì ra 4 thư mục Codex, 9 của pi, 10 của omp và 4 của agy, vì mỗi tài khoản đăng nhập có một thư mục riêng. Ai viết công cụ đọc lịch sử agent mà gắn cứng một đường dẫn thì chỉ thấy một tài khoản trong số đó, nên nên tìm theo mẫu tên thư mục.
  - *cho:* dev dùng nhiều agent AI, nhiều tài khoản và đang viết công cụ đọc lịch sử của chúng · dòng 3566, 3574
- **haiku:** Tưởng mỗi công cụ AI chỉ lưu dữ liệu ở một thư mục. Hoá ra một máy có thể đăng nhập nhiều tài khoản: 4 thư mục Codex, 9 của pi, 10 của omp, 4 của agy. Ai đọc log bằng một đường dẫn cố định sẽ bỏ sót các profile còn lại.
  - *cho:* dev dùng nhiều tài khoản AI trên cùng một máy · dòng 3566, 3574

