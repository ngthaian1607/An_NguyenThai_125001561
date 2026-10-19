# SpendWise - Ứng dụng Quản lý Chi tiêu Cá nhân

## 1. Thông tin sinh viên
- **Họ và tên:** Nguyễn Thái An
- **MSSV:** 125001561
- **Lớp:** 25CT113
- **Môn học:** Thiết kế Web

## 2. Mô tả dự án
SpendWise là một Landing Page giới thiệu ứng dụng di động quản lý tài chính thông minh. Giao diện được thiết kế tối ưu hóa nhằm phục vụ nhu cầu kiểm soát thu chi của mọi người dùng phổ thông trong đời sống hàng ngày, giúp bất kỳ ai cũng có thể dễ dàng xây dựng thói quen tài chính vững vàng. Dự án áp dụng triệt để tư duy Mobile First, hệ thống Design System chuẩn mực và hoàn toàn không phụ thuộc vào JavaScript để đảm bảo hiệu năng tối đa.

## 3. Công nghệ sử dụng
- **Cấu trúc:** Semantic HTML5 (Tối ưu SEO & Accessibility).
- **Giao diện & Bố cục:** CSS3 thuần (CSS Variables, Flexbox, CSS Grid).
- **Hiệu ứng & Tương tác (Zero JS):** 
  - CSS Animations (`@keyframes`, `transition`).
  - CSS Scroll Timeline (`@supports (animation-timeline: scroll())`).
  - CSS Checkbox Hack (`:has(:checked)`) cho tính năng Dark Mode.
  - Thư viện Animate.css.
- **Công cụ hỗ trợ (Vibe Coding):** Antigravity IDE, Gemini 3.8 Flash High.

## 4. Hướng dẫn chạy dự án (Live Demo)
- **Link Live Preview (GitHub Pages):** [Trải nghiệm SpendWise tại đây](https://ngthaian1607.github.io/An_NguyenThai_125001561/)

## 5. Danh sách Prompt "Đắt giá" nhất (Vibe Coding)
Dưới đây là 3 câu lệnh AI hiệu quả nhất đã được sử dụng để vượt qua các giới hạn kỹ thuật khắt khe (chỉ dùng HTML/CSS):
1. **Xử lý Dark Mode không cần JS:** *"Thêm tính năng Dark Mode bằng CSS thuần: Dùng thẻ `<input type="checkbox" hidden>` và bộ chọn CSS `:has(:checked)` trên thẻ body để ghi đè các biến CSS Variables sang bộ màu tối khi click. Không dùng thẻ `<script>`."*
2. **Tạo Scroll Progress Bar bằng CSS thuần:** *"Hãy tạo một thanh tiến trình cuộn trang dính chặt ở mép trên cùng màn hình. Bắt buộc sử dụng công nghệ CSS hiện đại `@supports (animation-timeline: scroll())` kết hợp `@keyframes` để thanh tự động dài ra từ 0% đến 100% dựa trên mức độ cuộn. Tuyệt đối không dùng JavaScript."*
3. **Hiệu ứng Card Flip 3D (UX nâng cao):** *"Áp dụng hiệu ứng Card Flip 3D thuần CSS cho các thẻ đánh giá. Sử dụng `transform-style: preserve-3d` và `backface-visibility: hidden` để thẻ xoay 180 độ lật mặt sau khi hover."*
