# **Class Design**

Chào mừng bạn đến với chặng dừng chân cuối cùng của Mô-đun 1: **Lecture 1-4: Class Design**\!

Nếu 3 bài học trước là lúc bạn cầm bút vẽ bản nháp khái niệm trên giấy, thì bài học này chính là khoảnh khắc bạn mở IDE lên để định hình cấu trúc code thực tế. Những khái niệm Boundary, Entity, Control bây giờ sẽ phải "biến hình" thành các Class thực sự trong Java.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu cách chuyển đổi Lớp phân tích (Analysis Class) sang Lớp thiết kế (Design Class) gắn liền với công nghệ thực tế.  
2. Cụ thể hóa đặc tả của một Class (Thuộc tính, Phương thức, Kiểu dữ liệu, Tầm vực).  
3. Nắm vững "Kim chỉ nam" của Lập trình Hướng đối tượng (OOP): **High Cohesion (Độ gắn kết cao)** và **Loose Coupling (Độ liên kết thấp)**.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Đưa công nghệ vào Bản vẽ (Implementation Domain)**

Khi thiết kế Class, bạn không thể nói chung chung nữa mà phải gắn nó với hệ sinh thái công nghệ bạn đang dùng:

* **Boundary Classes:** Chuyển hóa thành công nghệ UI. (Ví dụ: Nó sẽ là các trang JSP, hoặc các hàm API endpoint).  
* **Entity Classes:** Chuyển hóa thành công nghệ Quản lý dữ liệu. (Ví dụ: Nó sẽ là các class Model/DTO được map thẳng xuống các bảng trong SQL Server thông qua JDBC).  
* **Control Classes:** Chuyển hóa thành các class Xử lý logic (Controllers/Services), chịu trách nhiệm tính toán, quản lý luồng (transactions).

#### **2\. Hoàn thiện Đặc tả Class (Completing the Specification)**

Mỗi Class bây giờ phải được định nghĩa cực kỳ chặt chẽ bằng ngôn ngữ lập trình:

* Xác định rõ **Attributes (Thuộc tính)** và kiểu dữ liệu cụ thể (String, int, boolean...).  
* Xác định rõ **Operations (Phương thức)**.  
* Thiết lập **Visibility (Tầm vực)**: Cái nào là private để che giấu thông tin (Encapsulation), cái nào là public để bên ngoài gọi được.

#### **3\. Active Classes (Lớp Chủ động)**

Đa số các class bình thường nằm im chờ được gọi. Nhưng **Active Class** là một khái niệm đặc biệt: Nó sở hữu một **Thread (Luồng) điều khiển riêng**.

*(Mẹo thực chiến: Khái niệm này cực kỳ quan trọng khi bạn xử lý dữ liệu thời gian thực. Ví dụ, một class liên tục chạy ngầm trong một vòng lặp while(true) để lắng nghe tín hiệu RFID hoặc cảm biến vân tay gửi về từ vi điều khiển chính là một Active Class).*

#### **4\. Tối ưu hóa và Hai Nguyên lý "Vàng"**

Trọng tâm lớn nhất của bài học này là cách bạn đánh giá xem kiến trúc các class mình vừa tạo ra có "sạch" hay không. Thầy Kenneth đưa ra 2 thước đo sống còn:

* **High Cohesion (Độ gắn kết cao):** \* Một class chỉ nên làm ĐÚNG MỘT VIỆC (Single Responsibility).  
  * Nếu một class vừa lo tính toán, vừa lo kết nối database, vừa lo in hóa đơn... nó sẽ biến thành một **"God Class" (Lớp Chúa Tể)**. Việc bảo trì một God Class là ác mộng vì đụng vào đâu cũng sợ vỡ logic chỗ khác.  
* **Loose Coupling (Độ liên kết lỏng lẻo):**  
  * Là thước đo xem một class phụ thuộc vào *bao nhiêu* class khác.  
  * OOP hướng tới Loose Coupling. Nếu Class A gọi Class B, nó chỉ nên gọi thông qua các hàm public (Interface) chứ không được chọc thẳng vào các biến private của Class B. Nhờ đó, người ta có thể thoải mái sửa code bên trong Class B mà Class A không hề bị chết theo.

---

