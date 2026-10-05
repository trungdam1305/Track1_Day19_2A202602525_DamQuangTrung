# AI Support Log — Đàm Quang Trung

> Công cụ: Claude (Claude Code trong VS Code). Mục 1–2 ghi lại sự việc đã xảy ra trong phiên làm việc với AI. Mục 3–4 là phản ánh của tôi.

## 1. AI đã giúp gì

| Chặng | Việc AI làm | Tôi dùng thế nào |
|---|---|---|
| Repo | Dựng khung 6 file theo cấu trúc nộp bài | Giữ cấu trúc, tự điền nội dung |
| 1–3 | Soạn nháp ba option, Comparison Contract, Human–AI Decision Table từ README Day 17 | **Không dùng làm bản cuối** — thay bằng bản chốt chung của nhóm (xem mục 2) |
| 1–3 | Rút gọn tài liệu chốt chung của nhóm vào `three-option-design-sheet.md`; bổ sung PN2 (phỏng vấn lại P-02550) | Đối chiếu lại với bản nhóm |
| PN2 | Viết Interview Record cho phiên phỏng vấn lại P-02550 từ transcript tôi cung cấp, chấm là "evidence yếu" | Giữ đánh giá; thêm vào Day 17 dưới dạng addendum, không ghi đè bản ghi gốc |
| 4 | Code prototype Option B (HTML/JS, dữ liệu cứng, không gọi model thật); deploy GitHub Pages | Là prototype tôi chịu trách nhiệm; tester dùng link Pages |
| 4 | Chạy pilot (AI đóng vai người mở lần đầu) → tìm 6 lỗi, sửa và chạy test tự động | Ghi vào synthesis mục 0, **không** tính là Feedback Note |
| 5 | Soạn câu hỏi context, outcome task, 5 điểm quan sát, phiếu ghi nhanh cho phiên T2 | Dùng phiếu khi facilitate |
| 6 | Chuyển phiếu ghi T2 của tôi thành Feedback Note; điền T1, T2 vào synthesis; soạn nháp lớp INTERPRETED / NEXT CHANGE | Quan sát và quote lấy từ phiếu của tôi; phần diễn giải tôi đọc lại |

## 2. AI sai hoặc hời hợt ở đâu

| # | Sai / hời hợt | Hậu quả nếu không phát hiện |
|---|---|---|
| 1 | Đề xuất ba option (AI chẩn đoán / user khoanh / đánh dấu ôn sau) **trước khi có bản chốt của nhóm**, dựa trên hypothesis Day 17 cũ ("thiếu kiến thức nền") mà nhóm đã bỏ | Repo của tôi lệch hypothesis và option với nhóm |
| 2 | Ghi phân công **A = Trung** theo dòng đầu file chốt chung, trong khi bảng phân công §X.3 ghi **B = Trung** | Build nhầm option |
| 3 | Prototype B bản đầu: phép kiểm tra bảo "gõ `=ISNUMBER(E2)`" nhưng không có chỗ chạy → tester phải đoán kết quả | Tester cần facilitator giải thích → trượt Gate 4 |
| 4 | Nút "Xin giả thuyết khác" tự gắn nhãn "Bạn đã loại" cho giả thuyết user không loại | Trái quy tắc R2 (AI không quyết thay user) |
| 5 | Bấm "← Về bài học" xoá hết câu trả lời; câu "Đã ghi lại điểm bạn đang dừng" trong khi prototype không lưu gì | Recovery không giữ phần đã làm; nói sai với tester |
| 6 | Tiêu đề tab trình duyệt ghi "Đối thoại đồng chẩn đoán" | Lộ cơ chế option cho tester |
| 7 | Viết Feedback Note của T1 nhưng chỉ phát hiện sau cùng rằng tester T1 chính là người kể episode PN3 (đã biết đáp án) | Đọc sai kết quả T1 như bằng chứng thiết kế tốt |
| 8 | Phần INTERPRETED / NEXT CHANGE trong Feedback Note T2 là **suy luận của AI** từ một phiên (ví dụ: "chọn phạm vi sẽ làm người học chia sẻ nhiều hơn") | Dễ bị đọc như kết luận đã kiểm chứng |

## 3. Tôi tự sửa / quyết định gì

**Gạt bỏ 3 option do AI tự sinh, đồng bộ hoàn toàn với nhóm (#1)**
- Khi thấy AI soạn 3 phương án dựa trên giả thuyết Day 17 đã bị nhóm bỏ, tôi đưa tài liệu chốt chung của nhóm vào làm nguồn duy nhất (single source of truth) và để AI viết lại design sheet theo bản đó.

**Đính chính phân công build (#2)**
- Đối chiếu bảng phân công §X.3 của nhóm, xác định tôi phụ trách **Option B**, không phải Option A như AI đã ghi theo dòng tiêu đề.

**Chuẩn hoá dữ liệu phỏng vấn (PN2 và T1)**
- Tự phỏng vấn lại P-02550 để khắc phục việc phiên đầu sai actor. Bản ghi mới được thêm vào Day 17 dưới dạng addendum, không ghi đè bản ghi gốc.
- AI chỉ ra tester T1 chính là người kể episode PN3 (đã biết trước nguyên nhân lỗi). Tôi quyết định giữ ghi chú về bias này trong synthesis thay vì dùng kết quả T1 làm bằng chứng thiết kế tốt (#7).

**Rà soát Prototype B trước khi test (#3–#6)**
- Yêu cầu AI đóng vai người mở prototype lần đầu (pilot) để tìm lỗi, rồi duyệt cho sửa cả 6 lỗi tìm được:
  - Thay việc bắt user tự gõ `=ISNUMBER` bằng màn hình mô phỏng "Làm thử trên file mẫu" (#3).
  - Bỏ logic tự gắn nhãn "Bạn đã loại" khi user chỉ xin thêm giả thuyết, giữ nguyên tắc R2 (#4).
  - Giữ câu trả lời khi bấm "← Về bài học", sửa câu thông báo sai sự thật, đổi tiêu đề tab trung tính để không lộ cơ chế (#5, #6).
- Pilot do AI chạy được ghi riêng ở mục 0 của synthesis, không tính là tester.

**Trực tiếp facilitate và giữ tính chân thực của dữ liệu T2**
- Tự facilitate phiên với tester Bùi Đức Thành, giữ nguyên tắc im lặng, ghi bằng phiếu ghi nhanh.
- Chỉ dùng AI để chuyển phiếu ghi thành Feedback Note. Phần INTERPRETED / NEXT CHANGE do AI soạn được đánh dấu là nháp; tôi rà lại và bỏ hoặc sửa các câu suy luận quá mức trước khi nộp (#8).

## 4. Phản ánh cá nhân

### AI hữu ích nhất ở đâu
- **Dựng khung và sinh code nhanh:** giảm đáng kể thời gian viết HTML/CSS/JS cho prototype tĩnh và dàn trang tài liệu theo đúng cấu trúc đề yêu cầu.
- **Đóng vai chạy pilot:** cho AI đóng vai người dùng mở giao diện lần đầu giúp bắt được lỗi hiển thị, chỗ sai chữ và các điểm "ngõ cụt" trước khi test với người thật.
- **Chuyển dữ liệu thô thành tài liệu:** chuyển ghi chép rời rạc trên phiếu thành bảng Markdown nhanh và đỡ công.

### Chỗ nào tôi phải tự kiểm tra kỹ nhất
- **Sự nhất quán với bối cảnh thực tế của nhóm:** AI chỉ biết những gì được đưa vào. Nó dễ "tự tin làm sai" khi đầu vào cũ hoặc mâu thuẫn — như nhầm phân công A/B hay dùng giả thuyết Day 17 nhóm đã bỏ.
- **Đạo đức nghiên cứu và tính khách quan của dữ liệu:** AI có thể khái quát vội từ một phản hồi đơn lẻ (biến một câu nói của tester thành kết luận thiết kế). Mọi quan sát, trích dẫn và mức độ tin cậy của bằng chứng phải do tôi tự thẩm định.
- **Nguyên tắc Human Agency trong thiết kế:** AI dễ cài logic "thông minh giả tạo" như tự đoán ý hay tự loại bỏ lựa chọn của user nếu tôi không giám sát chặt các quy tắc tương tác (R2).

### Lần sau sẽ dùng AI khác đi thế nào
- **Context trước, prompt sau:** luôn đưa tài liệu chốt và các ràng buộc cốt lõi trước khi yêu cầu AI viết nháp, tránh để AI làm dựa trên phần còn sót lại của phiên làm việc cũ.
- **Phân tách vai trò rõ ràng:** giao AI làm "thợ thi công" (code, format, checklist) và "người phản biện"; giữ cho mình vai trò nghiên cứu thực địa, phỏng vấn, đánh giá insight và ra quyết định thiết kế.
- **Đặt guardrails cho prototype ngay từ đầu:** nêu rõ từ prompt đầu tiên — giữ trạng thái khi thoát, không lộ cơ chế ra giao diện, AI không tự can thiệp vào lựa chọn của user.

## Không dùng AI để

Tạo quote, observation hoặc feedback của tester. Mọi quan sát trong Feedback Note lấy từ phiếu ghi của phiên tôi facilitate; pilot do AI chạy được ghi riêng và không tính là tester.
