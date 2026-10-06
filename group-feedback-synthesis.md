# Chặng 6 — Group Feedback Synthesis

**Bản tổng hợp dữ liệu kiểm thử thực tế nhóm 3aecaykhe**  
*Thành viên:* Nguyễn Văn An (2A202602776), Lưu Xuân Dũng (2A202602746), Nguyễn Long Khánh  
*Case:* B — AI Notes: Personal Learning Notes · *Ngày tổng hợp:* 06/10/2026  
*Nguồn dữ liệu:* Ba biên bản quan sát thực tế độc lập: [An / T01](prototype-feedback-note.md), [Dũng / T02](feedback-templates/feedback-dung.md), [Khánh / T03](feedback-templates/feedback-khanh.md).

---

## Bảng đối chiếu chéo ba phiên kiểm thử (Cross-Session Comparison)

| Đối chiếu tiêu điểm | T01 / Thứ tự ABC (An điều phối) | T02 / Thứ tự BCA (Dũng điều phối) | T03 / Thứ tự CAB (Khánh điều phối) | Pattern / Đối lập & Event IDs |
|---|---|---|---|---|
| **First action** | A: Gõ `"giả thuyết"` (00:12); B: Gõ câu ý nghĩa (00:15); C: Mở 2 gợi ý (00:08). | B: Gõ câu ý nghĩa (00:10); C: Mở 2 gợi ý (00:06); A: Gõ từ đồng nghĩa `"thực hành"` (00:14). | C: Mở 2 gợi ý (00:05); A: Gõ từ kỹ thuật `"prototype"` (00:08); B: Gõ cụm từ (00:12). | **Pattern:** Ở C cả 3 đều mở gợi ý ngay (<10s). Ở A/B người dùng nhập truy vấn ngay mà không chần chừ (T01-E01, T02-E01, T03-E01). |
| **Major breakdown** | A: Suýt bấm `Back` trình duyệt khi xem xong slide e1 (01:10). C: Sợ nút "Bỏ gợi ý" làm mất note. | A: Gõ từ đồng nghĩa không ra kết quả, dừng >8s, phải cuộn tìm thủ công. C: Bấm nhầm `Slide tiếp →`. | B: Mất 4s đối chiếu để lọc note nhiễu n2 trước khi chọn n3. C: Lo ngại màn hình bị chật. | **Breakdown chung:** Vấn đề điều hướng quay lại slide học xuất hiện ở cả T01 (T01-E02) và T02 (T02-E02). Gõ sai từ khóa làm tê liệt A (T02-E03). |
| **Evidence checking** | Đọc badge nguồn `e1` ở cả 3 option; kiểm tra kỹ slide nguồn e1 trước khi quay về. | Đọc nhãn "Có thể phù hợp" ở B; mở slide e1 đọc kỹ rồi mới quay lại. | Đọc lý do khớp ở B; mở e1 đọc lướt 10s rồi bấm quay lại e2. | **Pattern:** 100% tester đều mở slide nguồn e1 để đối chiếu trước khi quay lại, xác nhận hành vi kiểm chứng nguồn là nhu cầu có thật. |
| **Control / Recovery** | Thử tắt gợi ý ở C để giải phóng không gian học; an tâm khi thấy note gốc còn nguyên sau khi bỏ gợi ý. | Tự khôi phục ở A bằng cách cuộn danh sách sổ thủ công sau khi từ khóa thất bại. | Bấm tắt gợi ý ở C (T03-E02); tự phân biệt note đúng/nhiễu ở B (T03-E04). | **Pattern:** Nhu cầu kiểm soát (tắt/bật gợi ý, giữ nguyên văn note gốc) được nhấn mạnh ở cả 3 phiên (T01-E03, T01-E05, T03-E02). |
| **Selected option** | **Option A** (kết hợp B khi bí từ khóa). | **Option B** (Tìm theo ý nhớ). | **Option B** (kết hợp A on-demand). | **Lựa chọn đa số:** 2/3 tester chọn Option B làm công cụ tìm kiếm chính; 1/3 chọn A vì tính an tâm kiểm soát. Không ai chọn C làm mặc định. |
| **Key trade-off** | Chấp nhận tự nhớ từ khóa/lướt sổ để đổi lấy sự tập trung, không bị gián đoạn. | Chấp nhận kết quả có thể có note chưa trúng để không phải vắt óc nhớ đúng từ khóa. | Chấp nhận tự bấm tìm kiếm on-demand đổi lấy không gian học yên tĩnh, không bị gợi ý tự động. | **Trade-off chung:** Đánh đổi công sức thao tác chủ động (On-demand) để giữ sự tập trung sâu; từ chối gợi ý chủ động tự động (Proactive) vì sợ phân tâm. |
| **Hoàn thành / Trợ giúp** | A: 115s (0 TG); B: 80s (0 TG); C: 135s (1 TG). | B: 70s (0 TG); C: 105s (0 TG); A: 150s (1 TG). | C: 75s (0 TG); A: 100s (0 TG); B: 90s (0 TG). | **Kết quả:** 100% hoàn thành task. B có thời gian trung bình nhanh và ổn định nhất (80s). C nhanh về cơ học nhưng tốn thời gian phân vân. |

---

## 1. Tầng Observed (Dữ kiện quan sát thực tế)

Từ ba phiên thực địa, nhóm ghi nhận các cụm sự kiện then chốt sau:

1. **Hành vi truy hồi note (Retrieval Behavior):**
   - Khi tester nhớ được từ khóa chính xác (T01 nhớ `"giả thuyết"` — T01-E01; T03 nhớ `"prototype"` — T03-E03), Option A hoạt động rất nhanh và dứt khoát (100s – 115s).
   - Khi tester dùng từ đồng nghĩa hoặc diễn giải (T02 gõ `"thực hành"` — T02-E03), Option A trả về rỗng, khiến tester dừng lại >8 giây và buộc phải cuộn duyệt thủ công (T02-E04), thời gian tăng vọt lên 150s.
   - Ở Option B, cả 3 tester đều nhập được câu văn tự nhiên và nhận ngay note n3 ở top 1 (T01-E03, T02-E01, T03-E04), giúp hoàn thành task với thời gian trung bình tốt nhất (80s).
2. **Hành vi kiểm chứng nguồn (Evidence Checking):**
   - Cả 3 tester (T01, T02, T03) đều nhấp vào thẻ note để mở slide nguồn e1 đối chiếu nội dung gốc trước khi tiếp tục học. Không có tester nào bỏ qua bước kiểm tra nguồn.
3. **Sự cố điều hướng quay lại slide đang học (Navigation Friction):**
   - T01 di chuột lên thanh công cụ trình duyệt và dừng 4s suýt bấm nút `Back` của Chrome do không thấy ngay nút quay lại trên trang (T01-E02).
   - T02 đọc xong slide nguồn e1 thì lúng túng bấm nút `Slide tiếp →` trên thanh phân trang slide để chuyển sang e2 thay vì dùng nút quay lại ở banner (T02-E02).
4. **Phản ứng với tính năng gợi ý chủ động (Option C):**
   - T01 hiểu nhầm nút "Bỏ gợi ý" là xóa hẳn note khỏi sổ (T01-E04).
   - Cả T01 (T01-E05) và T03 (T03-E02) đều chủ động bấm nút "Tắt gợi ý" để kiểm tra khả năng đóng panel, và đều nhận xét rằng gợi ý tự động liên tục sẽ gây xao nhãng trong bài học phức tạp.

---

## 2. Tầng Interpreted (Phân tích & Diễn giải giả thuyết)

- **Pattern 1 — Giá trị của Tìm kiếm theo ý nhớ (Option B):** Option B giải quyết triệt để vấn đề "lệch từ vựng" (vocabulary mismatch) của Option A. Với người học ghi chép tự do, khả năng tìm theo ý là một bước nhảy vọt về mặt tiện ích (giảm thời gian từ 150s xuống 70s ở T02). Tuy nhiên, cái giá phải trả là chi phí nhận thức để loại bỏ kết quả nhiễu (T03 mất 4s để đọc và loại bỏ n2).
- **Pattern 2 — Điểm gãy luồng điều hướng (The Return Navigation Breakdown):** Điểm yếu cốt tử trong trải nghiệm của cả 3 option không nằm ở khâu tìm kiếm, mà nằm ở **khâu quay trở lại mạch học sau khi xem nguồn**. Khi người học bị điều hướng sang một slide khác trong quá khứ (slide e1), họ bị mất neo ngữ cảnh (loss of context). Nút quay lại dạng banner chữ hiện tại quá chìm, khiến người dùng có xu hướng dùng các công cụ quen thuộc nhưng sai lầm (nút Back trình duyệt hoặc nút Next của slide).
- **Mâu thuẫn & Đối lập — Tốc độ cơ học vs Trải nghiệm học sâu:** Option C có thời gian cơ học nhanh nhất ở T03 (75s) và T01 (khi mở sẵn), nhưng cả T01 và T03 đều từ chối chọn C làm phương án ưa thích. Lý do: trong học tập, sự chủ động (Agency) và không gian yên tĩnh (Cognitive Flow) quan trọng hơn vài giây tiết kiệm được từ việc hệ thống tự đẩy nội dung ra. Người học muốn hệ thống ở trạng thái "gọi thì mới có" (On-demand) chứ không phải "tự động chen ngang" (Proactive).

---

## 3. Tầng Decided — Đúng một Group Next Change

Sau buổi họp tổng hợp kết quả của cả 3 thành viên (An, Dũng, Khánh) vào tối ngày 06/10/2026, nhóm thống nhất quyết định đúng một thay đổi duy nhất cho chu kỳ tiếp theo:

> **Ở thanh thông báo quay lại slide nguồn (Return banner / Source viewer), đổi nút quay lại dạng văn bản hiện tại thành thanh ghim nổi bật cố định (Sticky Return Bar) có màu nhấn tương phản, ghi rõ đích đến cụ thể: `← Quay lại slide đang học (Slide 2: Ai bắt đầu hỗ trợ?)` kèm phím tắt `Esc` và breadcrumb vị trí, đồng thời đổi nhãn "Bỏ gợi ý" ở Option C thành "Ẩn gợi ý này (giữ nguyên trong sổ)"; vì tester T01 do dự 4 giây và suýt bấm Back trình duyệt (T01-E02), tester T02 bấm nhầm nút phân trang slide và lo mất dấu bài học (T02-E02), và tester T01 lo sợ việc bỏ gợi ý sẽ xóa mất ghi chú gốc (T01-E04). Kiểm tra vòng sau bằng kịch bản mở slide nguồn ở khoảng cách xa (từ slide 15 quay lại slide 42), quan sát xem 100% người dùng có click ngay nút quay lại trong vòng dưới 2 giây mà không cần dò tìm hay bấm nhầm phím back trình duyệt.**

---

## 4. Tầng Still Unproven (Những điều chưa thể kết luận)

Sau 3 phiên kiểm thử thực tế, nhóm nhận thức rõ các giới hạn còn tồn tại:

1. **Quy mô dữ liệu dài hạn:** Dữ liệu thử nghiệm chỉ gồm 5 slide và 5 note mẫu. Chưa chứng minh được liệu khi một khóa học có 200 slide và hơn 50 note thì cơ chế tìm theo ý của Option B có giữ được độ chính xác cao hay sẽ trả về quá nhiều kết quả nhiễu khiến người dùng mất kiên nhẫn.
2. **Hiệu quả học tập và ghi nhớ thực tế (Retention & Learning Outcomes):** Thử nghiệm 20 phút đo lường được tính khả dụng tương tác (usability & task completion), nhưng chưa đo lường được liệu việc có liên kết slide nguồn có thực sự giúp người học hiểu bài sâu hơn và đạt điểm số cao hơn trong các bài kiểm tra VLearn hay không.
3. **Mức độ phụ thuộc vào gợi ý:** Chưa kiểm chứng được trong một khoảng thời gian dài (2-4 tuần), liệu người học có dần quen với các gợi ý của Option C và chuyển từ e ngại sang phụ thuộc hay không.
