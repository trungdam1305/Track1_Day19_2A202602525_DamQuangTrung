# Prototype Feedback Note — Đàm Quang Trung

> Nội dung chuyển từ phiếu ghi nhanh của phiên T2 do tôi facilitate. Không bổ sung observation hoặc quote ngoài phiếu. Mục 4–5 là diễn giải, tách khỏi quan sát.

## 1. Thông tin phiên

| Mục | Nội dung |
|---|---|
| Tester (ngoài nhóm) | Bùi Đức Thành |
| Ngày / thời lượng | 05/10/2026 · 14:20–14:50 (~30 phút) |
| Facilitator | Đàm Quang Trung |
| Thứ tự option | B (14:20–14:31) → C (14:32–14:41) → A (14:42–14:50) |
| Prototype | B: https://trungdam1305.github.io/Track1_Day19_2A202602525_DamQuangTrung/prototype/ · A, C: bản của Trang, Thái Anh |
| Đồng ý tham gia | Có · ghi âm: Có |
| Relevant context | Có context thực tế rõ nét: Tuần trước vừa tự học hàm VLOOKUP qua video hướng dẫn online nhưng khi làm trên file công ty thì kết quả ra toàn lỗi #N/A, loay hoay cả buổi tối mới tìm ra nguyên nhân do cột mã dính khoảng trắng ẩn. Tester thường xuyên đối mặt với dữ liệu tài chính/doanh thu thực tế tại doanh nghiệp (lý giải cho phản xạ nhạy cảm cao và tâm lý e ngại chia sẻ "số tiền thật trên file công ty" khi kiểm thử). |

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
| Option được chọn / trade-off | Hiểu rõ nhất vì sao sai: **B** (câu hỏi từng bước + "Làm thử trên file mẫu") | Khi gấp trước 17:00: **C** — đánh đổi phải tự khoanh vùng che dữ liệu và chưa hiểu sâu lỗi | Không thấy nút quay lại rõ khi vào sâu 2 cấp, phải dùng Back của trình duyệt |

**Ghi chú về độ chính xác của phiếu:** ở B, phiếu ghi kết quả "Làm thử" là *"Khớp lỗi"* — prototype chỉ có các nút "Ra FALSE / Ra TRUE / Không chắc", nên cần xác nhận tester đã bấm nút nào. Tên giả thuyết trong phiếu ("Dữ liệu số bị lưu dưới dạng Text") là cách facilitator diễn đạt lại; tên trên màn hình là "Excel không coi các ô trong cột Doanh thu là số".

## 3. Exact quotes — theo phiếu ghi

> "Đang cần tính doanh thu nên chắc chắn là Tổng tiền." (B, câu 1)

> "Nó chỉ hiện Count of Amount chứ không Sum được." (B, câu 2)

> "File công ty có số tiền thật nên hơi ngại tải lên." (B, câu 3)

> "À đúng y hệt lỗi của mình, cột tiền bị căn lề trái." (B, sau khi Làm thử)

> "Phải xem nó chỉ ra cái gì, lỡ nó đoán bừa." (C, mở bằng chứng)

> "Nhiều nhánh quá không biết mắt nhìn vào đâu trước." (A, màn chính)

> "Lúc đang cháy deadline thì C là cứu tinh, nhưng lúc muốn học nghề nghiêm túc thì B mới giúp mình không bị dốt đi." (hỏi sau)

> "May mà phương án C nó cho chọn 'Tạo bản sao mới', chứ nếu nó bấm thẳng đè lên file gốc của mình thì có cho tiền mình cũng không dám duyệt." (hỏi sau)

## 4. Tách bốn lớp

### OBSERVED — Tester thực sự làm hoặc nói gì?

**Ở Option B:**
- Trả lời ngay câu 1–2 ("Tổng tiền", "Sum mờ"), nhưng do dự ~8 giây ở câu 3 rồi chọn **Không chia sẻ** dữ liệu, nói rõ lý do: *"File công ty có số tiền thật nên hơi ngại tải lên."*
- Đọc kỹ từng dòng ở màn giả thuyết, gật gù ở giả thuyết về dữ liệu text. Đọc lâu tới mức facilitator dùng 1 câu cứu hộ ("Bạn cứ nói to suy nghĩ nhé").
- Chủ động bấm "Xin giả thuyết khác" để xem thêm, sau đó bấm "Làm thử trên file mẫu" và nói: *"À đúng y hệt lỗi của mình, cột tiền bị căn lề trái."*
- Tự đọc "Xem cách tự sửa" (Text to Columns) rồi quay lại bài học.

**Ở Option C:**
- Bấm ngay "Quét lỗi PivotTable", không đọc chữ giới thiệu.
- Do dự ~6 giây ở bước cấp quyền; chọn **Vùng sheet** và chủ động khoanh vùng hẹp (5 dòng tiêu đề + 3 dòng số), cố tình **né cột tên khách hàng**.
- Mở chi tiết bằng chứng trước khi duyệt: *"Phải xem nó chỉ ra cái gì, lỡ nó đoán bừa."*
- Thấy tuỳ chọn tạo bản sao mới nên Apply trên bản sao ngay, không dùng Undo hay Từ chối. Thấy AI tô vàng ô E14 dính text, hiểu lỗi, quay lại bài. Nhanh nhất, 0 lần cần trợ giúp.

**Ở Option A:**
- Đứng yên >30 giây ở màn chính (~40 giây đầu chỉ để định vị sơ đồ): *"Nhiều nhánh quá không biết mắt nhìn vào đâu trước."* Cần 1 câu cứu hộ ("Bạn sẽ làm gì tiếp theo?").
- Chọn nhầm nhánh "Ô trống trong vùng dữ liệu", lùi lại, đọc checklist "Dấu hiệu cần tìm" (tam giác xanh ở góc ô), lần theo nhánh định dạng tìm ra cách sửa rồi quay lại bài.

**Phần hỏi sau khi xong cả ba:**
- **Khi gấp trước 17:00:** chọn **Option C** — cần kết quả ngay để gửi sếp. Đánh đổi: chấp nhận mất công khoanh vùng che dữ liệu nhạy cảm và chưa hiểu sâu bản chất lỗi (*"xong việc tối về ngẫm sau"*).
- **Hiểu rõ nhất vì sao sai:** **Option B**, nhờ câu hỏi chẩn đoán từng bước và "Làm thử trên file mẫu".
- **Điểm nghẽn điều hướng:** ở A, khi vào sâu 2 cấp nhánh con thì không thấy nút quay lại rõ ràng, phải dùng nút Back của trình duyệt và sợ mất dấu chỗ đang đọc.

### INTERPRETED — Hành vi đó có thể có nghĩa gì?

1. **Tester chuyển giữa hai chế độ tuỳ áp lực thời gian.**
   - *Chế độ deadline:* trước hạn 17:00, ưu tiên "xong việc an toàn" — chọn C dù phải đánh đổi quyền riêng tư (tự che bớt dữ liệu) và bỏ qua việc hiểu sâu.
   - *Chế độ học:* khi không gấp, đánh giá cao B vì giúp hiểu từng bước (*"không bị dốt đi"*).
2. **Mức sẵn sàng chia sẻ dữ liệu có thể phụ thuộc vào mức kiểm soát.** Tester này không từ chối việc chẩn đoán, mà từ chối mất quyền kiểm soát: ở B, lựa chọn nhị phân (Chia sẻ / Không) khiến tester chọn phương án an toàn là "Không"; ở C, khi được tự khoanh vùng, tester chia sẻ phần dữ liệu đã lọc bỏ thông tin nhạy cảm.
3. **Niềm tin vào AI cần lưới an toàn và bằng chứng kiểm chứng được.** Tester không tin AI mặc định ("lỡ nó đoán bừa" → mở tab bằng chứng). Apply diễn ra dứt khoát chỉ khi có "Tạo bản sao mới" — nỗi sợ hỏng file thật có vẻ là rào cản lớn khi cho AI can thiệp vào trang tính.
4. **Quá tải ở cấu trúc cây (Option A).** Việc đứng yên >30 giây khớp với rủi ro nhóm đã dự đoán ở design sheet §2.3: người học khó tự ánh xạ triệu chứng vào các nhánh phân loại kỹ thuật khi cả sơ đồ hiện ra cùng lúc.
5. **Hiệu ứng thứ tự.** A tốn ít thời gian nhất (~8 phút) không có nghĩa A dễ dùng hơn: tới A, tester đã biết nguyên nhân (ô text giả số) sau khi qua B và C.

### DECIDED / NEXT CHANGE — Đề xuất gì sau phiên này?

**Option B (prototype của tôi):**
- **Đổi câu 3 (chia sẻ dữ liệu):** bỏ lựa chọn nhị phân "Chia sẻ / Không chia sẻ", thay bằng **"Chọn phạm vi kiểm tra"** — cho phép chỉ gửi cột số liệu / tiêu đề cột, tự ẩn hoặc loại trừ cột thông tin cá nhân như tên khách hàng. Học từ hành vi khoanh vùng ở Option C.
- **Rút gọn màn giả thuyết (progressive disclosure):** ban đầu chỉ hiện giả thuyết có mức phù hợp cao nhất kèm 1 dấu hiệu trực quan; phần giải thích chi tiết để sau nút "Tại sao lại có giả thuyết này?", để tester không bị ngợp chữ tới mức cần câu cứu hộ.
- **Giữ và làm nổi "Làm thử trên file mẫu":** đây là điểm tạo khoảnh khắc "à ra thế" rõ nhất cho tester ở B.

**Option C (góp ý cho Thái Anh):**
- Giữ mặc định "Tạo bản sao mới để thử" và "Khoanh vùng kiểm tra" — tester nói thẳng sẽ không dám duyệt nếu thiếu bản sao.
- Thêm 1 câu tóm tắt nguyên nhân sau khi Apply (ví dụ: "Đã đổi 1 ô từ text sang số"), để người học vẫn giữ lại được chút hiểu biết dù đang vội.

**Option A (góp ý cho Trang):**
- Tái cấu trúc điểm vào: thay vì mở cả sơ đồ cây, dùng ô tìm nhanh hoặc vài nút triệu chứng bề mặt thường gặp (ví dụ "Ra Count thay vì Sum").
- Thêm breadcrumbs và nút "Về đầu sơ đồ" rõ ràng, để người học dám thử các nhánh mà không sợ lạc.

### STILL UNPROVEN — Chưa thể kết luận điều gì?

- Hai "chế độ" deadline / học mới thấy ở **một tester**; chưa biết có lặp lại ở T1, T3 không.
- Đổi câu 3 thành chọn phạm vi có làm người học chia sẻ nhiều hơn ở B không — mới là suy luận từ hành vi ở C.
- Tester có chia sẻ dữ liệu với **file công việc thật** không — trong buổi test chỉ là fixture.
- Rút gọn màn giả thuyết có làm giảm thời gian đọc mà vẫn giữ được việc tester đọc bằng chứng không.
- Thời gian A/B/C không so sánh được vì hiệu ứng thứ tự.

## 5. Reflection cá nhân của Trung

### 5.1. Những quan sát đi ngược kỳ vọng ban đầu về Option B

- **Về việc chia sẻ dữ liệu:** khi thiết kế câu 3, tôi kỳ vọng người học đang bế tắc sẽ sẵn sàng gửi dữ liệu để nhận chẩn đoán chính xác hơn. Thực tế, tester Thành khựng lại ~8 giây rồi dứt khoát chọn "Không chia sẻ": *"File công ty có số tiền thật nên hơi ngại tải lên."* Tester giữ tâm thế bảo vệ dữ liệu công ty ngay cả khi đang làm bài thử nghiệm — tôi cần kiểm tra xem điều này có lặp lại ở người học văn phòng khác không.
- **Về màn hình giả thuyết:** tôi từng nghĩ đưa đầy đủ dấu hiệu +/–/? sẽ giúp người học đối chiếu và yên tâm hơn. Thực tế tester đọc kỹ từng dòng nhưng dừng lâu tới mức tôi phải dùng câu cứu hộ — có thể màn này đang quá nhiều chữ.
- **Điểm sáng bất ngờ:** "Làm thử trên file mẫu" ban đầu chỉ là cách sửa lỗi pilot (không bắt user tự gõ `=ISNUMBER`), nhưng lại thành điểm chạm rõ nhất: *"À đúng y hệt lỗi của mình, cột tiền bị căn lề trái."* Nó cho tester nhận ra lỗi mà không phải động vào file thật.

### 5.2. Những quyết định thiết kế của Option B cần xem lại

- **Câu hỏi chia sẻ dữ liệu dạng có/không quá thô:** hỏi "Có chia sẻ hay không?" đặt người học vào thế hoặc trao hết dữ liệu, hoặc không được hỗ trợ sâu. Ở Option C, khi được tự chọn vùng, tester Thành sẵn sàng khoanh 3 dòng số và chủ động né cột tên khách hàng. Option B nên học điều này: cho chọn phạm vi / che cột nhạy cảm thay vì hỏi có/không.
- **Chưa hiển thị tăng dần (progressive disclosure):** màn giả thuyết đang hiện toàn bộ suy luận cùng lúc, làm tăng tải đọc. Nên chỉ hiện kết luận trực quan nhất trước; phần dấu hiệu chi tiết để người học tự mở khi cần.

### 5.3. Tự soi vai trò facilitator: nguy cơ dẫn dắt từ các câu cứu hộ

Trong phiên T2, tôi dùng 2 câu cứu hộ. Nhìn lại, cả hai có thể đã làm lệch hành vi tự nhiên:

- **Ở Option B** ("Bạn cứ nói to suy nghĩ nhé"): tôi lên tiếng khi tester im lặng đọc màn giả thuyết quá lâu. Câu nói trung tính, nhưng việc facilitator lên tiếng có thể tạo áp lực, cắt mạch suy nghĩ của tester và khiến họ chuyển bước sớm hơn.
- **Ở Option A** ("Bạn sẽ làm gì tiếp theo?"): tester đứng hình >30 giây trước sơ đồ cây, và câu hỏi của tôi đã kéo họ ra khỏi trạng thái đó. Khi tự học một mình sẽ không có ai hỏi câu này — nhiều khả năng người học đã đóng tab. Tôi ghi nhận đây là **điểm gãy nghiêm trọng ở điểm vào của Option A**, không phải là tester tự vượt qua được.

### 5.4. Điều mang vào Group Feedback Synthesis

- **"Cứu deadline" và "học hiểu" là hai nhu cầu khác nhau:** *"Lúc đang cháy deadline thì C là cứu tinh, nhưng lúc muốn học nghề nghiêm túc thì B mới giúp mình không bị dốt đi."* Thay vì chọn một option thắng, tôi đề xuất nhóm kiểm tra với T1, T3 hướng kết hợp: sửa nhanh kiểu C khi sát giờ, kèm phần xem lại kiểu B để hiểu bản chất khi đã rảnh tay.
- **Lưới an toàn có vẻ là điều kiện tiên quyết:** tester chỉ dám duyệt ở C vì có "Tạo bản sao mới", và tin giả thuyết ở B nhờ "Làm thử trên file mẫu". Đề xuất nguyên tắc cho cả ba option: không động trực tiếp vào file thật của người học khi chưa có vùng đệm an toàn (bản sao, mô phỏng, preview).
