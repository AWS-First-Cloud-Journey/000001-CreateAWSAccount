+++
title = "Khám phá và cấu hình AWS Management Console"
date = 2024
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

![AWS Support](/images/5-console/01.png?width=70pc)

#### Tổng quan về AWS Management Console

AWS Management Console cung cấp giao diện web an toàn để truy cập và quản lý các dịch vụ AWS. Nó hỗ trợ xác thực thông qua cả thông tin đăng nhập tài khoản root user AWS và thông tin đăng nhập AWS Identity and Access Management (IAM).

> **ℹ️ Thông tin**  
> Mặc dù AWS Management Console cung cấp giao diện web thân thiện với người dùng, tất cả các tương tác đều được chuyển đổi thành các lệnh gọi AWS API ở phía sau.

Để biết thêm thông tin chi tiết, tham khảo: [What is the AWS Management Console?](https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/what-is.html)

#### Tính năng và Điều hướng chính

AWS Management Console bao gồm các tính năng chính sau:

- [Thiết lập Region mặc định](http://localhost:1313/vi/5-explore-and-configure-the-aws-management-console/5.1-config-default-region/#set-up-default-region)
- [Tìm kiếm các dịch vụ AWS bằng AWS MANAGEMENT CONSOLE](http://localhost:1313/vi/5-explore-and-configure-the-aws-management-console/5.2-search-with-the-aws-management-console/#search-with-the-aws-management-console)
- [Thêm Vào và Xóa Đi các dịch vụ AWS yêu thích](http://localhost:1313/vi/5-explore-and-configure-the-aws-management-console/5.3-add-and-remove-favorites/#add-and-remove-favorites) 
- [Khởi tạo và sử dụng Dashboard Widgets](http://localhost:1313/vi/5-explore-and-configure-the-aws-management-console/5.4create-and-use-dashboard-widgets/#create-and-use-dashboard-widgets)

> **💡 Mẹo hay**  
> Tùy chỉnh trải nghiệm AWS Management Console của bạn bằng cách thêm các dịch vụ thường sử dụng vào mục yêu thích và tạo các widget dashboard cá nhân hóa để truy cập nhanh vào các số liệu và tài nguyên quan trọng.

> **⚠️ Cảnh báo**  
> Để tăng cường bảo mật, luôn sử dụng người dùng IAM thay vì tài khoản root cho các hoạt động hàng ngày. Tài khoản root chỉ nên được sử dụng cho việc thiết lập ban đầu và các tác vụ quản lý tài khoản quan trọng.

> **ℹ️ Thông tin**  
> Đối với các thao tác AWS Command Line Interface (CLI), tham khảo bài lab: [Sử dụng AWS CLI trên các Amazon EC2 (Windows/Ubuntu)](https://000011.awsstudygroup.com/vi/)