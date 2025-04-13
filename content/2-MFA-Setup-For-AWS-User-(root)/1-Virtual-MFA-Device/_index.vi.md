---
title : "Thiết bị MFA ảo"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Giới thiệu

Bảo mật tài khoản AWS là một trong những yếu tố quan trọng nhất để bảo vệ tài nguyên cloud của bạn. Multi-Factor Authentication (MFA) cung cấp một lớp bảo mật bổ sung ngoài thông tin đăng nhập thông thường. Tài liệu này hướng dẫn cách thiết lập thiết bị MFA ảo cho tài khoản AWS của bạn.

#### Tổng quan về MFA trong AWS

MFA yêu cầu người dùng cung cấp hai hoặc nhiều yếu tố xác thực khi đăng nhập:
- Thông tin đăng nhập (username và password)
- Mã xác thực từ thiết bị MFA đã đăng ký

#### Yêu cầu

> **Lưu ý**: Để kích hoạt MFA, bạn cần đăng nhập vào AWS sử dụng tài khoản root.

#### Các loại thiết bị MFA được AWS hỗ trợ

AWS hỗ trợ nhiều loại thiết bị MFA khác nhau:
- Ứng dụng xác thực (Authenticator apps)
- Khóa bảo mật FIDO
- Thiết bị token phần cứng

#### Thiết lập thiết bị MFA ảo

##### Bước 1: Đăng nhập vào AWS Management Console

1. Truy cập [AWS Console](https://aws.amazon.com/console/)
2. Đăng nhập bằng thông tin tài khoản của bạn

##### Bước 2: Truy cập thiết lập bảo mật

1. Ở góc trên bên phải màn hình, nhấp vào tên tài khoản của bạn
2. Chọn **My Security Credentials** từ menu thả xuống

![Truy cập thiết lập bảo mật](/images/2/0001.png?featherlight=false&width=90pc)

##### Bước 3: Thiết lập MFA

1. Trong trang Security Credentials, mở rộng mục **Multi-factor authentication (MFA)**
2. Nhấp vào **Assign MFA**

![Thiết lập MFA](/images/2/0002.png?featherlight=false&width=90pc)

##### Bước 4: Chọn loại thiết bị MFA

1. Trong giao diện **Select MFA device**:
   - Nhập tên cho thiết bị MFA của bạn
   - Chọn **Authenticator app** làm loại thiết bị MFA
   - Nhấp vào **Next**

![Chọn loại thiết bị MFA](/images/2/0003.png?featherlight=false&width=90pc)

##### Bước 5: Cài đặt ứng dụng xác thực

1. Cài đặt một ứng dụng xác thực trên thiết bị di động hoặc trình duyệt của bạn
   - Danh sách [ứng dụng MFA tương thích với AWS](https://aws.amazon.com/iam/features/mfa/?audit=2019q1)

![Hướng dẫn cài đặt ứng dụng xác thực](/images/2/0004.png?featherlight=false&width=90pc)

##### Bước 6: Cài đặt Authenticator trên Chrome (tùy chọn)

Nếu bạn muốn sử dụng ứng dụng xác thực trên trình duyệt Chrome:

1. Truy cập [Authenticator trên Chrome Web Store](https://chrome.google.com/webstore/detail/authenticator/bhghoamapcdpbohphigoooaddinpkbai)
2. Nhấp vào **Add to Chrome** để cài đặt

![Cài đặt Authenticator trên Chrome](/images/2/0005.png?featherlight=false&width=90pc)

##### Bước 7: Quét mã QR

1. Sử dụng ứng dụng xác thực đã cài đặt để quét mã QR hiển thị trên màn hình AWS

![Quét mã QR](/images/2/0007.png?featherlight=false&width=90pc)

##### Bước 8: Xác nhận thiết lập

1. Sau khi quét mã QR, ứng dụng xác thực sẽ bắt đầu tạo mã
2. Nhập hai mã xác thực liên tiếp vào trường tương ứng trên AWS
3. Nhấp vào **Add MFA**

![Nhập mã xác thực](/images/2/0008.png?featherlight=false&width=90pc)

##### Bước 9: Hoàn tất thiết lập

1. Xác nhận yêu cầu thêm thiết bị MFA

![Hoàn tất thiết lập](/images/2/0009.png?featherlight=false&width=90pc)

##### Bước 10: Xác nhận thành công

1. Sau khi hoàn tất, bạn sẽ thấy thông báo xác nhận thiết lập MFA thành công

![Thiết lập MFA thành công](/images/2/00010.png?featherlight=false&width=90pc)

#### Sử dụng MFA

Từ lần đăng nhập tiếp theo, sau khi nhập thông tin đăng nhập, bạn sẽ được yêu cầu nhập mã xác thực từ thiết bị MFA đã đăng ký.

#### Xử lý sự cố

- **Mất thiết bị MFA**: Liên hệ với AWS Support để được hỗ trợ khôi phục quyền truy cập
- **Mã xác thực không hoạt động**: Đảm bảo thiết bị của bạn được đồng bộ hóa thời gian chính xác

#### Tài liệu tham khảo

- [AWS IAM MFA Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html)
- [AWS Security Best Practices](https://aws.amazon.com/architecture/security-identity-compliance/)