# **Use Case Analysis**

Chào mừng bạn đến với **Lecture 1-3: Use Case Analysis**\!

Nếu ở bài trước chúng ta nhìn hệ thống từ trên trời nhìn xuống (chia thành các cục Subsystem to đùng), thì ở bài này, Thầy Kenneth sẽ hạ cánh xuống mặt đất. Chúng ta sẽ "mổ xẻ" một Use Case (Ví dụ: Chức năng Đăng nhập) để xem bên trong nó cần những "mảnh ghép" nào để hoạt động.

Đây là một bài học mang tính nền tảng cực kỳ cao. Nó giới thiệu mô hình **B-C-E (Boundary \- Control \- Entity)** – cha đẻ của mô hình MVC (Model-View-Controller) mà bạn đang dùng hàng ngày\!

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu khái niệm **Analysis Class (Lớp phân tích)**: Đây là những bản nháp mang tính khái niệm (conceptual), chưa dính dáng gì đến ngôn ngữ lập trình (Java/C++) hay kiểu dữ liệu cụ thể.  
2. Phân loại được 3 mảnh ghép cấu thành nên bất kỳ chức năng nào: **Boundary (Biên)**, **Control (Điều khiển)**, và **Entity (Thực thể)**.  
3. Nắm vững **"Quy tắc giao tiếp Vàng"** giữa 3 loại Class này để đảm bảo hệ thống không bị "nhập nhằng" và dễ bảo trì.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Ba (03) Loại Lớp Phân Tích (Analysis Classes)**

Mọi chức năng phần mềm đều được cấu thành từ 3 thành phần này:

* **Boundary Class (Lớp Biên \- Giao diện):**  
  * **Bản chất:** Nơi hệ thống giao tiếp với thế giới bên ngoài (Người dùng hoặc Hệ thống khác).  
  * **Ví dụ:** Màn hình Đăng nhập (Login UI), API nhận dữ liệu từ ngân hàng.  
  * **Lưu ý:** Ở bước này, ta chỉ nói chung chung là "Cần một màn hình Đăng nhập", KHÔNG vẽ chi tiết nút bấm màu gì, text box để ở đâu.  
* **Entity Class (Lớp Thực thể \- Dữ liệu):**  
  * **Bản chất:** Chứa các dữ liệu sống thọ (long-lived), thường được lưu xuống Database. Nó đại diện cho các sự vật, hiện tượng trong đời thực.  
  * **Ví dụ:** Sinh viên, Khóa học, Hóa đơn.  
* **Control Class (Lớp Điều khiển \- Logic):**  
  * **Bản chất:** Là "bộ não" (Business logic), là chất keo kết dính Giao diện và Dữ liệu. Nó kiểm soát luồng chạy của chương trình.  
  * **Ví dụ:** Trình quản lý Đăng ký môn học (RegistrationManager), Hàm kiểm tra mật khẩu hợp lệ.  
  * **Lưu ý:** Mỗi Control Class chỉ nên phục vụ cho **Tối đa 1 Actor (Người dùng)** để đảm bảo khi yêu cầu của người đó thay đổi, ta không làm hỏng logic của người khác.

#### **2\. Quy tắc Giao tiếp Vàng (Thiết kế để thay đổi)**

Tại sao phải chia làm 3 loại nhọc nhằn như vậy? Mục đích tối thượng là **Localization of changes (Khoanh vùng sự thay đổi)**. Nếu khách hàng muốn đổi giao diện từ Web sang App Mobile, ta chỉ đập đi viết lại Boundary, giữ nguyên Control và Entity.

Để làm được điều đó, Thầy Kenneth đưa ra quy tắc giao tiếp cực kỳ nghiêm ngặt:

1. **Actor (Người dùng)** CHỈ ĐƯỢC giao tiếp với **Boundary**.  
2. **Boundary** CHỈ ĐƯỢC giao tiếp với **Control** (Không có chuyện Giao diện A gọi thẳng Giao diện B).  
3. **Entity** CHỈ ĐƯỢC giao tiếp với **Control** (Hai bảng dữ liệu không được tự nói chuyện với nhau).  
4. **Control** được phép giao tiếp với tất cả mọi thứ (Boundary, Entity, và các Control khác).

👉 **Nói tóm lại:** Mọi thứ đều phải đi qua "anh cò" Control. Không ai được đi đường tắt\! Lập trình viên rất hay mắc lỗi cho Giao diện (UI) chọc thẳng xuống Database (Entity) để lấy data cho nhanh, điều này phá vỡ hoàn toàn kiến trúc hệ thống\!

---

