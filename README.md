# SI-Prompt-EV-Translate

> **Cung cấp System Instructions (SI) và Prompt chất lượng cao chuyên dụng cho nhiệm vụ dịch thuật tài liệu khoa học (định dạng PDF) từ tiếng Anh sang tiếng Việt.**

Dự án này cung cấp bộ khung hướng dẫn tối ưu giúp AI xử lý các văn bản học thuật có độ phức tạp cao, đảm bảo độ chính xác về thuật ngữ và bảo toàn định dạng tốt nhất có thể.

**Lưu ý cần phải đọc**: Dịch máy chỉ nên áp dụng khi bạn không thể thuê dịch thuật viên chất lượng cao, đặc biệt thận trọng khi áp dụng dịch máy với các tài liệu quan trọng.

---

## 📚 Xem thử chất lượng

Ví dụ về chất lượng dịch của bộ SI/prompt này (bản tiêu chuẩn), bạn có thể xem khả năng của nó khi dịch khoảng 10 trang mở đầu trong cuốn **Book Of Proofs** của **Richard Hammack**:

- Bản tiếng Anh: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/Book-Of-Proofs-2-en.pdf
- Bản dịch tiếng Việt: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/Book-Of-Proofs-2-vi.pdf

---

## 🚀 Tại sao nên sử dụng với Gemini AI Studio?

Việc kết hợp bộ SI/prompt này với **Gemini AI Studio** (https://aistudio.google.com/) mang lại nhiều lợi thế vượt trội:

* **Tối ưu hóa hệ sinh thái:** Công cụ được tinh chỉnh và kiểm tra kỹ lưỡng trên model Gemini.
* **Tiết kiệm chi phí:** Hạn mức miễn phí rộng rãi, phù hợp cho nhu cầu dịch thuật cá nhân mà hầu như không phát sinh phí. Đăng ký nhanh chóng, không gặp rào cản.
* **Tùy chỉnh chuyên sâu:** Cung cấp nhiều thiết lập nâng cao và dễ dàng tùy chỉnh qua giao diện dễ hiểu.
* **Chất lượng cao:** Gemini hiện là một trong những AI có khả năng xử lý ngữ cảnh và dịch thuật tốt nhất.
* **Đủ sức mạnh:** Bản AI Studio có sức mạnh để dịch văn bản dài, mà nếu bạn sử dụng các AI giao diện người dùng phổ thông khác thì thường không đủ (bản dịch thường bị cắt ngắn hoặc chất lượng thấp do không hiểu rõ hướng dẫn hoặc thiếu năng lực).

---

## 🛠 Hướng dẫn thiết lập & Sử dụng

Để đạt kết quả tốt nhất, hãy thực hiện theo các bước sau trong AI Studio:

### 1. Cấu hình Model
* **Model:** Chọn model tiên tiến nhất (khuyến nghị: `Gemini 3.1 Pro Preview` hoặc các bản `Preview` hoặc chính thức mới nhất).
* **System Instructions:** Copy toàn bộ nội dung SI của công cụ này (`system_instructions.md`) và dán vào khung **System instructions** (ngay dưới phần chọn model).
* **Tham số kỹ thuật:**
    * `Temperature`: Điều chỉnh xuống mức **0.3** (thay vì mặc định là 1.0). 
    * *Lưu ý:* Mức nhiệt độ thấp giúp thắt chặt tính logic, tránh dịch quá đà, đảm bảo văn phong khoa học nghiêm túc.
 
Xem hướng dẫn trong hình bên dưới để biết thao tác cụ thể:

<p align="center">
  <img src="images/luu-SI.png" alt="Nhập vào thông tin của SI">
   <br><em>Nhập vào thông tin của SI</em>
</p>

<p align="center">
--
</p>

<p align="center">
  <img src="images/chon-model-temperature.png" alt="Chọn model AI và nhập vào thông số Temperature">
   <br><em>Chọn model AI và nhập vào thông số Temperature</em>
</p>

### 2. Thao tác dịch
1. Copy **Prompt** vào khung chat.
2. Nhấn nút **+** để tải file **PDF** cần dịch lên.
3. Nhấn **Ctrl + Enter** và đợi AI xử lý.

<p align="center">
  <img src="images/nhap-prompt.png" alt="Nhập Prompt và chọn file cần dịch">
  <br><em>Nhập Prompt và chọn file cần dịch</em>
</p>

### 3. Lưu ý về Độ dài của file PDF
1. Trong mỗi lần gửi dữ liệu dịch nên giới hạn độ dài file PDF khoảng **10 trang** (có thể điều chỉnh con số với tài liệu thực tế). Lý do là vì mặc dù ngữ cảnh đầu vào cho phép đến hàng triệu Token, ngữ cảnh đầu ra (bản dịch) chịu giới hạn khoảng 64 ngàn Token.
2. Đối với tài liệu PDF rất dài (ví dụ dịch sách), cần phải chia tách nó thành các file nhỏ hơn để dịch từng file nhỏ (vì giới hạn Token đầu ra), và nên chia tách sao cho nó không bị 'lửng lơ' (ngắt giữa chừng một khối văn bản cần dịch). Có rất nhiều công cụ trực tuyến chất lượng cao giúp tách file PDF, ví dụ: https://smallpdf.com/vi/split-pdf

---

## 📝 Lưu ý kỹ thuật quan trọng khác

* **Thời gian xử lý:** Do tính chất phức tạp của tài liệu khoa học, thời gian hoàn thành có thể dao động từ **150s đến 600s** tùy độ dài file.
* **Định dạng đầu ra:** Kết quả trả về ở dạng **mã HTML**.
    * *Lời khuyên:* Bạn phải lưu nội dung này thành file `.html` (ví dụ `bandich.html`) để xem đầy đủ định dạng qua trình duyệt (ưu tiên Google Chrome).
* **Khả năng bảo toàn:** Công cụ hỗ trợ giữ định dạng rất tốt nhưng không thể hoàn hảo 100% đối với mọi loại bố cục PDF phức tạp. Ảnh dạng sơ đồ biểu đồ không quá phức tạp thường được tái tạo lại tương đối tốt, riêng các ảnh dạng ảnh chụp (như ảnh chụp bằng điện thoại, máy ảnh, từ chuyên ngành gọi là bitmap/raster) trong file PDF sẽ không được tái tạo trong bản dịch.

--

Đoạn HTML kết quả dịch sẽ luôn bắt đầu bằng: 

```
<!DOCTYPE html>
<html lang="vi">
```

và kết thúc bằng:

```
</body>
</html>
```

Khi copy kết quả phản hồi từ AI rồi lưu lại, bạn cần xóa các thông tin dư thừa (nếu nó có) nằm phía phía trên ```<!DOCTYPE html>``` và xóa thông tin dư thừa (nếu có) phía dưới ```</html>``` để kết quả bản dịch được sạch sẽ.

Mấy thông tin dư thừa trong phản hồi thường là thông tin mà AI phân tích, suy ngẫm trước khi đưa ra câu trả lời chính thức.

---

# Các tùy chọn

Người dùng ngoài việc dùng bản tiêu chuẩn, bạn có thể sử dụng thêm một trong các tùy chọn dưới đây khi dịch tài liệu PDF từ Anh sang Việt.

Các bản tùy chỉnh khi được dùng phù hợp thường cho chất lượng dịch cao hơn đáng kể so với bản tiêu chuẩn, rất khuyên bạn tìm hiểu để dùng.

Mỗi tùy chọn có ưu điểm riêng, và cách tiếp cận khác nhau để cải thiện chất lượng dịch:

- Tùy chọn 1: giảm tải SI/prompt về dạng đơn giản hơn tùy theo loại tài liệu.
- Tùy chọn 2: chia pha dịch thành các giai đoạn nhỏ hơn để tránh quá tải AI.

Một số nhận xét:

- Tùy chọn 1 sẽ phù hợp với tài liệu có cấu trúc đơn giản, chẳng hạn như tài liệu các ngành khoa học xã hội.
- Tùy chọn 2 có khả năng đem lại cải thiện chất lượng ổn định nhất, rất phù hợp với nội dung cấu trúc phức tạp, đặc biệt là tài liệu chứa nhiều công thức toán hoặc/và biểu đồ toán.
- Với mỗi Tùy chọn, bạn có lựa chọn thêm việc bổ sung danh sách từ chuyên ngành, điều này có thể rất có ích cho các tài liệu có nhiều thuật ngữ.

--

## 🔄 SI và prompt bản tinh chỉnh (refine) | Tùy chọn 1

Trong thư mục `refine` chứa các SI & prompt được tinh chỉnh cho những tài liệu không quá phức tạp.

Về lý thuyết, SI & prompt tốt là các hướng dẫn phù hợp (đúng & đủ) với tài liệu, không nên chứa các chỉ thị thừa thãi. SI & prompt tiêu chuẩn rất mạnh xử lý các tài liệu khoa học phức tạp, nhưng với các tài liệu đơn giản hơn nó sẽ dư thừa ít nhiều, bạn có thể cân nhắc sử dụng phiên bản `refine`.

Hiện trong thư mục `refine` đang có những bản tinh chỉnh sau:

- `x_svg`: chứa SI & prompt loại bỏ chỉ thị liên quan đến tạo sơ đồ, biểu đồ toán học. Nhiều tài liệu không cần đến các chỉ thị này... Chỉ thị liên quan đến tạo sơ đồ biểu đồ chiếm khoảng 25% dung lượng của bản SI tiêu chuẩn, do vậy việc loại bỏ nó khi không cần thiết có khả năng cải thiện khá cao mức độ tập trung của SI.
- `x_math`: chứa SI & prompt loại bỏ hoàn toàn chỉ thị liên quan đến tạo công thức toán & cả svg. Một số tài liệu sẽ không cần cả hai chỉ thị này. PS: Nếu tài liệu của bạn vẫn có các công thức toán học nhưng không có sơ đồ, biểu đồ toán học thì nên dùng `x_svg` thay vì `x_math`.

Một số bài nghiên cứu, phê bình thuộc lĩnh vực xã hội có cách trình bày đơn giản, không cần cả công thức toán lẫn biểu đồ toán học phức tạp thì `x_math` là lựa chọn rất phù hợp. Tôi khuyến khích bạn dùng thay vì dùng bản tiêu chuẩn. 

Nếu muốn nâng cao hơn nữa chất lượng có thể bổ sung thêm từ chuyên ngành vào prompt (lúc đó cần dùng prompt mới lưu trong thư mục `glossary` tương ứng).

Về cách trích xuất các từ chuyên ngành tham khảo phần **Nâng cao thêm chất lượng dịch với danh sách từ chuyên ngành bổ sung vào prompt** ngay bên dưới.

--

### ⚡ Nâng cao thêm chất lượng dịch với danh sách từ chuyên ngành bổ sung vào prompt

Phần này là tùy ý. Không bắt buộc sử dụng. Nhưng khuyên dùng vì thường cải thiện chất lượng dịch, đặc biệt trên tài liệu dài hoặc khó (hoặc cả hai).

Mặc định SI/prompt mẫu là tương đối tốt để xử lý các tài liệu chuyên ngành. Tuy nhiên nếu bạn muốn cải thiện hơn nữa chất lượng dịch thì hãy sử dụng bộ SI/prompt trong thư mục **`glossary_ext`** để trích xuất cách dịch chuyên ngành & các từ cốt lõi trong tài liệu.

Vào thư mục đó bạn sẽ thấy các file `prompt_glossary_ext` & `system_instructions_glossary_ext` dùng để trích xuất cách dịch từ chuyên ngành.

Khi đẩy lên AI, cũng nên để **Temperature thấp**, thường là **0.3**

Sau đó copy danh sách kết quả đưa vào prompt có hậu tố `_glossary` trong mỗi tùy chọn trên (các prompt tùy chỉnh sẽ nằm trong thư mục `glossary` của Tùy chọn tương ứng):

```
<glossary>
[DÁN DANH SÁCH THUẬT NGỮ ĐÃ TRÍCH XUẤT TỪ TÀI LIỆU]
</glossary>
```

Lúc này **prompt mới** sẽ cung cấp thêm cho AI danh sách từ chuyên ngành để tham khảo trước khi dịch.

`system_instructions` tương ứng không phải chỉnh sửa gì, cứ thế dùng luôn.

Lưu ý: Lúc này prompt sẽ chuyên cho tài liệu nó cần dịch, mỗi khi bạn dịch tài liệu khác cần cập nhật danh sách thuật ngữ chuyên ngành này.

--

## 🔄 SI và prompt bản chia phase theo từng giai đoạn | Tùy chọn 2

Trong thư mục `pdf2html` chứa các SI & prompt được tinh chỉnh theo từng bước xử lý chứ không gộp chung như SI/prompt tiêu chuẩn.

Nó gồm 2 cặp SI/prompt sau:

- `phase_1`: Để chuyển file PDF thành HTML. Lưu kết quả của phase 1 để làm đầu vào của phase 2. Khi xử lý nên để **Temperature 0.3**
- `phase_2`: Tập trung vào nhiệm vụ dịch. Khi xử lý nên để **Temperature 0.5**

Tùy chọn này có khả năng cải thiện chất lượng dịch lên đáng kể (nhất là với file PDF cấu trúc phức tạp), vì nó giúp AI tránh bị quá tải chỉ thị như khi dùng bản tiêu chuẩn (dù đã dùng model tiên tiến nhất). Tuy nhiên nó sẽ khiến bạn mất thời gian và cả tốn Token hơn (thường là gấp đôi so với bản tiêu chuẩn) để tạo ra bản dịch hoàn chỉnh.

Ví dụ kết quả dịch bằng tùy chọn này: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/Book-Of-Proofs-2-vi-phase.pdf

Tùy chọn này còn có thêm 2 biến thể:

- Bổ sung glossary vào prompt (cho phase 2 khi dịch).
- Bỏ bớt chuyển đổi svg trong SI (cho phase 1 khi chuyển đổi sang HTML).

2 biến thể này có thể dùng đồng thời, hoặc dùng riêng. Các file tương ứng nằm trong thư mục tương ứng (`glossary` và `x_svg` trong thư mục tổng `pdf2html`.

---

## ⚖️ Giấy phép & Tuyên bố miễn trừ trách nhiệm

### Giấy phép (License)
Dự án được phát hành dưới bản quyền **MIT License**. Bạn hoàn toàn tự do sử dụng và tích hợp vào các dự án cá nhân hoặc thương mại.

### Tuyên bố từ chối trách nhiệm
Mặc dù đã được kiểm tra kỹ lưỡng, người phát triển không chịu trách nhiệm cho bất kỳ hệ quả nào phát sinh từ các quyết định dựa trên kết quả đầu ra của công cụ này.

> [!WARNING]
> **Lưu ý quan trọng:** Chỉ là nhắc lại lần nữa, không một công cụ dịch thuật tự động nào có thể thay thế hoàn toàn **dịch thuật viên chuyên nghiệp**. Đối với các tài liệu đặc biệt quan trọng, tôi khuyến nghị bạn nên thuê chuyên gia để đảm bảo độ tin cậy tuyệt đối.
