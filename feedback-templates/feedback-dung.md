# Prototype Feedback Note — Lưu Xuân Dũng

**Biên bản quan sát kiểm thử người dùng thực tế**  
*Mã phiên:* T02 · *Thực hiện bởi Facilitator:* Lưu Xuân Dũng

| Trường | Giá trị |
|---|---|
| Facilitator | Lưu Xuân Dũng (2A202602746) |
| Tester | T02 — Hoàng Thu Hà (21 tuổi, sinh viên năm 3 Kinh tế Quốc tế) |
| Ngoài nhóm / context thật | Người ngoài nhóm; đang tự học các khóa Quản trị kinh doanh trên VLearn, hay ghi chú bằng lời văn cá nhân |
| Ngày / thiết bị / consent | 06/10/2026 (15:30 – 15:55); Asus Zenbook 14, Windows 11, Chrome; Đã ký consent đồng ý quan sát và ghi chép |
| Thứ tự kiểm thử | B → C → A (Counterbalance) |
| Phiên bản prototype | Day19 An v2 (commit 1f43d01) |
| Câu trả lời context question | "Em hay ghi chép theo kiểu tóm tắt ý hiểu của mình. Nhiều khi tuần sau xem lại chỉ nhớ mang máng là mình từng ghi một ý liên quan đến chuyện đó, chứ không thể nào nhớ nổi lúc đó mình dùng từ khóa gì để search." |

---

## 1. Quan sát A/B/C theo 7 tiêu điểm

| Tiêu điểm | B — fact/mốc (Tìm theo ý nhớ) | C — fact/mốc (Gợi theo slide) | A — fact/mốc (Tự tìm từ khóa) |
|---|---|---|---|
| **First action** | 00:10: Đọc placeholder "Tả ý bạn muốn nhớ lại…", gõ câu tự nhiên: `"thử nghiệm ý tưởng chứ không phải đem đi biểu diễn"`. Bấm Tìm. | 00:06: Thấy khung "Note cũ liên quan" nằm bên dưới slide bài giảng, click ngay nút `"Mở 2 gợi ý"`. | 00:14: Click ô input tìm kiếm, gõ từ khóa `"thực hành"`. Kết quả rỗng, hệ thống báo "Chưa tìm thấy note phù hợp…". |
| **Hesitation >3 giây** | 00:25 (3 giây): Dừng mắt đọc kết quả note n3 đứng ở vị trí số 1, đọc nhãn "Có thể phù hợp". | 00:15 (5 giây): Dừng đọc 2 thẻ gợi ý, phân vân đối chiếu giữa tiêu đề slide đang học và nội dung note n3. | 00:28 (8 giây): Dừng cắn môi sau khi gõ từ khóa không ra kết quả, ngập ngừng không biết nên gõ từ gì tiếp theo. |
| **Evidence read/ignored** | 00:32: Đọc nhãn "Có thể phù hợp" và lý do "Khớp nhóm ý trong mô tả". Bấm note n3 mở slide e1 để xem lại bối cảnh gốc. | 00:35: Click vào thẻ note n3, chuyển sang slide e1 đọc nội dung slide gốc trong 15 giây. | 00:50: Xóa trắng ô tìm kiếm, cuộn chuột qua từng thẻ trong danh sách toàn bộ 5 note để đọc thủ công từng cái. |
| **Misunderstanding** | Không có hiểu lầm; nhận ra ngay hệ thống trả về đúng các ghi chú cũ của mình theo mức độ liên quan. | 00:55: Khi đang ở slide nguồn e1, tester bấm nút chuyển slide kế tiếp (`Slide tiếp →`) trên thanh pager thay vì nút banner "Quay lại slide đang học". | 00:40: Tưởng hệ thống bị lỗi tìm kiếm khi gõ "thực hành" không ra kết quả; facilitator giữ im lặng để tester tự nhận ra tính năng tìm từ khóa chính xác. |
| **Help needed: câu/số lần** | **0 lần** (Tự thao tác rất trôi chảy). | **0 lần** (Tự điều hướng được sau một nhịp khựng lại). | **1 lần** (00:45): Hỏi: *"Có cách nào xem hết ghi chú theo thứ tự từng bài học không anh?"*. Facilitator chỉ vào dropdown bộ lọc bài học. |
| **Correction/recovery** | Kết quả khớp ngay note n3 ở đầu danh sách, không cần phục hồi hay sửa câu truy vấn. | Sau khi bấm nhầm nút pager sang e2, tester thốt lên: *"May là slide 1 sang slide 2 luôn, chứ nếu xa nhau thì lạc mất"*. | Xóa từ khóa, dùng bộ lọc hoặc cuộn danh sách thủ công để tìm ra note n3. |
| **Note chọn / nguồn / quay lại** | Chọn n3; mở slide e1; bấm "Quay lại slide đang học (e2)" thành công. | Chọn n3; mở slide e1; quay về e2 thành công. | Chọn n3; mở slide e1; bấm "Quay lại slide đang học (e2)" thành công. |
| **Hoàn thành / giây / trợ giúp** | **Hoàn thành** / **70 giây** (1p10s) / 0 trợ giúp. | **Hoàn thành** / **105 giây** (1p45s) / 0 trợ giúp. | **Hoàn thành** / **150 giây** (2p30s) / 1 trợ giúp. |

---

## 2. Event Register (Biên bản sự kiện)

| ID | Option/mốc | OBSERVED (Hành vi & lời nói nguyên văn) | INTERPRETED (Diễn giải & giả thuyết) | Probe / Đối chiếu |
|---|---|---|---|---|
| **T02-E01** | Option B / 00:10 | Nhập câu diễn đạt tự nhiên: `"thử nghiệm ý tưởng chứ không phải đem đi biểu diễn"`, kết quả trả về n3 đầu tiên. Tester thốt lên: *"Ồ tiện thế, em không cần nhớ chính xác từ khóa luôn"*. | Khả năng truy hồi theo ngữ nghĩa (semantic retrieval) giải phóng gánh nặng trí nhớ cho người học ghi chép tự do. | Phù hợp giả thuyết thiết kế của Option B. |
| **T02-E02** | Option C / 00:55 | Mở slide e1 đọc xong, tester bối rối tìm đường quay lại, bấm nút `Slide tiếp →` trên thanh điều hướng slide thay vì nút banner `Quay lại slide đang học`. | Nút quay lại slide học hiện tại đang bị chìm vào giao diện slide, khiến người dùng dùng quán tính bấm nút phân trang slide. | Tín hiệu mạnh mẽ cho thấy cần thiết kế nút quay lại nổi bật và định vị rõ rệt. |
| **T02-E03** | Option A / 00:28 | Tester gõ từ đồng nghĩa `"thực hành"` nhưng note dùng từ `"prototype"` và `"giả thuyết"`, danh sách trả về rỗng. Tester dừng >8 giây, cắn môi suy nghĩ. | Điểm nghẽn lớn nhất của Option A (tìm từ khóa truyền thống): sự không trùng khớp từ vựng giữa lúc nhớ lại và lúc ghi chép. | Tester thừa nhận: *"Bí từ là đứng hình luôn"*. |
| **T02-E04** | Option A / 00:50 | Sau khi bí từ khóa, tester xóa ô input và phải dùng mắt quét thủ công qua từng note trong sổ để tìm kiếm ý cần thiết. | Khi tìm kiếm thất bại, chi phí thời gian và công sức tăng vọt do phải duyệt tuần tự. | Thời gian hoàn thành Option A tăng lên 150s (gấp đôi Option B). |

---

## 3. So sánh và Đánh đổi (Trade-off)

- **Selected Option:** **Option B** (Tìm theo ý nhớ).
- **Lý do của người dùng:** *"Option B cứu cánh cực kỳ cho người hay nhớ ý như em. Em không cần nhớ chính xác từ 'prototype' hay 'giả thuyết', chỉ cần gõ đúng ý mình nhớ trong đầu là ra ngay note gốc. Option A bắt em phải đoán đúng từ khóa thì rất mệt mỏi."*
- **Đánh đổi chấp nhận:** Chấp nhận hệ thống có thể trả ra 1-2 note gợi ý chưa trúng hẳn và phải liếc mắt đọc đối chiếu, miễn là không bắt người học phải vắt óc nhớ đúng từng con chữ đã viết như Option A.
- **Bước muốn tự làm / giao hệ thống:**
  - *Muốn tự làm:* Đọc và đối chiếu nội dung slide nguồn gốc để tự kiểm tra kiến thức.
  - *Giao hệ thống:* Tự động xếp hạng và tìm kiếm theo ngữ nghĩa các ghi chú có liên quan.
- **Counter-evidence:** Nếu người dùng nhớ chính xác từ khóa ngắn (như T01 nhớ từ "giả thuyết"), Option A gõ rất nhanh; nhưng với người dùng quen viết diễn giải như T02, Option A gây nghẽn nghiêm trọng.
- **Quote nguyên văn:** *"Gõ câu văn tự nhiên thoải mái hơn nhiều so với việc ngồi vắt óc đoán xem hôm trước mình đã dùng từ khóa gì."*

---

## 4. Bốn tầng phân tích (Four Layers)

- **Observed:**
  - T02 hoàn thành Option B nhanh nhất (70s), Option C (105s), Option A chậm nhất (150s).
  - T02 gặp điểm nghẽn nghiêm trọng ở Option A khi gõ từ đồng nghĩa không khớp (T02-E03, dừng >8s).
  - T02 bấm nhầm nút chuyển slide thay vì nút quay lại slide học ở Option C (T02-E02).
- **Interpreted:**
  - Sự cách biệt thời gian (70s vs 150s) chứng minh giá trị vượt trội của cơ chế tìm theo ý nhớ (Option B) đối với đối tượng học viên không ghi nhớ chính xác thuật ngữ.
  - Vấn đề điều hướng "Quay lại slide đang học" tiếp tục xuất hiện ở T02 (tương tự như T01 suýt bấm Back trình duyệt), khẳng định đây là lỗi tương tác mang tính hệ thống cần ưu tiên xử lý.
- **Decided — Next Change đề xuất cá nhân:**
  - Nâng cấp thành phần quay lại slide đang học thành **nút ghim nổi (floating sticky button)** với màu sắc nhận diện rõ ràng và ghi rõ số slide đích, ví dụ: `← Quay lại Slide đang học: e2`.
- **Still Unproven:**
  - Chưa chứng minh được độ chính xác của cơ chế tìm theo ý khi số lượng ghi chú trong sổ lên tới hàng ngàn note với nhiều chủ đề tương tự nhau.
