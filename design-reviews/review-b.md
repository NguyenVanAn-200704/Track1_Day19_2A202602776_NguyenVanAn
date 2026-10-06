# Đánh giá thiết kế trước kiểm thử — Option B

**Tài liệu phân tích tương tác và rủi ro thiết kế**  
*Phụ trách phân tích:* Lưu Xuân Dũng (2A202602746) · *Case B:* AI Notes  
*Mục đích:* Phân tích luồng tương tác, dự đoán các điểm ma sát (friction points) và chuẩn bị giả thuyết kiểm chứng cho phiên kiểm thử người dùng Option B.

---

## 1. Bối cảnh và Nhiệm vụ kiểm thử

- **Kịch bản thiết kế:** Người học nhớ ý nghĩa khái niệm nhưng không nhớ chính xác từ khóa hoặc vị trí slide đã ghi chú.
- **Nhiệm vụ chung (Outcome task):** Đang ở slide e2 (*Thiết kế thử nghiệm — Ai bắt đầu hỗ trợ?*), tìm ghi chú về việc *"thử ý tưởng thay vì chỉ trình diễn"*, mở slide nguồn e1 để kiểm tra đối chiếu bối cảnh, rồi quay trở lại slide đang học e2.
- **Thứ tự thực hiện đề xuất trong phiên T02:** B → C → A (để kiểm tra phản ứng của người dùng với tính năng tìm theo ý ngay từ đầu trước khi tiếp xúc với từ khóa truyền thống).

---

## 2. Bằng chứng kỹ thuật và Các thành phần tương tác

| ID | Thành phần / Cơ chế | Vai trò trong tương tác |
|---|---|---|
| **B-R01** | Ô nhập tìm kiếm ngữ nghĩa (`#query`) | Cho phép người học nhập câu mô tả tự nhiên thay vì từ khóa đơn lẻ. |
| **B-R02** | Xếp hạng và nhãn "Có thể phù hợp" | Trả về note nguyên bản kèm nhãn cảnh báo độ không chắc chắn (Uncertainty) và giải thích lý do khớp. |
| **B-R03** | Khung hiển thị nguyên văn ghi chú | Tuyệt đối không tự ý viết lại, tóm tắt hoặc sinh thêm nội dung mới, bảo toàn nguyên bản ghi chép của người học. |
| **B-R04** | Nút "Không note nào đúng ý · Tả lại" & Tab "Từ khóa" | Cơ chế phục hồi (Recovery) cho phép người học viết lại câu mô tả hoặc fallback về tìm kiếm từ khóa truyền thống. |

---

## 3. Bảy tiêu điểm dự đoán trước kiểm thử (Hypothesis Matrix)

| Tiêu điểm | Giả thuyết thiết kế | Điểm quan sát thực địa |
|---|---|---|
| **First Action** | Người dùng sẽ đọc gợi ý placeholder và nhập một câu diễn đạt ý thay vì gõ 1 từ đơn. | Quan sát nội dung và độ dài câu truy vấn đầu tiên. |
| **Hesitation** | Có thể dừng lại vài giây khi đọc nhãn "Có thể phù hợp" để suy nghĩ xem kết quả có chuẩn xác không. | Đo thời gian do dự (>3s) tại danh sách kết quả. |
| **Evidence Read** | Người dùng sẽ đọc dòng lý do "Vì sao" và bấm mở slide nguồn để kiểm chứng. | Kiểm tra hành vi click vào badge nguồn slide. |
| **Misunderstanding** | Người dùng có thể tưởng đây là chatbot hỏi đáp kiến thức chứ không phải công cụ lọc note cá nhân. | Lắng nghe câu hỏi hoặc nhận xét phát biểu thành lời. |
| **Help Needed** | Lời giải thích capability text có đủ giúp người học hiểu phạm vi hoạt động của hệ thống hay không. | Ghi nhận số lần cần can thiệp giải thích. |
| **Recovery** | Nếu kết quả không trúng, người dùng có nhận biết được nút "Tả lại" hoặc tab "Từ khóa" không. | Quan sát cách người học xử lý khi truy vấn thất bại. |
| **Option & Trade-off** | Người dùng thích sự tiện lợi khi không cần nhớ từ khóa, nhưng phải chấp nhận công sức đọc lọc kết quả. | Ghi nhận đánh giá so sánh sau khi thử đủ cả ba option. |

---

## 4. Đánh giá bốn tầng trước kiểm thử

- **Observed (Kỹ thuật):** Cơ chế lọc ngữ nghĩa hoạt động ổn định trên môi trường máy cục bộ; trả về đúng note n3 lên đầu danh sách với câu truy vấn mô tả ý tưởng.
- **Interpreted:** Điểm mạnh lớn nhất của B là giải phóng người học khỏi áp lực nhớ từ khóa. Tuy nhiên, rủi ro tương tác nằm ở chỗ nếu câu truy vấn chung chung, hệ thống có thể xếp các note tương tự nhau lên cùng lúc, buộc người học phải tốn thêm thời gian đọc đối chiếu để loại bỏ note nhiễu.
- **Next Change dự kiến trước test:** Nếu người dùng nhầm lẫn ô tìm kiếm với khung chat hỏi đáp, cần tinh chỉnh lời dẫn placeholder thành: *"Mô tả ý bạn muốn tìm lại trong các ghi chú đã lưu…"*.
- **Still Unproven:** Độ nhạy của cơ chế tìm theo ý khi số lượng ghi chú tăng lên hàng trăm note; mức độ sẵn lòng đọc các nhãn giải thích lý do của người học trong bối cảnh học tập áp lực cao.
