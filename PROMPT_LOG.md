# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Trần Gia Thịnh
- **MSSV:** 125000948
- **Tên đề tài Website:** TechVibe Store – cửa hàng công nghệ
- **Công cụ AI đã sử dụng:** ChatGPT
- **Ghi chú:** Nội dung dưới đây là bản nháp dựa trên cấu trúc website hiện có. Hãy chỉnh lại các prompt, kết quả và sự cố cho đúng với quá trình bạn thực sự đã làm, không ghi nhận những thao tác chưa diễn ra.

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> Hãy xây dựng một website bán hàng công nghệ tên TechVibe Store bằng HTML5 và CSS3. Giao diện theo phong cách công nghệ hiện đại, nền tối, điểm nhấn neon xanh cyan và hồng. Trang cần có header, thanh điều hướng, hero giới thiệu, danh sách sản phẩm, khu vực khuyến mãi, cam kết cửa hàng, câu hỏi thường gặp, đăng ký nhận tin và footer. Dùng các thẻ semantic HTML5 phù hợp, CSS Variables trong :root, Flexbox/Grid và thiết kế responsive. Tích hợp Animate.css cho phần tiêu đề/hero, hiệu ứng hover/focus cho nút và thẻ sản phẩm. Tách HTML và CSS thành index.html và style.css.

## 2. Quá trình tinh chỉnh & giải quyết sự cố (Iteration)

### Lần 1: Dựng khung Semantic HTML và CSS Variables

- **Prompt đã dùng (mẫu):** Hãy kiểm tra cấu trúc HTML hiện tại. Giữ lại thiết kế, nhưng bảo đảm có `header`, `nav`, `main`, `section`/`article` và `footer` đúng ngữ nghĩa. Hạn chế dùng `div` cho các khối có ý nghĩa nội dung. Trong CSS, dùng biến trong `:root` để quản lý màu sắc, font chữ và kích thước chung. Bố cục sản phẩm cần dùng CSS Grid và hiển thị tốt trên màn hình nhỏ.
- **Kết quả trong mã hiện tại:** Website đã có `header`, `nav`, `main`, nhiều `section`, các thẻ `article` cho sản phẩm và `footer`. CSS có các biến màu, font, container và hiệu ứng; các khu vực chính sử dụng Grid/Flexbox.
- **Nhận xét và tinh chỉnh:** Cần tự kiểm tra ở trình duyệt trên cả máy tính và điện thoại. Nếu có khối `div` chỉ dùng để bao nội dung, có thể giữ khi cần cho mục đích layout; không nên thay thẻ một cách máy móc nếu làm hỏng cấu trúc.

### Lần 2: Tích hợp Animate.css và AOS

- **Prompt đã dùng (mẫu):** Giữ các hiệu ứng Animate.css đang dùng ở phần hero. Tích hợp thư viện AOS bằng CDN, thêm thuộc tính `data-aos` cho các khu vực cần xuất hiện khi cuộn và gọi `AOS.init()` sau khi tài liệu tải xong. Chọn hiệu ứng nhẹ, chạy một lần và không gây rối mắt.
- **Kết quả sau khi hoàn thiện:** `index.html` nạp Animate.css và AOS CSS/JavaScript từ CDN. Các phần tử có lớp `reveal` được thêm `data-aos="fade-up"`; AOS được khởi tạo khi DOM đã sẵn sàng.
- **Thách thức cần kiểm tra:** Nếu hiệu ứng cuộn không chạy, kiểm tra kết nối Internet/CDN, bảng Console trong Developer Tools, đường dẫn thư viện và xem phần tử có `data-aos` hay chưa.
- **Debug prompt (mẫu):** Hãy kiểm tra vì sao AOS không chạy. Xác nhận tệp AOS CSS và JavaScript được nạp thành công, `AOS.init()` chạy sau khi DOM tải xong, và phần tử cần hiệu ứng có `data-aos`. Không viết lại toàn bộ giao diện; chỉ sửa phần gây lỗi.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

### AI đã giúp tiết kiệm thời gian ở phần nào nhất?

AI hỗ trợ lên bố cục trang, đề xuất phối màu, tạo các quy tắc CSS và gợi ý cách tích hợp thư viện hiệu ứng. Nhờ đó, quá trình dựng giao diện ban đầu nhanh hơn. Tuy nhiên, mã do AI tạo vẫn cần được đọc, chạy thử và chỉnh sửa.

### Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?

Prompt nên nêu rõ mục tiêu, cấu trúc HTML, phong cách giao diện, yêu cầu responsive và giới hạn cần giữ nguyên. Khi sửa lỗi, nên mô tả hiện tượng cụ thể và yêu cầu chỉ chỉnh phần liên quan. Sau mỗi lần AI sửa mã, cần kiểm tra lại giao diện và chức năng thực tế thay vì mặc định rằng mã đã đúng.
