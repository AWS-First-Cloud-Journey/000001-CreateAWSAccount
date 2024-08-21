+++
title = "Thiết lập Region Mặc Định"
date = 2024
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++


#### Set up Default Region

Trong bước này, chúng ta sẽ chọn một Khu vực AWS (Region) cụ thể để quản lý tài nguyên! Với **Region** là tập hợp các tài nguyên AWS nằm trong cùng một khu vực địa lý.

Theo ví dụ trong hình bên dưới, chúng ta đang ở Region Virginia (us-east-1)

![AWS Support](/images/5-console/5.1/1.1.png?width=90pc)

Tuy nhiên, thông thường khách hàng của chúng ta là người dùng cuối ở Việt Nam, vậy Region gần nhất sẽ là Singapore (ap-southeast-1) để giảm độ trễ (latency)

#### Thực hiện chuyển đổi Region

- Bấm vào ký hiệu hình tam giác tại Region Virginia (us-east-1)

![AWS Support](/images/5-console/5.1/2.2.png?width=90pc)

- Chọn Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/3.3.png?width=90pc)

- Kết quả thể hiện trên thanh điều hướng đã là Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/4.png?width=90pc)

Ngoài ra, để đảm bảo chúng ta luôn hiện diện tại đúng Region phù hợp với yêu cầu của tổ chức mỗi khi đăng nhập vào AWS console, thì việc thiết lập Vùng mặc định (default Region) là rất cần thiết.

#### Thiết lập Region mặc định

- Trọn ký hiệu bánh răng trên thành điều hướng

![AWS Support](/images/5-console/5.1/5.png?width=90pc)

- Chọn **More user settings**

![AWS Support](/images/5-console/5.1/6.png?width=90pc)

- Tại mục **Localization and default Region** chọn **Edit**

![AWS Support](/images/5-console/5.1/7.png?width=90pc)

- Tại mục **Default Region** chọn biểu tượng tam giác

![AWS Support](/images/5-console/5.1/8.png?width=90pc)

- Chọn **Asia Pacific (Singapore) ap-southeast-1**, chọn **Save settings**

![AWS Support](/images/5-console/5.1/9.png?width=90pc)

- Kết quả:

![AWS Support](/images/5-console/5.1/10.png?width=90pc)

**Lưu Ý:** việc thiết lập Region mặc định rất quan trọng, tránh trường hợp triển khai các dịch vụ trên AWS Region khác mà không đúng với định hướng ban đầu

Chúc mừng Bạn đã hoàn thành bài lab