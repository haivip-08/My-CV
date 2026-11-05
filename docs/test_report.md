# BÁO CÁO KIỂM THỬ PHẦN MỀM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| **Tên dự án** | Portfolio CV - Đinh Văn Hải |
| **Phiên bản** | v1.0 |
| **Ngày kiểm thử** | 05/11/2026 |
| **Người thực hiện/đánh giá** | QA/QC - rà soát tĩnh mã nguồn và tài liệu; cần bổ sung người xác nhận trước khi bàn giao |
| **Phạm vi** | Website tĩnh trong repository: HTML, CSS, tài nguyên hình ảnh và tài liệu bàn giao |
| **Môi trường kiểm thử** | Trình duyệt tích hợp, mở trang từ `index.html`; viewport giả lập mobile 390×844, tablet 834×1112 và desktop 1440×1000 |
| **Phương pháp** | Đối chiếu yêu cầu/tài liệu, rà soát HTML/CSS và kiểm tra trực quan responsive bằng viewport giả lập; chưa kiểm thử trên thiết bị vật lý hoặc ma trận nhiều trình duyệt |

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ phạm vi kiểm tra đã thực hiện.
- **Chưa đạt:** Đã xác nhận có sai lệch hoặc chức năng không đáp ứng mô tả.
- **Cần cải thiện:** Đáp ứng một phần, còn hạn chế, hoặc chưa có minh chứng kiểm thử đủ để kết luận.

> Báo cáo này phản ánh rà soát tĩnh, không thay thế kiểm thử thực tế trên các trình duyệt và thiết bị mục tiêu. Những hạng mục chưa có minh chứng chạy thử được ghi là **Cần cải thiện**, không được hiểu là đã kiểm thử thành công.

## 2. Bảng tổng quan trạng thái

| STT | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các khu vực chính và điều hướng nội bộ có trong mã nguồn; liên kết dự án chưa hoạt động và tên hiển thị có lỗi gõ. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Đã chụp và kiểm tra responsive ở ba viewport; chưa kiểm thử thiết bị vật lý hoặc nhiều trình duyệt. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | README hướng dẫn chạy cục bộ và Docker; chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra lỗi tải tài nguyên. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy backend hay cấu hình bí mật theo tài liệu; biểu mẫu không gửi dữ liệu và liên kết mở tab mới cần được gia cố. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có README, release note và báo cáo; còn nội dung cần đồng bộ, dọn dẹp và xác nhận trước bàn giao. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã có ba ảnh responsive; chưa có kết quả kiểm thử triển khai và chức năng. |

## 3. Nội dung kiểm thử chi tiết

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ được khai báo | Đạt | Các section tương ứng có trong `index.html`. |
| Điều hướng nội bộ trỏ đến các khu vực chính | Đạt | Menu dùng các liên kết `#about`, `#skills`, `#projects`, `#contact`; cần xác nhận thao tác thực tế trên trình duyệt. |
| Nội dung tên cá nhân hiển thị chính xác và nhất quán | Chưa đạt | Tiêu đề hero trong `index.html` hiển thị “Đinh Văn Hảiii”, không khớp tên “Đinh Văn Hải” ở README và footer. |
| Liên kết “Xem chi tiết” mở đúng nội dung dự án | Chưa đạt | Các thẻ dự án dùng `href="#"`; README cũng ghi rõ chưa có trang dự án đích. |
| Biểu mẫu liên hệ/đăng nhập xử lý gửi thông tin | Cần cải thiện | Form có trường email `required`, nhưng dùng `action="#"` và không có dịch vụ backend; chỉ phù hợp minh họa, không xác nhận gửi dữ liệu. |
| Các nút gửi yêu cầu thực hiện đúng chức năng | Cần cải thiện | Hai nút nằm trong giao diện; một nút bị disabled và chưa thấy xử lý tương tác trong mã nguồn. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có bố cục responsive theo kích thước màn hình | Đạt | Đã kiểm tra viewport giả lập mobile/tablet/desktop; lưới dự án lần lượt hiển thị 1/2/3 cột. Ảnh: [mobile](screenshots/responsive-mobile.png), [tablet](screenshots/responsive-tablet.png), [desktop](screenshots/responsive-desktop.png). |
| Điều hướng, lưới dự án và nội dung có quy tắc co giãn | Đạt | Có Flexbox/Grid; trong lần kiểm tra, chiều rộng tài liệu bằng chiều rộng viewport và không phát hiện ảnh bị lỗi tải. |
| Có dấu hiệu focus cho thao tác bàn phím | Đạt | CSS khai báo `:focus-visible` với outline dễ nhận biết. |
| Tôn trọng tùy chọn giảm chuyển động của người dùng | Đạt | CSS có `prefers-reduced-motion: reduce` để tắt animation/transition và cuộn mượt. |
| Giao diện và điều hướng hiển thị đúng trên Chrome, Firefox, Edge, Safari | Cần cải thiện | README nêu trình duyệt mục tiêu nhưng chưa có biên bản kiểm tra tương thích trên từng trình duyệt. |
| Nội dung, hình ảnh và khoảng cách không tràn/vỡ ở các kích thước phổ biến | Cần cải thiện | Có ảnh chụp viewport giả lập ở ba kích thước; chưa kiểm tra trên thiết bị vật lý hoặc nhiều trình duyệt. |

#### Minh chứng responsive

Ảnh được chụp từ trang đang chạy trong trình duyệt tích hợp với viewport giả lập; đây không phải ảnh chụp thiết bị vật lý.

| Loại viewport | Kích thước viewport | Minh chứng |
|---|---:|---|
| Mobile | 390 × 844 | [responsive-mobile.png](screenshots/responsive-mobile.png) |
| Tablet | 834 × 1112 | [responsive-tablet.png](screenshots/responsive-tablet.png) |
| Desktop | 1440 × 1000 | [responsive-desktop.png](screenshots/responsive-desktop.png) |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn chạy website cục bộ | Đạt | README hướng dẫn dùng Python HTTP server và cổng mặc định `8000`; chưa thực hiện chạy thử trong lần rà soát này. |
| Có hướng dẫn triển khai thử bằng Docker/Nginx | Đạt | README có lệnh Docker phục vụ nội dung tại cổng `8080`; chưa xác nhận container khởi động thành công. |
| Tài nguyên trang được tải đầy đủ, không có lỗi 404 | Cần cải thiện | Chưa kiểm tra Network Console; cần xác nhận các ảnh trong `assets/img/` được tải khi mở trang. |
| Biểu mẫu xử lý lỗi nhập liệu và thông báo kết quả rõ ràng | Cần cải thiện | Trường email có kiểu `email` và `required`, nhưng chưa có phản hồi ứng dụng về kết quả gửi hoặc lỗi máy chủ. |
| Thời gian tải và hiệu năng cơ bản đáp ứng yêu cầu | Cần cải thiện | Chưa đo thời gian tải, dung lượng tài nguyên, chỉ số hiệu năng hoặc hành vi ở kết nối chậm. |
| Trang hoạt động khi JavaScript không khả dụng | Đạt | Trang được mô tả là website tĩnh HTML/CSS; README nêu trang không cần JavaScript để chạy. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có backend hoặc nơi lưu trữ dữ liệu biểu mẫu | Đạt | README nêu website hiện không có backend; không được xem biểu mẫu hiện tại là kênh gửi dữ liệu thật. |
| Cấu hình và bí mật được quản lý an toàn | Cần cải thiện | README cho biết không dùng biến môi trường/tệp cấu hình; chưa thực hiện quét toàn repository để xác nhận không có bí mật bị đưa vào mã nguồn. |
| Biểu mẫu không tạo kỳ vọng rằng dữ liệu đã được gửi an toàn | Cần cải thiện | Đây là biểu mẫu minh họa và có cảnh báo trong README; nên hiển thị cảnh báo ngay cạnh form nếu tiếp tục giữ giao diện đăng nhập. Không nhập dữ liệu nhạy cảm. |
| Liên kết mở tab mới có biện pháp hạn chế quyền truy cập tab nguồn | Cần cải thiện | Các liên kết mạng xã hội dùng `target="_blank"` nhưng chưa khai báo `rel="noopener noreferrer"` trong `index.html`. |
| Bảo mật tổng thể đã được đánh giá đầy đủ | Cần cải thiện | Chưa thực hiện kiểm thử bảo mật chuyên sâu; nhận định trong mục này chỉ dựa trên rà soát tĩnh phạm vi website hiện tại. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc mã nguồn và tài nguyên chính dễ nhận biết | Đạt | Có `index.html`, `assets/css/styles.css` và thư mục ảnh trong repository. |
| Có tài liệu cài đặt/chạy và mô tả giới hạn sản phẩm | Đạt | README mô tả chức năng, yêu cầu môi trường, cách chạy và giới hạn của form/liên kết dự án. |
| Có release note cho phiên bản bàn giao | Đạt | `docs/RELEASENOTE.md` ghi phiên bản v1.0, chức năng, lỗi đã sửa và hạn chế. |
| Nội dung và metadata nhất quán, không có lỗi gõ rõ ràng | Chưa đạt | Tiêu đề hero thừa ký tự “i”; cần đồng bộ trước khi bàn giao. |
| HTML/CSS đã được kiểm tra bằng validator/linter | Cần cải thiện | Chưa có kết quả validator, linter hoặc kiểm tra tự động kèm theo báo cáo. |
| Repository và tài liệu không còn nội dung thử nghiệm dư thừa | Cần cải thiện | Cuối `index.html` còn một khối `<article>` cũ đang bị comment; nên xác nhận có cần giữ trước khi bàn giao. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn triển khai đủ để người khác chạy thử | Đạt | README cung cấp hướng dẫn máy chủ cục bộ và Docker/Nginx; cần thực hiện theo hướng dẫn để xác nhận. |
| Có kết quả kiểm thử triển khai trên môi trường sạch | Cần cải thiện | Chưa có log chạy server/container hoặc xác nhận mở trang thành công từ máy khác. |
| Có minh chứng giao diện và kiểm thử chức năng | Cần cải thiện | Đã đính kèm ảnh responsive ở [mobile](screenshots/responsive-mobile.png), [tablet](screenshots/responsive-tablet.png) và [desktop](screenshots/responsive-desktop.png); chưa có minh chứng kiểm thử liên kết/form hoặc ma trận trình duyệt. |
| Có thể lặp lại và đối chiếu kết quả kiểm thử | Cần cải thiện | Báo cáo này ghi phạm vi rà soát tĩnh; cần bổ sung môi trường, bước thực hiện, kết quả và người xác nhận của lần kiểm thử thực tế. |
| Tài liệu bàn giao nêu rõ giới hạn của tính năng minh họa | Đạt | README và release note thông báo form chưa kết nối máy chủ, các liên kết chi tiết chưa hoạt động. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm hiện phù hợp để **trình diễn portfolio tĩnh ở mức cơ bản**: các khu vực nội dung chính, điều hướng nội bộ và bố cục responsive đã được rà soát; đã có ảnh chụp ở ba viewport giả lập. Tuy nhiên, chưa kiểm tra trên thiết bị vật lý, nhiều trình duyệt, hiệu năng hoặc môi trường triển khai thực tế.

**Trạng thái sẵn sàng bàn giao: Cần cải thiện trước khi bàn giao chính thức.** Nếu phạm vi bàn giao chỉ là bản demo tĩnh, cần ghi rõ form và liên kết dự án là phần minh họa, đồng thời hoàn tất các xác nhận dưới đây.

### Vấn đề cần ưu tiên

1. Sửa lỗi tên hiển thị “Đinh Văn Hảiii” thành tên chính xác và kiểm tra đồng nhất các vị trí liên quan.
2. Thay các liên kết `href="#"` bằng đích đến hợp lệ hoặc thể hiện rõ chúng chưa khả dụng.
3. Làm rõ ngay tại biểu mẫu rằng dữ liệu không được gửi/lưu; không yêu cầu người dùng nhập thông tin nhạy cảm khi chưa có backend.
4. Bổ sung `rel="noopener noreferrer"` cho các liên kết ngoài mở bằng `target="_blank"`.
5. Mở rộng kiểm thử sang thiết bị/trình duyệt mục tiêu; xác nhận liên kết nội bộ, biểu mẫu và lỗi console/network ngoài các viewport responsive đã chụp.
6. Thử triển khai theo hướng dẫn README bằng HTTP server và/hoặc Docker; lưu lại kết quả, môi trường và ảnh chụp minh chứng.
7. Chạy validator HTML/CSS, xử lý lỗi phát hiện được và cân nhắc loại bỏ khối HTML cũ đang bị comment.

### Điều kiện đề xuất để xác nhận bàn giao

- Các lỗi ưu tiên đã được xử lý hoặc được chủ sản phẩm chấp thuận giữ lại như giới hạn đã biết.
- Bổ sung kiểm tra chức năng trên trình duyệt mục tiêu; minh chứng responsive viewport desktop và mobile đã được đính kèm ở mục 3.2.
- Có xác nhận chạy trang theo ít nhất một phương thức triển khai được README hướng dẫn.
- Báo cáo được cập nhật tên người thực hiện, môi trường, ngày chạy và liên kết/đường dẫn đến minh chứng.