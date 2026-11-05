# AI Log

Tệp này ghi lại các thay đổi lớn do AI thực hiện trong dự án để tiện theo dõi và nạp lại ngữ cảnh khi tiếp tục công việc.

## Quy ước ghi log

Chỉ thêm mục khi có thay đổi lớn ảnh hưởng đến chức năng, cấu trúc, giao diện chính hoặc tài liệu quan trọng. Mỗi mục nên ghi ngày, nội dung thay đổi, các tệp liên quan và kết quả kiểm tra. Khi tiếp tục làm việc sau một thay đổi lớn, đọc lại tệp này để nắm ngữ cảnh trước khi chỉnh sửa.

## Lịch sử thay đổi

### 2026-11-05 — Bổ sung release note v1.0

- **Nội dung:** Tạo release note phiên bản v1.0, gồm ngày phát hành, chức năng mới, lỗi đã sửa và hạn chế còn tồn tại.
- **Tệp liên quan:** `docs/RELEASENOTE.md`
- **Kiểm tra:** `git diff --check` hoàn tất, không phát hiện lỗi định dạng.

### 2026-11-05 — Tạo báo cáo kiểm thử trước bàn giao

- **Nội dung:** Tạo báo cáo kiểm thử gồm sáu nhóm tiêu chí, checklist trạng thái, minh chứng rà soát tĩnh và đề xuất trước bàn giao. Các kiểm thử trình duyệt/triển khai chưa thực hiện được đánh dấu cần cải thiện.
- **Tệp liên quan:** `docs/test_report.md`
- **Kiểm tra:** Xác nhận đủ sáu nhóm tiêu chí, đủ ba trạng thái và không có khoảng trắng cuối dòng.

### 2026-11-05 — Bổ sung minh chứng kiểm thử responsive

- **Nội dung:** Chụp giao diện ở viewport giả lập mobile (390 × 844), tablet (834 × 1112) và desktop (1440 × 1000); cập nhật báo cáo kèm liên kết và kết quả kiểm tra số cột, chiều rộng tài liệu, tải ảnh.
- **Tệp liên quan:** `docs/test_report.md`, `docs/screenshots/responsive-mobile.png`, `docs/screenshots/responsive-tablet.png`, `docs/screenshots/responsive-desktop.png`
- **Kiểm tra:** Ba ảnh PNG đã được xác nhận tồn tại; lưới dự án hiển thị lần lượt 1/2/3 cột, không phát hiện tràn chiều rộng tài liệu hoặc ảnh lỗi trong các viewport đã kiểm tra.

### 2026-11-05 — Nâng cấp giao diện hiện đại và bổ sung hiệu ứng animation

- **Nội dung:** Tái thiết kế toàn diện giao diện Portfolio theo phong cách Modern UI & Glassmorphism: tích hợp font Plus Jakarta Sans, hệ màu Indigo & Cyan, huy hiệu trạng thái nhấp nháy (pulse), avatar bay bổng với hào quang (floating + glow), hiệu ứng phóng to ảnh dự án khi hover, thẻ kỹ năng sinh động kèm icon SVG, bố cục liên hệ 2 cột, và nâng cấp khối keyframes animation `.box` chuyển động 4 góc vô tận kèm biến dạng hình khối và đổi dải màu mượt mà.
- **Tệp liên quan:** `index.html`, `assets/css/styles.css`
- **Kiểm tra:** `git diff --check` hoàn tất không lỗi định dạng; bảo toàn đầy đủ các thẻ ngữ nghĩa HTML5, cấu trúc Flexbox/Grid, selector bài tập và khả năng responsive mobile-first.

### 2026-11-05 — Tăng cường màu sắc nổi bật và bổ sung hiệu ứng đom đóm bay

- **Nội dung:** Bổ sung hiệu ứng 15 đom đóm bay lơ lửng phát sáng lung linh (Pure CSS Fireflies với đa quỹ đạo `fireflyFloat` và nhịp thở phát quang `fireflyGlow`); tăng cường phối màu nổi bật với dải gradient hoàng hôn (Sunset Gradient) trên tiêu đề, hiệu ứng cực quang mờ (Aurora orbs) ở Hero, viền màu gradient nhận diện riêng cho từng dự án (Gemini, TikTok, Spotify), màu đặc trưng khi hover cho từng chip kỹ năng và mạng xã hội.
- **Tệp liên quan:** `index.html`, `assets/css/styles.css`
- **Kiểm tra:** `git diff --check` hoàn tất không phát hiện lỗi định dạng; hiệu ứng đom đóm sử dụng `pointer-events: none` không cản trở thao tác chuột; tự động ẩn khi kích hoạt `prefers-reduced-motion`.

### 2026-11-05 — Chuyển khối Animation lên khu vực Dự án và đồng bộ màu viền

- **Nội dung:** Di chuyển khối animation showcase (`.animation-showcase`, `.demo-stage`, `.box`) từ section Liên hệ lên nằm ngay dưới 3 thẻ trong section "Dự án tiêu biểu"; đồng bộ hóa màu 2 đường viền trên/dưới của section Dự án (`border-top` & `border-bottom` dùng chung `var(--color-border-subtle)` mềm mại); tinh chỉnh màu sắc các dải viền accent trên đầu các thẻ dự án và khối animation showcase theo gam màu chủ đạo hài hòa, liền mạch.
- **Tệp liên quan:** `index.html`, `assets/css/styles.css`
- **Kiểm tra:** `git diff --check` hoàn tất; cấu trúc section Dự án và Liên hệ hiển thị cân đối, không phát hiện lỗi vỡ layout.