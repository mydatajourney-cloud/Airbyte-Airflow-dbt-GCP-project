# Airbyte-projects
Airbyte
-Source: tính năng Source trong Airbyte là thành phần kết nối và trích xuất dữ liệu từ các nguồn dữ liệu khác nhau như cơ sở dữ liệu, dịch vụ web, hoặc ứng dụng. Source chịu trách nhiệm thiết lập kết nối, cấu hình truy vấn, và đồng bộ hóa dữ liệu để cung cấp dữ liệu cho các quy trình tiếp theo trong hệ thống tích hợp của Airbyte.
![Picture1](https://github.com/user-attachments/assets/0e6b156d-8acc-4a65-9cd0-07b627eac8a4)

Để thiết lập một kết nối Source tới MySQL trong Airbyte, bạn có thể làm theo các bước sau:
Bước 1: Tạo một Source mới
1.Trên trang chính của Airbyte, nhấp vào “Sources” trong menu điều hướng.
2.Nhấp vào nút “+ New Source” hoặc “Add Source”.
![image](https://github.com/user-attachments/assets/86051a4b-9fa0-47f1-96ca-bbca38aeb054)

Bước 2: Chọn MySQL làm loại nguồn dữ liệu
1.Trong danh sách các nguồn dữ liệu, chọn “MySQL”.
![image](https://github.com/user-attachments/assets/21a71df1-3646-4b99-9bc8-1a455ea98b2f)

Bước 3: Cung cấp thông tin kết nối
1.Điền các thông tin cần thiết vào biểu mẫu cấu hình nguồn MySQL:
1.Host: Địa chỉ IP hoặc tên miền của máy chủ MySQL.
2.Port: Cổng mà MySQL đang lắng nghe (mặc định là 3306).
3.Database: Tên cơ sở dữ liệu mà bạn muốn kết nối.
4.Username: Tên người dùng để kết nối vào cơ sở dữ liệu MySQL.
5.Password: Mật khẩu tương ứng với tên người dùng.
6.Additional Parameters (tùy chọn): Cung cấp bất kỳ tham số bổ sung nào nếu cần (ví dụ: mã hóa SSL).

Bước 4: Lưu cấu hình
1.Nếu kết nối thành công, nhấp vào “Set up source” hoặc “Save” để lưu cấu hình nguồn dữ liệu

- Destination: tính năng Destination trong Airbyte là thành phần chịu trách nhiệm lưu trữ và xử lý dữ liệu sau khi được trích xuất từ các nguồn dữ liệu. Nó kết nối với các hệ thống lưu trữ, cơ sở dữ liệu, hoặc kho dữ liệu (như BigQuery, Snowflake, hoặc Amazon Redshift) để nhận và lưu trữ dữ liệu, đồng thời hỗ trợ các tùy chọn cấu hình như xác định dataset, cấu trúc bảng, và phương thức đồng bộ hóa 
Để thiết lập một kết nối Destination tới BigQuery trong Airbyte, hãy thực hiện theo các bước sau:
Bước 1: Truy cập Airbyte
1.Mở trình duyệt web và đăng nhập vào giao diện quản lý Airbyte.
![Picture2](https://github.com/user-attachments/assets/db635b4e-1bb8-4fc5-9b77-8a7b36523f5e)

Bước 2: Tạo một Destination mới
1.Trên trang chính của Airbyte, nhấp vào “Destinations” trong menu điều hướng.
2.Nhấp vào nút “+ New Destination” hoặc “Add Destination”.
3.Trong danh sách các đích dữ liệu, chọn “BigQuery”.
![image](https://github.com/user-attachments/assets/909ac9dc-74b7-46ba-a229-eec305957359)

Bước 3: Cung cấp thông tin cấu hình BigQuery
1.Điền các thông tin cần thiết vào biểu mẫu cấu hình đích BigQuery:
1.Project ID: ID của dự án Google Cloud nơi BigQuery được cấu hình.
2.Dataset: Tên dataset mà bạn muốn lưu dữ liệu vào trong BigQuery.
3.JSON Key File: Tải lên tệp JSON chứa khóa dịch vụ của tài khoản Google Cloud có quyền truy cập vào BigQuery. (Tệp này có thể được tạo từ Google Cloud Console).
![image](https://github.com/user-attachments/assets/379ead50-1407-41d2-b548-5b26b530ed5c)

Bước 4: Lưu cấu hình
1.Nếu kết nối thành công, nhấp vào “Set up destination” hoặc “Save” để lưu cấu hình đích dữ liệu.
-Connection: là một cấu hình liên kết giữa một Source (nguồn dữ liệu) và một Destination (đích dữ liệu), cho phép truyền tải và đồng bộ hóa dữ liệu từ nguồn đến đích. Tính năng này cho phép bạn thiết lập các chế độ đồng bộ hóa (như full refresh hoặc incremental), cấu hình các tùy chọn đồng bộ hóa như tần suất và khóa chính, và quản lý cách dữ liệu được chuyển giao giữa các hệ thống.
Để thiết lập một kết nối Connection hãy làm theo các bước sau:
Bước 1: Truy cập Airbyte
1.Mở trình duyệt web và đăng nhập vào giao diện quản lý Airbyte.
![Picture3](https://github.com/user-attachments/assets/0180224c-5588-46d5-bcb7-f6eef484e49b)


Bước 2: Tạo một Connection mới
1.Trên trang chính của Airbyte, nhấp vào “Connections” trong menu điều hướng.
2.Nhấp vào nút “+ New Connection” hoặc “Add Connection”.
Bước 3: Chọn Source và Destination
1.Trong phần cấu hình Connection, chọn Source và Destination từ danh sách các nguồn và đích đã được tạo trước đó.
1.Source: Chọn nguồn dữ liệu mà bạn đã cấu hình trước đó.
![Picture4](https://github.com/user-attachments/assets/80a08b17-5aa1-40ac-a885-95a330ac64ad)

2.Destination: Chọn đích dữ liệu mà bạn đã cấu hình trước đó.
![Picture5](https://github.com/user-attachments/assets/2ee404a1-76fb-4319-929a-264008ea2e3f)

Bước 4: Cấu hình đồng bộ hóa dữ liệu
1.Configure Sync Options:
1.Sync Mode: Chọn chế độ đồng bộ hóa dữ liệu “Append Historical Changes” và chọn “Append New Rows and Updates Only” 
![Picture6](https://github.com/user-attachments/assets/1147879c-36ea-4fa4-92cb-5c24d168267f)

2.Field Mapping:
1.Chọn schema: Chọn các toàn bộ các table đưa vào BigQuery bằng cách ấn vào nút “Sync”
![Picture7](https://github.com/user-attachments/assets/6c3963c1-f051-441f-8470-23804e30076b)

Bước 5: Xem trước và kiểm tra kết nối
1.Setup Sync Frequency: Chọn tần suất đồng bộ hóa (ví dụ: theo lịch trình hàng ngày, hàng giờ, hoặc đồng bộ hóa theo yêu cầu).
![Picture7](https://github.com/user-attachments/assets/4bc29415-02d6-4d04-bbc1-97a4fd90afe7)

2.Test Connection: (Tùy chọn) Kiểm tra kết nối để xác nhận rằng dữ liệu có thể được đồng bộ hóa từ Source đến Destination thành công.
Bước 7: Lưu và kích hoạt Connection
1.Nhấp vào “Save” hoặc “Create Connection” để lưu cấu hình.
2.Start Sync: Nếu bạn đã cấu hình tần suất đồng bộ hóa, kết nối sẽ tự động bắt đầu theo lịch trình. Bạn cũng có thể nhấp vào “Manual Sync” để thực hiện đồng bộ hóa ngay lập tức
 



