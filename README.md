# Track1_Day19_2A202602776_NguyenVanAn

## 1. Thông tin cá nhân và đội ngũ

| Thông tin | Nội dung |
|---|---|
| Họ tên | Nguyễn Văn An |
| Mã học viên | 2A202602776 |
| Nhóm | 3aecaykhe |
| Thành viên | Nguyễn Văn An, Lưu Xuân Dũng, Nguyễn Long Khánh |
| Case | B — AI Notes: Personal Learning Notes |
| Bài lab | Track 1 — Day19: Design the Experiment |

Bài làm tiếp nối trực tiếp từ giai đoạn Day17, tập trung giải quyết bài toán tìm lại ghi chú khi học trên nền tảng VLearn. Hướng tiếp cận thống nhất của nhóm là **một sổ ghi chú tập trung cạnh slide, mỗi note có liên kết về slide nguồn gốc và đường dẫn quay lại slide đang học**.

Giai đoạn 1 tham chiếu: [Repo Day17](https://github.com/NguyenVanAn-200704/Track1_Day17_2A202602776_NguyenVanAn) · [Bản ghi chép phỏng vấn Day17](https://github.com/NguyenVanAn-200704/Track1_Day17_2A202602776_NguyenVanAn/blob/main/interview/notes.md).

---

## 2. Hypothesis Problem (Giả thuyết bài toán)

**Khi cần xem lại một ý đã ghi để tiếp tục hiểu bài trên VLearn, người học tự ghi chú gặp khó khăn trong việc tiếp cận đúng note và quay về slide gốc, vì note nằm rải rác theo từng slide hoặc lưu ở công cụ khác, dẫn đến phải dò lại vị trí và chuyển đổi qua nhiều thao tác.**

| Thành tố | Nội dung |
|---|---|
| **Target User** | Học viên VLearn có thói quen tự ghi chép bài học |
| **Situation** | Đang học một slide mới và cần xem lại một ý tưởng đã ghi chú ở bài trước |
| **Job** | Tìm đúng ghi chú, mở slide gốc để kiểm tra bối cảnh rồi quay lại học tiếp |
| **Barrier** | Ghi chú bị phân tán theo từng slide, thiếu lối truy cập tập trung và đường dẫn nguồn |
| **Consequence** | Tốn công sức tìm kiếm, làm đứt mạch tư duy và phải chuyển đổi qua lại giữa nhiều công cụ |

### Bằng chứng thực tế kế thừa từ Day17

- **03:53 — An-P01:** Chia sẻ đã phải từ bỏ tính năng note mặc định theo slide của VLearn để chuyển sang chia đôi màn hình vừa xem slide vừa ghi trên Notion vì ghi chú bị phân tán rải rác: *"những cái note đó thì phân bố khá là rải rác chứ nó không có tập trung vào một file"*.
- **02:09 — Phản chứng (Counter-evidence):** P01 cho biết khi đã đưa ghi chú vào hệ thống riêng (Notion) thì việc tìm lại nhìn chung không mất thời gian nhờ search từ khóa và đặt tên theo ngày. Điều này chứng minh pain point nằm ở khâu tổ chức truy cập của VLearn chứ không phải do người học không biết tìm kiếm.
- **05:13 — Hướng giải pháp đề xuất:** Đề xuất gom toàn bộ ghi chú vào một sổ chung và có liên kết quay về slide gốc để mở nhanh.

Chi tiết tổng hợp bằng chứng nằm trong [Evidence Snapshot](evidence-snapshot.md).

---

## 3. Ba phương án giải pháp (Three Solution Options)

| Option | Cơ chế giải quyết | Vai trò người học | Prototype |
|---|---|---|---|
| **A — Tự tìm từ khóa** | Gom note vào một sổ chung; người học tìm bằng từ khóa hoặc lướt danh sách | Chủ động tìm kiếm, tự chọn note và mở nguồn | [Option A](option-a.html) |
| **B — Tìm theo ý nhớ** | Người học mô tả ý nhớ; hệ thống xếp các note nguyên bản phù hợp lên đầu | Nhập câu mô tả ý, đối chiếu ứng viên và chọn note | [Option B](option-b.html) |
| **C — Gợi theo slide** | Hệ thống chủ động hiển thị note cũ liên quan tới slide đang mở | Duyệt danh sách gợi ý, ghim, ẩn hoặc tắt gợi ý | [Option C](option-c.html) |

Option A đóng vai trò là Baseline (không AI). Option B và C ứng dụng cơ chế truy hồi ngữ nghĩa và gợi ý theo ngữ cảnh, tuyệt đối không tự ý sinh nội dung mới, không viết lại ghi chú của người học và không tự động chuyển slide khi chưa có sự đồng ý.

### Comparison Contract (Nguyên tắc so sánh công bằng)

Cả ba phương án được đóng băng chung 70% các thành phần:
- Cùng một đối tượng người dùng (học viên VLearn).
- Cùng một tình huống và vị trí xuất phát: Bắt đầu tại slide e2 (*Thiết kế thử nghiệm — Ai bắt đầu hỗ trợ?*).
- Cùng một bộ dữ liệu fixture: 5 slide và 5 note mẫu giống nhau hoàn toàn.
- Cùng một outcome task duy nhất: **Tìm ghi chú về việc "thử ý tưởng thay vì chỉ trình diễn", mở slide gốc (e1) để đối chiếu, rồi quay trở lại slide đang học (e2)** trong tối đa 4 phút mỗi option.

Bốn trụ cột Human–AI (Expectation, Agency, Evidence & Uncertainty, Control & Recovery) được chi tiết hóa trong [Three-option Design Sheet](three-option-design-sheet.md).

### Hướng dẫn mở và trải nghiệm Prototype

[Trang điều hướng tổng hợp](index.html) · [Chi tiết liên kết và hướng dẫn vận hành](prototype-link.md)

Khởi chạy local server qua PowerShell:
```powershell
Set-Location 'D:\NguyenVanAn\2026_Vin_AI_ThucChien\TongHop_LAB\Track1_Day19_2A202602776_NguyenVanAn'
python -m http.server 8765 --bind 127.0.0.1
```
Mở trình duyệt tại địa chỉ `http://127.0.0.1:8765/`. Nhấn `Ctrl + C` trên terminal để dừng server.

---

## 4. Phạm vi đóng góp cá nhân và phối hợp nhóm

Trong bài làm này, tôi (Nguyễn Văn An) sử dụng bản ghi phỏng vấn Day17 của mình làm đầu vào cốt lõi để kế thừa bằng chứng thực tế cho Case B. 

Phân công trách nhiệm và phối hợp trong nhóm 3aecaykhe:
- **Nguyễn Văn An:** Phụ trách phát triển **Option A** (Sổ chung tìm từ khóa, luồng mở nguồn và quay lại slide học); chuẩn hóa bộ dữ liệu fixture 5 slide / 5 note; trực tiếp điều phối phiên kiểm thử thực tế **T01** theo thứ tự A → B → C.
- **Lưu Xuân Dũng:** Phụ trách phát triển **Option B** (Cơ chế tìm theo ý nhớ, nhãn ứng viên và fallback từ khóa); trực tiếp điều phối phiên kiểm thử thực tế **T02** theo thứ tự B → C → A.
- **Nguyễn Long Khánh:** Phụ trách phát triển **Option C** (Gợi ý theo slide, ghim/ẩn/tắt panel và quyền kiểm soát giao diện); trực tiếp điều phối phiên kiểm thử thực tế **T03** theo thứ tự C → A → B.

Sau khi hoàn tất ba phiên kiểm thử độc lập, cả ba thành viên đã cùng họp thảo luận, đối chiếu chéo các quan sát, rút ra các pattern hành vi chung và thống nhất quyết định đúng một thay đổi cải tiến (Group Next Change).

---

## 5. Kiểm thử người dùng và Hướng cải tiến

### Kịch bản và Tổ chức kiểm thử

Kiểm thử được tiến hành với 3 người dùng độc lập ngoài nhóm theo kịch bản 20 phút mỗi người, tuân thủ nguyên tắc Counterbalance (luân phiên thứ tự ABC / BCA / CAB) để giảm thiểu tối đa sai số học tập (learning effect). Mỗi option giới hạn trong 4 phút. Quá trình quan sát tập trung vào 7 tiêu điểm fact-first: *Hành động đầu tiên, Do dự >3s, Kiểm chứng nguồn, Hiểu sai, Yêu cầu trợ giúp, Khôi phục/sửa lỗi, Lựa chọn & Đánh đổi*.

Hệ thống tài liệu kiểm thử:
- [Kế hoạch kiểm thử chi tiết](test-plan.md)
- [Biên bản kiểm thử T01 — Nguyễn Văn An](prototype-feedback-note.md)
- [Biên bản kiểm thử T02 — Lưu Xuân Dũng](feedback-templates/feedback-dung.md)
- [Biên bản kiểm thử T03 — Nguyễn Long Khánh](feedback-templates/feedback-khanh.md)
- [Bản tổng hợp dữ liệu nhóm](group-feedback-synthesis.md)
- Phân tích thiết kế trước test: [Review Option B](design-reviews/review-b.md) · [Review Option C](design-reviews/review-c.md)
- Bằng chứng kỹ thuật: [Kiểm chứng chức năng](verification.md)

### Kết quả kiểm thử thực địa

1. **Hiệu suất hoàn thành nhiệm vụ:** 100% tester hoàn thành outcome task ở cả 3 option. Thời gian trung bình: Option B nhanh và ổn định nhất (80s), tiếp theo là Option A (121s) và Option C (105s).
2. **Hành vi kiểm chứng nguồn (Evidence Checking):** 100% tester đều click vào thẻ note để mở slide nguồn e1 đối chiếu nội dung trước khi bấm quay lại slide học e2.
3. **Phát hiện điểm nghẽn tương tác lớn nhất (Critical Navigation Breakdown):**
   - Khi đang ở slide nguồn e1, người dùng gặp khó khăn trong việc nhận diện đường quay lại slide đang học. T01 do dự 4 giây và suýt bấm phím `Back` của trình duyệt Chrome (T01-E02). T02 bấm nhầm nút chuyển tiếp slide trên thanh pager của bài học vì tưởng nút quay lại là nút phân trang (T02-E02).
   - Nút quay lại dạng banner văn bản hiện tại bị chìm vào bố cục bài giảng, thiếu chỉ báo rõ ràng về slide đích.
4. **Hiểu nhầm về quyền kiểm soát ở Option C:** T01 lo ngại rằng việc bấm "Bỏ gợi ý" sẽ xóa vĩnh viễn ghi chú khỏi sổ lưu trữ (T01-E04).
5. **Lựa chọn của người dùng (Selected Option):** 2/3 tester (T02, T03) chọn Option B vì sự tiện lợi của việc tìm bằng ý tự nhiên; 1/3 tester (T01) chọn Option A vì cảm giác an tâm kiểm soát. Không tester nào chọn Option C làm mặc định vì lo ngại ô nhiễm thị giác và làm đứt mạch tư duy khi học sâu.

### Quyết định cải tiến — Đúng một Group Next Change

Dựa trên các sự kiện quan sát thực tế từ cả ba phiên, nhóm thống nhất chốt đúng một thay đổi duy nhất:

> **Ở thanh thông báo quay lại slide nguồn (Return banner / Source viewer), đổi nút quay lại dạng văn bản hiện tại thành thanh ghim nổi bật cố định (Sticky Return Bar) có màu nhấn tương phản, ghi rõ đích đến cụ thể: `← Quay lại slide đang học (Slide 2: Ai bắt đầu hỗ trợ?)` kèm phím tắt `Esc` và breadcrumb vị trí, đồng thời đổi nhãn "Bỏ gợi ý" ở Option C thành "Ẩn gợi ý này (giữ nguyên trong sổ)"; vì tester T01 do dự 4 giây và suýt bấm Back trình duyệt (T01-E02), tester T02 bấm nhầm nút phân trang slide và lo mất dấu bài học (T02-E02), và tester T01 lo sợ việc bỏ gợi ý sẽ xóa mất ghi chú gốc (T01-E04). Kiểm tra vòng sau bằng kịch bản mở slide nguồn ở khoảng cách xa (từ slide 15 quay lại slide 42), quan sát xem 100% người dùng có click ngay nút quay lại trong vòng dưới 2 giây mà không cần dò tìm hay bấm nhầm phím back trình duyệt.**

### Still Unproven (Những điều chưa thể kết luận)

- Thử nghiệm 20 phút trên 5 slide mẫu chưa thể kết luận về độ chính xác của cơ chế tìm theo ý khi sổ ghi chú có hàng trăm note.
- Chưa đo lường được tác động dài hạn của liên kết slide nguồn tới khả năng ghi nhớ kiến thức (learning retention) và kết quả học tập thực tế của học viên.

---

## 6. Tổng kết và Bài học kinh nghiệm (Reflection & Tool Log)

Qua quá trình xây dựng ba prototype và trực tiếp tiến hành kiểm thử thực địa, tôi rút ra ba bài học kinh nghiệm sâu sắc:
1. **Giả định lý thuyết khác xa hành vi thực tế:** Trước khi test, tôi cho rằng luồng quay lại slide học là thao tác hiển nhiên vì đã có nút quay lại. Tuy nhiên, khi quan sát T01 suýt bấm Back trình duyệt và T02 bấm nhầm nút pager của slide, tôi nhận ra người dùng trong trạng thái đọc hiểu rất dễ bị mất phương hướng (disorientation) khi chuyển đổi không gian. Thiết kế điều hướng phải luôn có tính neo giữ ngữ cảnh mạnh mẽ.
2. **Sự đánh đổi giữa On-demand và Proactive:** Tính năng gợi ý chủ động (Option C) có thể tạo ấn tượng ban đầu về tốc độ cơ học, nhưng trong môi trường học tập đòi hỏi tập trung cao độ, sự can thiệp tự động không mong muốn sẽ phản tác dụng. Trao quyền chủ động (Agency) cho người dùng gọi hệ thống khi cần (On-demand) mang lại sự thoải mái và bền vững hơn nhiều.
3. **Giá trị của việc kiểm chứng fact-first:** Việc quan sát hành động cụ thể, đo đếm giây do dự và ghi lại đúng lời thoại nguyên văn giúp nhóm tìm ra đúng điểm nghẽn tương tác cốt lõi thay vì tranh cãi dựa trên cảm tính hay sở thích cá nhân.

Chi tiết nhật ký minh bạch về việc sử dụng các công cụ trợ lý lập trình nằm trong [ai-support-log.md](ai-support-log.md).
