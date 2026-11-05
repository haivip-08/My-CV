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