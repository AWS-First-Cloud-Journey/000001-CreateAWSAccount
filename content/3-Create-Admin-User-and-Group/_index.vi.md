---
title : "Tạo Admin Group và Admin User"
date :  "2025-10-05" 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---


#### Tạo Admin Group

1. Đăng nhập vào AWS Management Console tại [https://aws.amazon.com/](https://aws.amazon.com/)

2. Nhấn vào tên tài khoản ở góc trên bên phải và chọn **My Security Credentials**

   ![Truy cập Security Credentials](/images/01/0001.png)

   > **Lưu ý:** Nếu không thấy menu **My Security Credentials**, bạn có thể tìm kiếm và chọn dịch vụ **IAM** để truy cập vào IAM console.

   ![Tìm kiếm dịch vụ IAM](/images/01/0002.png)

3. Trong navigation pane bên trái, chọn **User Groups** và nhấn **Create Group**

   ![Tạo User Group](/images/01/0003.png)

4. Trong mục **User group name**, nhập tên group (ví dụ: *AdminGroup*)

   ![Đặt tên User Group](/images/01/0004.png)

5. Trong phần **Attach permissions policies**, tìm và chọn policy **AdministratorAccess**. Sau đó chọn **Create Group**

   ![Gán permissions](/images/01/0005.png)

6. Group đã được tạo thành công

   ![Hoàn thành tạo group](/images/01/0006.png)

#### Tạo Admin User 

1. Trong navigation pane, chọn **Users** và nhấn **Add users**

   ![Tạo User mới](/images/02/0001.png)

2. Cấu hình thông tin user:
   - Nhập **User name** (ví dụ: *AdminUser*)
   - Chọn **AWS Management Console access**
   - Chọn **Programmatic access** 
   - Chọn **Custom password** và nhập mật khẩu
   - Bỏ chọn **User must create a new password at next sign-in**
   - Nhấn **Next: Permissions**

   ![Cấu hình User](/images/02/0002.png)

3. Chọn tab **Add user to group** và chọn group **AdminGroup** đã tạo

   ![Thêm user vào group](/images/02/0003.png)

4. Nhấn **Next: Tags** (Tags là tùy chọn để tổ chức và quản lý tài nguyên)

5. Nhấn **Next: Review**

   ![Review thông tin](/images/02/0004.png)

6. Kiểm tra lại thông tin và chọn **Create user**

   ![Xác nhận tạo user](/images/02/0005.png)

7. Tải xuống file .csv chứa access key (nếu cần)

   ![Download credentials](/images/02/0006.png)

8. User đã được tạo thành công

   ![Hoàn thành tạo user](/images/02/0007.png)

9. Xem chi tiết thông tin user

   ![Chi tiết user](/images/02/0008.png)

> **Lưu ý:** Sau khi tạo user, AWS sẽ hiển thị access key ID và secret access key. Đây là thông tin quan trọng để truy cập AWS thông qua AWS CLI và AWS SDK.

#### Đăng nhập với Admin User

1. Trong IAM console, chọn **Users** ở navigation pane
2. Chọn IAM user vừa tạo
3. Trong tab **Security credentials**, copy đường link console sign-in

   ![Copy sign-in link](/images/03/0001.png)

4. Mở tab ẩn danh mới và truy cập link sign-in

   ![Truy cập bằng tab ẩn danh](/images/03/0002.png)

5. Nhập thông tin đăng nhập:
   - IAM user name
   - Password đã tạo
   - Nhấn **Sign in**

   ![Đăng nhập IAM user](/images/03/0003.png)

6. Đăng nhập thành công với IAM user

   ![Đăng nhập thành công](/images/03/0004.png)

#### Tài liệu tham khảo

#### IAM User và Đăng nhập AWS

IAM user là một entity được tạo trong AWS account, có quyền tương tác với AWS resources. IAM user có thể đăng nhập bằng:
- Account ID/alias 
- User name
- Password

User name có thể là tên thường (*zhang*) hoặc email (*zhang@example.com*), không chứa khoảng trắng nhưng có thể chứa:
- Chữ hoa và chữ thường
- Số
- Ký tự đặc biệt: + = , . @ _ -


#### Tạo Access Key cho Root User

#### Quyền yêu cầu

- Cần đăng nhập bằng root user (không thể thực hiện với IAM user hoặc role)

#### Các bước thực hiện

1. Đăng nhập vào AWS Management Console bằng email và password của root user

2. Click vào tên account ở góc trên phải, chọn **Security Credentials**

3. Trong phần **Access keys**, chọn **Create access key**

   > **Lưu ý:** Nếu không thấy tùy chọn này, có thể bạn đã đạt giới hạn số lượng access key. Cần xóa một key hiện có trước khi tạo mới.

4. Trên trang **Alternatives to root user access keys**, đọc các khuyến nghị bảo mật. Tích vào checkbox và chọn **Create access key**

5. Trên trang **Retrieve access key**:
   - Access key ID sẽ được hiển thị
   - Click **Show** để xem Secret access key
   - Copy và lưu cả Access key ID và Secret key vào nơi an toàn
   - Hoặc tải file rootkey.csv để lưu thông tin

6. Click **Done** để hoàn tất

> **Khuyến nghị:** Nên xóa hoặc vô hiệu hóa access key khi không còn sử dụng để đảm bảo an toàn.

#### Xóa Access Key cho Root User

#### Quyền yêu cầu

- Cần đăng nhập bằng root user (không thể thực hiện với IAM user hoặc role)

#### Các bước thực hiện

1. Đăng nhập vào AWS Management Console bằng root user

2. Click vào tên account ở góc trên phải, chọn **Security Credentials**

3. Trong phần **Access keys**, tìm key cần xóa:
   - Click **Delete** trong menu **Actions** để xóa vĩnh viễn
   - Hoặc click **Deactivate** để vô hiệu hóa tạm thời

4. Trên hộp thoại xác nhận:
   - Nhập Access key ID để xác nhận
   - Click **Delete** để hoàn tất

> **Lưu ý về vô hiệu hóa key:**
> - Key bị vô hiệu hóa có thể kích hoạt lại sau này
> - Không cần thay đổi ID và Secret
> - Các API call sử dụng key đã vô hiệu hóa sẽ bị từ chối với lỗi "access denied"

Best Practices:
- Hạn chế sử dụng access key của root user
- Nên tạo IAM user có quyền phù hợp thay vì dùng root user
- Luôn bảo mật thông tin access key
- Xoá hoặc vô hiệu hóa key không sử dụng
- Định kỳ xoay vòng (rotate) các access key
- Sử dụng AWS CloudTrail để giám sát hoạt động của access key

#### Chi tiết về Multi-Factor Authentication (MFA)

Khi MFA được bật, người dùng cần:
- Đăng nhập bình thường với username/password
- Nhập mã xác thực từ thiết bị MFA

AWS hỗ trợ các loại thiết bị MFA:
- Virtual MFA (Google Authenticator, Authy)  
- Hardware MFA token
- U2F security key

> **Khuyến nghị:** Nên bật MFA cho cả root user và IAM user để tăng cường bảo mật.

Tham khảo thêm:
- [IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS Security Best Practices](https://aws.amazon.com/security/security-learning/)
- [AWS CloudTrail Documentation](https://docs.aws.amazon.com/cloudtrail/)