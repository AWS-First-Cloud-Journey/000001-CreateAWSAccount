---
title : "Khóa bảo mật U2F"
date :  "2025-10-05" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---



**Nội dung**
- [Kích hoạt khóa bảo mật U2F qua Console](#kích-hoạt-khóa-bảo-mật-u2f-qua-console)

{{%notice tip%}}
Nếu bạn không có thiết bị phần cứng, bạn có thể bỏ qua các bước bên dưới.
{{%/notice%}}

#### Kích hoạt khóa bảo mật U2F qua Console

**U2F Security Key** là một giao thức xác thực mở cho phép người dùng truy cập các dịch vụ trực tuyến bằng một khóa bảo mật vật lý duy nhất mà không cần cài phần mềm.

1. Đăng nhập vào **AWS Management Console**.
2. Ở góc trên bên phải, chọn tên tài khoản → **My Security Credentials**, sau đó mở rộng **Multi-factor authentication (MFA)**.

3. Để quản lý khóa bảo mật U2F, bạn cần có quyền từ tập quyền sau.  
   Ở thanh bên trái, chọn **Policies** → **Create policy** → tab **JSON** và dán đoạn sau:

```js
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowManageOwnUserMFA",
            "Effect": "Allow",
            "Action": [
                "iam:DeactivateMFADevice",
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}"
        },
        {
            "Sid": "DenyAllExceptListedIfNoMFA",
            "Effect": "Deny",
            "NotAction": [
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}",
            "Condition": {
                "BoolIfExists": {
                    "aws:MultiFactorAuthPresent": "false"
                }
            }
        }
    ]
}
