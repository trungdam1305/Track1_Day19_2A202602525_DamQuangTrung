# Annotation — Option B (không cho tester xem)

```text
OPTION B — Đối thoại đồng chẩn đoán (Trung)

We expect the tester to:
  Bấm "Tôi đang bị kẹt" → trả lời 3 câu (hoặc bỏ qua / "Không biết") → đọc danh sách
  giả thuyết kèm dấu hiệu → tự chọn một giả thuyết để kiểm tra → báo kết quả →
  tự quyết sửa hay để sau → quay lại bài.

Watch for:
  - Câu 3: tester có chia sẻ dữ liệu không? Có do dự / hỏi "dữ liệu đi đâu"?
  - Tester trả lời "Không biết" bao nhiêu câu? (bác bỏ B nếu phần lớn là "không biết")
  - Tester có đọc phần "Mình đang dựa vào" và dấu hiệu +/–/? không, hay bấm thẳng giả thuyết đầu?
  - Tester có dùng "sửa", "Không phải cái này", "Hoàn tác", "← Về bài học" không — ở bước nào?
  - Tester có hỏi "tại sao lại là cái này?" — tự trả lời được từ dấu hiệu không?
  - Sau khi xác nhận FALSE: chọn "Xem cách tự sửa" hay "Để sau"?
  - Thời gian từ lúc bấm "kẹt" tới lúc quay lại bài.

Do not explain:
  - Nguyên nhân thật (cột Doanh thu là text).
  - Ý nghĩa ISNUMBER, Count/Sum, dấu tam giác xanh.
  - Nút nào để quay lại / sửa câu trả lời.
  - Rằng AI "sẽ tìm ra" nguyên nhân — câu dẫn chỉ được nói: "AI giúp tìm ra cần kiểm tra gì, không thay bạn kết luận."
```

## Ánh xạ tới Decision Table (§3.4) và lỗi (§3.9)

| Quyết định | Thể hiện trong prototype |
|---|---|
| Ask trước, Act khi có evidence | 3 câu hỏi lần lượt; chỉ sau đó mới hiện giả thuyết |
| Capability / limit | Bubble đầu: "không tự kết luận, có thể đoán sai, trả lời Không biết cũng được" |
| Evidence | Khung "Mình đang dựa vào" + mỗi giả thuyết có dấu hiệu ủng hộ (+) / chống (–) / còn thiếu (?) |
| Uncertainty | Mức định tính "Khả năng cao / Có thể / Ít khả năng", không dùng %; mức thay đổi theo câu trả lời và việc có chia sẻ dữ liệu |
| Mức 2 (§3.7) | AI chỉ nói dấu hiệu; chỉ sau khi **user tự kiểm tra ra FALSE** mới hiện "bạn vừa xác nhận…" |
| Control | Sửa từng câu trả lời (giữ các câu khác) · bỏ qua câu · xoá dữ liệu đã chia sẻ · "Không phải cái này" · Hoàn tác · Xin giả thuyết khác · Bắt đầu lại |
| Recovery | Sau 2 lần loại → AI nói "Mình không chắc" + tóm tắt để gửi mentor (§3.9 #4) |
| R3 lối thoát | "← Về bài học" cố định trên header ở mọi màn |
| Không tự sửa file | Kiểm tra bằng cột tạm; cách sửa do user tự làm, có bước lưu bản sao |
| Dữ liệu | Che tên khách; "chỉ dùng trong phiên này, không lưu" |

## Phần dùng chung với A/C (≈70%)
Header + nút "← Về bài học", thẻ "Tình huống của bạn", khung video Bước 4, PivotTable Count + Value Field Settings (Sum mờ), 5 dòng dữ liệu gốc, nút "Tôi đang bị kẹt ở bước này". A và C có thể copy nguyên `#scrContext` và CSS, chỉ thay phần sau nút "kẹt".
