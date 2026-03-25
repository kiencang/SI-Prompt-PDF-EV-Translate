# SI-Prompt-EV-Translate

> **System Instructions (SI) và Prompt chất lượng cao chuyên dụng cho nhiệm vụ dịch thuật tài liệu khoa học PDF (Anh - Việt).**

Dự án này cung cấp bộ khung hướng dẫn tối ưu giúp AI xử lý các văn bản học thuật có độ phức tạp cao, đảm bảo độ chính xác về thuật ngữ và bảo toàn định dạng tốt nhất có thể.

---

## 🚀 Tại sao nên sử dụng với Gemini AI Studio?

Việc kết hợp bộ SI/Prompt này với **Gemini AI Studio** mang lại nhiều lợi thế vượt trội:

* **Tối ưu hóa hệ sinh thái:** Công cụ được tinh chỉnh và kiểm tra kỹ lưỡng trên model Gemini.
* **Tiết kiệm chi phí:** Hạn mức miễn phí rộng rãi, phù hợp cho nhu cầu dịch thuật cá nhân mà hầu như không phát sinh phí.
* **Tùy chỉnh chuyên sâu:** Cung cấp nhiều thiết lập nâng cao và khả năng đăng ký dễ dàng.
* **Hiệu suất hàng đầu:** Gemini hiện là một trong những AI có khả năng xử lý ngữ cảnh và dịch thuật tốt nhất.

---

## 🛠 Hướng dẫn thiết lập & Sử dụng

Để đạt kết quả tốt nhất, hãy thực hiện theo các bước sau trong AI Studio:

### 1. Cấu hình Model
* **Model:** Chọn model tiên tiến nhất (khuyến nghị: `Gemini 3.1 Pro Preview` hoặc các bản `Preview` mới nhất).
* **System Instructions:** Copy toàn bộ nội dung SI của công cụ này và dán vào khung **System instructions** (ngay dưới phần chọn model).
* **Tham số kỹ thuật:**
    * `Temperature`: Điều chỉnh xuống mức **0.3** (thay vì mặc định là 1.0). 
    * *Lưu ý:* Mức nhiệt độ thấp giúp thắt chặt tính logic, tránh dịch quá đà, đảm bảo văn phong khoa học nghiêm túc.

### 2. Thao tác dịch
1. Copy **Prompt** vào khung chat.
2. Nhấn nút **+** để tải file **PDF** cần dịch lên.
3. Nhấn **Enter** và đợi AI xử lý.

### 3. Độ dài của file PDF
1. Trong mỗi lần gửi dữ liệu dịch nên giới hạn độ dài file PDF khoảng **10 trang** (có thể điều chỉnh con số với tài liệu thực tế). Lý do là vì mặc dù ngữ cành đầu vào cho phép đến hàng triệu Token, ngữ cảnh đầu ra (bản dịch) chịu giới hạn khoảng 64 ngàn Token.
2. Đối với tài liệu PDF rất dài (ví dụ dịch sách), cần phải chia tách nó thành các file nhỏ hơn để dịch từng file nhỏ (vì giới hạn Token đầu ra), và nên chia tách sao cho nó không bị 'lửng lơ' (ngắt giữa chừng một khối văn bản cần dịch). Có rất nhiều công cụ trực tuyến chất lượng cao giúp tách file PDF, ví dụ: https://smallpdf.com/vi/split-pdf

---

## 📝 Lưu ý kỹ thuật quan trọng

* **Thời gian xử lý:** Do tính chất phức tạp của tài liệu khoa học, thời gian hoàn thành có thể dao động từ **150s đến 600s** tùy độ dài file.
* **Định dạng đầu ra:** Kết quả trả về ở dạng **mã HTML**.
    * *Lời khuyên:* Bạn nên lưu nội dung này thành file `.html` để xem đầy đủ định dạng qua trình duyệt (ưu tiên Google Chrome).
* **Khả năng bảo toàn:** Công cụ hỗ trợ giữ định dạng rất tốt nhưng không thể hoàn hảo 100% đối với mọi loại bố cục PDF phức tạp.

---

## 🚀 Nâng cao với danh sách thuật ngữ chuyên ngành

Phần này là tùy chọn. Không bắt buộc sử dụng.

Mặc định SI/prompt chính là đủ để xử lý tốt các tài liệu chuyên ngành. Tuy nhiên nếu bạn muốn cải thiện hơn nữa chất lượng dịch thì trước khi dịch hãy sử dụng thêm SI/prompt trong thư mục **glossary**. Mục đích là để trích xuất cách dịch chuyên ngành của các từ quan trọng nhất trong tài liệu.

Sau đó copy danh sách đó đưa vào dưới mục 4.  **Thuật ngữ Chuyên ngành (Đặc biệt Quan trọng cho Tài liệu Khoa học):** trong SI chính.

Đặt tên nó như sau:

4.1 **Bảng thuật ngữ chuyên ngành**

Hãy sử dụng cách dịch trong bảng thuật ngữ chuyên ngành dưới đây để xử lý các từ chuyên ngành trong tài liệu.

Copy/Past danh sách mà bạn có được ở trên. Lưu SI lại.

--

Lưu ý 1: Lúc này SI sẽ chuyên cho tài liệu nó cần dịch, mỗi khi bạn dịch tài liệu khác cần cập nhật danh sách thuật ngữ chuyên ngành này.

Lưu ý 2: Cách này thường chỉ tốt hơn khi tài liệu cần dịch có độ dài cao và phức tạp.

---

## ⚖️ Giấy phép & Tuyên bố miễn trừ

### Giấy phép (License)
Dự án được phát hành dưới bản quyền **MIT License**. Bạn hoàn toàn tự do sử dụng và tích hợp vào các dự án cá nhân hoặc thương mại.

### Tuyên bố từ chối trách nhiệm
Mặc dù đã được kiểm tra kỹ lưỡng, người phát triển không chịu trách nhiệm cho bất kỳ hệ quả nào phát sinh từ các quyết định dựa trên kết quả đầu ra của công cụ này.

> [!WARNING]
> **Lưu ý quan trọng:** Không một công cụ dịch thuật tự động nào có thể thay thế hoàn toàn **dịch thuật viên chuyên nghiệp**. Đối với các tài liệu đặc biệt quan trọng, tôi khuyến nghị bạn nên thuê chuyên gia để đảm bảo độ tin cậy tuyệt đối.
