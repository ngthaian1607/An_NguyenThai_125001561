# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

**Họ và tên:** Nguyễn Thái An
**MSSV:** 125001561
**Tên đề tài Website:** Landing Page giới thiệu ứng dụng di động quản lý chi tiêu (SpendWise)
**Công cụ AI đã sử dụng:** Gemini 3.8 Flash High (Antigravity IDE)

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> *Hãy đóng vai một chuyên gia Front-end, viết cho tôi cấu trúc chuẩn Semantic HTML5 cho Landing Page giới thiệu ứng dụng di động quản lý chi tiêu cá nhân. Bắt buộc dùng các thẻ `<header>`, `<nav>`, `<main>`, `<section>`, và `<footer>`. Chia `<main>` thành 4 `<section>`: Hero, Tính năng, Đánh giá, và Tải app. Tuyệt đối chỉ viết HTML, không viết CSS, không dùng thẻ `<div>` vô nghĩa bao ngoài các vùng nội dung lớn.*

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung CSS Layout & CSS Variables
- **Prompt đã dùng:** 
> *Dựa trên cấu trúc HTML vừa tạo, hãy viết toàn bộ mã cho file style.css. Yêu cầu bắt buộc: 1. Sử dụng CSS Variables (trong :root) để khai báo ít nhất 3 biến: màu chủ đạo (primary), màu nền (background), và font chữ. 2. Sử dụng CSS Flexbox để dàn ngang thanh menu điều hướng (<nav>) và căn giữa các phần tử. 3. Sử dụng CSS Grid để dàn trang các khối tính năng và đánh giá thành 3 cột đều nhau trên màn hình lớn. 4. Giao diện sáng sủa, hiện đại, tuyệt đối không dùng JavaScript.*
- **Kết quả AI tạo ra:** CSS Variables được khai báo chuẩn, Flexbox và Grid dàn trang tốt trên Desktop.
- **Nhận xét & Tinh chỉnh của SV:** Layout đã thành hình nhưng thiếu hình ảnh minh họa thực tế khiến thuộc tính `alt` bị lộ. Tôi đã tự động thêm prompt yêu cầu AI chèn link ảnh từ Unsplash và Pravatar để UI trực quan hơn.

### Lần 2: Tích hợp Animate.css & Xử lý sự cố "Không dùng JS"
- **Prompt đã dùng:**
> *Bây giờ hãy nhúng thư viện Animate.css qua CDN vào thẻ `<head>`. Thêm class của Animate.css vào phần Hero. Thay vì dùng thư viện AOS cần JavaScript, hãy tự viết các hiệu ứng `:hover`, `:focus` và giả lập hiệu ứng xuất hiện (fade-in) bằng pure CSS (`@keyframes`, `transition`) cho các section bên dưới. Tuyệt đối không thêm thẻ `<script>` hay mã JS nào.*
- **Thách thức gặp phải:** Đề bài yêu cầu dùng thư viện AOS để tạo hiệu ứng cuộn trang, nhưng quy định của giảng viên trên lớp là chỉ dùng HTML/CSS thuần (không gọi `AOS.init()`).
- **Cách sửa prompt (Debug prompt):** Tôi đã ra lệnh cho AI tuyệt đối không dùng AOS, thay vào đó dùng CSS thuần với thuộc tính hiện đại `@supports (animation-timeline: view())` kết hợp Animate.css để giả lập hiệu ứng Scroll Reveal hoàn hảo mà không vi phạm luật cấm JS.

### Lần 3: Nâng cấp Micro-interactions & UI/UX (Nâng cao)
- **Prompt đã dùng:** 
> *Hãy nâng cấp tính năng web bằng CSS thuần (Tuyệt đối không dùng JS): 1. Tạo Dark Mode bằng Checkbox Hack (dùng `:has(:checked)`). 2. Áp dụng hiệu ứng Card Flip 3D (xoay 180 độ) cho các thẻ Đánh giá khi hover, dùng `transform-style: preserve-3d`. 3. Tạo thanh cuộn tiến trình (Scroll Progress Bar) dính ở mép trên cùng màn hình bằng `@keyframes` và `animation-timeline: scroll()`.*
- **Kết quả AI tạo ra:** Website trở nên cực kỳ chuyên nghiệp và sống động với hiệu ứng lật thẻ 3D, chế độ Dark Mode và thanh tiến trình cuộn trang.
- **Nhận xét & Tinh chỉnh của SV:** AI thực hiện xuất sắc các kỹ thuật CSS nâng cao. Đây là minh chứng cho việc nếu biết cách ra lệnh (Prompt Engineering), CSS thuần hoàn toàn có thể làm được những việc trước đây bắt buộc phải dùng JavaScript.

## 3. Đánh giá cá nhân về quá trình Vibe Coding
- **AI đã giúp tiết kiệm thời gian ở phần nào nhất?** AI giúp tôi rút ngắn 80% thời gian gõ các thẻ HTML lặp đi lặp lại và thiết lập khung layout Grid/Flexbox phức tạp. Việc căn chỉnh Breakpoints cho Responsive cũng được AI tính toán tỷ lệ rất nhanh.
- **Bài học rút ra khi đặt câu hỏi (Prompt):** Cần phải ra lệnh một cách chi tiết và áp đặt các giới hạn kỹ thuật rõ ràng. Nếu chỉ nói "làm web cho tôi", AI sẽ lạm dụng thẻ `<div>` và tự ý chèn JavaScript. Bằng cách thiết lập "biên giới" chặt chẽ (nhấn mạnh chuẩn Semantic, cấm thẻ Script), tôi có thể ép AI viết ra những đoạn mã sạch và tuân thủ đúng yêu cầu học thuật của môn học.