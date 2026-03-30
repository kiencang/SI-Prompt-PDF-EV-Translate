**LỆNH THỰC THI CHÍNH:** 
Dựa trên vai trò và toàn bộ quy tắc đã được nạp trong **System Instructions (SI)**, hãy tiếp nhận tài liệu đầu vào và thực hiện:
1.	Dịch thuật toàn bộ nội dung sang tiếng Việt.
2.	Tái tạo tài liệu dưới dạng một tệp HTML/CSS hoàn chỉnh.

**[A] BẢNG THUẬT NGỮ ÉP BUỘC (GLOSSARY TỐI CAO):**
Áp dụng tuyệt đối Bảng thuật ngữ dưới đây cho toàn bộ bản dịch theo đúng quy tắc Mục 4.1 trong System Instructions. Nhắc lại: Bạn phải tự động nhận diện và điều chỉnh viết hoa/viết thường (Casing) cho phù hợp với ngữ pháp thực tế của câu lệnh/tiêu đề.

<glossary>
[DÁN DANH SÁCH THUẬT NGỮ ĐÃ TRÍCH XUẤT TỪ BƯỚC 1 VÀO ĐÂY]
</glossary>

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

**[D] BƯỚC TỰ ĐỐI SOÁT VÀ TINH CHỈNH (INTERNAL QA - BẮT BUỘC):**
Trước khi xuất kết quả cuối cùng, bạn PHẢI tự kiểm tra nội bộ bằng cách in suy nghĩ vào thẻ `<thinking>`:
1. Đối soát rà quét xem các từ trong `<glossary>` (Mục A) đã được áp dụng đúng và đủ vào bản dịch chưa? Có bị sai lỗi viết hoa/thường ở đầu câu hoặc tiêu đề không?
2. Văn phong đã đủ tự nhiên, trôi chảy chưa hay vẫn còn "mùi" dịch máy (word-by-word)? -> Lên phương án tái cấu trúc lại những câu gượng gạo.
3. Mã HTML có rủi ro tràn lề (overflow) hay cấu trúc thẻ sai logic không?

**[E] ĐỊNH DẠNG ĐẦU RA (STRICT OUTPUT BOUNDARY):**
1. Mở thẻ `<thinking>` để thực hiện phân tích của Bước [D].
2. Ngay sau khi đóng thẻ `</thinking>`, chỉ trả về **MÃ HTML THÔ** của toàn bộ trang.
3. Mã HTML bắt đầu chính xác bằng `<!DOCTYPE html>` và kết thúc bằng `</html>`.