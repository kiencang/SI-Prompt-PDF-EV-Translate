**Nhiệm vụ Chính**: Dựa trên vai trò và các nguyên tắc hoạt động đã được định nghĩa chi tiết trong System Instructions (SI) nâng cao của bạn, hãy thực hiện:

1.  **Dịch thuật Anh-Việt**: Dịch **cực kỳ chính xác về ý nghĩa** và **tuyệt đối tự nhiên về văn phong tiếng Việt** toàn bộ **nội dung văn bản có thể đọc được** và các thành phần có ngữ nghĩa (như alt text cho ảnh) từ tài liệu PDF tiếng Anh được cung cấp. **TUÂN THỦ NGHIÊM NGẶT Ưu tiên #1 và #2** trong SI, đặc biệt là yêu cầu **tái cấu trúc câu/đoạn một cách quyết liệt và sáng tạo**.
2.  **Tái tạo sang HTML**: Trình bày bản dịch dưới dạng một **đoạn mã HTML thô hoàn chỉnh và ngữ nghĩa**. **Nỗ lực tối đa (best-effort)** để **bảo toàn layout và định dạng gốc** của PDF bằng HTML/CSS, nhưng **TUYỆT ĐỐI KHÔNG VI PHẠM Ưu tiên #3 (Tránh vỡ layout/Đảm bảo đọc được)** và luôn tuân thủ **Thứ tự Ưu tiên**, **Quy tắc Giải quyết Xung đột**, và các hướng dẫn xử lý yếu tố đặc biệt (ảnh, bảng, cột, header/footer, accessibility) trong SI.

**Đầu vào**: Tài liệu PDF tiếng Anh.
**Đầu ra**: Một đoạn mã HTML thô hoàn chỉnh, **không chứa bất kỳ văn bản nào khác ngoài mã HTML đó** (không lời dẫn, không giải thích, không markdown bao quanh).

---
**## Yêu cầu TUYỆT ĐỐI (Không được vi phạm):**

1.  **Phạm vi Dịch & Xử lý**: Tuân thủ mục "Phạm vi Xử lý" trong SI. Chỉ dịch text đọc được, tạo alt text Việt hóa cho ảnh, giữ nguyên code/URL, bỏ qua metadata ẩn...
2.  **Định dạng Output**: **CHỈ MÃ HTML THÔ.**
3.  **Chất lượng Dịch thuật (NHẮC LẠI ƯU TIÊN CAO NHẤT):**
    *   **#1: CHÍNH XÁC Ý NGHĨA.**
    *   **#1A: CHÍNH XÁC VÀ CHUẨN HÓA THUẬT NGỮ CHUYÊN NGÀNH (Đặc biệt cho tài liệu khoa học):** Tuân thủ nghiêm ngặt các hướng dẫn chi tiết trong Mục 3 của SI về xử lý thuật ngữ (ưu tiên thuật ngữ Việt chuẩn hóa, giữ nguyên gốc nếu không chắc/không có, giải thích lần đầu nếu cần, nhất quán tuyệt đối).
    *   **#2: TIẾNG VIỆT TỰ NHIÊN TUYỆT ĐỐI (Bao gồm TÁI CẤU TRÚC MẠNH MẼ).**
        *   **Ưu tiên giọng chủ động (Có điều kiện):** Ưu tiên chuyển đổi câu bị động sang chủ động nếu phù hợp. **TUY NHIÊN, đối với tài liệu KHOA HỌC/KỸ THUẬT, hãy duy trì cấu trúc bị động (ví dụ: "được tiến hành", "được đo lường") nếu việc này giúp bảo đảm tính khách quan của thực nghiệm và giữ trọng tâm vào đối tượng nghiên cứu thay vì người thực hiện.**
        *   *Ví dụ Tái cấu trúc (Nhấn mạnh lại tầm quan trọng: Bạn hãy thấm nhuần tư duy này và áp dụng một cách sáng tạo, quyết liệt cho TOÀN BỘ bản dịch. Hãy thoát ly hoàn toàn khỏi cấu trúc câu tiếng Anh gốc, ưu tiên hàng đầu cho sự mạch lạc, tự nhiên và dễ hiểu trong tiếng Việt):*

            1.  `Gốc`: `The system requires **immediate attention** due to a critical error.`
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Do phát sinh lỗi nghiêm trọng, hệ thống **cần được xử lý/can thiệp ngay lập tức**.`
                    *   `Hệ thống **cần được chú ý xử lý ngay** vì đã xảy ra lỗi nghiêm trọng.`
                    *   `Một lỗi nghiêm trọng vừa xuất hiện, **đòi hỏi hệ thống phải được xử lý tức thì**.`

            2.  `Gốc`: `Users *who have completed the training* can access the advanced features.`
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Người dùng có thể truy cập các tính năng nâng cao *sau khi hoàn thành khóa đào tạo*.`
                    *   `Các tính năng nâng cao chỉ dành cho những người dùng *đã hoàn thành khóa đào tạo*.`
                    *   `*Hoàn tất khóa đào tạo* là điều kiện để người dùng truy cập các tính năng nâng cao.`

            3.  `Gốc`: `The research findings **were meticulously analyzed** by the committee before the final decision was made.` (Câu bị động, mệnh đề thời gian ở cuối)
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Trước khi đưa ra quyết định cuối cùng, hội đồng **đã phân tích tỉ mỉ** các kết quả nghiên cứu.`
                    *   `Các kết quả nghiên cứu **đã được hội đồng phân tích kỹ lưỡng** trước khi đi đến quyết định sau cùng.`
                    *   `Hội đồng **đã tiến hành phân tích một cách cẩn trọng** các kết quả nghiên cứu rồi mới đưa ra quyết định cuối cùng.`

            4.  `Gốc`: `It is *imperative for all employees to understand* the new data privacy regulations.` (Cấu trúc "It is + adj + for sb + to do sth")
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Tất cả nhân viên *bắt buộc phải nắm vững* các quy định mới về bảo mật dữ liệu.`
                    *   `Việc *toàn thể nhân viên hiểu rõ* các quy định mới về bảo mật dữ liệu là yêu cầu cấp thiết.`
                    *   `Các quy định mới về bảo mật dữ liệu *đòi hỏi mọi nhân viên phải thông hiểu*.`

            5.  `Gốc`: `The *successful implementation of advanced machine learning algorithms* has led to a significant improvement in prediction accuracy.` (Chủ ngữ là một cụm danh từ dài, phức tạp)
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Việc *triển khai thành công các thuật toán học máy tiên tiến* đã giúp cải thiện đáng kể độ chính xác của dự đoán.`
                    *   `Nhờ *ứng dụng thành công các thuật toán học máy tiên tiến*, độ chính xác trong dự đoán đã được nâng cao rõ rệt.`
                    *   `Độ chính xác của các mô hình dự đoán đã được cải thiện vượt bậc *sau khi áp dụng thành công những thuật toán học máy tiên tiến*.`

            6.  `Gốc`: `This paper presents a novel approach *that addresses the limitations of existing methods* by incorporating contextual information.` (Mệnh đề quan hệ dài, "by + V-ing")
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Bài báo này giới thiệu một phương pháp tiếp cận mới, *khắc phục được những hạn chế của các phương pháp hiện hành* bằng cách tích hợp thông tin theo ngữ cảnh.`
                    *   `Bằng việc kết hợp thông tin ngữ cảnh, phương pháp mới được trình bày trong bài báo này *đã giải quyết những tồn tại của các phương pháp trước đó*.`
                    *   `Phương pháp mới trong bài viết này, với việc tích hợp thông tin ngữ cảnh, *mang đến giải pháp cho những điểm yếu cố hữu của các phương pháp cũ*.`

            7.  `Gốc`: `There is a *growing consensus among researchers* that climate change is primarily driven by human activities.` (Cấu trúc "There is + Noun + that...")
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Giới nghiên cứu đang *ngày càng có chung nhận định* rằng biến đổi khí hậu chủ yếu do các hoạt động của con người gây ra.`
                    *   `Ngày càng nhiều nhà khoa học *đi đến sự đồng thuận* rằng các hoạt động của con người là nguyên nhân chính dẫn đến biến đổi khí hậu.`
                    *   `Một *quan điểm ngày càng được chấp nhận rộng rãi trong giới học thuật* là biến đổi khí hậu phần lớn bắt nguồn từ các hoạt động của con người.`

            8.  `Gốc`: `The data suggests a *strong correlation between regular exercise and improved mental well-being*, although a causal link has not yet been definitively established.` (Hai mệnh đề đối lập, một mệnh đề phức tạp)
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Dữ liệu cho thấy *mối liên hệ chặt chẽ giữa việc tập thể dục đều đặn và sức khỏe tinh thần được cải thiện*; tuy nhiên, mối quan hệ nhân quả vẫn chưa được khẳng định chắc chắn.`
                    *   `Mặc dù mối liên hệ nhân quả chưa được xác lập một cách rõ ràng, dữ liệu vẫn chỉ ra rằng việc tập thể dục thường xuyên *có tác động tích cực và mạnh mẽ đến trạng thái tinh thần*.`
                    *   `Số liệu thu thập được hé lộ *sự gắn kết mật thiết giữa luyện tập thể chất thường xuyên và đời sống tinh thần khởi sắc hơn*, dẫu cho mối liên hệ nguyên nhân - kết quả trực tiếp vẫn còn là một dấu hỏi.`

            9.  `Gốc`: `Effective communication is _crucial for ensuring that project goals are met_ and stakeholders remain informed.` (Tính từ + for + V-ing, hai mục đích song song)
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Giao tiếp hiệu quả đóng vai trò _then chốt trong việc đảm bảo các mục tiêu của dự án được hoàn thành_ và các bên liên quan luôn được cập nhật thông tin.`
                    *   `Để _đảm bảo các mục tiêu dự án được đáp ứng_ và các bên liên quan luôn nắm bắt tình hình, việc giao tiếp hiệu quả là cực kỳ quan trọng.`
                    *   `Việc giao tiếp một cách hiệu quả là _yếu tố quyết định để dự án đạt được mục tiêu đề ra_, đồng thời giúp các bên liên quan luôn được thông tin đầy đủ.`

            10. `Gốc`: `The company's decision *to invest in renewable energy sources* reflects its commitment to sustainability.` (Noun + to-infinitive làm định ngữ cho danh từ)
                *   `Tự nhiên (Khuyến khích)`:
                    *   `Quyết định *đầu tư vào các nguồn năng lượng tái tạo* của công ty thể hiện rõ cam kết của họ đối với sự phát triển bền vững.`
                    *   `Việc công ty quyết định *rót vốn vào các nguồn năng lượng tái tạo* cho thấy sự theo đuổi mục tiêu phát triển bền vững của họ.`
                    *   `Cam kết của công ty đối với phát triển bền vững được minh chứng qua quyết định *đầu tư mạnh vào các nguồn năng lượng tái tạo*.`
        *   **Lưu ý khi AI áp dụng (nhắc lại và nhấn mạnh thêm):**
            *   **Ưu tiên tuyệt đối ý nghĩa gốc:** Mọi sự tái cấu trúc phải xuất phát từ việc hiểu chính xác 100% ý định và sắc thái của câu gốc.
            *   **Mạnh dạn và sáng tạo:** Đừng ngần ngại phá vỡ hoàn toàn cấu trúc ngữ pháp Anh. Hãy tư duy như một người viết tiếng Việt thực thụ, tìm cách diễn đạt ý tưởng đó một cách tự nhiên và hiệu quả nhất trong tiếng Việt.
            *   **Ngữ điệu và dòng chảy:** Chú ý đến nhịp điệu, sự trôi chảy của câu văn tiếng Việt. Đôi khi việc tách một câu dài thành hai câu ngắn hoặc nối hai câu ngắn lại có thể giúp cải thiện điều này.
            *   **Lựa chọn từ đồng nghĩa/gần nghĩa:** Cân nhắc các từ đồng nghĩa hoặc gần nghĩa để tìm ra từ phù hợp nhất với ngữ cảnh và văn phong của tài liệu. Ví dụ: "understand" có thể dịch là "hiểu rõ", "nắm vững", "thông hiểu", "thấu suốt" tùy sắc thái.
            *   **Tránh lặp từ/cấu trúc:** Nếu một cấu trúc câu tiếng Anh lặp lại nhiều lần, hãy cố gắng đa dạng hóa cách diễn đạt trong tiếng Việt.
            *   **Kiểm tra lại sau khi dịch:** Luôn đọc lại bản dịch tiếng Việt một cách độc lập để đảm bảo nó thực sự tự nhiên, dễ hiểu và không còn "dấu vết" của câu gốc tiếng Anh.

4.  **Xử lý Layout, Định dạng & Cấu trúc HTML (NHẮC LẠI ƯU TIÊN KỸ THUẬT):**
    *   Luôn nhớ **Ưu tiên #3 (Không vỡ layout/Đọc được)** > **Ưu tiên #4 (Cố gắng bảo toàn layout)**.
    *   **ĐẢM BẢO KÍCH THƯỚC FONT CHỮ ĐỌC ĐƯỢC:** Kích thước font chữ của **nội dung chính** (các đoạn văn bản `<p>`) phải đủ lớn để đọc thoải mái trên web (khuyến nghị tối thiểu 14px-16px), ngay cả khi phải **tăng kích thước so với PDF gốc**.
    *   **BẮT BUỘC** chuyển thân văn bản chính nhiều cột thành **1 cột** trong HTML.
    *   Xử lý **Hình ảnh (`<img>`)**: Đảm bảo có thẻ `<img>` với `src` hợp lý (hoặc placeholder) và **thuộc tính `alt` tiếng Việt có ý nghĩa** (hoặc `alt=""` nếu trang trí).
    *   Xử lý **Văn bản trong Ảnh/Biểu đồ**: Định vị CSS khéo léo, không che khuất.
    *   Xử lý **Bảng biểu (`<table>`)**: Đảm bảo **cấu trúc ngữ nghĩa** (`thead`, `tbody`, `th`, `td`), đơn giản hóa nếu cần để dễ đọc.
    *   Xử lý **Header/Footer**: Tích hợp hợp lý, không gây xáo trộn.
    *   Đảm bảo **HTML ngữ nghĩa** (semantic HTML) và tuân thủ **accessibility cơ bản** (cấu trúc heading, alt text, table headers).
	*   **Tinh chỉnh Typography (Tùy chọn):** Trong khối `<style>`, hãy cân nhắc thêm các thuộc tính xử lý ngắt trang/ngắt cột cơ bản cho thẻ `<p>` (ví dụ: `orphans: 2; widows: 2;` hoặc `3`) để đảm bảo các đoạn văn không bị đứt gãy mồ côi/góa phụ khi người dùng in tài liệu hoặc xem trên các thiết bị có kích thước màn hình đặc thù, tăng tối đa tính chuyên nghiệp cho bản dịch.

5.  **Xử lý Tài liệu Tham khảo (References/Bibliography)**: **TUÂN THỦ NGHIÊM NGẶT** các quy tắc trong SI: **KHÔNG dịch** tên tác giả, tiêu đề (bài báo, sách, tạp chí), nhà xuất bản, thông tin xuất bản, DOI, URL. **Chỉ dịch** các ghi chú/bình luận do tác giả gốc viết thêm (nếu có). **Bảo toàn định dạng gốc** (đậm, nghiêng, cấu trúc list) và **đảm bảo DOI/URL là link hoạt động**.

---
**## Quy trình Thực hiện & KIỂM TRA CUỐI CÙNG (Bắt buộc):**

1.  **Phân tích PDF Toàn diện**: Hiểu rõ nội dung, cấu trúc logic, layout, định dạng, hình ảnh, bảng biểu.
2.  **Dịch thuật Tập trung (Ưu tiên #1, #1A & #2)**: Tạo bản dịch tiếng Việt chuẩn xác, tự nhiên nhất, tái cấu trúc không khoan nhượng. Xác định nội dung cho `alt` text của ảnh.
3.  **Tạo HTML/CSS Ngữ nghĩa & Accessibile (Ưu tiên #3 & #4)**: Xây dựng cấu trúc HTML ngữ nghĩa, nhúng bản dịch, tích hợp ảnh (`<img>` với `alt`), bảng (`<table>`), áp dụng CSS để cố gắng tái tạo giao diện gốc. **Luôn kiểm soát chặt chẽ** để không vỡ layout và đảm bảo khả năng truy cập cơ bản. Xử lý các yếu tố đặc biệt (ảnh, cột, header/footer, bảng phức tạp) theo đúng hướng dẫn SI. Giải quyết xung đột theo đúng thứ tự ưu tiên và quy tắc trong SI.
4.  **KIỂM TRA CHẤT LƯỢNG TOÀN DIỆN (CỰC KỲ QUAN TRỌNG):**
    *   Đọc lại **TOÀN BỘ nội dung tiếng Việt** trong mã HTML được tạo ra (bao gồm cả `alt` text nếu có thể xem được).
    *   **Tự vấn nghiêm khắc dựa trên các Nguyên tắc và Yêu cầu trong SI & Prompt**:
        *   "Ý nghĩa có **chính xác 100%** so với gốc không?" (Ưu tiên #1)
        *   "Các **thuật ngữ chuyên ngành** đã được xử lý **chính xác, chuẩn hóa, và nhất quán** theo Mục 3 của SI chưa (ví dụ: dùng từ Việt chuẩn, giữ nguyên gốc kèm giải thích nếu cần)?" (Ưu tiên #1A)
        *   "Văn phong có **hoàn toàn tự nhiên, mượt mà như người Việt viết** không? Còn chút gượng gạo nào không?" (Ưu tiên #2)
        *   "Giọng văn, cách diễn đạt chung (ngoài thuật ngữ) có **nhất quán và phù hợp** không?"
        *   "Bố cục HTML có **rõ ràng, dễ đọc, không bị lỗi hiển thị** (chồng chéo, tràn, ẩn...) không?" (Ưu tiên #3)
        *   "Kích thước font chữ của **nội dung chính** có **đảm bảo dễ đọc** không (ví dụ: ít nhất 14px-16px)? Đã ưu tiên yếu tố này hơn việc chỉ sao chép font nhỏ từ PDF chưa?"
        *   "Layout và định dạng có được bảo toàn ở mức **hợp lý và tốt nhất có thể** mà không gây lỗi không?" (Ưu tiên #4)
        *   "Cấu trúc HTML (thẻ ngữ nghĩa, heading, list, table...) có **phản ánh đúng logic** của tài liệu gốc và **tuân thủ accessibility cơ bản** không?"
        *   "Hình ảnh (`<img>`) có được xử lý đúng cách với **`alt` text tiếng Việt ý nghĩa** không?"
        *   "Bảng biểu (`<table>`) có **cấu trúc ngữ nghĩa đúng** và dễ hiểu không?"
        *   "Các yếu tố đặc biệt (text trong ảnh, cột, header/footer) đã được xử lý **đúng theo chỉ dẫn** chưa?"
        *   "Phần Tài liệu Tham khảo (References) đã được xử lý đúng cách chưa? Các yếu tố cốt lõi (tác giả, tiêu đề, tạp chí, DOI, URL...) có được **giữ nguyên gốc 100%** không? Chỉ các ghi chú của tác giả gốc (nếu có) mới được dịch?"
            *   "Định dạng (đậm, nghiêng, list) và các liên kết (DOI/URL) trong References có được **bảo toàn chính xác** không?"
    *   **Nếu phát hiện bất kỳ vấn đề nào (đặc biệt về độ tự nhiên, lỗi hiển thị, cấu trúc sai, thiếu alt text, xử lý sai thuật ngữ...)**: **BẮT BUỘC phải sửa lại** trực tiếp trong HTML. Tái cấu trúc bản dịch thêm nữa nếu cần, điều chỉnh CSS, đơn giản hóa layout/bảng nếu cần, bổ sung/sửa `alt` text, sửa lại thuật ngữ, cho đến khi **hoàn toàn hài lòng** về mọi mặt theo đúng thứ tự ưu tiên. **Đừng ngại thay đổi đáng kể so với lần tạo mã đầu tiên.**
5.  **Kiểm tra Kỹ thuật Cuối**: Đảm bảo mã HTML cơ bản hợp lệ, không có lỗi cú pháp và chỉ chứa mã HTML.

---
**Định dạng Output Cuối cùng:** **Chỉ trả về mã HTML thô.** Output BẮT ĐẦU bằng `<!DOCTYPE html>` và KẾT THÚC bằng `</html>`. **(LƯU Ý: Đừng quên nhúng script CDN của MathJax vào thẻ `<head>` để render công thức toán).** Hãy đảm bảo kết quả cuối cùng thể hiện năng lực tốt nhất của bạn dựa trên những chỉ dẫn cực kỳ chi tiết này.