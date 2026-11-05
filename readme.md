# Thành viên tự kích hoạt 2FA trên tài khoản cá nhân:
- Truy cập GitHub: nháp vào avatar -> Setting -> Password and authentication -> kéo xuống Two-factor authentication -> Chọn Enable two-factor authentication.
- Quét mã QR bằng ứng dụng Google Authenticator và lưu lại những mã code xác thực 

## Trưởng nhóm bật tính năng bắt buộc 2FA trên Organization:
- Vào Organization -> Settings -> Chọn Authentication security.
- Tại mục Two-factor authentication -> tích chọn Require two-factor authentication for everyone in (tên) organization.
- Bấm Save và bất kỳ tài khoản nào chưa bật 2FA sẽ tự động bị tước quyền truy cập repo cho đến khi hoàn tất thiết lập 2FA.

### Bản báo cáo đánh giá rủi ro nếu thiếu tệp .gitignore.
- Các DB_USER, DB_PASSWORD bị lộ giúp hacker đăng nhập trực tiếp vào hệ thống.
- Khi không có .gitignore, các file chứa cấu hình nhạy cảm như .env sẽ bị đẩy thẳng lên GitHub Public.
- Hacker có thể đánh cắp toàn bộ thông tin khách hàng hoặc ra lệnh xóa sạch dữ liệu để tống tiền
- API_KEY cho phép ứng dụng của mình gọi dịch vụ có phí, không có .gitignore thì nó sẽ bị lộ và sẽ bị đào tiền ảo