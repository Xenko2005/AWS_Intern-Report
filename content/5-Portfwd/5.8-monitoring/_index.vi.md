---
title: "Dọn dẹp tài nguyên"
weight: 9
chapter: false
pre: " <b> 4.8. </b> "
---

### Tổng quan
Sau khi hoàn thành việc triển khai, thử nghiệm hệ thống **AnTiScaQ** (hoặc kết thúc các bài thực hành Workshop), bước quản trị cuối cùng và cực kỳ quan trọng là **Dọn dẹp tài nguyên (Clean up)**. Việc vô tình để quên các dịch vụ đám mây tiếp tục chạy ngầm khi không còn nhu cầu sử dụng sẽ dẫn đến những khoản chi phí phát sinh không mong muốn trên AWS.

Trong phần này, chúng ta sẽ thực hiện quy trình gỡ bỏ an toàn và dọn dẹp triệt để toàn bộ hệ sinh thái hạ tầng AWS đã được cấp phát cho dự án, bao gồm:

* **Tính toán & Ứng dụng (Elastic Beanstalk, ECR):** Chấm dứt hoàn toàn hoạt động của môi trường backend (Terminate environment) và xóa các kho lưu trữ Docker image của ứng dụng.
* **Lưu trữ & Dữ liệu (RDS, S3):** Xóa vĩnh viễn cơ sở dữ liệu quan hệ MySQL (không tạo bản sao lưu cuối) và dọn dẹp các bucket lưu trữ frontend/tài nguyên tĩnh.
* **Mạng & Phân phối (VPC, CloudFront):** Vô hiệu hóa mạng phân phối nội dung toàn cầu và xóa bỏ hạ tầng mạng ảo nội bộ của ứng dụng.
* **Giám sát (CloudWatch):** Dọn dẹp và gỡ bỏ các luồng cảnh báo (Alarms) tự động đã thiết lập.

### Nội dung thực hiện
* [Dọn dẹp tài nguyên](5.8.1-cloudwatch//)
