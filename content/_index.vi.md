+++
title = "Thiết lập Tài Khoản AWS"
date = 2021
weight = 1
chapter = false
+++

# Thiết lập Tài Khoản AWS
Tài liệu này hướng dẫn chi tiết quy trình thiết lập tài khoản AWS từ đầu, bao gồm tạo tài khoản, cấu hình bảo mật, và thiết lập quyền quản trị. Hướng dẫn này giúp bạn bắt đầu sử dụng AWS một cách an toàn và hiệu quả.

## Mục lục
- [Tạo tài khoản AWS đầu tiên](#tạo-tài-khoản-aws-đầu-tiên)
- [Thiết lập MFA cho tài khoản Root](#thiết-lập-mfa-cho-tài-khoản-root)
- [Tạo Admin Group và Admin User](#tạo-admin-group-và-admin-user)
- [Hỗ trợ xác thực tài khoản](#hỗ-trợ-xác-thực-tài-khoản)
- [Khám phá AWS Management Console](#khám-phá-aws-management-console)

## Tạo tài khoản AWS đầu tiên

### Tổng quan
Trong phần này, bạn sẽ tạo mới **tài khoản AWS**, thiết lập **MFA** (Multi-factor Authentication) để bảo vệ tài khoản. Tiếp theo, bạn sẽ tạo **Admin Group** và **Admin User** để quản lý tài nguyên AWS thay vì sử dụng tài khoản root. Cuối cùng, nếu gặp vấn đề trong quá trình xác thực, bạn sẽ được hướng dẫn liên hệ **AWS Support**.

### Các khái niệm cơ bản

#### Tài khoản AWS (AWS Account)
**Tài khoản AWS** là phương tiện để truy cập và sử dụng các dịch vụ AWS. Mỗi tài khoản mặc định có một **root user** với toàn quyền quản trị không thể giới hạn. Khi đăng nhập lần đầu, bạn sẽ sử dụng tài khoản root user này.

> **Lưu ý**: AWS khuyến nghị không sử dụng root user cho các tác vụ hàng ngày. Thay vào đó, hãy tạo IAM User với quyền quản trị phù hợp để giảm thiểu rủi ro bảo mật.

#### MFA (Multi-factor Authentication)
**MFA** là tính năng bảo mật nâng cao cho tài khoản AWS. Khi kích hoạt, bạn sẽ cần nhập mã OTP (One-time Password) mỗi lần đăng nhập vào tài khoản AWS, tạo lớp bảo vệ thứ hai ngoài mật khẩu thông thường.

#### IAM Group
**IAM Group** là công cụ quản lý người dùng của AWS, cho phép gom nhiều IAM User vào một nhóm. Tất cả IAM User trong cùng một nhóm sẽ được thừa hưởng các quyền được gán cho nhóm đó, giúp quản lý quyền dễ dàng hơn.

#### IAM User
**IAM User** là đơn vị người dùng trong AWS. Mỗi IAM User có thông tin đăng nhập riêng và được cấp quyền truy cập cụ thể vào tài nguyên AWS. IAM User được tạo để cấp quyền truy cập **dài hạn** vào tài khoản AWS.

#### AWS Support
**AWS Support** là đơn vị cung cấp dịch vụ hỗ trợ khách hàng của AWS, giúp giải quyết các vấn đề kỹ thuật và hỗ trợ xác thực tài khoản.

#### AWS Management Console
**AWS Management Console** là giao diện web cho phép quản lý và tương tác với các dịch vụ AWS một cách trực quan.

## Nội dung chính

### Tạo tài khoản AWS

#### Bước 1: Truy cập trang đăng ký AWS
1. Mở trình duyệt web và truy cập địa chỉ [aws.amazon.com](https://aws.amazon.com)
2. Nhấp vào nút **Create an AWS Account** ở góc phải trên cùng của trang

#### Bước 2: Điền thông tin tài khoản
1. Nhập địa chỉ email của bạn
2. Tạo tên tài khoản AWS (AWS account name)
3. Nhấp vào **Verify email address** và xác minh email của bạn

#### Bước 3: Tạo mật khẩu
1. Tạo mật khẩu mạnh cho tài khoản AWS của bạn
2. Mật khẩu cần đáp ứng các yêu cầu sau:
   - Tối thiểu 8 ký tự
   - Bao gồm ít nhất một chữ cái viết hoa
   - Bao gồm ít nhất một chữ cái viết thường
   - Bao gồm ít nhất một số
   - Bao gồm ít nhất một ký tự đặc biệt

#### Bước 4: Điền thông tin liên hệ
1. Chọn loại tài khoản (Cá nhân hoặc Doanh nghiệp)
2. Điền đầy đủ thông tin cá nhân hoặc thông tin doanh nghiệp
3. Đọc và chấp nhận AWS Customer Agreement

#### Bước 5: Điền thông tin thanh toán
1. Nhập thông tin thẻ tín dụng hợp lệ
2. Lưu ý: AWS sẽ thực hiện một khoản giữ tiền nhỏ để xác minh thẻ của bạn

#### Bước 6: Xác minh danh tính
1. Nhập số điện thoại di động của bạn
2. Chọn phương thức xác minh (SMS hoặc cuộc gọi thoại)
3. Nhập mã xác minh được gửi đến điện thoại của bạn

#### Bước 7: Chọn gói hỗ trợ
1. Chọn gói hỗ trợ AWS phù hợp (Basic, Developer, Business, hoặc Enterprise)
2. Gói Basic miễn phí và phù hợp cho người mới bắt đầu

#### Bước 8: Hoàn tất quá trình đăng ký
1. Nhấp vào nút **Complete sign up**
2. Đợi email xác nhận từ AWS (có thể mất vài phút đến vài giờ)
3. Sau khi nhận được email xác nhận, bạn có thể đăng nhập vào AWS Management Console

### Thiết lập MFA cho tài khoản Root

#### Bước 1: Đăng nhập vào AWS Management Console
1. Truy cập [console.aws.amazon.com](https://console.aws.amazon.com)
2. Đăng nhập bằng email và mật khẩu của tài khoản root

#### Bước 2: Truy cập trang quản lý tài khoản
1. Nhấp vào tên tài khoản của bạn ở góc phải trên cùng
2. Chọn **My Security Credentials** từ menu thả xuống

#### Bước 3: Thiết lập MFA
1. Mở rộng phần **Multi-factor authentication (MFA)**
2. Nhấp vào **Activate MFA**
3. Chọn loại thiết bị MFA:
   - **Virtual MFA device**: Sử dụng ứng dụng xác thực như Google Authenticator
   - **Hardware TOTP token**: Sử dụng thiết bị phần cứng chuyên dụng
   - **Security key**: Sử dụng khóa bảo mật FIDO

#### Bước 4: Cấu hình MFA cho thiết bị ảo (phổ biến nhất)
1. Cài đặt ứng dụng xác thực trên điện thoại của bạn (Google Authenticator, Authy, Microsoft Authenticator, v.v.)
2. Nhấp vào **Show QR code** và quét mã QR bằng ứng dụng xác thực
3. Nhập hai mã xác thực liên tiếp từ ứng dụng xác thực
4. Nhấp vào **Assign MFA**

#### Bước 5: Sao lưu thông tin MFA
1. Lưu mã QR hoặc khóa bí mật được cung cấp trong quá trình thiết lập
2. Lưu trữ an toàn thông tin này để phòng trường hợp mất thiết bị

### Tạo Admin Group và Admin User

#### Bước 1: Truy cập dịch vụ IAM
1. Đăng nhập vào AWS Management Console bằng tài khoản root
2. Tìm kiếm "IAM" trong thanh tìm kiếm dịch vụ
3. Chọn dịch vụ **IAM** (Identity and Access Management)

#### Bước 2: Tạo Admin Group
1. Trong dashboard IAM, nhấp vào **User groups** ở menu bên trái
2. Nhấp vào nút **Create group**
3. Nhập tên cho nhóm (ví dụ: "Administrators")
4. Tìm và chọn policy **AdministratorAccess** trong danh sách policies
5. Nhấp vào **Create group** để hoàn tất

#### Bước 3: Tạo Admin User
1. Trong dashboard IAM, nhấp vào **Users** ở menu bên trái
2. Nhấp vào nút **Add users**
3. Nhập tên người dùng (ví dụ: "AdminUser")
4. Chọn **AWS Management Console access** trong phần Access type
5. Cấu hình mật khẩu:
   - Chọn **Custom password** và nhập mật khẩu mạnh
   - Bỏ chọn "User must create a new password at next sign-in" nếu bạn không muốn thay đổi mật khẩu ở lần đăng nhập đầu tiên

#### Bước 4: Thêm User vào Admin Group
1. Trong trang "Add user to group", chọn nhóm Administrators đã tạo ở bước trước
2. Nhấp vào **Next: Tags**
3. (Tùy chọn) Thêm tags nếu cần
4. Nhấp vào **Next: Review**
5. Xem lại thông tin và nhấp vào **Create user**

#### Bước 5: Lưu thông tin đăng nhập
1. Tải xuống hoặc sao chép thông tin đăng nhập (bao gồm đường dẫn đăng nhập, tên người dùng và mật khẩu)
2. Lưu trữ thông tin này một cách an toàn

#### Bước 6: Thiết lập MFA cho Admin User
1. Quay lại danh sách Users trong IAM
2. Chọn tên người dùng vừa tạo
3. Chọn tab **Security credentials**
4. Trong phần **Multi-factor authentication (MFA)**, nhấp vào **Assign MFA device**
5. Làm theo các bước tương tự như khi thiết lập MFA cho tài khoản root

### Hỗ trợ xác thực tài khoản

#### Các vấn đề phổ biến khi xác thực tài khoản
1. Không nhận được email xác nhận
2. Thẻ tín dụng không được chấp nhận
3. Xác minh danh tính thất bại
4. Không thể đăng nhập sau khi đăng ký

#### Liên hệ AWS Support
1. Truy cập [aws.amazon.com/support](https://aws.amazon.com/support)
2. Nhấp vào **Create case**
3. Chọn loại hỗ trợ **Account and billing support**
4. Điền đầy đủ thông tin về vấn đề của bạn
5. Nhấp vào **Submit** để gửi yêu cầu hỗ trợ

### Khám phá AWS Management Console

#### Tổng quan về AWS Management Console
1. Thanh điều hướng phía trên cùng:
   - Menu dịch vụ: Truy cập nhanh đến các dịch vụ AWS
   - Thanh tìm kiếm: Tìm kiếm dịch vụ, tài liệu và tài nguyên
   - Khu vực: Chọn khu vực AWS để làm việc
   - Tài khoản: Quản lý cài đặt tài khoản và đăng xuất
   - Hỗ trợ: Truy cập tài liệu và hỗ trợ

#### Các dịch vụ AWS cơ bản cho người mới bắt đầu
1. **EC2**: Máy chủ ảo
2. **S3**: Lưu trữ đối tượng
3. **RDS**: Cơ sở dữ liệu quan hệ
4. **Lambda**: Tính toán không cần máy chủ
5. **CloudWatch**: Giám sát và nhật ký

#### Cá nhân hóa AWS Management Console
1. Tạo trang chủ tùy chỉnh:
   - Nhấp vào **Edit** ở góc phải trên cùng của trang chủ console
   - Thêm, xóa hoặc sắp xếp lại các widget theo nhu cầu
   - Nhấp vào **Save** để lưu thay đổi

2. Tạo bookmark cho các dịch vụ thường dùng:
   - Nhấp vào dấu sao bên cạnh tên dịch vụ trong menu dịch vụ
   - Các dịch vụ đã đánh dấu sẽ xuất hiện trong phần **Recently visited services**

## Tài liệu tham khảo
- [AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [AWS Security Best Practices](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)
- [Getting Started with AWS](https://aws.amazon.com/getting-started/)