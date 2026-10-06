# Chặng 2–3 — Three-option Design Sheet

Nhóm 3aecaykhe · Case B · Baseline [evidence](evidence-snapshot.md). Phiên bản 06/10/2026. A/B/C là ba flow riêng; không coi thiết kế là kết quả người dùng đã chấp nhận.

## Solution Parking Lot

| Hướng | Cơ chế | Quyết định |
|---|---|---|
| Sổ chung, tìm từ khóa, link slide | Không AI, người học tự tìm | Chọn A, baseline |
| Mô tả ý nhớ để tìm note gốc | AI đáp ứng yêu cầu, chỉ truy hồi | Chọn B |
| Gợi note cũ theo slide đang học | AI chủ động, user duyệt | Chọn C |
| Cornell/Outline cạnh slide | Template không AI | Giữ cho vòng sau, không kiểm retrieval |
| Bookmark/highlight | Không AI, gắn vị trí | Hữu ích cho capture, không phải trọng tâm vòng này |
| Tóm tắt cuối bài có review | AI sinh nội dung | Chưa chọn: evidence chưa đủ về khó capture |
| Câu hỏi ôn từ note đã duyệt | AI sinh câu hỏi | Chưa chọn: khác job cần so sánh |
| Note theo câu hỏi lớn xuyên bài | Không AI | Giữ alternative từ Khánh-SV2 |

Các hướng kế thừa parking lot Day17 và thiết kế của Dũng; việc chọn A/B/C là solution hypothesis.

## Comparison Contract

| Thành phần chung | Quyết định đóng băng |
|---|---|
| User | Learner VLearn đã tự ghi note; ưu tiên có lần mở lại gần đây |
| Situation | Đang học slide mẫu “Ai bắt đầu hỗ trợ?”, cần nhớ lại ý về mục đích prototype |
| Outcome task | Tìm note nói về thử ý tưởng thay vì chỉ trình diễn, mở slide gốc để kiểm tra, rồi quay lại slide đang học |
| Success quan sát | Chọn n3, mở e1, quay về e2 trong 4 phút, ghi rõ có/không trợ giúp; không tự suy là nhớ bài tốt hơn |
| Fixture | 5 slide/5 note giống nhau, cùng thứ tự; nội dung minh họa, không phải dữ liệu thực VLearn |
| Common flow | Cùng sổ, note nguyên bản, viết/lưu/sửa, nguồn, quay lại, bộ lọc và lỗi mẫu |
| Khác biệt | A keyword; B tìm theo ý; C đề xuất từ context |
| So sánh công bằng | Cùng máy/viewport, reset fixture, cùng task/giới hạn thời gian; T01 ABC, T02 BCA, T03 CAB |

“70% chung” là nguyên tắc đóng băng context/content/components, không phải tỷ lệ đo từ số dòng code. Toàn bộ fixture/task/shared flow giống nhau; vùng retrieval và trigger là phần biến thiên. Note mới dùng cùng một sổ trên từng option; dữ liệu từng option được tách để reset công bằng, không sync backend.

## Ba flow riêng — 3 trạng thái chính/option

### A — Sổ chung tự tìm

1. **Slide + sổ:** viết note, nguồn được chốt khi bắt đầu nhập, lưu vào sổ.
2. **Tìm từ khóa/duyệt:** gõ “prototype”, chọn thẻ note n3. Không có AI.
3. **Nguồn + quay lại:** thẻ mở e1, user đọc rồi dùng nút quay lại e2. Không tìm thấy thì đổi từ hoặc xem tất cả.

### B — Tìm theo ý nhớ

1. **Slide + ô mô tả:** mặc định chế độ tìm theo ý; capability nói rõ chỉ tìm note có sẵn.
2. **Ứng viên:** nhập “thử ý tưởng chứ không chỉ trình diễn”; trả note nguyên bản, lý do khớp mô phỏng và nhãn có thể phù hợp. User quyết định, không có câu trả lời kiến thức sinh mới.
3. **Kiểm nguồn + quay lại:** mở e1, đối chiếu, quay lại e2. Sai thì tả lại/chuyển Từ khóa; lỗi AI giữ note và nháp.

### C — Gợi theo slide

1. **Slide + gợi ý thu gọn:** khi mở e2, hệ thống tính ứng viên từ title/lead/points mẫu; không cần user nhập query.
2. **Duyệt gợi ý:** mở danh sách, xem note/lý do/nguồn; ghim để giữ, bỏ gợi ý để giảm nhiễu; note gốc không bị xóa.
3. **Nguồn + quay lại:** chọn n3 để mở e1, quay lại e2. Tắt gợi ý dừng panel, vẫn tự tìm trong sổ; không tự chuyển slide hoặc sửa note.

## Distance Check

| Cặp | Khác cơ chế | Đánh đổi |
|---|---|---|
| A–B | Khớp chuỗi user nhớ ↔ mô tả ý và xếp ứng viên | A dễ dự đoán; B chịu lỗi ghép ý |
| B–C | User khởi tạo truy vấn ↔ hệ thống khởi tạo từ slide | B cần nói nhu cầu; C có nguy cơ nhiễu |
| A–C | User tự tìm ↔ hệ thống chọn trước để user duyệt | Kiểm soát trực tiếp ↔ giảm bước bắt đầu nhưng cần kiểm nguồn |

## Human–AI Decision Table

| Quyết định | A | B | C |
|---|---|---|---|
| Expectation | Tìm từ khóa trong sổ | Tìm note theo ý; kết quả là ứng viên | Gợi note có thể liên quan slide, user tự quyết |
| Role & Agency | User chọn, hệ thống khớp chữ | AI xếp note, user kiểm nguồn/chọn | AI khởi tạo, user mở/bỏ/ghim/tắt |
| Act | Tìm sau thao tác user | Chạy sau yêu cầu tìm | Gợi khi slide đổi và đang bật |
| Ask | User tự đổi từ khóa | Không note đúng thì mời tả lại; không giả vờ có hội thoại thu hẹp thật | User chọn xem/giữ/bỏ; không hỏi xin quyền mỗi slide |
| Don't Act | Không suy luận, không sửa note | Không tạo đáp án/note hay sửa ghi chú | Không tự mở nguồn, thêm note hoặc overwrite nháp |
| Evidence | Nội dung note gốc + nguồn mẫu | Note gốc + lý do khớp mô phỏng + nguồn mẫu | Note gốc + chủ đề trùng + nguồn mẫu |
| Uncertainty | Thiếu nguồn ghi “Chưa gắn nguồn” | Có thể phù hợp, không hiển thị % tin cậy giả | Có thể liên quan, cần tự đối chiếu |
| Control | Đổi từ/lọc, sửa note | Tả lại, Từ khóa, xem tất cả | Ghim/bỏ, tắt/bật, tìm từ khóa |
| Recovery | Không kết quả → duyệt toàn sổ | AI lỗi/sai → keyword, không mất nháp | Lỗi/nhiễu → tắt panel, tự tìm; note nguyên vẹn |
| Shared recovery | Lưu lỗi giữ nháp/nguồn; sửa có hoàn tác; nguồn lỗi báo và thử lại | Như A | Như A |
| Data | localStorage riêng theo option, không gửi mạng | Mô tả dùng trong phiên, không huấn luyện | Context slide mẫu, không đọc dữ liệu ngoài |

Nguồn nháp khóa tại lần nhập đầu; chuyển slide không âm thầm đổi nguồn. Đổi nguồn nháp là thao tác rõ ràng. Sửa note giữ nguồn. Thiếu nguồn chỉ gắn sau user mở slide để đối chiếu và xác nhận; không tự đoán. Nháp chưa lưu không tồn tại sau reload; UI và hướng dẫn nêu giới hạn này.

## Fixture manifest

| ID | Nội dung note | Nguồn mẫu |
|---|---|---|
| n1 | Build trap: làm rất tốt một thứ không ai cần. | f1 — Nền tảng, slide 1 |
| n2 | Đo outcome thay vì chỉ đếm tính năng. | f1 |
| n3 | Prototype để thử giả thuyết, không chỉ demo. | e1 — Thiết kế thử nghiệm, slide 1 |
| n4 | Ba cách khác nhau ở ai bắt đầu hỗ trợ. | e2 — Thiết kế thử nghiệm, slide 2 |
| n5 | Cần quan sát hành vi, không chỉ nghe lời khen. | Không nguồn — phục vụ nhánh recovery |

Phân công phát triển: Option A — Nguyễn Văn An; Option B — Lưu Xuân Dũng; Option C — Nguyễn Long Khánh. Bản thiết kế chuẩn hóa bối cảnh học slide trên VLearn, sử dụng bộ dữ liệu 5 slide và 5 note mẫu độc lập để so sánh công bằng giữa ba phương án.
