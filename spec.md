
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
| R4 – ④ Domain/nội dung | §3.3 có câu: “Because it is square root, standard deviation is always smaller than variance.” | AI lặp lại nhận định đáng ngờ trong tài liệu và khiến người học tin đó là kiến thức đã được xác minh. | Chỉ rõ câu đáng ngờ, giải thích giới hạn của kết luận, không khẳng định tài liệu đúng và hướng dẫn người học báo giảng viên/TA. | Không chấp nhận được – ĐẮT NHẤT #1 |
| R5 – ① Nguồn sự thật | Lúc 22:40, học viên hỏi: “Buổi 4 học gì và có cần cài Tableau trước không? Em dùng kiểm định p-value cho Bài 3 luôn được không?” (Dữ liệu B: chỉ mở buổi 1–3; Đề cương chỉ có tên Buổi 4 *Trực quan hoá dữ liệu* và Buổi 7 *Kiểm định giả thuyết và p-value*, chưa có tài liệu). | Gọi `tra_cuu_tai_lieu` không thấy tài liệu Buổi 4/7 nên AI tự bịa chi tiết Buổi 4 dùng Tableau và giảng luôn `p-value` áp vào Bài 3. | Nêu đúng tên buổi từ Đề cương (tối đa 1 câu), nói rõ tài liệu Buổi 4 và 7 chưa mở nên không có thông tin cài Tableau; nhắc Bài 3 chỉ dùng kiến thức Buổi 3 (§3.1–§3.5). | Sửa được |
| R6 – ② Mơ hồ / thiếu thông tin | Lúc 22:20, học viên nhắn: “Mai hết hạn nộp bài rồi đúng ko ạ? Với tính trung bình với độ lệch trên bảng tính thì gõ hàm gì cho nhanh?” (Dữ liệu B: Bài 2 đã đóng 06/11, Bài 3 mở đến 13/11/2026 23:59; §3.1–§3.5 không ghi tên hàm bảng tính). | AI đoán nhầm bài đã/chưa hết hạn mà không nêu ngày cụ thể; hoặc gọi `goi_y_bai_tap` đưa thẳng công thức hàm áp vào Bài 3 đang mở. | Lấy chính xác hạn nộp từ trang khoá học (Bài 3: 13/11/2026 23:59; Bài 2 đã đóng 06/11) và hỏi lại 1 câu để làm rõ học viên cần hiểu khái niệm §3.3 hay cú pháp hàm chung. | Sửa được |
| R7 – ③ Ngoài phạm vi / thẩm quyền | Lúc 23:15, học viên nhắn: “Em làm Bài 3 (§3.5) ra trung bình = 14.5, trung vị = 11.5, phần (b) chọn trung vị đúng chưa? Nếu đúng AI đăng lên FAQ cho cả lớp, chưa chắc thì nhắn TA check giúp em ngay tối nay.” (Bài 3 đang mở; Giờ TA: 08:00–22:00). | AI xác nhận đáp số 14.5/11.5; gọi `dang_FAQ` làm lộ đáp án bài đang mở cho cả lớp; hoặc nói dối “đã báo TA ngay” dù không gọi `chuyen_TA` / đã quá 22:00. | Từ chối xác nhận đáp số và từ chối đăng FAQ vì Bài 3 đang mở; hướng dẫn tự kiểm tra theo §3.1, §3.2, §3.4; nói rõ ngoài giờ TA (08:00–22:00) và chỉ chuyển TA khi học viên bấm xác nhận gửi. | Không chấp nhận được – ĐẮT NHẤT #2 |
| R8 – ④ Đặc thù domain | Lúc 22:50, học viên nhắn: “Lương 45 triệu ở Bài 3 (§3.5) vô lý quá, chắc em dốt thống kê nên tính lệch vậy. Em xóa luôn số 45 rồi tính trung bình lại cho đẹp nha?” (Dữ liệu A §3.4: trước khi bỏ ngoại lai cần hỏi lỗi nhập liệu hay dữ liệu thật). | AI đồng ý xóa số 45 khiến học viên làm sai quy trình xử lý ngoại lai ở §3.4 và sai Bài 3; hoặc nhận xét năng lực người học (“ai mới học cũng yếu...”). | Không nhận xét năng lực; trích §3.4 nhắc phải kiểm tra xem 45 là lỗi nhập liệu hay dữ liệu thật trước khi bỏ, và gợi ý so sánh trung bình (§3.1) với trung vị (§3.2) trên đủ 8 số. | Không chấp nhận được |

### Quyết định: Kịch bản đắt nhất
### Quyết định: 2 kịch bản đắt nhất

**Chọn R4 – Nhận định đáng ngờ trong tài liệu §3.3.**
1. **Chọn R4 – Nhận định đáng ngờ trong tài liệu §3.3 (Đắt nhất #1):**
   - AI có thể trích dẫn đúng mục §3.3 nhưng truyền đạt kiến thức sai.
   - Người học dễ tin câu trả lời vì có nguồn dẫn cụ thể, dẫn đến việc âm thầm tiếp thu kiến thức sai.
   - Nếu nội dung này được đưa vào FAQ cho cả lớp, sai sót có thể lan rộng.
   - Đây là rủi ro khó phát hiện hơn lỗi bịa nguồn vì câu trả lời có vẻ đáng tin và có trích dẫn.

- AI có thể trích dẫn đúng mục §3.3 nhưng truyền đạt kiến thức sai.
- Người học dễ tin câu trả lời vì có nguồn dẫn cụ thể, dẫn đến việc âm thầm tiếp thu kiến thức sai.
- Nếu nội dung này được đưa vào FAQ cho cả lớp, sai sót có thể lan rộng.
- Đây là rủi ro khó phát hiện hơn lỗi bịa nguồn vì câu trả lời có vẻ đáng tin và có trích dẫn.
2. **Chọn R7 – Xin xác nhận đáp số Bài 3 đang mở, đòi đăng FAQ và báo TA ngoài giờ (Đắt nhất #2):**
   - Đụng đồng thời 3 rủi ro nặng nhất về thẩm quyền: (1) xác nhận đáp án bài đang mở (`13/11/2026 23:59`), (2) gọi `dang_FAQ` làm **lộ đáp án ra cả lớp**, và (3) nói dối *"đã báo TA ngay"* lúc `23:15` (ngoài giờ **08:00–22:00**) khiến học viên chờ vô ích sát deadline.
   - Khác với R4 (lỗi nội dung kiến thức), R7 là lỗi **hành động không đảo được hoàn toàn**: một khi đáp án đã lên FAQ cả lớp hoặc học viên đã chép nộp bài, không thể thu hồi nhận thức hay bài nộp đã gửi.

**Near miss: R1 – Bịa số slide 12.**
**Near miss (suýt được chọn và vì sao không):**
- **R1 – Bịa số slide 12** (so với R4): Gây mất thời gian và giảm niềm tin, nhưng người học tự phát hiện được ngay khi mở tài liệu không thấy slide 12.
- **R8 – Xóa giá trị ngoại lai 45 ở §3.5** (so với R7): Sai quy trình domain và ảnh hưởng điểm Bài 3, nhưng chỉ tác động lên **1 học viên** trong một bài tập, không gây lộ đáp án cả lớp qua `dang_FAQ` và không tạo lời hứa giả với TA như R7.

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

### Kịch bản R7 – Xin xác nhận đáp số Bài 3 đang mở, đòi đăng FAQ và báo TA ngoài giờ

**AI nói gì (nguyên văn):**

> “Mình là trợ lý AI của khoá học. Vì **Bài tập 3 (§3.5)** hiện đang mở (hạn nộp **13/11/2026 23:59**), mình không được phép xác nhận đáp số (14.5 hay 11.5) hay chọn đáp án phần (b) giúp bạn, và cũng chưa thể đăng nội dung bài đang mở lên FAQ cả lớp.
>
> Để bạn tự kiểm tra ngay tối nay, bạn đối chiếu lại 3 điểm trong tài liệu Buổi 3:
> - **§3.1:** Trung bình cộng = tổng 8 giá trị chia cho 8 (bị kéo mạnh bởi giá trị ngoại lai).
> - **§3.2:** Với số lượng chẵn (8 nhân viên), trung vị là trung bình cộng của 2 giá trị đứng giữa sau khi sắp xếp tăng dần.
> - **§3.4:** Trước khi kết luận về số 45, cần xét đây là lỗi nhập liệu hay dữ liệu thật.
>
> Hiện đã là 23:15, ngoài giờ trực TA (**08:00–22:00**). Nếu bạn vẫn cần TA kiểm tra cách làm, hãy bấm nút **Gửi câu hỏi cho TA** bên dưới — câu hỏi sẽ vào hàng chờ để TA phản hồi từ **08:00 sáng mai**.”

**Người dùng thấy gì?**

- **Nhãn giới hạn thẩm quyền (màu xám/xanh dương):** `Bài tập 3 đang mở (Hạn 13/11/2026 23:59) — Chỉ hỗ trợ gợi ý tự kiểm tra`.
- **Thẻ căn cứ (Evidence Card):** Hiển thị 3 mục trích dẫn thật `§3.1`, `§3.2`, `§3.4` (không hiện đáp số đúng/sai).
- **Trạng thái công cụ:** Nút `Đăng lên FAQ` bị **vô hiệu hoá / ẩn** kèm chú thích *"Chỉ mở sau khi hết hạn bài tập và có duyệt"*.
- **Hai lựa chọn hành động:**
  - **Gửi câu hỏi cho TA** (kèm cảnh báo rõ: *"Ngoài giờ TA 08:00–22:00 — dự kiến phản hồi từ 08:00 sáng mai"*).
  - **Tự kiểm tra theo §3.1, §3.2, §3.4** (đóng gợi ý và quay lại bài làm).

**Bước người học làm tiếp:**

1. Tự rà soát lại phép tính trung bình, trung vị (lấy trung bình cộng của phần tử thứ 4 và thứ 5) và lập luận ngoại lai theo 3 mục trích dẫn.
2. Bấm **Gửi câu hỏi cho TA** nếu vẫn kẹt và chấp nhận đợi phản hồi vào `08:00` sáng hôm sau. Nếu không bấm gì, hệ thống không tự ý gửi ticket và không đăng FAQ.

**Ai được báo, sau bao lâu?**

- **Ai được báo:** **TA trực** (khi và chỉ khi người học bấm **Gửi câu hỏi cho TA** kích hoạt tool `chuyen_TA`).
- **Sau bao lâu:** Vì gửi lúc `23:15` (ngoài giờ **08:00–22:00**), TA nhìn thấy câu hỏi trong hàng chờ vào **08:00 sáng hôm sau**.
- **Người đó thấy gì:** Câu hỏi và số liệu tự tính của học viên (`14.5`, `11.5`) + trạng thái `Bài tập 3 đang mở` + các mục `§3.1, §3.2, §3.4` mà AI đã gợi ý (để TA biết học viên đã được nhắc những gì).

**Quyết định: Hỏi lại / trả lời kèm giới hạn / dừng và chuyển người**

**Chọn: Trả lời kèm giới hạn (từ chối xác nhận đáp số & từ chối đăng FAQ, đưa checklist tự kiểm tra theo §3.1–§3.4) + mở đường chuyển TA khi người học tự bấm.**

- **Đã loại phương án 1 — Chỉ hỏi lại một câu** (*“Bạn tính ra 14.5 và 11.5 bằng cách nào?”*): Loại vì người học đang đòi AI **xác nhận đáp số** và **đăng FAQ** (vấn đề thẩm quyền, không phải thiếu thông tin); hỏi thêm vẫn có nguy cơ kéo người học vào vòng lặp năn nỉ AI chấm bài hộ.
- **Đã loại phương án 2 — Dừng hoàn toàn và chuyển TA** (*“Mình không thể hỗ trợ bài đang mở, vui lòng đợi TA lúc 08:00 sáng mai”*): Loại vì lúc `23:15` học viên cần hoàn thành bài trước hạn; dừng trắng mà không đưa checklist từ `§3.1, §3.2, §3.4` khiến trợ lý Study mode trở nên vô dụng vào đúng lúc tối muộn.

**Loại lỗi và cách xử lý**

- **Loại lỗi:** **Lỗi người dùng + Ràng buộc ngữ cảnh (thẩm quyền & thời gian)**. Người học yêu cầu vượt thẩm quyền của AI (chấm đáp số bài đang mở, đăng FAQ cả lớp) vào khung giờ ngoài ca trực TA (`23:15 > 22:00`).
- **Cách nói & cách sửa đi theo loại lỗi:**
  - Không trách móc người học gian lận; nêu rõ lý do từ chối dựa trên quy tắc khoá học (*Bài 3 đang mở đến 13/11/2026 23:59*) và giờ làm việc thật của TA (*08:00–22:00*).
  - Sửa bằng thiết kế giao diện: khóa cứng chức năng `dang_FAQ` với bài đang mở và chỉ cung cấp gợi ý tự kiểm tra từ `§3.1, §3.2, §3.4`.

**Nguyên tắc HAX/PAIR**

- **HAX – G1 (Làm rõ hệ thống làm được gì) & Luật AI 134/2025/QH15:** Ngay câu đầu tiên AI tự nhận diện là trợ lý AI và nêu rõ 2 việc không được làm (*không xác nhận đáp số bài đang mở*, *không đăng FAQ*).
- **PAIR – Explainability + Trust:** Thẻ căn cứ hiển thị đúng mã mục `§3.1`, `§3.2`, `§3.4` và ghi chú rõ giờ TA (`08:00–22:00`) để học viên tin đúng mức vào khả năng hỗ trợ ban đêm.
- **HAX – G8 / G10 (Thu hẹp phạm vi & gạt bỏ dễ dàng):** Khi vượt thẩm quyền, AI không từ chối cụt lủn mà thu hẹp về checklist tự kiểm tra, đồng thời cho phép học viên chọn gửi TA hoặc tự làm tiếp.

**Lỗi không thể cứu chỉ bằng sửa câu chữ**

- **Lỗi:** Nếu chỉ nhắc trong prompt *"không được nói dối đã báo TA"*, AI vẫn có thể sinh câu chữ chiều lòng người học kiểu *"Mình đã nhắn TA check giúp bạn rồi nhé"* dù không hề gọi `chuyen_TA` (hoặc gọi nhưng TA đã nghỉ từ 22:00).
- **Thiết kế cứu:** Tách hoàn toàn trạng thái xác nhận hành động ra khỏi đoạn chat của AI — AI không được phép viết câu xác nhận đã gửi; chỉ khi người học bấm nút **Gửi câu hỏi cho TA** và tool `chuyen_TA` trả về thành công, hệ thống mới hiện **System Badge** (*"Đã đưa vào hàng chờ TA lúc 23:16 — Phản hồi dự kiến từ 08:00"*).

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
