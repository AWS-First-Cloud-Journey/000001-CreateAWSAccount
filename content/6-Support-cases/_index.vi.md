---
title: "Tạo và Quản Lý Các Trường Hợp Hỗ Trợ trong AWS"
date: "2025-10-05"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Tạo và Quản Lý Các Trường Hợp Hỗ Trợ trong AWS

Hướng dẫn này bao gồm cách tạo và quản lý các trường hợp hỗ trợ trong AWS, bao gồm các loại trường hợp khác nhau, mức độ nghiêm trọng, và quy trình xử lý các yêu cầu hỗ trợ khác nhau.

#### Các Loại Trường Hợp Hỗ Trợ trong AWS

Trong Bảng Điều Khiển Quản Lý AWS, bạn có thể tạo ba loại trường hợp hỗ trợ khách hàng:

1. **Hỗ Trợ Tài Khoản và Thanh Toán**
   - Có sẵn cho tất cả khách hàng AWS cho các yêu cầu liên quan đến thanh toán và tài khoản.

2. **Tăng Giới Hạn Dịch Vụ**
   - Có sẵn cho tất cả khách hàng AWS. Để biết thêm thông tin về hạn mức dịch vụ mặc định, xem tài liệu [hạn mức dịch vụ AWS](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html).

3. **Trường Hợp Hỗ Trợ Kỹ Thuật**
   - Có sẵn cho khách hàng có gói Hỗ Trợ Nhà Phát Triển, Doanh Nghiệp, Enterprise On-Ramp, hoặc Hỗ Trợ Doanh Nghiệp. Không có sẵn cho gói Hỗ Trợ Cơ Bản.

**Lưu ý:**
- Để thay đổi gói hỗ trợ của bạn, xem [Thay đổi Gói Hỗ Trợ AWS](https://docs.aws.amazon.com/premiumsupport/latest/user/change-support-plan.html).
- Để đóng tài khoản, tham khảo [Đóng Tài Khoản](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/close-account.html).
- Đối với các chủ đề khắc phục sự cố phổ biến, kiểm tra [tài nguyên khắc phục sự cố](https://aws.amazon.com/premiumsupport/knowledge-center/).

#### Cách Tạo Trường Hợp Hỗ Trợ

1. Đăng nhập vào [Trung Tâm Hỗ Trợ AWS](https://console.aws.amazon.com/support/home#/).

   **Mẹo:** Trong Bảng Điều Khiển Quản Lý AWS, nhấp vào biểu tượng dấu hỏi ( ? ) và chọn **Trung Tâm Hỗ Trợ**.

2. Chọn **Tạo trường hợp**.

3. Chọn loại trường hợp:
   - **Tài khoản và thanh toán**
   - **Kỹ thuật**
   - Đối với tăng hạn mức dịch vụ, chọn **Tìm kiếm tăng hạn mức dịch vụ?** và làm theo hướng dẫn.

4. Chọn **Dịch vụ**, **Danh mục**, và mức độ **Nghiêm trọng**.

   **Mẹo:** AWS cung cấp các giải pháp được đề xuất cho các câu hỏi thường gặp.

5. Cung cấp các chi tiết sau:
   - **Chủ đề:** Tiêu đề cho trường hợp của bạn.
   - **Mô tả:** Mô tả vấn đề bao gồm thông báo lỗi, các bước khắc phục sự cố, và cách bạn truy cập dịch vụ (Bảng Điều Khiển, CLI, API).
   - (Tùy chọn) **Đính kèm tệp**: Thêm nhật ký lỗi, ảnh chụp màn hình, v.v., tối đa 3 tệp (tối đa 5 MB mỗi tệp).

6. Chọn **Bước tiếp theo: Giải quyết ngay hoặc liên hệ với chúng tôi**.

7. Trên trang **Liên hệ với chúng tôi**, chọn ngôn ngữ và phương thức liên hệ ưa thích của bạn:
   - **Web**: Trả lời trong Trung Tâm Hỗ Trợ.
   - **Trò chuyện**: Trò chuyện trực tiếp với nhân viên hỗ trợ.
   - **Điện thoại**: Nhận cuộc gọi từ nhân viên hỗ trợ (nhập quốc gia, số điện thoại, và phần mở rộng tùy chọn).

**Lưu ý:**
- Các tùy chọn liên hệ phụ thuộc vào loại trường hợp và gói hỗ trợ.
- Bạn có thể hủy bản nháp trường hợp hỗ trợ bằng cách chọn **Hủy bản nháp**.
- Đối với các gói Doanh Nghiệp, Enterprise On-Ramp, hoặc Hỗ Trợ Doanh Nghiệp, các tùy chọn liên hệ bổ sung cho phép bạn thông báo cho người khác về các thay đổi trạng thái.

8. Xem lại chi tiết trường hợp của bạn và chọn **Gửi**. ID trường hợp và tóm tắt sẽ được hiển thị.

#### Mô Tả Vấn Đề Của Bạn

Cung cấp càng nhiều chi tiết càng tốt, bao gồm các tài nguyên AWS liên quan, dấu thời gian, nhật ký, và mô tả môi trường để tăng cơ hội giải quyết nhanh chóng.

#### Mức Độ Nghiêm Trọng và Thời Gian Phản Hồi

Chọn mức độ nghiêm trọng dựa trên tác động đến ứng dụng của bạn. Mức độ nghiêm trọng cao hơn dành cho các vấn đề nghiêm trọng không có giải pháp thay thế.

| Mức Độ Nghiêm Trọng                | Mã Nghiêm Trọng | Thời Gian Phản Hồi Đầu Tiên | Mô Tả (Gói Hỗ Trợ)                                                                                                                                             |
|------------------------------------|-----------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hướng dẫn chung                    | Thấp            | 24 giờ                      | Câu hỏi phát triển chung hoặc yêu cầu tính năng (*Nhà Phát Triển, Doanh Nghiệp, Enterprise On-Ramp, Hỗ Trợ Doanh Nghiệp*)                                     |
| Hệ thống bị suy giảm               | Bình thường     | 12 giờ                      | Các chức năng không quan trọng hoạt động bất thường (*Nhà Phát Triển, Doanh Nghiệp, Enterprise On-Ramp, Hỗ Trợ Doanh Nghiệp*)                                  |
| Hệ thống sản xuất bị suy giảm      | Cao             | 4 giờ                       | Các chức năng ứng dụng quan trọng bị suy giảm hoặc giảm chất lượng (*Doanh Nghiệp, Enterprise On-Ramp, Hỗ Trợ Doanh Nghiệp*)                                    |
| Hệ thống sản xuất ngừng hoạt động  | Khẩn cấp        | 1 giờ                       | Tác động kinh doanh đáng kể, các chức năng quan trọng không khả dụng (*Doanh Nghiệp, Enterprise On-Ramp, Hỗ Trợ Doanh Nghiệp*)                                 |
| Hệ thống kinh doanh quan trọng ngừng hoạt động | Rất nghiêm trọng | 15 phút                     | Các chức năng kinh doanh quan trọng không khả dụng (*Hỗ Trợ Doanh Nghiệp*), 30 phút cho *Hỗ Trợ Enterprise On-Ramp*                                            |

**Lưu ý:** Mã nghiêm trọng không thể thay đổi sau khi tạo trường hợp. Nếu tình huống của bạn thay đổi, hãy làm việc với nhân viên hỗ trợ AWS.

#### Thời Gian Phản Hồi và Giờ Hỗ Trợ

AWS cố gắng phản hồi trong khung thời gian quy định cho mỗi mức độ nghiêm trọng. Đối với các gói Doanh Nghiệp, Enterprise On-Ramp, hoặc Hỗ Trợ Doanh Nghiệp, có sẵn truy cập 24/7. Thời gian phản hồi của Hỗ Trợ Nhà Phát Triển được tính theo giờ làm việc (thường là 8:00 AM - 6:00 PM giờ địa phương, không bao gồm cuối tuần và ngày lễ).

Để biết chi tiết về các tính năng Hỗ Trợ AWS, xem trang [tính năng Hỗ Trợ AWS](https://aws.amazon.com/premiumsupport/features/).

#### Hỗ Trợ Đa Ngôn Ngữ

AWS cung cấp hỗ trợ bằng nhiều ngôn ngữ cho các cấp độ hỗ trợ khác nhau:

- **Tiếng Nhật**: Hỗ trợ kỹ thuật 24/7 cho các gói Doanh Nghiệp, Enterprise On-Ramp, và Hỗ Trợ Doanh Nghiệp. Hỗ trợ nhà phát triển có sẵn trong giờ làm việc của Nhật Bản.
- **Tiếng Trung**: Hỗ trợ kỹ thuật 24/7 cho các gói Doanh Nghiệp, Enterprise On-Ramp, và Hỗ Trợ Doanh Nghiệp. Hỗ trợ nhà phát triển có sẵn trong giờ làm việc của Trung Quốc.
- **Tiếng Hàn**: Hỗ trợ kỹ thuật 24/7 cho các gói Doanh Nghiệp, Enterprise On-Ramp, và Hỗ Trợ Doanh Nghiệp. Hỗ trợ nhà phát triển có sẵn trong giờ làm việc của Hàn Quốc. 