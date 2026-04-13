Với dự án website thương mại điện tử thời trang mà bạn đang xây dựng, **Sơ đồ lớp (Class Diagram)** ở mô-đun này chính là công cụ đắc lực nhất. Nó ánh xạ trực tiếp ra các file `.java` và các bảng trong cơ sở dữ liệu SQL của bạn. Thay vì cắm cúi gõ code ngay và dễ dẫn đến lỗi logic, bạn chỉ cần thiết kế chuẩn sơ đồ này, sau đó việc code sẽ giống như trò chơi "điền vào chỗ trống".

Dựa vào các bài giảng bạn đã hoàn thành, đây là 3 khái niệm cốt lõi nhất cần nắm vững:

* **Class Diagram (Sơ đồ Lớp):** Mỗi hình chữ nhật trong sơ đồ đại diện cho một thực thể trong hệ thống (ví dụ: `User`, `Product`, `Order`). Nó được chia làm 3 ngăn: Tên Lớp, Thuộc tính (Attributes \- ví dụ: `price`, `color`), và Phương thức (Operations \- ví dụ: `addToCart()`).  
* **Association (Mối quan hệ Kết hợp):** Đây là mối quan hệ cơ bản nhất, thể hiện hai Lớp "biết" và tương tác với nhau. Ví dụ: `Customer` (Khách hàng) có thể "thực hiện" nhiều `Order` (Đơn hàng).  
* **Aggregation (Mối quan hệ Tập hợp):** Đây là mối quan hệ "Toàn thể \- Bộ phận" (Has-a) mang tính chất lỏng lẻo. Ví dụ: Một `ShoppingCart` (Giỏ hàng) sẽ chứa nhiều `Product` (Quần áo). Điểm mấu chốt là: Nếu bạn xóa đối tượng Giỏ hàng đi, đối tượng Quần áo **vẫn tồn tại** độc lập trong kho hàng.

Trong thiết kế UML, các mối quan hệ này được phân biệt bằng các loại mũi tên rất đặc trưng. Để giúp bạn dễ nhớ cách vẽ chúng trước khi làm các bài tập thực hành (phần Exercise đang bị làm mờ trong ảnh), mình đã tạo một công cụ mô phỏng trực quan dưới đây:

