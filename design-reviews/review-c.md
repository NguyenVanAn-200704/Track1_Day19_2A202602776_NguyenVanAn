# Đánh giá thiết kế trước kiểm thử — Option C

**Tài liệu phân tích tương tác và rủi ro thiết kế**  
*Phụ trách phân tích:* Nguyễn Long Khánh · *Case B:* AI Notes  
*Mục đích:* Phân tích luồng tương tác, dự đoán các điểm ma sát (friction points) và chuẩn bị giả thuyết kiểm chứng cho phiên kiểm thử người dùng Option C.

---

## 1. Bối cảnh và Nhiệm vụ kiểm thử

- **Kịch bản thiết kế:** Người học đang học một slide mới và muốn hệ thống chủ động gợi nhắc lại các ghi chú cũ có liên quan mà không cần phải tự mình nghĩ ra từ khóa tìm kiếm.
- **Nhiệm vụ chung (Outcome task):** Đang ở slide e2 (*Thiết kế thử nghiệm — Ai bắt đầu hỗ trợ?*), tìm ghi chú về việc *"thử ý tưởng thay vì chỉ trình diễn"*, mở slide nguồn e1 để kiểm tra đối chiếu bối cảnh, rồi quay trở lại slide đang học e2.
- **Thứ tự thực hiện đề xuất trong phiên T03:** C → A → B (kiểm tra phản ứng của người dùng với tính năng gợi ý chủ động ngay từ đầu).

---

## 2. Bằng chứng kỹ thuật và Các thành phần tương tác

| ID | Thành phần / Cơ chế | Vai trò trong tương tác |
|---|---|---|
| **C-R01** | Khung gợi ý thu gọn (`#suggestions`) | Hiển thị số lượng gợi ý liên quan theo slide hiện tại; mặc định thu gọn để tránh choán màn hình. |
| **C-R02** | Thẻ note kèm nhãn "Liên quan rõ" / "Chưa chắc liên quan" | Cung cấp thông tin mức độ liên quan và lý do gắn kết theo nội dung slide đang học. |
| **C-R03** | Các nút thao tác quyền kiểm soát: Ghim / Bỏ gợi ý | Cho phép người học ghim note để giữ lại, hoặc bấm bỏ gợi ý nếu thấy không liên quan (không xóa note gốc). |
| **C-R04** | Nút "Tắt gợi ý" (`#disable`) | Quyền kiểm soát tối cao (User Agency) cho phép tắt hoàn toàn panel gợi ý để lấy lại không gian học tập tĩnh lặng. |

---

## 3. Bảy tiêu điểm dự đoán trước kiểm thử (Hypothesis Matrix)

| Tiêu điểm | Giả thuyết thiết kế | Điểm quan sát thực địa |
|---|---|---|
| **First Action** | Người dùng sẽ nhìn thấy panel gợi ý trước tiên và bấm nút mở xem nội dung. | Quan sát thời gian và thao tác đầu tiên trên màn hình. |
| **Hesitation** | Có thể do dự khi thấy nhiều gợi ý hoặc phân vân về nút "Bỏ gợi ý". | Đo thời gian dừng đọc nội dung panel gợi ý (>3s). |
| **Evidence Read** | Người học có bấm mở slide nguồn gốc để kiểm chứng hay tin ngay vào gợi ý của hệ thống. | Kiểm tra hành vi mở slide e1 đối chiếu. |
| **Misunderstanding** | Người dùng có thể hiểu nhầm thao tác "Bỏ gợi ý" là xóa hẳn ghi chú khỏi sổ lưu trữ cá nhân. | Lắng nghe câu hỏi hoặc thắc mắc của người học. |
| **Help Needed** | Người học có cần trợ giúp để tìm lại cách bật lại gợi ý sau khi đã tắt hay không. | Ghi nhận câu hỏi trợ giúp về giao diện. |
| **Recovery** | Thao tác tắt/bật gợi ý có diễn ra mượt mà và trực quan hay không. | Đánh giá tốc độ phục hồi trạng thái giao diện. |
| **Option & Trade-off** | Người dùng đánh đổi sự yên tĩnh để đổi lấy tốc độ truy cập nhanh, hay ngược lại. | Ghi nhận phản hồi so sánh giữa Option C và Option A/B. |

---

## 4. Đánh giá bốn tầng trước kiểm thử

- **Observed (Kỹ thuật):** Cơ chế gợi ý tự động kích hoạt khi chuyển sang slide e2, trích xuất đúng note n3 liên quan đến chủ đề prototype; các nút ghim/bỏ/tắt hoạt động chính xác.
- **Interpreted:** Điểm mạnh của C là giảm thiểu số thao tác xuống mức tối đa (Zero-query retrieval). Tuy nhiên, rủi ro lớn nhất là sự xâm lấn không gian thị giác (Visual Clutter) và nguy cơ làm gián đoạn dòng tư duy học sâu của người học nếu gợi ý không thực sự chuẩn xác hoặc nhảy ra quá thường xuyên.
- **Next Change dự kiến trước test:** Nếu người dùng băn khoăn về nút "Bỏ gợi ý", cần đổi nhãn thành *"Ẩn gợi ý này"* để làm rõ rằng ghi chú gốc trong sổ vẫn được bảo toàn nguyên vẹn.
- **Still Unproven:** Mức độ chấp nhận của người học đối với panel gợi ý khi học các bài học dài liên tục nhiều giờ; liệu tính năng này có gây mất tập trung nhiều hơn là hỗ trợ hay không.
