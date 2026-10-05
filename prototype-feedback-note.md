# Prototype Feedback Note — Đàm Quang Trung

> Nội dung chuyển từ phiếu ghi nhanh của phiên T2 do tôi facilitate. Không bổ sung observation hoặc quote ngoài phiếu. Mục 4–5 là diễn giải, tách khỏi quan sát.

## 1. Thông tin phiên

| Mục | Nội dung |
|---|---|
| Tester (ngoài nhóm) | Bùi Đức Thành |
| Ngày / thời lượng | 05/10/2026 · 14:20–14:50 (~30 phút) |
| Facilitator | Đàm Quang Trung |
| Thứ tự option | B (14:20–14:31) → C (14:32–14:41) → A (14:42–14:50) |
| Prototype | B: https://trungdam1305.github.io/Track1_Day18_2A202602525_DamQuangTrung/prototype/ · A, C: bản của Trang, Thái Anh |
| Đồng ý tham gia | Có · ghi âm: TODO |
| Relevant context | TODO — phiếu chưa ghi câu trả lời cho câu hỏi context. Trong lúc test tester nói *"đúng y hệt lỗi của mình"* và nhắc tới *"file công ty"* → có vẻ có context, cần xác nhận |

## 2. Ghi chép theo observation focus

| Observation | B — Đối thoại đồng chẩn đoán | C — AI kiểm tra artefact | A — Bản đồ tự kiểm tra |
|---|---|---|---|
| First action | Đọc thẻ tình huống ~10 giây, lẩm bẩm đề bài, rồi mới bấm "Tôi đang bị kẹt" | Bấm ngay "Quét lỗi PivotTable", không đọc phần giải thích xung quanh | Lướt tìm cụm từ giống triệu chứng; chọn nhánh "Kết quả ra Count thay vì Sum" |
| Trả lời / lựa chọn chính | Câu 1: Tổng tiền · Câu 2: Sum mờ · Câu 3: **không chia sẻ** dữ liệu · không sửa câu trả lời | Chọn **vùng sheet**: khoanh dòng tiêu đề + 3 dòng dữ liệu, **tránh cột tên khách** | Đọc checklist "Dấu hiệu cần tìm" |
| Hesitation (>5 giây) | ~8 giây ở câu 3 (chia sẻ dữ liệu); lúc cân nhắc giữa 2 giả thuyết về format | ~6 giây lúc cấp quyền và kéo chọn vùng dữ liệu | **Đứng yên >30 giây** ở màn chính (~40 giây đầu để định vị sơ đồ cây); do dự giữa "Lỗi nguồn" và "Lỗi thiết lập Pivot" |
| Evidence read / ignored | Đọc kỹ từng dòng ở màn giả thuyết, gật gù ở giả thuyết về số lưu dạng text | Mở tab bằng chứng trước khi duyệt | Có đọc "Dấu hiệu cần tìm" (tam giác xanh ở góc ô) |
| Correction / recovery | Bấm "Xin giả thuyết khác" để xem còn nguyên nhân nào; bấm "Làm thử trên file mẫu" | Xem preview → Apply trên bản sao (không dùng Undo, không từ chối) | Bấm nhầm nhánh "Ô trống trong vùng dữ liệu" rồi lùi lại |
| Help needed | **1 lần** — dừng đọc màn giả thuyết quá lâu → "Bạn cứ nói to suy nghĩ nhé" | **0** | **1 lần** — đứng hình ở màn chính >30 giây → "Bạn sẽ làm gì tiếp theo?" |
| Kết quả | Đọc các bước Text to Columns ("Xem cách tự sửa") rồi quay lại bài học | Thấy AI tô vàng ô E14 dính text, hiểu lỗi, quay lại bài học | Lần theo nhánh định dạng, tìm ra cách sửa, quay lại bài học |
| Thời gian | ~11 phút | ~9 phút | ~8 phút |
| Option được chọn / trade-off | TODO — phiếu chưa ghi phần hỏi sau khi xong cả ba | | |

**Ghi chú về độ chính xác của phiếu:** ở B, phiếu ghi kết quả "Làm thử" là *"Khớp lỗi"* — prototype chỉ có các nút "Ra FALSE / Ra TRUE / Không chắc", nên cần xác nhận tester đã bấm nút nào. Tên giả thuyết trong phiếu ("Dữ liệu số bị lưu dưới dạng Text") là cách facilitator diễn đạt lại; tên trên màn hình là "Excel không coi các ô trong cột Doanh thu là số".

## 3. Exact quotes — theo phiếu ghi

> "Đang cần tính doanh thu nên chắc chắn là Tổng tiền." (B, câu 1)

> "Nó chỉ hiện Count of Amount chứ không Sum được." (B, câu 2)

> "File công ty có số tiền thật nên hơi ngại tải lên." (B, câu 3)

> "À đúng y hệt lỗi của mình, cột tiền bị căn lề trái." (B, sau khi Làm thử)

> "Phải xem nó chỉ ra cái gì, lỡ nó đoán bừa." (C, mở bằng chứng)

> "Nhiều nhánh quá không biết mắt nhìn vào đâu trước." (A, màn chính)

## 4. Tách bốn lớp

### OBSERVED — Tester thực sự làm hoặc nói gì?

- Ở **B**, tester trả lời ngay câu 1–2 nhưng do dự ~8 giây ở câu 3 rồi **không chia sẻ** dữ liệu, nói ngại vì "file công ty có số tiền thật". Đọc kỹ màn giả thuyết, bấm "Xin giả thuyết khác", dùng "Làm thử trên file mẫu", rồi tự đọc cách sửa và quay lại bài. Cần 1 câu cứu hộ khi dừng lâu ở màn giả thuyết.
- Ở **C**, tester bấm quét ngay, do dự ~6 giây ở bước cấp quyền rồi **chủ động khoanh vùng nhỏ, tránh cột tên khách**. Mở bằng chứng trước khi duyệt, apply trên bản sao. Không cần trợ giúp, nhanh hơn B.
- Ở **A**, tester **đứng yên >30 giây** ở màn chính, nói "nhiều nhánh quá", cần 1 câu cứu hộ. Chọn nhầm một nhánh rồi lùi lại, cuối cùng tìm ra cách sửa.
- Cả ba option đều kết thúc bằng việc tìm ra cách sửa và quay lại bài học.

### INTERPRETED — Hành vi đó có thể có nghĩa gì? *(nháp — Trung xác nhận)*

- Tester **ngại chia sẻ dữ liệu ở cả B và C**, nhưng phản ứng khác nhau: ở B từ chối hẳn, ở C chấp nhận nhưng tự thu hẹp phạm vi. Có thể khi được chọn **phạm vi cụ thể** thì người học sẵn sàng chia sẻ hơn so với câu hỏi có/không.
- B vẫn đi tới được nguyên nhân khi user **không chia sẻ**: "Làm thử trên file mẫu" giúp tester nhận ra dấu hiệu (căn lề trái). Nhưng màn giả thuyết đọc lâu tới mức cần câu cứu hộ — có thể quá nhiều chữ.
- Câu "lỡ nó đoán bừa" ở C cho thấy tester **không tin AI mặc định**; đường xem bằng chứng được dùng thật.
- A gặp đúng rủi ro nhóm đã dự đoán ở design sheet §2.3 ("đứng yên 30 giây không biết bấm gì") — điểm vào chưa đủ gắn với triệu chứng.
- Thứ tự B → C → A: tới A tester đã gặp nguyên nhân hai lần, nên thời gian ngắn hơn ở A **không** có nghĩa A nhanh hơn.

### DECIDED / NEXT CHANGE — Đề xuất gì sau phiên này? *(nháp — Trung xác nhận)*

- **B (option của tôi):** đổi câu 3 từ "chia sẻ / không chia sẻ" sang **chọn phạm vi** (ví dụ chỉ cột Doanh thu, che các cột khác), vì ở C tester chấp nhận chia sẻ khi tự chọn được vùng. Rút gọn màn giả thuyết (ẩn bớt dấu hiệu, mở khi cần) và quan sát lại xem còn cần câu cứu hộ không.
- **A:** đưa tester vào thẳng nhánh khớp triệu chứng thay vì hiện cả cây — trùng với khoảng trống đã ghi ở §3.6.
- Đưa observation vào synthesis cùng T1, T3; không kết luận option nào tốt hơn từ một phiên.

### STILL UNPROVEN — Chưa thể kết luận điều gì?

- Tester sẽ chọn option nào khi gấp, và đánh đổi gì — phiếu chưa có phần hỏi sau.
- Tester có chia sẻ dữ liệu với **file công việc thật** không — trong buổi test chỉ là fixture.
- Đổi câu 3 thành chọn phạm vi có làm người học chia sẻ nhiều hơn không — mới là suy luận từ hành vi ở C.
- Thời gian A/B/C không so sánh được vì hiệu ứng thứ tự.

## 5. Reflection cá nhân của Trung

TODO — tự viết: observation nào khác kỳ vọng của tôi về Option B; quyết định thiết kế nào của B cần xem lại; chỗ tôi có thể đã vô tình dẫn dắt (2 lần dùng câu cứu hộ); điều mang vào Group Feedback Synthesis.
