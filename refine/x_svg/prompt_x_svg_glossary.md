**LỆNH THỰC THI CHÍNH:** 
Dựa trên vai trò và toàn bộ quy tắc đã được nạp trong **System Instructions (SI)**, hãy tiếp nhận tài liệu đầu vào và thực hiện:
1.	Dịch thuật toàn bộ nội dung sang tiếng Việt.
2.	Tái tạo tài liệu dưới dạng một tệp HTML/CSS hoàn chỉnh.

**[A] Danh sách tham khảo các thuật ngữ chuyên ngành:**
Dưới đây là danh sách cách dịch các từ cốt lõi & từ chuyên môn hẹp của tài liệu. Nếu từ nào có gắn dấu `[*]` ở cuối là từ còn rất mới chưa có từ tiếng Việt chuẩn thống nhất.

<glossary>
[DÁN DANH SÁCH THUẬT NGỮ ĐÃ TRÍCH XUẤT ]
</glossary>

*	Tuy nhiên chúng không phải cách dịch mà bạn cần tuân thủ tuyệt đối. Hãy sử dụng & điều chỉnh nó linh hoạt dựa theo bối cảnh của tài liệu gốc.
*	Vẫn áp dụng các quy tắc trong phần *4. Thuật ngữ Chuyên ngành (Đặc biệt Quan trọng cho Tài liệu Khoa học)* của SI, mục đích là để bạn có được cách dịch từ chuyên ngành tốt nhất.

**[B] KÍCH HOẠT BỘ NHỚ HỆ THỐNG (TUÂN THỦ NGHIÊM NGẶT):**
Hãy gọi lại và áp dụng tuyệt đối **"Hệ thống Thứ tự Ưu tiên (1-4)"** và **"Quy tắc Giải quyết Xung đột"** trong SI:
*	**[#1 & #1A]** Ý nghĩa chính xác 100% & Chuẩn hóa thuật ngữ học thuật.
*	**[#2]** Tiếng Việt tự nhiên và trôi chảy (BẮT BUỘC phá vỡ và tái cấu trúc câu quyết liệt để thoát ly ngữ pháp tiếng Anh).
*	**[#3]** HTML hiển thị hoàn hảo, không vỡ layout, font chữ nội dung chính đủ lớn để đọc.
*	**[#4]** Bảo toàn định dạng gốc ở mức nỗ lực tối đa (Best-effort).

**[C] CHECKLIST KỸ THUẬT QUAN TRỌNG:**
*	**Cột & Layout:** Ép luồng văn bản chính về **1 CỘT DUY NHẤT**.
*	**Bảng biểu:** BẮT BUỘC bọc mọi `<table>` bằng `<div class="table-wrapper">` (áp dụng CSS cơ sở trong SI) để chống tràn ngang.
*	**Công thức Toán học:** Phải dùng cú pháp LaTeX `\(\)` và `\[\]`. BẮT BUỘC nhúng thẻ `<script>` MathJax vào `<head>`. (Giữ nguyên dấu chấm `.` thập phân bên trong block LaTeX).
*	**Tài liệu tham khảo (References):** KHÔNG DỊCH các thành phần nhận diện (Tác giả, Tên sách/báo, Tạp chí, DOI, URL...). Giữ nguyên định dạng gốc.
*	**Hình ảnh:** Thẻ `<img>` phải có `alt` text tiếng Việt có ý nghĩa.
*	**Tối ưu thiết kế cho màn hình lớn**: Bản dịch cuối cùng có khả năng đọc được trên nhiều kích cỡ màn hình khác nhau, nhưng kích cỡ màn hình lớn (trên laptop/desktop) vẫn là ưu tiên cao nhất.

**[D] BƯỚC TỰ ĐỐI SOÁT VÀ TINH CHỈNH (Internal QA - Thực hiện ngầm):**
Trước khi xuất kết quả cuối cùng, tự kiểm tra nội bộ:
1.	*Văn phong đã đủ tự nhiên, trôi chảy chưa hay vẫn còn "mùi" dịch máy (word-by-word)?* -> Tự động sửa lại câu từ nếu thấy gượng gạo.
2.	*Mã HTML có rủi ro tràn lề (overflow) hay cấu trúc thẻ sai logic không?* -> Tự động tối ưu lại CSS/HTML.

**[E] ĐỊNH DẠNG ĐẦU RA BẮT BUỘC (STRICT OUTPUT BOUNDARY):**
*	Chỉ trả về MÃ HTML THÔ.
*	Bắt đầu chính xác bằng `<!DOCTYPE html>` và kết thúc bằng `</html>`.