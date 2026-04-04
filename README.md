# SI-Prompt-PDF-EV-Translate

> **Cung cấp System Instructions (SI) và Prompt chất lượng cao chuyên dụng cho nhiệm vụ dịch thuật tài liệu khoa học (định dạng PDF) từ tiếng Anh sang tiếng Việt.**

Dự án này cung cấp bộ khung hướng dẫn tối ưu giúp AI xử lý các văn bản học thuật có độ phức tạp cao, đảm bảo độ chính xác về thuật ngữ và bảo toàn định dạng tốt nhất có thể.

--

Dịch giả Cưu-ma-la-thập chuyên dịch kinh sách Phật từ tiếng Phạn sang tiếng Hán được cho là từng nói đại ý thế này:

> Dịch giống như đút cho người khác đồ ăn đã nhai rồi, điều đó vừa làm đồ ăn mất hết mùi vị và còn gây cảm giác kinh tởm nữa!

Điều này nếu suy nghĩ kỹ thì có 2 hướng:

- Người đọc, nếu có khả năng, tốt nhất nên học ngoại ngữ để đỡ phải 'ăn cơm nhai lại'.
- Người/công cụ dịch, khi làm nhiệm vụ này thì phải cố gắng tối đa để 'đồ ăn còn vị' & giảm thiểu 'cảm giác kinh tởm'.

'Đồ ăn còn vị' tôi nghĩ là hàm ý rằng những cái hay, thú vị của văn bản gốc phải được truyền lại trọn vẹn trong bản dịch (hoặc ít nhất là càng nhiều càng tốt).

'Cảm giác kinh tởm' thì tôi nghĩ là bản dịch phải tối thiểu hóa việc đưa 'cá tính riêng' vào bản gốc, dù dịch (kể cả dịch máy) bao giờ cũng mang ảnh hưởng ít nhiều của cá tính người/công cụ dịch.

Tôi sẽ cố gắng để công cụ này làm được nhiệm vụ đó!

--

**Lưu ý cần phải đọc**: 

- Dịch máy chỉ nên áp dụng khi bạn không thể thuê dịch thuật viên chất lượng cao, đặc biệt thận trọng khi áp dụng dịch máy với các tài liệu quan trọng.
- Bất kể dịch máy có chất lượng tốt đến đâu, bạn vẫn cần xem xét nó, do vậy bạn nên có tiếng Anh cơ bản để khi cần có thể kiểm tra.
- Cùng một SI/prompt nhưng chất lượng đầu ra thường khác nhau, và đôi khi khác nhau đáng kể! (giống anh em sinh đôi khi trưởng thành vậy). Do đó có một mẹo hơi mất thời gian chút để có bản dịch hay là cho AI dịch lại, và bạn sẽ chọn đọc bản nào chất lượng nhất.
- Kết quả dịch sẽ được lưu ở định dạng web (html) và bất cứ trình duyệt nào cũng có thể đọc được. Ngoài ra nó có thể đọc được trên nhiều kích cỡ màn hình khác nhau, nhưng được tối ưu cho kích cỡ màn hình lớn (laptop/desktop).

---

## Về bản tiêu chuẩn:

- Bản tiêu chuẩn: Nằm ngay ngoài thư mục chính, gồm `prompt.md` & `system_instructions.md`
- Bản tiêu chuẩn có một phiên bản khác là đưa thêm từ chuyên ngành vào prompt (để cải thiện chất lượng dịch), lúc đó prompt mới cần dùng sẽ là `prompt_glossary.md`
- Để trích xuất được danh sách từ chuyên ngành thì dùng SI/prompt nằm trong thư mục `glossary_ext` (là `prompt_glossary_ext` và `system_instructions_glossary_ext`).

Bản tiêu chuẩn là các nhanh để bạn dịch file PDF, khi đã làm quen một chút với nó bạn nên sử dụng các Tùy chọn khác như `refine` (tinh chỉnh SI/prompt) hoặc `pdf2html` (chia giai đoạn dịch) để hiệu quả dịch được cao hơn. Các hướng dẫn chi tiết sẽ có ở các phần sau của hướng dẫn này.

---

## 📚 Xem thử chất lượng

Ví dụ về chất lượng dịch của bộ SI/prompt này (bản tiêu chuẩn), bạn có thể xem khả năng của nó khi dịch khoảng 10 trang mở đầu trong cuốn **Book Of Proofs** của **Richard Hammack**:

- Bản tiếng Anh: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/examples/Book-Of-Proofs-2-en.pdf
- Bản dịch tiếng Việt: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/examples/Book-Of-Proofs-2-vi.pdf

---

## 🚀 Tại sao nên sử dụng với Gemini AI Studio?

Việc kết hợp bộ SI/prompt này với **Gemini AI Studio** (https://aistudio.google.com/) mang lại nhiều lợi thế vượt trội:

* **Tối ưu hóa hệ sinh thái:** Công cụ được tinh chỉnh và kiểm tra kỹ lưỡng trên model Gemini.
* **Tiết kiệm chi phí:** Hạn mức miễn phí rộng rãi, phù hợp cho nhu cầu dịch thuật cá nhân mà hầu như không phát sinh phí. Đăng ký nhanh chóng, không gặp rào cản. Tôi ước chừng mức độ miễn phí tương đương với khoảng 20 trang PDF/ngày, thường là đủ cho đa số trường hợp.
* **Tùy chỉnh chuyên sâu:** Cung cấp nhiều thiết lập nâng cao và dễ dàng tùy chỉnh qua giao diện dễ hiểu. Ví dụ điều chỉnh Temperature / Mức độ sáng tạo (nên để từ 0.3 đến 0.5 thay vì mặc định 1 / Sẽ được hướng dẫn kỹ khi thao tác cụ thể), hay chỉnh Thinking level / Mức độ suy luận trước khi đưa ra câu trả lời (với suy luận nên để là `Hight` như mặc định, vì dịch rất phức tạp).
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
3. Một lưu ý nhỏ giúp việc dịch file PDF hiệu quả hơn là nên cắt đi những nội dung không quan trọng trong file PDF trước khi gửi (ví dụ các trang trắng dư thừa, bìa dạng ảnh chụp, các mục lục tham khảo thường giữ nguyên không cần dịch, v.v..).

---

## ⚡ Lưu ý kỹ thuật quan trọng khác

* **Thời gian xử lý:** Do tính chất phức tạp của tài liệu khoa học, thời gian hoàn thành có thể dao động từ **150s đến 600s** tùy độ dài file.
* **Định dạng đầu ra:** Kết quả trả về ở dạng **mã HTML**.
    * 💡 *Lời khuyên:* Mở ứng dụng Notepad trên Windows (hoặc TextEdit trên Mac), dán đoạn mã vào, chọn File -> Save As. Tại mục 'Save as type' chọn 'All Files', và đặt tên file có đuôi `.html` (Ví dụ: `bandich.html`). Sau đó click đúp vào file để mở bằng trình duyệt. Xem hình bên dưới để rõ hơn cách làm.

<p align="center">
  <img src="images/paste-notepad.png" alt="Copy - Paste vào NotePad">
   <br><em>Copy - Paste mã nguồn vào NotePad</em>
</p>

--

<p align="center">
  <img src="images/luu-file-html.png" alt="Lưu file dưới định dạng html">
   <br><em>Lưu file dưới định dạng .html</em>
</p>

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

# ✅ Các tùy chọn

Người dùng ngoài việc dùng bản tiêu chuẩn, bạn có thể sử dụng thêm một trong các tùy chọn dưới đây khi dịch tài liệu PDF từ Anh sang Việt.

Các bản tùy chỉnh *khi được dùng phù hợp* thường *cho chất lượng dịch cao hơn đáng kể* so với bản tiêu chuẩn, rất khuyên bạn tìm hiểu để dùng.

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

### 📝 Nâng cao thêm chất lượng dịch với danh sách từ chuyên ngành bổ sung vào prompt

Phần này là tùy ý. Không bắt buộc sử dụng. Nhưng khuyên dùng vì thường cải thiện chất lượng dịch, đặc biệt trên tài liệu dài hoặc khó (hoặc cả hai).

Mặc định SI/prompt mẫu là tương đối tốt để xử lý các tài liệu chuyên ngành. Tuy nhiên nếu bạn muốn cải thiện hơn nữa chất lượng dịch thì hãy sử dụng bộ SI/prompt trong thư mục **`glossary_ext`** để trích xuất cách dịch chuyên ngành & các từ cốt lõi trong tài liệu.

Vào thư mục đó bạn sẽ thấy các file `prompt_glossary_ext` & `system_instructions_glossary_ext` dùng để trích xuất cách dịch từ chuyên ngành.

Khi đẩy lên AI, cũng nên để **Temperature thấp**, thường là **0.3**

PS: Riêng với trích xuất từ chuyên ngành, có thể bật thêm tính năng `Grounding with Google Search` trong AI Studio để nó có khả năng phân tích sâu hơn các từ khó thông qua việc tìm kiếm.

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

Ví dụ kết quả đầu ra khi chạy SI/prompt trích xuất từ chuyên ngành, cốt lõi của một tài liệu khoảng 12 trang:

```
**B**
- behavioral theory: lý thuyết hành vi

**C**
- cognitive burden: gánh nặng nhận thức
- concentrated urban disadvantage: bất lợi đô thị tập trung
- culture of poverty: văn hóa nghèo đói

**D**
- deindustrialization: phi công nghiệp hóa
- demographic context: bối cảnh nhân khẩu học
- disciplining institution: thể chế kỷ luật

**E**
- economic development: phát triển kinh tế
- endogeneity problem: vấn đề nội sinh

**F**
- female labor force participation: sự tham gia lực lượng lao động của nữ giới

**H**
- housing displacement: sự dịch chuyển chỗ ở

**I**
- incarceration: sự giam giữ
- incentive: động cơ
- income distribution: phân phối thu nhập
- institution: thể chế
- institutionalized power: quyền lực được thể chế hóa

**L**
- labor market context: bối cảnh thị trường lao động

**M**
- market inefficiency: sự kém hiệu quả của thị trường
- moral hazard: rủi ro đạo đức

**N**
- neighborhood effect: hiệu ứng khu dân cư

**P**
- path dependency: sự phụ thuộc đường dẫn
- political theory: lý thuyết chính trị
- poverty trap: bẫy nghèo
- power relation: quan hệ quyền lực
- power resources theory: lý thuyết nguồn lực quyền lực
- present bias: thiên kiến hiện tại

**R**
- relational perspective: quan điểm quan hệ
- residential segregation: sự phân biệt nơi cư trú

**S**
- single motherhood: làm mẹ đơn thân
- skills mismatch: sự không khớp về kỹ năng
- social policy: chính sách xã hội
- spatial mismatch: sự không khớp về không gian
- status attainment: đạt được địa vị
- structural theory: lý thuyết cấu trúc
- structural violence: bạo lực cấu trúc

**U**
- upward mobility: di động xã hội lên trên

**W**
- welfare dependency: sự phụ thuộc vào phúc lợi
- welfare state: nhà nước phúc lợi
- working poverty: nghèo đói ở người có việc làm
```

--

## 🔄 SI và prompt bản chia phase theo từng giai đoạn | Tùy chọn 2

Trong thư mục `pdf2html` chứa các SI & prompt được tinh chỉnh theo từng bước xử lý chứ không gộp chung như SI/prompt tiêu chuẩn.

Nó gồm 2 cặp SI/prompt sau:

- `phase_1`: Để chuyển file PDF thành HTML. Lưu kết quả của phase 1 để làm đầu vào của phase 2. Khi xử lý nên để **Temperature 0.3**
- `phase_2`: Tập trung vào nhiệm vụ dịch. Khi xử lý nên để **Temperature 0.5**

Tùy chọn này có khả năng cải thiện chất lượng dịch lên đáng kể (nhất là với file PDF cấu trúc phức tạp), vì nó giúp AI tránh bị quá tải chỉ thị như khi dùng bản tiêu chuẩn (dù đã dùng model tiên tiến nhất). Tuy nhiên nó sẽ khiến bạn mất thời gian và cả tốn Token hơn (thường là gấp đôi so với bản tiêu chuẩn) để tạo ra bản dịch hoàn chỉnh.

Ví dụ kết quả dịch bằng tùy chọn này: https://github.com/kiencang/SI-Prompt-EV-Translate/blob/main/examples/Book-Of-Proofs-2-vi-phase.pdf

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
