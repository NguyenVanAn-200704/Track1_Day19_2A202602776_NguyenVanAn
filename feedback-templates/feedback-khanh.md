# Prototype Feedback Note — Nguyễn Long Khánh

**Biên bản quan sát kiểm thử người dùng thực tế**  
*Mã phiên:* T03 · *Thực hiện bởi Facilitator:* Nguyễn Long Khánh


| Trường | Giá trị |
|---|---|
| Facilitator | Nguyễn Long Khánh |
| Tester | T03 — Lê Quốc Bảo (23 tuổi, học viên lớp Data Science) |
| Ngoài nhóm / context thật | Người ngoài nhóm; thường xuyên học các slide kỹ thuật chuyên sâu trên VLearn, đề cao khả năng tập trung cao độ |
| Ngày / thiết bị / consent | 06/10/2026 (16:30 – 16:55); PC Desktop, Windows 11, màn hình 24 inch, Chrome; Đã ký consent đồng ý quan sát và ghi chép |
| Thứ tự kiểm thử | C → A → B (Counterbalance) |
| Phiên bản prototype | Day19 An v2 (commit 1f43d01) |
| Câu trả lời context question | "Khi học các thuật toán liên quan, mình rất cần mở lại note của các bài toán cơ sở trước đó. Nhưng ngại nhất là việc tìm kiếm làm mình đứt dòng suy nghĩ khi đang cố hiểu slide hiện tại." |

---

## 1. Quan sát A/B/C theo 7 tiêu điểm

| Tiêu điểm | C — fact/mốc (Gợi theo slide) | A — fact/mốc (Tự tìm từ khóa) | B — fact/mốc (Tìm theo ý nhớ) |
|---|---|---|---|
| **First action** | 00:05: Thấy ngay khung "Note cũ liên quan" nằm bên dưới slide bài giảng, click `"Mở 2 gợi ý"`. | 00:08: Nhấp ô input tìm kiếm, gõ từ khóa kỹ thuật ngắn `"prototype"`. Bấm Tìm. | 00:12: Chuyển tab sang ô tìm kiếm, gõ cụm từ: `"thử nghiệm ý tưởng"`. Bấm Tìm. |
| **Hesitation >3 giây** | 00:15 (3 giây): Dừng đọc tiêu đề note n3 trong danh sách gợi ý. | 00:18 (2 giây): Dừng lướt mắt nhanh thấy ngay n3 là kết quả duy nhất. | 00:26 (4 giây): Dừng khi kết quả hiển thị 2 note (n3 và n2), phân vân so sánh lý do vì sao note n2 ("Đo outcome...") lại xuất hiện. |
| **Evidence read/ignored** | 00:25: Thấy n3 ghi "Prototype để thử giả thuyết...", click mở slide e1, đọc lướt nội dung slide e1 trong 10 giây rồi bấm nút quay lại. | 00:30: Click n3, mở slide e1, xem nội dung gốc và bấm quay lại e2. | 00:38: Đọc lướt cả 2 thẻ note n3 và n2, đọc dòng giải thích vì sao khớp rồi mới chọn n3 để mở slide e1. |
| **Misunderstanding** | 00:45: Thấy tính năng gợi ý tiện nhưng nhận xét: *"Nếu slide nào cũng nhảy ra gợi ý thì hơi rối mắt và dễ phân tâm"*. Thử bấm nút `Tắt gợi ý`. | Không có hiểu lầm nào; thao tác tìm kiếm từ khóa rất chuẩn xác. | 00:30: Tự hỏi khẽ: *"Tại sao câu này lại hiện cả note về đo outcome nhỉ?"*. Tự nhận ra do có từ "thử nghiệm/ý tưởng" mang nét nghĩa tương đồng. |
| **Help needed: câu/số lần** | **0 lần** (Tự thao tác hoàn toàn). | **0 lần** (Tự thao tác hoàn toàn). | **0 lần** (Tự thao tác hoàn toàn). |
| **Correction/recovery** | Thử bấm nút "Tắt gợi ý" và "Bật lại" để kiểm tra tính năng khôi phục không gian học; bấm nút quay lại slide e2 mượt mà. | Thao tác rất thuần thục, không cần trợ giúp hay khôi phục. | Tự phân biệt kết quả dựa trên nội dung gốc để loại bỏ note nhiễu n2. |
| **Note chọn / nguồn / quay lại** | Chọn n3; mở slide e1; bấm "Quay lại slide đang học (e2)" thành công. | Chọn n3; mở slide e1; bấm "Quay lại slide đang học (e2)" thành công. | Chọn n3; mở slide e1; bấm "Quay lại slide đang học (e2)" thành công. |
| **Hoàn thành / giây / trợ giúp** | **Hoàn thành** / **75 giây** (1p15s) / 0 trợ giúp. | **Hoàn thành** / **100 giây** (1p40s) / 0 trợ giúp. | **Hoàn thành** / **90 giây** (1p30s) / 0 trợ giúp. |

---

## 2. Event Register (Biên bản sự kiện)

| ID | Option/mốc | OBSERVED (Hành vi & lời nói nguyên văn) | INTERPRETED (Diễn giải & giả thuyết) | Probe / Đối chiếu |
|---|---|---|---|---|
| **T03-E01** | Option C / 00:05 | Vừa vào slide e2, bấm ngay `Mở 2 gợi ý`, thấy n3 và hoàn thành nhanh nhất (75s), nhưng nhận xét: *"Thấy sẵn thì tiện thật, nhưng nếu slide nào cũng gợi ý thì màn hình rất chật"*. | Tốc độ nhanh trong kịch bản mẫu không đồng nghĩa với trải nghiệm học tập tốt về lâu dài nếu gây ô nhiễm thị giác. | Cần cơ chế bật/tắt rõ ràng. |
| **T03-E02** | Option C / 00:45 | Tester chủ động tìm và click nút `Tắt gợi ý`, panel co lại gọn gàng, tester khen: *"Phải cho tắt như này thì lúc học bài khó mới không bị ngắt dòng suy nghĩ"*. | Nhu cầu kiểm soát (User Agency) là yếu tố quyết định sự chấp nhận của người học đối với các tính năng gợi ý chủ động. | Khẳng định giá trị của nút Tắt gợi ý. |
| **T03-E03** | Option A / 00:08 | Gõ từ khóa chuẩn xác `"prototype"`, hệ thống trả về đúng note n3 duy nhất, tester click và hoàn thành trong 100s mà không gặp bất kỳ vướng víu nào. | Với người học có trí nhớ tốt về thuật ngữ, tìm kiếm từ khóa truyền thống vẫn là luồng làm việc trực quan và đáng tin cậy nhất. | Đối lập rõ rệt với trường hợp T02 bí từ khóa. |
| **T03-E04** | Option B / 00:26 | Khi tìm bằng ý `"thử nghiệm ý tưởng"`, hệ thống hiển thị 2 kết quả (n3 đứng đầu, n2 đứng nhì). Tester mất 4 giây đọc so sánh để loại bỏ n2 trước khi bấm n3. | Sự đánh đổi của cơ chế tìm theo ý: giảm công nhớ từ khóa nhưng tăng công sức lọc nhiễu kết quả đối chiếu. | Đòi hỏi giao diện phải làm nổi bật note có độ phù hợp cao nhất. |

---

## 3. So sánh và Đánh đổi (Trade-off)

- **Selected Option:** **Option B** kết hợp với sự chủ động của **Option A**.
- **Lý do của người dùng:** *"Option C ban đầu nhìn thì thấy nhanh nhất vì nó nằm sẵn ở đó, nhưng khi học bài thực tế, việc hệ thống tự đẩy nội dung ra rất dễ làm mình xao nhãng. Option B là phương án cân bằng tốt nhất: mình chỉ gọi khi mình thực sự cần (On-demand), và nó cho phép mình tìm bằng ý hiểu mà không phải nhớ chính xác từ khóa."*
- **Đánh đổi chấp nhận:** Chấp nhận phải tự tay nhập câu mô tả và phải liếc qua 2 kết quả để lọc kết quả nhiễu, đổi lấy một không gian học tập yên tĩnh, tập trung và quyền chủ động 100%.
- **Bước muốn tự làm / giao hệ thống:**
  - *Muốn tự làm:* Chủ động kích hoạt việc tìm kiếm khi có nhu cầu; tự đánh giá và chọn note.
  - *Giao hệ thống:* Thực hiện tìm kiếm ngữ nghĩa ngầm khi được yêu cầu.
- **Counter-evidence:** Option C hoàn thành với thời gian ngắn nhất (75s), nhưng vẫn bị người dùng từ chối làm phương án mặc định vì rủi ro gây mất tập trung (trade-off giữa tốc độ cơ học và sự tĩnh tâm trong học tập).
- **Quote nguyên văn:** *"Học slide phức tạp cần tập trung cao độ. Mình muốn hệ thống hỗ trợ khi mình gọi (On-demand), chứ đừng tự động xuất hiện (Proactive) làm phân mảnh tư duy."*

---

## 4. Bốn tầng phân tích (Four Layers)

- **Observed:**
  - T03 hoàn thành cả 3 option trong thời gian ngắn (C: 75s, B: 90s, A: 100s).
  - T03 chủ động bấm "Tắt gợi ý" ở Option C để kiểm tra quyền kiểm soát giao diện (T03-E02).
  - T03 mất thêm 4s đối chiếu để lọc kết quả nhiễu n2 ở Option B (T03-E04).
- **Interpreted:**
  - Sự khác biệt về quan điểm giữa các tester: người học có tư duy hệ thống và chú trọng tập trung sâu (như T03) sẽ ưu tiên mô hình On-demand (B/A) hơn mô hình Proactive (C).
  - Tốc độ hoàn thành task trong bài test ngắn hạn không phản ánh đầy đủ sự hài lòng hay hiệu quả học tập thực tế; yếu tố "giữ mạch học" (cognitive flow) quan trọng hơn vài giây bấm phím.
- **Decided — Next Change đề xuất cá nhân:**
  - Thiết kế mặc định thu gọn cho panel gợi ý Option C (hoặc cho phép ghi nhớ trạng thái tắt trong cài đặt học tập), đồng thời bổ sung chỉ báo slide đích cụ thể trên nút quay lại slide đang học.
- **Still Unproven:**
  - Chưa chứng minh được liệu sau 1-2 tuần sử dụng liên tục, người học có thay đổi thói quen và dần phụ thuộc vào gợi ý của Option C hay không.
