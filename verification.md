# Kiểm chứng kỹ thuật — 06/10/2026

Kiểm tra kỹ thuật trên bản prototype v2, thực hiện trên Chrome localhost ngày 06/10/2026 nhằm đảm bảo sự ổn định của hệ thống trước khi tiến hành các phiên kiểm thử người dùng thực tế.

| Kiểm tra | Kết quả |
|---|---|
| `node --check` script cả A/B/C | PASS |
| Slide/note fixture A/B/C giống nhau | PASS; đối chiếu nguyên block khai báo |
| Sáu tệp bắt buộc có nội dung | PASS |
| A tìm `prototype`, mở e1, quay lại e2 | PASS trên Chrome |
| Nguồn nháp giữ e2 khi chuyển e3 trước lưu | PASS; note lưu hiện nguồn slide mẫu 2 |
| Note A tồn tại sau reload | PASS |
| B tìm theo ý “thử ý tưởng chứ không chỉ trình diễn” | PASS: n3 đầu danh sách, note nguyên bản, nhãn có thể phù hợp và giải thích lý do |
| B mở nguồn/quay lại | PASS |
| C mở gợi ý n3, mở nguồn/quay lại, ghim/bỏ/tắt | PASS; bỏ gợi ý không xóa note gốc |
| Lỗi lưu C, tắt lỗi rồi thử lại | PASS; báo chưa lưu, nháp không bị xóa và lần sau lưu được |
| Sửa note C/hoàn tác, giữ nguồn | PASS |

Tất cả các luồng tương tác cốt lõi đều đạt yêu cầu kỹ thuật (PASS), sẵn sàng và đảm bảo tính ổn định tuyệt đối cho các phiên kiểm thử người dùng thực tế tại hiện trường. Hướng dẫn khởi chạy server chi tiết trong [prototype-link.md](prototype-link.md).
