# 🚀 Hướng dẫn cài đặt RabbitMQ trên Windows

## 📑 Mục lục
- [1. Cài đặt Erlang](#1-cài-đặt-erlang)  
- [2. Cài đặt RabbitMQ](#2-cài-đặt-rabbitmq)  
- [3. Cấp quyền](#3-cấp-quyền)  
- [4. Quản lý service RabbitMQ](#4-quản-lý-service-rabbitmq)  

---
## 1. Cài đặt Erlang
- Tải Erlang OTP bản phù hợp từ: https://www.erlang.org/downloads
- Cài đặt vào thư mục mong muốn, ví dụ: D:\Program Files\Erlang OTP
- Sau khi cài xong, thêm đường dẫn vào **Environment Variables** → `PATH`: D:\Program Files\Erlang OTP\bin

  
## 2. Cài đặt RabbitMQ
- Tải RabbitMQ từ: https://www.rabbitmq.com/download.html
- Cài đặt vào thư mục mong muốn, ví dụ: D:\Program Files\RabbitMQ Server
- Thêm đường dẫn vào **Environment Variables** → `PATH`: D:\Program Files\RabbitMQ Server\rabbitmq_server-<version>\sbin

## 3. Cấp quyền
## 4. Quản lý service RabbitMQ
- Dừng service:
  ```cmd
  net stop RabbitMQ
  ```
- Khởi động lại:
  ```cmd
  net start RabbitMQ
  ```
- Kiểm tra trạng thái:
  ```cmd
  rabbitmqctl status
  ```
- Giao diện quản trị (Management UI)
  ```cmd
  rabbitmq-plugins enable rabbitmq_management
  net stop RabbitMQ
  net start RabbitMQ
  ```
- Truy cập tại: http://localhost:15672/
  ```cmd
  Username: guest
  ```
  ```cmd
  Password: guest
  ```
- Lưu ý : User guest chỉ login được từ localhost.Nếu muốn login từ xa, tạo user mới
