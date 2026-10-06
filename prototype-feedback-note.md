# Prototype Feedback Note — Nguyễn Văn An

**Biên bản quan sát kiểm thử người dùng thực tế**  
*Mã phiên:* T01 · *Thực hiện bởi Facilitator:* Nguyễn Văn An

| Trường | Giá trị |
|---|---|
| Facilitator | Nguyễn Văn An (2A202602776) |
| Tester | T01 — Trần Minh Tuấn (22 tuổi, sinh viên CNTT, học viên tự học trên VLearn) |
| Ngoài nhóm / context thật | Người ngoài nhóm; đang học khóa Product Management trên VLearn, có thói quen vừa học vừa ghi chép |
| Ngày / thiết bị / consent | 06/10/2026 (14:00 – 14:25); Dell XPS 13, Windows 11, Chrome 129; Đã ký consent đồng ý quan sát và ghi chép |
| Thứ tự kiểm thử | A → B → C (Counterbalance) |
| Phiên bản prototype | Day19 An v2 (commit 1f43d01) |
| Câu trả lời context question | "Tuần trước học phần Product Metrics, mình muốn tìm lại công thức North Star Metric ghi hồi bài trước. Vì note nằm rải rác ở từng slide của bài cũ, mình phải bấm qua từng bài rồi click từng slide để tìm, mất gần 10 phút rất bực nên sau đó phải mở Google Docs ra note riêng." |

---

## 1. Quan sát A/B/C theo 7 tiêu điểm

| Tiêu điểm | A — fact/mốc (Tự tìm từ khóa) | B — fact/mốc (Tìm theo ý nhớ) | C — fact/mốc (Gợi theo slide) |
|---|---|---|---|
| **First action** | 00:12: Click ngay ô input tìm kiếm, gõ từ khóa `"giả thuyết"`. | 00:15: Đọc placeholder ô tìm kiếm, gõ câu tự nhiên: `"làm prototype để test ý tưởng chứ ko phải show"`. | 00:08: Nhìn thấy panel "Note cũ liên quan", bấm ngay nút `"Mở 2 gợi ý"`. |
| **Hesitation >3 giây** | 00:28 (4 giây): Dừng chuột khi thẻ note n3 xuất hiện trong danh sách, đọc lướt nội dung trước khi click. | 00:35 (3 giây): Dừng đọc nhãn "Có thể phù hợp" trên thẻ n3, kiểm tra xem note có bị sửa câu chữ không. | 00:18 (6 giây): Dừng mắt đọc cả 2 note gợi ý (n3 và n1), phân vân vì sao n1 ("Build trap...") lại được gợi ý ở slide này. |
| **Evidence read/ignored** | 00:45: Đọc kỹ badge nguồn `e1 — Thiết kế thử nghiệm, slide 1`. Bấm vào thẻ, mở slide e1 đối chiếu nội dung định nghĩa prototype. | 00:40: Đọc nhãn "Có thể phù hợp" và lý do "Khớp nhóm ý trong mô tả". Bấm n3 để mở slide e1 đối chiếu. | 00:30: Đọc nhãn "Liên quan rõ" ở n3 và "Chưa chắc liên quan" ở n1. Bấm n3 để mở slide e1. |
| **Misunderstanding** | 01:10: Đọc xong slide e1, tester di chuột lên góc trên định bấm nút Back của trình duyệt Chrome, nhưng kịp nhìn thấy nút `"Quay lại slide đang học (e2)"` ở banner. | 00:25: Tưởng ban đầu là ô chat hỏi đáp với trợ giảng AI, nhưng thấy trả ra đúng thẻ note cũ thì nhận xét: *"À, nó chỉ lọc đúng note cũ của mình thôi"*. | 01:05: Hiểu nhầm nút "Bỏ gợi ý" là xóa hẳn ghi chú khỏi sổ ghi chép cá nhân. |
| **Help needed: câu/số lần** | **0 lần** (Tự thao tác hoàn toàn). | **0 lần** (Tự thao tác hoàn toàn). | **1 lần** (01:08): Hỏi: *"Nút Bỏ gợi ý này là xóa hẳn note khỏi sổ luôn à anh?"*. Facilitator hỏi lại: *"Theo bạn nó nên hoạt động thế nào?"*. Tester thử bấm n1, thấy toast báo note gốc còn nguyên thì thở phào. |
| **Correction/recovery** | Tự nhận diện nút quay lại banner sau 4 giây phân vân định bấm browser back. | Kết quả trả đúng n3 ở top 1, không cần chỉnh sửa lại câu truy vấn. | Bấm "Bỏ gợi ý" ở n1 để dọn dẹp panel; thử bấm "Tắt gợi ý" để kiểm tra cách khôi phục lại không gian học. |
| **Note chọn / nguồn / quay lại** | Chọn đúng n3; mở slide e1; bấm "Quay lại slide đang học (e2)" về e2 an toàn. | Chọn đúng n3; mở slide e1; bấm "Quay lại slide đang học (e2)" về e2 an toàn. | Chọn đúng n3; mở slide e1; bấm "Quay lại slide đang học (e2)" về e2 an toàn. |
| **Hoàn thành / giây / trợ giúp** | **Hoàn thành** / **115 giây** (1p55s) / 0 trợ giúp. | **Hoàn thành** / **80 giây** (1p20s) / 0 trợ giúp. | **Hoàn thành** / **135 giây** (2p15s) / 1 trợ giúp. |

---

## 2. Event Register (Biên bản sự kiện)

| ID | Option/mốc | OBSERVED (Hành vi & lời nói nguyên văn) | INTERPRETED (Diễn giải & giả thuyết) | Probe / Đối chiếu |
|---|---|---|---|---|
| **T01-E01** | Option A / 00:12 | Tester gõ `"giả thuyết"` vào ô tìm kiếm, hệ thống hiển thị duy nhất note n3. | Nhớ được một từ khóa đinh trong câu ghi chú giúp tìm kiếm trực tiếp rất hiệu quả. | Tester xác nhận: *"Mình còn nhớ chữ giả thuyết nên gõ là ra ngay"*. |
| **T01-E02** | Option A / 01:10 | Sau khi đọc slide nguồn e1, tester di chuột lên thanh công cụ trình duyệt định bấm `Back`, dừng lại 4s rồi nhìn thấy nút `Quay lại slide đang học (e2)` ở đầu trang slide. | Nguy cơ mất context học khi chuyển trang: người dùng quen dùng phím back trình duyệt nếu nút quay lại không đủ nổi bật. | Cần làm nút quay lại slide đang học thành dạng sticky/nổi bật hơn để tránh bấm nhầm Back trình duyệt. |
| **T01-E03** | Option B / 00:35 | Tester nhìn nhãn `"Có thể phù hợp"`, đọc kỹ từng chữ của n3 và thốt lên: *"May quá chữ mình viết vẫn nguyên xi, không bị sửa"*. | Nỗi sợ AI tự ý tóm tắt hoặc viết lại làm sai lệch ý hiểu cá nhân của người học. | Tester đánh giá cao việc hiển thị nguyên văn nội dung note gốc. |
| **T01-E04** | Option C / 01:05 | Thấy note n1 hiển thị cùng n3, tester chỉ vào nút `Bỏ gợi ý` và hỏi facilitator: *"Nút Bỏ gợi ý này là xóa hẳn note khỏi sổ luôn à anh?"*. | Từ ngữ "Bỏ gợi ý" có thể gây mơ hồ giữa "ẩn gợi ý" và "xóa dữ liệu gốc". | Toast xác nhận sau click giúp tester an tâm: *"May quá, note gốc vẫn còn"*. |
| **T01-E05** | Option C / 01:45 | Tester bấm nút `Tắt gợi ý`, panel đóng lại gọn gàng, tester gật gù: *"Khi nào cần tập trung đọc slide thì tắt đi thế này đỡ bị ngứa mắt"*. | Nhu cầu kiểm soát không gian thị giác và quyền tắt gợi ý chủ động khi cần học sâu. | Khẳng định tầm quan trọng của Agency và Control trong thiết kế gợi ý chủ động. |

---

## 3. So sánh và Đánh đổi (Trade-off)

- **Selected Option:** **Option A** (đối với việc học thường nhật), kết hợp **Option B** (khi hoàn toàn quên từ khóa).
- **Lý do của người dùng:** *"Option A mang lại cảm giác an tâm và kiểm soát 100%. Mình tự quản lý sổ ghi chép của mình, khi nào cần tìm thì gõ từ khóa. Option B tìm theo ý rất thông minh khi mình bí từ, nhưng Option C thì gợi ý tự động làm mình mất tập trung vào slide chính."*
- **Đánh đổi chấp nhận:** Chấp nhận mất công nhớ mang máng từ khóa hoặc phải lướt danh sách sổ ghi chép, để đổi lấy sự tập trung tối đa trong lúc nghe giảng, không bị các khối gợi ý tự động làm phân tán tư duy.
- **Bước muốn tự làm / giao hệ thống:**
  - *Muốn tự làm:* Tự quyết định thời điểm tìm kiếm, tự chọn note và tự đánh giá độ liên quan.
  - *Sẵn lòng giao hệ thống:* Hỗ trợ tìm kiếm ngữ nghĩa khi quên từ khóa (cơ chế Option B).
- **Counter-evidence:** Khi người học quên bẵng từ khóa lúc trước đã viết, Option A sẽ bị nghẽn (phải lướt thủ công); lúc đó cơ chế tìm theo ý của Option B tỏ ra vượt trội rõ rệt về tốc độ (80s vs 115s).
- **Quote nguyên văn:** *"Option A cho mình cảm giác kiểm soát hoàn toàn 100%. Option C tiện nhưng mình cứ bị chú ý vào cái khung gợi ý xem nó nói cái gì, thành ra mất tập trung vào bài giảng chính."*

---

## 4. Bốn tầng phân tích (Four Layers)

- **Observed:**
  - T01 hoàn thành task ở cả 3 option (B nhanh nhất: 80s, A: 115s, C: 135s).
  - T01 suýt bấm Back trình duyệt khi mở slide nguồn ở Option A (T01-E02).
  - T01 do dự và đặt câu hỏi về nguy cơ mất note khi thấy nút "Bỏ gợi ý" ở Option C (T01-E04).
  - T01 đánh giá cao việc giữ nguyên văn note gốc ở Option B (T01-E03).
- **Interpreted:**
  - Việc gom ghi chú vào một sổ chung và có đường dẫn quay về nguồn slide giải quyết trúng pain phân tán từ Day17.
  - Tuy nhiên, luồng "Quay lại slide đang học" sau khi nhảy sang slide nguồn là điểm ma sát tương tác lớn nhất: người dùng rất dễ nhầm lẫn hoặc hoang mang về vị trí hiện tại nếu giao diện không chỉ rõ lối thoát.
  - Gợi ý chủ động (Option C) tạo ra gánh nặng nhận thức (cognitive load) ngoài dự kiến nếu người học phải phân vân giải mã lý do tại sao hệ thống lại gợi ý một ghi chú không liên quan.
- **Decided — Next Change đề xuất cá nhân:**
  - Đổi nút quay lại sau khi xem nguồn thành **thanh thông báo cố định (Sticky Return Bar)** với thông tin ngữ cảnh rõ ràng: `← Quay lại slide đang học (Slide 2: Ai bắt đầu hỗ trợ?)` kèm phím tắt `Esc`, đồng thời đổi nhãn "Bỏ gợi ý" ở Option C thành **"Ẩn gợi ý này"**.
- **Still Unproven:**
  - Chưa chứng minh được liệu khi số lượng ghi chú lên tới hàng trăm note trong cả kỳ học thì việc tìm kiếm từ khóa ở Option A có còn giữ được hiệu quả không.
  - Chưa đo lường được mức độ ảnh hưởng của panel gợi ý Option C tới khả năng ghi nhớ dài hạn (retention) của học viên sau buổi học.
