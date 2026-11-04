# Portfolio CV - Đinh Văn Hải

Trang portfolio cá nhân giới thiệu Đinh Văn Hải và các kỹ năng, dự án Frontend. Giao diện được xây dựng dưới dạng website tĩnh, có bố cục responsive cho điện thoại, máy tính bảng và máy tính để bàn.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Hiển thị các kỹ năng: HTML5, CSS3, Flexbox, Grid, JavaScript, responsive design, Git/GitHub và Figma.
- Trưng bày các dự án mẫu: Gemini, ứng dụng TikTok và ứng dụng nghe nhạc.
- Điều hướng nhanh đến phần giới thiệu, kỹ năng, dự án và liên hệ.
- Cung cấp liên kết mạng xã hội và biểu mẫu giao diện minh họa.
- Hiển thị hiệu ứng CSS và bố cục tự điều chỉnh theo kích thước màn hình.

> Đây là website tĩnh để giới thiệu và minh họa giao diện. Biểu mẫu đăng nhập chưa kết nối máy chủ, nút gửi và các liên kết “Xem chi tiết” chưa thực hiện chức năng gửi dữ liệu hoặc mở trang dự án.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid, responsive và animation.
- JavaScript: được liệt kê trong phần kỹ năng của portfolio; trang hiện tại không cần JavaScript để chạy.
- Python hoặc Docker/Nginx: tùy chọn để chạy máy chủ web cục bộ.

## Cấu trúc dự án

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
│       ├── dvh.jpg
│       ├── gmn.png
│       ├── spf.png
│       └── tt.png
└── README.md
```

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài thư viện hay chạy bước biên dịch.
- Để chạy máy chủ cục bộ: Python 3 (tùy chọn).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động (tùy chọn).

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở terminal tại thư mục dự án. Ví dụ:

```bash
git clone https://github.com/haivip-08/My-CV.git
cd My-CV
```

Nếu đã có mã nguồn trên máy, chỉ cần mở terminal tại thư mục chứa `index.html`. Dự án không có bước cài đặt dependencies.

## Cấu hình và tùy chỉnh

Website hiện không sử dụng tệp cấu hình, biến môi trường hay dịch vụ backend.

- Sửa nội dung, thông tin liên hệ và liên kết dự án trong `index.html`.
- Sửa màu sắc, bố cục, breakpoint và hiệu ứng trong `assets/css/styles.css`.
- Thay ảnh trong `assets/img/`; nếu đổi tên hoặc vị trí ảnh, cập nhật đường dẫn tương ứng trong `index.html`.
- Không nhập thông tin nhạy cảm vào biểu mẫu: biểu mẫu hiện chỉ là giao diện minh họa và không gửi dữ liệu đến máy chủ.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử:

```powershell
python -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

> Nếu cổng `8000` đã được sử dụng, thay `8000` trong lệnh bằng một cổng khác, chẳng hạn `8080`, rồi truy cập đúng cổng đó.

### Mở trực tiếp

Cũng có thể mở `index.html` trực tiếp bằng trình duyệt. Chạy qua HTTP server được khuyến nghị để mô phỏng cách website được phục vụ trên web.

## Chạy bằng Docker

Cần cài và khởi động Docker trước. Các lệnh dưới đây dùng ảnh Nginx chính thức, gắn thư mục dự án ở chế độ chỉ đọc và phục vụ trang tại cổng `8080`.

#### Windows PowerShell

Chạy tại thư mục dự án:

```powershell
docker run --rm -d --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

#### macOS và Linux

Chạy tại thư mục dự án:

```bash
docker run --rm -d --name my-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, mở <http://localhost:8080>. Dừng container bằng:

```bash
docker stop my-cv
```

## Thông tin liên hệ

- GitHub: [github.com/haivip-08](https://github.com/haivip-08)
- Instagram: [@_dinhhai08_](https://www.instagram.com/_dinhhai08_/)
- Facebook: [Trang Facebook](https://www.facebook.com/share/1CLcLUSBoJ/)

## Bản quyền

© 2026 Đinh Văn Hải.
