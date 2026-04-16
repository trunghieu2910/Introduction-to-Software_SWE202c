# **Refactoring**

Chào mừng bạn đến với kỹ năng phân định ranh giới giữa một "Coder" (thợ gõ phím) và một "Software Engineer" (Kỹ sư phần mềm thực thụ): **Refactoring (Tái cấu trúc mã nguồn)\!**

Trong giới lập trình có một câu nói nổi tiếng: *"Code chạy được chưa chắc đã là code tốt"*. Bài giảng Lecture 3-3 của Thầy Kenneth sẽ giải thích chính xác tại sao chúng ta phải liên tục "dọn dẹp" mã nguồn của mình.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

Bạn sẽ hiểu được khái niệm Refactoring, nhận diện được hiện tượng "code mục nát" (Code Rot), phân biệt được các cấp độ tái cấu trúc (Thấp và Cao), và biết cách xử lý căn bệnh phổ biến nhất của các lập trình viên mới vào nghề: "God Class" (Lớp Chúa tể).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Tại sao phải sửa Code khi nó không bị lỗi?**

Nhiều lập trình viên (và cả quản lý) có tư duy: *"Nó đang chạy ngon thì đừng có đụng vào\!"*. Tuy nhiên, Thầy Kenneth chỉ ra rằng một đoạn code được sinh ra phải hoàn thành tới **3 mục đích**:

1. Thực thi đúng chức năng (Execute functionality).  
2. Cho phép dễ dàng thay đổi/mở rộng trong tương lai (Allow change).  
3. Giao tiếp tốt với các lập trình viên khác (Communicate well).

Nếu code của bạn chạy đúng, nhưng đọc vào không ai hiểu gì và không thể nâng cấp thêm tính năng mới, thì **đoạn code đó bị coi là hỏng (broken)**.

Nếu không tái cấu trúc, những đoạn vá lỗi tạm bợ (workarounds) sẽ tích tụ lại, dẫn đến hiện tượng **"Code Rots" (Code bị mục nát/bốc mùi)** theo thời gian.

#### **2\. Phân loại Refactoring**

**A. Low-level Refactoring (Tái cấu trúc cấp độ thấp)**

Đây là những thao tác dọn dẹp cơ bản, thường được các công cụ IDE (như IntelliJ, Eclipse, Visual Studio) hỗ trợ làm tự động:

* **Đổi tên (Renaming):** Đừng đặt tên biến là x, y, z hay tên hàm là function1(). Hãy đổi thành studentName, calculateTax().  
* **Tiêu diệt Magic Constants (Hằng số ma thuật):** Không viết if (x \== 40\). Số 40 ở đây chả ai hiểu là gì. Hãy đổi thành một biến có nghĩa: if (enrollment \== MAX\_STUDENTS).  
* **Tách hàm (Extract Method):** Tách một đoạn code dài thành một hàm riêng biệt để dễ gọi lại.

**B. High-level Refactoring (Tái cấu trúc cấp độ cao)**

Đây là việc sắp xếp lại toàn bộ kiến trúc, đòi hỏi tư duy của lập trình viên và **không** có tool nào làm thay được:

* Sửa các cú pháp viết code đánh đố (Ví dụ: Viết lệnh if/else lồng nhau phức tạp trên đúng 1 dòng để ra vẻ "nguy hiểm") thành các dòng code an toàn, trong sáng, dễ hiểu.  
* Áp dụng các Mẫu thiết kế (Design Patterns).  
* Chuyển các hàm/phương thức về đúng "ngôi nhà" tự nhiên của nó.

#### **3\. Căn bệnh "God Class" (Lớp Chúa tể)**

* **Triệu chứng:** Bạn tạo ra một Class khổng lồ tên là MainClass, và nhồi nhét mọi thứ vào đó: từ kiểm tra giỏ hàng, in hóa đơn, tìm kiếm danh mục, kết nối cơ sở dữ liệu... Class này đóng vai "Chúa tể" làm mọi việc trong hệ thống.  
* **Cách chữa trị:** Phân loại lại. Các hàm liên quan đến món đồ (checkout, addItem) thì cắt nó mang sang Item Class. Các hàm liên quan đến danh mục (printCatalog, sortCatalog) thì cắt mang sang Catalog Class.

#### **4\. Quy tắc Sinh tồn khi thêm tính năng vào "Code Rác"**

Khi bạn tiếp nhận một dự án có đống code cực kỳ lộn xộn, bạn tuyệt đối không được nhào vô viết tính năng mới ngay. Quy trình chuẩn phải là:

1. Viết **Unit Tests** cho các tính năng cũ để đảm bảo hiểu rõ chúng đang hoạt động ra sao.  
2. **Refactor** (dọn dẹp, cấu trúc lại) đoạn code đó cho gọn gàng. Lúc này Unit Test sẽ báo cho bạn biết bạn có lỡ làm hỏng chức năng cũ hay không.  
3. Cuối cùng mới **Viết tính năng mới** lên cái nền móng vừa dọn dẹp sạch sẽ đó.

#### **5\. Khi nào nên Refactor?**

Phải làm **Liên tục (Continuously)** trong suốt quá trình phát triển (Code \-\> Refactor \-\> Code \-\> Refactor). Tuyệt đối không để dồn đến cuối dự án mới dọn dẹp, vì lúc đó hệ thống đã quá phức tạp, rút một sợi dây có thể làm sập toàn bộ hệ thống.

---

### **📊 Thực hành: Phân loại Tái cấu trúc**

Hãy đóng vai một Software Engineer đang tiến hành dọn dẹp dự án. Bạn hãy phân loại các hành động chỉnh sửa mã nguồn dưới đây vào đúng nhóm:

