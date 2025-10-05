---
title : "MFA cho Tài khoản AWS"
date :  "2025-10-05" 
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

#### Giới thiệu

Multi-Factor Authentication (MFA) là một lớp bảo mật quan trọng cho tài khoản AWS của bạn. Bằng cách yêu cầu một yếu tố xác thực thứ hai bên cạnh mật khẩu, MFA bảo vệ tài khoản AWS của bạn khỏi truy cập trái phép ngay cả khi mật khẩu bị lộ.

#### Lợi ích của MFA

- **Tăng cường bảo mật**: Yêu cầu yếu tố xác thực thứ hai ngoài mật khẩu
- **Giảm thiểu rủi ro**: Bảo vệ tài khoản ngay cả khi thông tin đăng nhập bị xâm phạm
- **Tuân thủ**: Đáp ứng các yêu cầu tuân thủ bảo mật của nhiều tổ chức

#### Các loại thiết bị MFA hỗ trợ

##### 1. Thiết bị MFA ảo

Sử dụng ứng dụng xác thực trên điện thoại thông minh để tạo mã OTP (One-Time Password).

**Ứng dụng được hỗ trợ:**
- Microsoft Authenticator
- Google Authenticator
- Okta Verify
- Authy

##### 2. Khóa bảo mật U2F

Khóa bảo mật vật lý tuân theo chuẩn FIDO Universal 2nd Factor (U2F).

**Thiết bị được hỗ trợ:**
- YubiKey
- Feitian
- HyperFIDO

##### 3. Thiết bị MFA phần cứng khác

Thiết bị phần cứng phát sinh mã xác thực.

**Thiết bị được hỗ trợ:**
- Gemalto SafeNet IDProve
- RSA SecurID

#### Hướng dẫn thiết lập

##### 1. Thiết lập thiết bị MFA ảo

1. Đăng nhập vào AWS Management Console
2. Truy cập IAM Dashboard
3. Chọn "Users" và chọn tên người dùng của bạn
4. Chọn tab "Security credentials"
5. Tại mục "Assigned MFA device", chọn "Manage"
6. Chọn "Virtual MFA device" và nhấn "Continue"
7. Tải và cài đặt một trong các ứng dụng xác thực được hỗ trợ trên điện thoại
8. Quét mã QR bằng ứng dụng hoặc nhập mã cài đặt thủ công
9. Nhập hai mã xác thực liên tiếp từ ứng dụng
10. Chọn "Assign MFA" để hoàn tất

##### 2. Thiết lập Khóa bảo mật U2F

1. Đăng nhập vào AWS Management Console
2. Truy cập IAM Dashboard
3. Chọn "Users" và chọn tên người dùng của bạn
4. Chọn tab "Security credentials"
5. Tại mục "Assigned MFA device", chọn "Manage"
6. Chọn "Security Key" và nhấn "Continue"
7. Cắm khóa bảo mật U2F vào cổng USB của máy tính
8. Nhấn vào nút trên khóa khi được nhắc
9. Đặt tên cho khóa bảo mật
10. Chọn "Assign MFA" để hoàn tất

##### 3. Thiết lập thiết bị MFA phần cứng khác

1. Đăng nhập vào AWS Management Console
2. Truy cập IAM Dashboard
3. Chọn "Users" và chọn tên người dùng của bạn
4. Chọn tab "Security credentials"
5. Tại mục "Assigned MFA device", chọn "Manage"
6. Chọn "Hardware MFA device" và nhấn "Continue"
7. Nhập số sê-ri của thiết bị MFA
8. Nhập hai mã xác thực liên tiếp từ thiết bị
9. Chọn "Assign MFA" để hoàn tất

#### Khắc phục sự cố

##### Mất thiết bị MFA

Nếu bạn mất quyền truy cập vào thiết bị MFA:

1. Liên hệ với quản trị viên AWS của tổ chức
2. Đối với tài khoản root, sử dụng phương pháp khôi phục thông qua email và số điện thoại đã đăng ký
3. Xem thêm tài liệu AWS về [khôi phục quyền truy cập khi mất thiết bị MFA](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_lost-or-broken.html)

##### Lỗi đồng bộ

Nếu thiết bị MFA ảo không đồng bộ:

1. Kiểm tra thời gian trên thiết bị của bạn có chính xác không
2. Sử dụng tùy chọn đồng bộ lại trong AWS Management Console
3. Nếu vẫn gặp vấn đề, xóa và thiết lập lại thiết bị MFA

#### Bài thực hành

1. [Thiết lập MFA cho tài khoản root AWS](/labs/mfa-root-account)
2. [Thiết lập MFA cho IAM User](/labs/mfa-iam-user)
3. [Thử nghiệm xác thực với MFA](/labs/test-mfa-authentication)

#### Tài liệu tham khảo

- [AWS IAM User Guide - Using MFA](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html)
- [AWS Security Best Practices](https://aws.amazon.com/architecture/security-identity-compliance/)
- [AWS Well-Architected Framework - Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)

#### FAQs

**Q: Tôi có thể đăng ký nhiều thiết bị MFA cho một tài khoản không?**  
A: Đối với IAM user, bạn có thể đăng ký tối đa 8 thiết bị MFA thuộc bất kỳ kết hợp nào của các loại được hỗ trợ.

**Q: MFA có tính phí không?**  
A: AWS không tính phí cho việc sử dụng MFA. Tuy nhiên, bạn có thể phải trả chi phí cho thiết bị phần cứng.

**Q: Tài khoản root có bắt buộc phải dùng MFA không?**  
A: Mặc dù không bắt buộc, AWS đặc biệt khuyến nghị bảo vệ tài khoản root bằng MFA.