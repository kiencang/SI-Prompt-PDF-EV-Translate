# SI-Prompt-EV-Translate

> **Cung cấp System Instructions (SI) và Prompt chất lượng cao chuyên dụng cho nhiệm vụ dịch thuật tài liệu khoa học (định dạng PDF) từ tiếng Anh sang tiếng Việt.**

Dự án này cung cấp bộ khung hướng dẫn tối ưu giúp AI xử lý các văn bản học thuật có độ phức tạp cao, đảm bảo độ chính xác về thuật ngữ và bảo toàn định dạng tốt nhất có thể.

---

## 📚 Xem thử chất lượng

Ví dụ về chất lượng dịch của bộ SI/prompt này, bạn có thể xem khả năng của nó khi dịch khoảng 10 trang mở đầu trong cuốn **Book Of Proofs** của **Richard Hammack**:

- Bản tiếng Anh: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/Book-Of-Proofs-2-en.pdf
- Bản dịch tiếng Việt: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/Book-Of-Proofs-2-vi.pdf

---

## 🚀 Tại sao nên sử dụng với Gemini AI Studio?

Việc kết hợp bộ SI/Prompt này với **Gemini AI Studio** (https://aistudio.google.com/) mang lại nhiều lợi thế vượt trội:

* **Tối ưu hóa hệ sinh thái:** Công cụ được tinh chỉnh và kiểm tra kỹ lưỡng trên model Gemini.
* **Tiết kiệm chi phí:** Hạn mức miễn phí rộng rãi, phù hợp cho nhu cầu dịch thuật cá nhân mà hầu như không phát sinh phí. Đăng ký nhanh chóng, không gặp rào cản.
* **Tùy chỉnh chuyên sâu:** Cung cấp nhiều thiết lập nâng cao và dễ dàng tùy chỉnh qua giao diện dễ hiểu.
* **Chất lượng cao:** Gemini hiện là một trong những AI có khả năng xử lý ngữ cảnh và dịch thuật tốt nhất.
* **Đủ sức mạnh:** Bản AI Studio có sức mạnh để dịch văn bản dài, mà nếu bạn sử dụng các AI giao diện người dùng phổ thông khác thì thường không đủ (bản dịch thường bị cắt ngắn hoặc chất lượng thấp do không hiểu rõ hướng dẫn).

---

## 🛠 Hướng dẫn thiết lập & Sử dụng

Để đạt kết quả tốt nhất, hãy thực hiện theo các bước sau trong AI Studio:

### 1. Cấu hình Model
* **Model:** Chọn model tiên tiến nhất (khuyến nghị: `Gemini 3.1 Pro Preview` hoặc các bản `Preview` mới nhất).
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
1. Trong mỗi lần gửi dữ liệu dịch nên giới hạn độ dài file PDF khoảng **10 trang** (có thể điều chỉnh con số với tài liệu thực tế). Lý do là vì mặc dù ngữ cành đầu vào cho phép đến hàng triệu Token, ngữ cảnh đầu ra (bản dịch) chịu giới hạn khoảng 64 ngàn Token.
2. Đối với tài liệu PDF rất dài (ví dụ dịch sách), cần phải chia tách nó thành các file nhỏ hơn để dịch từng file nhỏ (vì giới hạn Token đầu ra), và nên chia tách sao cho nó không bị 'lửng lơ' (ngắt giữa chừng một khối văn bản cần dịch). Có rất nhiều công cụ trực tuyến chất lượng cao giúp tách file PDF, ví dụ: https://smallpdf.com/vi/split-pdf

---

## 📝 Lưu ý kỹ thuật quan trọng khác

* **Thời gian xử lý:** Do tính chất phức tạp của tài liệu khoa học, thời gian hoàn thành có thể dao động từ **150s đến 600s** tùy độ dài file.
* **Định dạng đầu ra:** Kết quả trả về ở dạng **mã HTML**.
    * *Lời khuyên:* Bạn phải lưu nội dung này thành file `.html` (ví dụ `bandich.html`) để xem đầy đủ định dạng qua trình duyệt (ưu tiên Google Chrome).
* **Khả năng bảo toàn:** Công cụ hỗ trợ giữ định dạng rất tốt nhưng không thể hoàn hảo 100% đối với mọi loại bố cục PDF phức tạp. Ảnh dạng sơ đồ biểu đồ không quá phức tạp thường được tái tạo lại tương đối tốt, riêng các ảnh dạng ảnh chụp (như ảnh chụp bằng điện thoại, máy ảnh) trong file PDF sẽ không được tái tạo trong bản dịch.

--

Đoạn HTML sẽ luôn bắt đầu bằng: 

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

# 🔄 SI và prompt bản tinh chỉnh (refine)

Trong thư mục `refine` chứa các SI & prompt được tinh chỉnh cho những tài liệu không quá phức tạp.

Về lý thuyết, SI & prompt tốt là các hướng dẫn phù hợp (đúng & đủ) với tài liệu, không nên chứa các chỉ thị thừa thãi. SI & prompt tiêu chuẩn rất mạnh xử lý các tài liệu khoa học phức tạp, nhưng với các tài liệu đơn giản hơn nó sẽ dư thừa ít nhiều, bạn có thể cân nhắc sử dụng phiên bản refine.

Hiện trong thư mục đang có những bản tinh chỉnh sau:

- `x_svg`: chứa SI & prompt loại bỏ chỉ thị liên quan đến tạo sơ đồ, biểu đồ toán học. Nhiều tài liệu không cần đến các chỉ thị này... Chỉ thị liên quan đến tạo sơ đồ biểu đồ chiếm khoảng 25% dung lượng của bản SI tiêu chuẩn, do vậy việc loại bỏ nó khi không cần thiết có khả năng cải thiện khá cao mức độ tập trung của SI. Đây có thể là phiên bản tinh chỉnh bạn sẽ hay dùng nhất.
- `x_math`: chứa SI & prompt loại bỏ hoàn toàn chỉ thị liên quan đến tạo công thức toán & cả svg. Một số tài liệu sẽ không cần cả hai chỉ thị này. Nếu tài liệu của bạn vẫn có các công thức toán học nhưng không có sơ đồ, biểu đồ thì nên dùng `x_svg` thay vì `x_math`.

---

## 🎨 Nâng cao SI với danh sách thuật ngữ chuyên ngành

Phần này là tùy chọn. Không bắt buộc sử dụng.

Mặc định SI/prompt chính là đủ để xử lý rất tốt các tài liệu chuyên ngành. Tuy nhiên nếu bạn muốn cải thiện hơn nữa chất lượng dịch thì trước khi dịch hãy sử dụng thêm SI/prompt trong thư mục **glossary**. Mục đích là để trích xuất cách dịch chuyên ngành của các từ quan trọng nhất trong tài liệu.

Lưu ý: Khi dùng, nhớ điền tên chuyên ngành của tài liệu vào trong prompt của phần glossary. Và khi đẩy lên AI yêu cầu cũng nên để **Temperature thấp**, từ 0.1 đến 0.3

Sau đó copy danh sách kết quả đưa vào dưới mục 4.  **Thuật ngữ Chuyên ngành (Đặc biệt Quan trọng cho Tài liệu Khoa học)** trong SI chính.

Đặt tên nó như sau:

4.1 **Bảng thuật ngữ chuyên ngành**: BẮT BUỘC (Strictly Enforced) khi gặp các từ tiếng Anh nằm trong bảng thuật ngữ dưới đây, bạn PHẢI sử dụng chính xác từ tiếng Việt tương ứng ở bên phải. Tuyệt đối không sử dụng từ đồng nghĩa khác.

Copy/Paste danh sách mà bạn có được ở trên. Lưu SI lại.

Ví dụ mẫu:

```
4.1 **Bảng thuật ngữ chuyên ngành**: BẮT BUỘC (Strictly Enforced) khi gặp các từ tiếng Anh nằm trong bảng thuật ngữ dưới đây, bạn PHẢI sử dụng chính xác từ tiếng Việt tương ứng ở bên phải. Tuyệt đối không sử dụng từ đồng nghĩa khác.
**A**
- Absolute value: Giá trị tuyệt đối
- Addition principle: Nguyên lý cộng

**B**
- Basis step: Bước cơ sở
- Biconditional statement: Mệnh đề hai chiều
- Bijection: Song ánh
- Bijective function: Hàm song ánh
- Binomial theorem: Định lý nhị thức
```

--

Lưu ý 1: Lúc này SI sẽ chuyên cho tài liệu nó cần dịch, mỗi khi bạn dịch tài liệu khác cần cập nhật danh sách thuật ngữ chuyên ngành này.

Lưu ý 2: Cách này thường chỉ tốt hơn mặc định khi tài liệu cần dịch có độ dài cao và phức tạp. Ngoài ra, tuy có triển vọng cải thiện chất lượng dịch, điều này không chắc chắn luôn đúng. Cách tốt nhất là bạn thử kiểm tra trên một số tài liệu và so sánh để có kết luận cụ thể.

---

# ⚡ SI và prompt bản mini

Nhìn chung trong hầu hết trường hợp tôi khuyến khích bạn sử dụng SI/prompt tiêu chuẩn, nó là cái `system_instructions.md` và `prompt.md`, bởi vì nó cho **chất lượng bản dịch cao hơn đáng kể**.

Tuy nhiên nếu bạn muốn dùng phiên bản tinh gọn (chủ yếu để thấy sự khác biệt trong chỉ thị ảnh hưởng đến kết quả dịch thế nào), bạn có thể dùng phiên bản mini để kiểm tra, nó là cái `system_instructions_mini.md` và `prompt_mini.md` nằm trong thư mục `mini`. Bạn nên dùng cùng một model AI để test, điều đó giúp kết quả khách quan hơn.

---

## ⚖️ Giấy phép & Tuyên bố miễn trừ trách nhiệm

### Giấy phép (License)
Dự án được phát hành dưới bản quyền **MIT License**. Bạn hoàn toàn tự do sử dụng và tích hợp vào các dự án cá nhân hoặc thương mại.

### Tuyên bố từ chối trách nhiệm
Mặc dù đã được kiểm tra kỹ lưỡng, người phát triển không chịu trách nhiệm cho bất kỳ hệ quả nào phát sinh từ các quyết định dựa trên kết quả đầu ra của công cụ này.

> [!WARNING]
> **Lưu ý quan trọng:** Không một công cụ dịch thuật tự động nào có thể thay thế hoàn toàn **dịch thuật viên chuyên nghiệp**. Đối với các tài liệu đặc biệt quan trọng, tôi khuyến nghị bạn nên thuê chuyên gia để đảm bảo độ tin cậy tuyệt đối.
