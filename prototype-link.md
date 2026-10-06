# Chặng 4 — Prototype Link và hướng dẫn demo

**Danh mục liên kết và hướng dẫn vận hành prototype**  
*Môi trường:* Local HTTP Server · *Trình duyệt khuyến nghị:* Google Chrome

| Option | File | Link khi server chạy |
|---|---|---|
| **A — Tự tìm từ khóa** | [option-a.html](option-a.html) | http://127.0.0.1:8765/option-a.html |
| **B — Tìm theo ý nhớ** | [option-b.html](option-b.html) | http://127.0.0.1:8765/option-b.html |
| **C — Gợi theo slide** | [option-c.html](option-c.html) | http://127.0.0.1:8765/option-c.html |
| **Trang chọn tổng hợp** | [index.html](index.html) | http://127.0.0.1:8765/index.html |

Ba file HTML được xây dựng hoàn toàn độc lập, không phụ thuộc thư viện mạng bên ngoài (Zero-dependency), đảm bảo khả năng chạy mượt mà và bảo mật dữ liệu cục bộ.

---

## Hướng dẫn khởi chạy máy chủ cục bộ

Chạy lệnh PowerShell tại thư mục dự án để khởi động local web server phục vụ các phiên kiểm thử:

```powershell
Set-Location 'D:\NguyenVanAn\2026_Vin_AI_ThucChien\TongHop_LAB\Track1_Day19_2A202602776_NguyenVanAn'
python -m http.server 8765 --bind 127.0.0.1
```

Mở trình duyệt truy cập `http://127.0.0.1:8765/`. Dừng server bằng tổ hợp phím `Ctrl + C`.

---

## Luồng tương tác End-to-End và Kịch bản kiểm thử

1. **Viết và lưu ghi chú:** Viết note tại slide e2, chuyển sang slide khác trước khi lưu: nguồn gốc ghi chú vẫn được neo chắc chắn tại e2. Dữ liệu lưu vào một sổ chung thống nhất.
2. **Cơ chế tìm lại:**
   - **Option A:** Người học gõ từ khóa chính xác vào ô tìm kiếm.
   - **Option B:** Người học nhập câu mô tả ý nhớ tự nhiên; hệ thống xếp các note phù hợp lên đầu.
   - **Option C:** Hệ thống tự động hiển thị số lượng note liên quan khi mở slide; người học duyệt mở hoặc ẩn.
3. **Mở nguồn và Quay lại:** Bấm vào thẻ note để nhảy tới slide nguồn gốc đối chiếu nội dung, sau đó sử dụng nút `Quay lại slide đang học` để trở về mạch bài giảng hiện tại.
4. **Sửa và hoàn tác:** Chỉnh sửa ghi chú giữ nguyên nguồn gốc; hỗ trợ hoàn tác 1 lần sửa nếu cần.
5. **Cơ chế phục hồi (Recovery):** Khung điều khiển cho phép kiểm tra xử lý khi gặp lỗi lưu dữ liệu hoặc lỗi kết nối. Nhấn nút *"Khôi phục dữ liệu mẫu"* để reset trạng thái sạch sẽ trước mỗi lượt test.
