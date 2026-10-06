# Chặng 5 — Test Plan

## Chuẩn bị

Ba người ngoài nhóm, ưu tiên learner có tự ghi và mở lại note. Phân công: An–T01 (ABC); Dũng–T02 (BCA); Khánh–T03 (CAB). Mỗi người thử đủ cả ba, không chỉ option owner dựng. Xác nhận consent ghi chép; dùng mã T01–03 để bảo mật danh tính người tham gia.

Chạy server theo `prototype-link.md`. Trước mỗi option, khôi phục dữ liệu mẫu và reload để về e2, query rỗng, gợi ý thu gọn và bật. Kiểm tra nhãn option và 5 note. Không cho xem đáp án trước task. Cùng máy, viewport, task, 4 phút/option. Counterbalance giảm nhưng không loại bỏ learning effect: tester có thể nhớ nguồn sau option đầu; ghi giới hạn này, không suy tốc độ là thắng thua khách quan.

## Script 20 phút

0–2 phút: giải thích đang thử giao diện, không kiểm năng lực; người dùng tự thao tác/nói suy nghĩ, có thể dừng. Một context question: “Lần gần đây bạn mở lại ghi chú của một bài học, bạn muốn làm gì và đã tìm lại thế nào?” Không mớm rằng họ phải gặp khó khăn.

2–14 phút: 4 phút/option, đọc **cùng một task**: “Bạn đang học slide ‘Ai bắt đầu hỗ trợ?’. Bạn nhớ đã ghi một ý về việc thử ý tưởng thay vì chỉ trình diễn. Hãy tìm ghi chú đó, xem lại nội dung gốc để đối chiếu, rồi tiếp tục ở slide đang học.” Không nói tên nút, query chuẩn hoặc note ID.

14–18 phút: hỏi “Trong tình huống này bạn chọn cách nào, vì sao?”, “Bạn muốn tự làm bước nào, sẵn lòng giao hệ thống bước nào?”, “Bạn chấp nhận mất gì để có điều đó?”, “Có lúc nào bạn nghi ngờ kết quả hoặc không biết quay lại không?”. Không hỏi “có thích không?” và không pitch AI.

18–20 phút: rà notes, tách Observed/Interpreted/Decided/Still Unproven. Câu người dùng nói chỉ ghi nguyên văn khi nghe rõ; không nhớ thì paraphrase có nhãn. Nhóm họp sau đủ ba phiên để chốt đúng một Next Change.

## 7 Observation Focus

| Focus | Cách ghi fact-first |
|---|---|
| First Action | Bấm/nhập đầu tiên; không suy ánh mắt nếu không quan sát được |
| Hesitation | Dừng >3 giây, vị trí và mốc tương đối; không tự gọi là lo lắng |
| Evidence Read / Ignored | Có mở nguồn/đọc nhãn không; mở nguồn không tự chứng minh đã hiểu |
| Misunderstanding | User dự đoán thao tác A nhưng hệ thống B, ghi lời/thao tác cụ thể |
| Help Needed | Số lần hỏi, câu hỏi và phản hồi facilitator |
| Correction / Recovery | Đổi query, fallback, bỏ/tắt, quay lại; có mất nháp/note không |
| Selected Option & Trade-offs | Chọn sau đủ ba và lý do chấp nhận đánh đổi, không chỉ preference |

Ghi thời điểm bắt đầu/kết thúc, hoàn thành/không hoàn thành, note/nguồn đã chọn, số trợ giúp. “Không quan sát được” khác “không xảy ra”. Không ghi thời gian task hoặc help count trước phiên.

## Facilitation và rescue

User giữ chuột/bàn phím. Im lặng khi họ nghĩ. Khi hỏi cách dùng, hỏi ngược “Theo bạn nó nên hoạt động thế nào?”. Nếu bế tắc, hỏi “Bạn định làm gì tiếp theo?” và ghi lần cứu hộ. Hết 4 phút dừng option, ghi incomplete, không bấm hộ để tạo success. Không chỉ dẫn trong lượt chính.

Recovery drill **sau task chính**, giống nhau cho cả ba: giả lập lỗi lưu để kiểm giữ nháp; dùng note thiếu nguồn để kiểm gắn nguồn. B/C thêm lỗi AI là probe bổ sung, không gộp vào thời gian task chính. Facilitator kích hoạt lỗi chỉ khi đã thông báo đang thử một trạng thái lỗi; không giả vờ đó là outage thật.

## Đọc kết quả

Đối chiếu hành vi và trade-off trước preference. Pattern cần trỏ ID sự kiện ở ít nhất hai phiên; giữ trường hợp đối lập. Không tính ba lựa chọn là validation thị trường. Mục tiêu chính là phát hiện interaction breakdown và kiểm chứng tính khả thi của các cơ chế tương tác.
