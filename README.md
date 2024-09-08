# Airbyte-practices-
## Overview
Project này sẽ trình bày một số khái niệm cơ bản về tool airbyte, hướng dẫn tính năng khi sử dựng airbyte. Chương trình trong demo được triển khai trên k8s của google cloud cùng với postgree database đặt trong vpc. 
## Airbyte là gì ?
Airbyte là một nền tảng mã nguồn mở giúp kết nối và đồng bộ hóa dữ liệu giữa các hệ thống khác nhau. Nó chủ yếu được sử dụng để di chuyển dữ liệu từ các nguồn dữ liệu (như cơ sở dữ liệu, dịch vụ web, API) vào các kho dữ liệu (như data warehouses) hoặc hệ thống lưu trữ khác.

## Source 
![Screenshot 2024-09-07 211640](https://github.com/user-attachments/assets/60c136f6-4a40-4496-ae8c-263628410aa5)
Để cài đặt điểm để ingest dữ liệu, ta chọn vào mục source trong giao diện Airbyte. Ta sẽ thấy các source đã được tạo, các source ở đây là các kết nối đã được thiết lập từ airbyte đến source để lấy dữ liệu. 
Khi tạo source mới ta có thể chọn nhiều Source đã được Airbyte build sẵn để dễ dàng thiết lập kết nối. 
![image](https://github.com/user-attachments/assets/04c8eed2-87ba-44d1-8ba9-01f945ec156d)
Khi ấn vào một source ta thấy bên trái sẽ là setting cho kết nối: port, databasename, username. Còn bên trái sẽ hướng dẫn về cách setting
![Screenshot 2024-09-08 073307](https://github.com/user-attachments/assets/335b3442-b352-4c84-a26d-1e03a0266103)

