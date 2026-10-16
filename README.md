# Bật chế độ giao tiếp tiếng Hàn — Hi Korean

Website HTML/CSS/JavaScript thuần, không cần cài thư viện hay build.

## Chạy trên GitHub Pages

Đưa mã nguồn vào nhánh `main`. Trong Settings → Pages → Build and deployment, chọn **GitHub Actions**. Workflow `.github/workflows/pages.yml` xuất bản website và chạy lại khi nhánh main có thay đổi.

## Gắn tên miền ebookgiaotiep.hikorean.vn

Tài khoản GitHub: `thuyhikorean-coder`.

1. Điền `ebookgiaotiep.hikorean.vn` trong Settings → Pages → Custom domain, lưu lại.
2. Tại nhà cung cấp DNS, tạo CNAME tên `ebookgiaotiep`, trỏ đến `thuyhikorean-coder.github.io`, không thêm tên repository.
3. Khi DNS hợp lệ và chứng chỉ đã cấp, bật Enforce HTTPS.

DNS cần được cấu hình tại nhà cung cấp tên miền. Không thay đổi DNS của tên miền gốc hikorean.vn.

## Hiện trạng chức năng

Khi học viên hoàn tất đăng ký và khảo sát, form gửi dữ liệu tới bộ nhận Google Apps Script thuộc nguyenphuongthuy@hikorean.vn. Bộ nhận chỉ thêm dòng vào tab EBOOKGIAOTIEP (sheetId 897791773) của file DATA 2026. Không sửa các tab khác. Mã đăng ký ngăn việc gửi lại tạo dòng trùng; form chỉ mở khóa khi nhận xác nhận thành công. Tiến độ vẫn lưu trên trình duyệt. Chưa có hệ thống tài khoản/mật khẩu hay gửi email tự động. Video Shadowing, toàn bộ nội dung bài học, các liên kết quà tặng và CTA Zalo được đóng gói sẵn.

Tên miền đã bật Enforce HTTPS. Thanh vàng “Bản mẫu để duyệt” đã bỏ. Website đang giữ thẻ noindex của bản duyệt; có thể bỏ khi chốt phát hành/tên miền chính thức.

## Tài liệu triển khai chính thức

- https://docs.github.com/en/get-started/start-your-journey/deploying-your-website-automatically
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
