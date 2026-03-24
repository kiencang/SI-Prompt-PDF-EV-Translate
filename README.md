# SI-Prompt-EV-Translate

> **System Instructions (SI) và Prompt chất lượng cao chuyên dụng cho nhiệm vụ dịch thuật tài liệu khoa học PDF (Anh - Việt).**

Dự án này cung cấp bộ khung hướng dẫn tối ưu giúp AI xử lý các văn bản học thuật có độ phức tạp cao, đảm bảo độ chính xác về thuật ngữ và bảo toàn định dạng tốt nhất có thể.

---

## 🚀 Tại sao nên sử dụng với Gemini AI Studio?

Việc kết hợp bộ SI/Prompt này với **Gemini AI Studio** mang lại nhiều lợi thế vượt trội:

* **Tối ưu hóa hệ sinh thái:** Công cụ được tinh chỉnh và kiểm tra kỹ lưỡng trên các dòng model Gemini.
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

---

## 📝 Lưu ý kỹ thuật quan trọng

* **Thời gian xử lý:** Do tính chất phức tạp của tài liệu khoa học, thời gian hoàn thành có thể dao động từ **150s đến 600s** tùy độ dài file.
* **Định dạng đầu ra:** Kết quả trả về ở dạng **mã HTML**.
    * *Lời khuyên:* Bạn nên lưu nội dung này thành file `.html` để xem đầy đủ định dạng qua trình duyệt (ưu tiên Google Chrome).
* **Khả năng bảo toàn:** Công cụ hỗ trợ giữ định dạng rất tốt nhưng không thể hoàn hảo 100% đối với mọi loại bố cục PDF phức tạp.

---

## ⚖️ Giấy phép & Tuyên bố miễn trừ

### Giấy phép (License)
Dự án được phát hành dưới bản quyền **MIT License**. Bạn hoàn toàn tự do sử dụng và tích hợp vào các dự án cá nhân hoặc thương mại.

### Tuyên bố từ chối trách nhiệm
Mặc dù đã được kiểm tra kỹ lưỡng, người phát triển không chịu trách nhiệm cho bất kỳ hệ quả nào phát sinh từ các quyết định dựa trên kết quả đầu ra của công cụ này.

> [!WARNING]
> **Lưu ý quan trọng:** Không một công cụ dịch thuật tự động nào có thể thay thế hoàn toàn **dịch thuật viên chuyên nghiệp**. Đối với các tài liệu đặc biệt quan trọng, tôi khuyến nghị bạn nên thuê chuyên gia để đảm bảo độ tin cậy tuyệt đối.
