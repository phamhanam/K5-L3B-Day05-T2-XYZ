
# Bài nộp LAB5 — T2 Giáo dục · Nhóm [Tên nhóm]

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| [Thành viên 1] | [Mã học viên] | [Chưa điền] |
| [Thành viên 2] | [Mã học viên] | [Chưa điền] |
| [Thành viên 3] | [Mã học viên] | [Chưa điền] |

---

## §1. Lát cắt & phạm vi

- Lát cắt: Trong một trợ lý học tập tích hợp trên trang môn học (theo phong cách ChatGPT Study mode), người học đặt câu hỏi vào buổi tối. AI phải quyết định nên hướng dẫn kèm trích dẫn, hỏi lại để làm rõ, đưa gợi ý từng bước hay thông báo không có tài liệu và đề nghị hỏi giảng viên.
- Mục tiêu: Giúp người học hiểu bài hiện tại, không chép đáp án và không vô tình tiếp thu kiến thức sai.
- 3 việc tính năng KHÔNG làm:
  - Không giải toàn bộ bài tập đang mở vì có thể khiến người học chép đáp án thay vì tự làm.
  - Không tự đăng câu trả lời thành FAQ cho cả lớp vì nội dung chưa được người có thẩm quyền xác minh có thể lan truyền.
  - Không tự sửa hoặc khẳng định tài liệu môn học là đúng khi phát hiện nội dung đáng ngờ vì AI không có thẩm quyền thay giảng viên.

## §2. Kịch bản rủi ro (chặng 2)

*Bản hiện tại có 4 kịch bản đại diện cho 4 lớp rủi ro. Cần bổ sung lên ít nhất 8 kịch bản nếu áp dụng đầy đủ yêu cầu trong rubric.*

| ID / Lớp | Tin người dùng / Bằng chứng từ track | AI có thể sai thế nào? | Sản phẩm tốt nên làm gì? | Nhãn |
|---|---|---|---|---|
| R1 – ① System/tool | Người học hỏi về “slide 12”. Tài liệu bài 3 chỉ có các mục §3.1–§3.5, không có số slide. | AI tự tạo nguồn “slide 12” và trích dẫn như thể nguồn có thật. | Thông báo không tìm thấy slide 12; chỉ dẫn người học đến mục tài liệu có thật hoặc hỏi lại nội dung cần tìm. | Sửa được |
| R2 – ② User/input | Người học hỏi: “Cái độ lệch ấy là gì ạ, em đọc không hiểu.” §3.3 có cả phương sai và độ lệch chuẩn. | AI tự đoán người học muốn hỏi về độ lệch chuẩn trong khi câu hỏi chưa rõ. | Hỏi lại người học đang muốn tìm hiểu phương sai hay độ lệch chuẩn trước khi giải thích. | Nhẹ |
| R3 – ③ Context | Người học yêu cầu giải bài tập 3. Bài tập về lương của 8 nhân viên có hạn nộp 13/11/2026 23:59 và đang mở. | AI giải toàn bộ bài hoặc xác nhận đáp án, khiến người học có thể chép bài thay vì tự làm. | Chỉ đưa gợi ý bước đầu; không đưa đáp án hoàn chỉnh hoặc xác nhận đáp án khi bài còn mở. | Không chấp nhận được |
| R4 – ④ Domain/nội dung | §3.3 có câu: “Because it is square root, standard deviation is always smaller than variance.” | AI lặp lại nhận định đáng ngờ trong tài liệu và khiến người học tin đó là kiến thức đã được xác minh. | Chỉ rõ câu đáng ngờ, giải thích giới hạn của kết luận, không khẳng định tài liệu đúng và hướng dẫn người học báo giảng viên/TA. | Không chấp nhận được – ĐẮT NHẤT |

### Quyết định: Kịch bản đắt nhất

**Chọn R4 – Nhận định đáng ngờ trong tài liệu §3.3.**

- AI có thể trích dẫn đúng mục §3.3 nhưng truyền đạt kiến thức sai.
- Người học dễ tin câu trả lời vì có nguồn dẫn cụ thể, dẫn đến việc âm thầm tiếp thu kiến thức sai.
- Nếu nội dung này được đưa vào FAQ cho cả lớp, sai sót có thể lan rộng.
- Đây là rủi ro khó phát hiện hơn lỗi bịa nguồn vì câu trả lời có vẻ đáng tin và có trích dẫn.

**Near miss: R1 – Bịa số slide 12.**

- AI bịa ra slide 12 khiến người học tìm kiếm một nguồn không tồn tại.
- Lỗi gây mất thời gian và giảm niềm tin, nhưng người học có thể phát hiện khi không tìm thấy slide đó.
- Vì vậy, mức độ ảnh hưởng lâu dài thấp hơn R4.

## §3. Khi AI sai (chặng 3)

### Kịch bản R4 – Tài liệu có nhận định đáng ngờ về độ lệch chuẩn

**AI nói gì (nguyên văn):**

> “Mình tìm thấy trong §3.3 câu: ‘Because it is square root, standard deviation is always smaller than variance.’ Tuy nhiên, đây là nhận định đáng ngờ. Không thể kết luận độ lệch chuẩn luôn nhỏ hơn phương sai chỉ vì độ lệch chuẩn là căn bậc hai của phương sai. Mình chưa thể xác nhận câu này là đúng. Bạn nên báo giảng viên hoặc TA kiểm tra lại nội dung §3.3 trước khi sử dụng kết luận này.”

**Người dùng thấy gì?**

- Câu đáng ngờ được trích nguyên văn từ §3.3.
- Cảnh báo: **“Nội dung tài liệu cần giảng viên/TA xác minh.”**
- Giải thích ngắn: không thể kết luận độ lệch chuẩn luôn nhỏ hơn phương sai chỉ dựa vào phép lấy căn bậc hai.
- Hai lựa chọn:
  - **Báo nội dung đáng ngờ:** gửi câu trích dẫn và câu hỏi đến TA.
  - **Tiếp tục học:** bỏ qua nội dung đang chờ xác minh và chuyển sang phần khác.
- Không có chức năng tự động đăng câu trả lời thành FAQ cho cả lớp.

**Bước người học làm tiếp:**

1. Xem lại câu được đánh dấu trong §3.3.
2. Chọn “Báo nội dung đáng ngờ” nếu muốn yêu cầu kiểm tra.
3. Tiếp tục học phần khác trong khi chờ xác minh.

**Ai được báo, sau bao lâu?**

- TA/giảng viên được báo khi người học chủ động chọn “Báo nội dung đáng ngờ”.
- Hệ thống sử dụng tool `chuyen_TA` để gửi câu hỏi và trích dẫn §3.3.
- Chỉ hiển thị “Đã gửi đến TA” khi tool xác nhận gửi thành công.
- Giờ hỗ trợ TA theo dữ liệu track là 08:00–22:00. Nếu gửi ngoài giờ, giao diện thông báo TA có thể phản hồi trong giờ hỗ trợ tiếp theo.
- Nếu gửi thất bại, hiển thị lỗi và cho phép người học thử lại; không tuyên bố TA đã nhận được câu hỏi.

### Quyết định: Hỏi lại / trả lời kèm giới hạn / dừng và chuyển người

**Chọn: Trả lời kèm giới hạn và cho phép chuyển người có thẩm quyền xác minh.**

- Không chỉ hỏi lại vì bằng chứng đáng ngờ đã nằm cụ thể trong §3.3; người học cần được cảnh báo ngay.
- Không tiếp tục trả lời như thể nội dung tài liệu chắc chắn đúng.
- Không tự sửa tài liệu hoặc khẳng định một phiên bản sửa đổi là chính thức vì AI không có thẩm quyền thay giảng viên.
- Giữ nguyên câu trích dẫn, chỉ rõ giới hạn xác minh và cung cấp lựa chọn báo TA.

### Loại lỗi và cách xử lý

- **Loại lỗi:** Lỗi ngữ cảnh/nội dung nguồn (domain/content). Tài liệu môn học có câu nhận định đáng ngờ; AI có nguy cơ lặp lại nội dung đó như kiến thức đúng.
- **Cách nói:** Trích đúng câu và đúng mục §3.3, dùng từ “đáng ngờ” và “cần xác minh”, không khẳng định tài liệu đã được kiểm chứng.
- **Cách sửa:** Chuyển câu hỏi đến TA/giảng viên khi người học chủ động yêu cầu; chỉ báo gửi thành công sau khi tool xác nhận.

### Nguyên tắc HAX/PAIR

- **PAIR – Giải thích được (Explainability):** Hiển thị câu trích dẫn từ §3.3 để người học biết cảnh báo dựa trên bằng chứng nào.
- **PAIR – Xây dựng niềm tin phù hợp (Trust):** Nói rõ AI chưa thể xác nhận câu này là đúng, tránh tạo cảm giác chắc chắn giả.
- **HAX – G10 (Support efficient dismissal):** Cho phép người học bỏ qua nội dung đang chờ xác minh và tiếp tục học phần khác mà không bị buộc phải chờ TA.

### Lỗi không thể cứu chỉ bằng sửa câu chữ

- Nếu tool `chuyen_TA` gửi thất bại, chỉ đổi câu chữ cảnh báo không thể làm cho TA nhận được câu hỏi.
- Thiết kế xử lý: hiển thị trạng thái gửi thất bại, cho phép thử lại và không tuyên bố TA đã nhận được thông tin.
- Nếu nội dung sai được đăng thành FAQ cho cả lớp, cần có bước duyệt của con người trước khi đăng; không thể chỉ thêm lời cảnh báo sau khi nội dung đã được phổ biến.

## §4. Mức tự chủ (chặng 4)

Với mỗi tool:

- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.

Thêm:

- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype (chặng 5)

- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)

- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo

- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
