# Changelog

Tất cả những thay đổi đáng chú ý của dự án kiencang/SI-Prompt-EV-Translate sẽ được ghi lại trong file này.

Định dạng dựa trên [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
và dự án này tuân thủ [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Riêng các chỉnh sửa nhỏ không liên quan đến code, như chỉnh sửa hướng dẫn sử dụng, đưa thêm các file ví dụ, v.v.. sẽ có thêm đuôi .ndc đằng sau để phân biệt.

Ví dụ phiên bản `v1.3.31.ndc` có nghĩa là phần code giống hệt phiên bản `v1.3.31`, chỉ có một số thông tin khác, không ảnh hưởng đến chức năng chính.

## [v1.3.46] - 2026-08-06
### Fixed
- Cập nhật cho cả phase1 phần xử lý ảnh vector (v1.3.45 chỉ mới cập nhật 3 kiểu dịch đầu tiên);

## [v1.3.45] - 2026-08-06
### Fixed
- Cập nhật các prompt để nó xử lý ảnh vector tốt hơn;
- Phân biệt rõ ảnh raster và vector. Ảnh raster được công cụ tách ra khỏi file PDF và chèn vào bản dịch, còn ảnh vector được AI vẽ lại bằng HTML, CSS;
- Với sơ đồ, biểu đồ vector đặc thù toán học thì có chỉ thị xử lý riêng;

## [v1.3.44] - 2026-07-22
### Fixed
- Cập nhật để các SI đồng bộ với prompt;

## [v1.3.43] - 2026-07-16
### Fixed
- Điều chỉnh prompt của phase2 để nó phù hợp hơn, vì phase2 không cần gửi ảnh base64 cho AI nữa, chỉ cần giữ nguyên placeholder trong bản dịch để khi dịch xong thay thế lại là ổn.

## [v1.3.42] - 2026-07-16
### Fixed
- Thêm phần xử lý ảnh, để chèn placeholder của ảnh vào bản dịch.

## [v1.3.41] - 2026-04-15
### Fixed
- Điều chỉnh SI phase 2 phần CSS có thể bổ sung thêm.

## [v1.3.40] - 2026-04-15
### Fixed
- Điều chỉnh SI phase 2 để tránh dài dòng.

## [v1.3.39] - 2026-04-15
### Fixed
- Cải tiến, loại bỏ lặp thông tin thừa trong SI phase 1.

## [v1.3.38] - 2026-04-14
### Fixed
- Đổi tên file trong `refine` để tránh hiểu nhầm ý nghĩa.
- Xóa các biến thể không cần thiết cho `refine` và `pdf2html`. (Về lý thuyết các biến thể có thể cần, nhưng thực tế rất hiếm khi dùng, chỉ giữ lại ví dụ về glossary cho file master).
- Chỉnh hướng dẫn sử dụng để phù hợp hơn.

## [v1.3.37] - 2026-04-14
### Fixed
- Đưa thẻ xml vào để nhóm riêng các chỉ thị liên quan.
- Loại bỏ việc tab và space lần lộn. Thống nhất về space. 4 space thụt lề tiêu chuẩn.
- Sửa một lỗi trùng lặp trong prompt do trước đây sơ ý.

## [v1.3.36] - 2026-04-09
### Fixed
- Làm gọn lại các ví dụ liên quan đến tạo SVG. Tránh làm loãng SI.
- Điều chỉnh chỉ thị liên quan đến footet/header của PDF để tránh nó làm gãy luồng đọc.

## [v1.3.34] - 2026-04-08
### Fixed
- Tinh chỉnh prompt liên quan đến phần dịch có ký hiệu toán học, nhằm đẩy cao mức độ thống nhất của bản dịch, tránh AI hiểu nhầm ý định.

## [v1.3.33] - 2026-04-07
SI/Prompt chính của repo không thay đổi.
### Removed
- Loại bỏ Prompt tạo app vì không cần thiết / Đã đưa sang repo khác.

### Fixed
- Cập nhật link app tiện dùng luôn vào hướng dẫn sử dụng.

## [v1.3.32] - 2026-04-06
SI/Prompt chính của repo không thay đổi.
### Added
- Bổ sung khả năng tạo ra một ứng dụng riêng trên Gemini nếu muốn.
- Các file cần thiết để làm điều này nằm trong build_an_app.

## [v1.3.31.ndc] - 2026-04-03
### Fixed
- Đưa các ví dụ file dịch vào thư mục examples cho gọn.
- Điều chỉnh hướng dẫn sử dụng (README.md).

## [v1.3.31] - 2026-04-02
### Fixed
- Tinh chỉnh SI & prompt cho glossary_ext

## [v1.3.29] - 2026-04-02
### Fixed
- Thêm CHANGELOG
- Chỉnh một chút SI cho glossary_ext
