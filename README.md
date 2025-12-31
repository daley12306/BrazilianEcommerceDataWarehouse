# Dự án Xây Dựng Kho Dữ Liệu từ Nền Tảng Olist tại Brazil

## Mô tả dự án
Dự án này nhằm thiết kế và triển khai một hệ thống kho dữ liệu (Data Warehouse) từ bộ dữ liệu thương mại điện tử Olist - nền tảng marketplace tại Brazil. Dữ liệu phản ánh toàn bộ quy trình mua sắm, thanh toán và vận chuyển của khách hàng.

Thông qua các công cụ Microsoft SQL Server, SSIS, SSAS, Excel và Power BI, nhóm xây dựng quy trình ETL, mô hình dữ liệu đa chiều (Star Schema), triển khai OLAP Cube và trực quan hóa các insight phục vụ phân tích nghiệp vụ.

## Mục tiêu
- Thiết kế kiến trúc kho dữ liệu từ dữ liệu thực tế.
- Thực hiện quy trình ETL bằng SSIS.
- Xây dựng Data Cube trong SSAS để phân tích OLAP.
- Tạo báo cáo phân tích bằng Excel và Power BI.

## Công nghệ sử dụng
- **SQL Server**: Lưu trữ dữ liệu, xử lý truy vấn.
- **SSIS**: Thực hiện ETL.
- **SSAS**: Xây dựng mô hình dữ liệu OLAP.
- **Excel (Pivot Table)**: Phân tích dữ liệu.
- **Power BI**: Trực quan hóa kết quả phân tích.

## Dữ liệu đầu vào
Nguồn dữ liệu từ [Kaggle - Olist Brazilian E-commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

Các bảng chính bao gồm:
- `orders`, `order_items`, `order_reviews`, `order_payments`
- `customers`, `sellers`, `products`, `geolocation`
- `product_category_name_translation`

![Lược đồ dữ liệu](Diagram-Image.png)

## Kiến trúc kho dữ liệu

### Star Schema
- **Fact tables**:
  - `FactSales`: Theo dõi đơn hàng và doanh thu.
  - `FactOrderDelivery`: Theo dõi hiệu quả giao hàng.
  - `FactProductPrice`: Theo dõi giá và số lượng sản phẩm.

- **Dimension tables**:
  - `DimCustomer`, `DimProduct`, `DimOrder`, `DimDate`

## Quy trình ETL
1. Trích xuất dữ liệu từ file CSV.
2. Làm sạch và chuyển đổi dữ liệu.
3. Nạp vào các bảng Staging.
4. Tải lên Data Warehouse sử dụng SCD (Slowly Changing Dimension).

## Phân tích & Báo cáo

### OLAP với SSAS
- Tổng doanh thu theo năm, tháng, ngày.
- Top 10 thành phố có doanh thu cao nhất.
- Hiệu quả giao hàng theo thời gian.
- Phân tích sản phẩm theo danh mục và xu hướng.

### Power BI Dashboard
- Tổng quan đơn hàng, doanh thu, chi phí vận chuyển.
- Phân tích theo thời gian, vị trí, trạng thái đơn hàng.
- Biểu đồ trực quan giúp hỗ trợ ra quyết định.

## Kết quả đạt được
- Thiết kế đầy đủ kho dữ liệu với khả năng mở rộng.
- Trích xuất insight giá trị từ dữ liệu thực tế.
- Hỗ trợ ra quyết định chiến lược trong TMĐT.

## Thành viên nhóm
- Võ Minh Hoàng - 22133021
- Nguyễn Thanh Thiên Phúc - 22133042
- Nguyễn Ngọc Anh Thư (Nhóm trưởng) - 22133059

## Học kỳ II - Năm học 2024-2025  
GV hướng dẫn: **ThS. Nguyễn Văn Thành**  
Trường ĐH Sư phạm Kỹ thuật TP.HCM - Khoa CNTT

---

<br><br><br>

---

# Olist Brazilian E-Commerce Data Warehouse Project

## Project Description
This project focuses on designing and implementing a Data Warehouse system using the Brazilian e-commerce dataset from Olist — a large-scale marketplace platform. The data captures the entire purchasing, payment, and delivery lifecycle of customers.

## Objectives
- Design a Data Warehouse architecture using real-world e-commerce data.
- Perform ETL processes using SSIS.
- Build OLAP cubes in SSAS for multidimensional analysis.
- Visualize insights via Excel Pivot Tables and Power BI dashboards.

## Technologies Used
- **SQL Server**: Data storage and querying.
- **SSIS**: ETL process implementation.
- **SSAS**: OLAP modeling and cube creation.
- **Excel (Pivot Table)**: Pivot-based data exploration.
- **Power BI**: Data visualization and business reporting.

## Input Dataset
Data source: [Kaggle - Olist Brazilian E-commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

Tables used:
- `orders`, `order_items`, `order_reviews`, `order_payments`
- `customers`, `sellers`, `products`, `geolocation`
- `product_category_name_translation`

![Data schema](Diagram-Image.png)

## Data Warehouse Architecture

### Star Schema Model
**Fact tables:**
- `FactSales`: Tracks order count and revenue.
- `FactOrderDelivery`: Monitors delivery performance and timelines.
- `FactProductPrice`: Analyzes product pricing and sales volume.

**Dimension tables:**
- `DimCustomer`, `DimProduct`, `DimOrder`, `DimDate`

## ETL Workflow
1. Extract raw data from CSV files.
2. Clean and transform datasets.
3. Load into staging tables.
4. Load to DW using Slowly Changing Dimensions (SCD).

## Analysis & Reporting

### OLAP via SSAS
- Revenue breakdown by year, month, weekday.
- Top 10 cities by order revenue.
- Delivery performance trends.
- Category-based product performance.

### Power BI Dashboard
- Sales, revenue, and freight overview.
- Insights by time, city, order status.
- Interactive visuals for better decision-making.

## Outcomes
- Scalable and modular warehouse design.
- Actionable insights extracted from historical data.
- Decision-support for e-commerce operations.

## Team Members
- Võ Minh Hoàng – 22133021
- Nguyễn Thanh Thiên Phúc – 22133042
- Nguyễn Ngọc Anh Thư (Team Leader) – 22133059

## Course Information
**Semester II – Academic Year 2024-2025**  
**Supervisor**: *ThS. Nguyễn Văn Thành*  
**Ho Chi Minh City University of Technology and Education – Faculty of IT**
