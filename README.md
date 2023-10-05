# Kafka-streaming-data
Creating Streaming Data Pipelines using Kafka

# OVERVIEW
Dự án nhằm giảm ùn tắc trên các tuyến đường quốc lộ bằng cách phân tích dữ liệu giao thông đường bộ từ các trạm thu phí khác nhau. Khi một phương tiện đi qua trạm thu phí, dữ liệu của phương tiện như Vehicle_id, vehicle_type, toll_plaza_id và timestamp sẽ được truyền tới Kafka. Công việc là tạo một đường ống dữ liệu để thu thập dữ liệu phát trực tuyến và tải nó vào cơ sở dữ liệu.

# OBJECTIVES
Trong nhiệm vụ này, tạo một đường ồng dữ liệu streaming data bằng các thực hiện các bước sau:
- Tạo bảng chứa dữ liệu truyền về
- Khởi động máy chủ Kafka
- Cài đặt Kafka Python driver
- Cài đặt MySQL python driver
- Tạo topic có tên "toll" trong Kafka
- Chương trình giả lập tạo dữ liệu streaming data
- Tùy chỉnh chương trình máy phát điện để thu phí theo chủ đề.
- Tải xuống và tùy chỉnh dữ liệu phát trực tuyến của người tiêu dùng.
- Tùy chỉnh chương trình tiêu dùng để ghi vào bảng cơ sở dữ liệu MySQL.
- Xác minh rằng dữ liệu truyền phát đang được thu thập trong bảng cơ sở dữ liệu.

# PROCESS
### 1. Tạo database và table chứa dữ liệu truyền về
![create database](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/66ad47d0-609c-48ec-b0c6-8086feeec516)
