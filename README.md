# Track1_Day18_2A202602525_DamQuangTrung

## 1. Thông tin cá nhân và nhóm
| Mục | Nội dung |
|---|---|
| MHV | 2A202602525 |
| Họ tên | Đàm Quang Trung |
| Tên nhóm | AAA |
| Thành viên | Đàm Quang Trung, Đặng Văn Thái Anh, Nguyễn Thị Bảo Trang |
| Case | Case A — AI Tutor: Diagnostic Refresher |
| Option tôi phụ trách | **B — Đối thoại đồng chẩn đoán** |

## 2. Hypothesis Problem (bản nhóm chốt ở Day 18)
> **Khi** học viên tự học trực tuyến theo nhịp cá nhân để áp dụng ngay vào việc thật, và kết quả trên dữ liệu thật khác với hướng dẫn, **học viên** gặp khó khăn trong việc **xác định điểm vướng và dùng đúng điều mình đã biết**, **vì** không biết mình đã biết gì / đang thiếu gì liên quan tới đúng triệu chứng này, và nguồn ngoài viết cho người chưa từng gặp tình huống đó trên dữ liệu thật của họ, **dẫn đến** lặp lại thao tác, dò nhiều nguồn không khớp, mất thời gian, gián đoạn luồng học; đôi khi bỏ hẳn phần học tiếp theo.

**Observation Day 17:**
- PN1: kẹt ở Hybrid Retrieval, dò 6 nguồn trong khoảng một giờ, thoát kẹt nhờ ví dụ thực tế. *"Mình chỉ biết là mình không hiểu hybrid retrieval…"*
- PN3 (chưa đối chiếu file nguồn): PivotTable hiện Count thay vì Sum. Người học tua video và làm lại khoảng 10 phút. Người học đã biết chuyện số lưu dạng text nhưng không liên hệ với triệu chứng (03:27).
- **PN2 (phiên tôi hỏi):** phiên cũ P-02550 bị loại vì sai actor (học workshop live) và không có consent trong bản ghi. Tôi đã phỏng vấn lại chính P-02550, lần này hỏi về tự học: người này nêu khó khăn ở chọn tài liệu (*"không biết tài liệu nào chính xác và phù hợp"*) nhưng không kể được lần cụ thể nào → evidence yếu, không dùng làm căn cứ.

**Chưa biết:** học viên có sẵn sàng chia sẻ file công việc cho AI không · Lớp 1 (không biết mình thiếu gì) hay Lớp 2 (biết nhưng không nối được) phổ biến hơn · học viên tin AI tới đâu. Hai note khác chủ đề nên chưa nói được gì về tần suất.

## 3. Three Solution Options
Cùng user, situation (PivotTable trên file thật hiện Count thay vì Sum, nút Sum mờ), task, data fixture và outcome. Khác nhau ở **ai làm việc định vị điểm vướng**. Chi tiết: [three-option-design-sheet.md](three-option-design-sheet.md).

| Option | Mechanism | Ai giữ quyền | Người làm |
|---|---|---|---|
| A — Bản đồ tự kiểm tra | Cây kiểm tra theo triệu chứng, user tự chạy từng bước, AI chỉ giải thích khi được gọi | User-led, AI Don't Act | Trang |
| B — Đối thoại đồng chẩn đoán | AI hỏi 2–3 câu thích ứng, hai bên thu hẹp nguyên nhân | Co-create, Ask → Act | Trung |
| C — AI kiểm tra artefact | Sau consent, AI phân tích file, chỉ dấu hiệu, tạo preview; user duyệt | AI-led, user duyệt | Thái Anh |

Link prototype: [prototype-link.md](prototype-link.md)

## 4. Đóng góp của tôi trong nhóm
- Thiết kế và build **Option B — Đối thoại đồng chẩn đoán** (prototype: `prototype/index.html`).
- TODO (tự viết): phần shared context/content, Human–AI decisions tôi góp ý, phiên test tôi facilitate, phần tổng hợp.
- Day 17: thực hiện phiên PN2. Phiên này bị nhóm loại vì sai actor. Bài học từ đó tôi đưa vào Conversation Guide v2: hỏi đủ hai câu sàng lọc, xin phép ghi âm trong bản ghi, thêm probe cho thuật ngữ lạ.

## 5. Prototype Feedback
- Observation từ phiên tôi facilitate ([prototype-feedback-note.md](prototype-feedback-note.md), tester Bùi Đức Thành, 05/10/2026, thứ tự B → C → A): cả ba option tester đều tìm ra cách sửa và quay lại bài. Ở B, tester **không chia sẻ** dữ liệu (*"File công ty có số tiền thật nên hơi ngại tải lên"*) nhưng vẫn nhận ra dấu hiệu nhờ "Làm thử trên file mẫu"; cần 1 câu cứu hộ khi đọc lâu màn giả thuyết. Ở C, tester chia sẻ nhưng tự khoanh vùng nhỏ, tránh cột tên khách, và mở bằng chứng trước khi duyệt. Ở A, tester đứng yên >30 giây ở màn chính (*"Nhiều nhánh quá…"*).
- Tổng hợp ba feedback: [group-feedback-synthesis.md](group-feedback-synthesis.md) — TODO sau khi test
- Next Change: TODO (mẫu: "đã thử ba cách giải; tester đã làm…; vì vậy lần sau sẽ…")
- Still Unproven: TODO

## 6. AI Support Log
Chi tiết: [ai-support-log.md](ai-support-log.md)
