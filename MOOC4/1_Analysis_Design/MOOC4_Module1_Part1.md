# **Introduction to System Design and Analysis**

Ở bài **Lecture 1-1: Introduction to System Design and Analysis**, Thầy Kenneth giải quyết một câu hỏi kinh điển mà có lẽ khi làm leader của Team 2 bạn cũng đã từng thắc mắc (hoặc bị các thành viên hối thúc): *"Yêu cầu đã rõ ràng rồi, sao không chia task để anh em nhảy vào gõ code Java luôn cho nhanh mà phải ngồi vẽ sơ đồ làm gì?"*

Dưới đây là phần bóc tách chi tiết lý do tại sao chúng ta phải "phanh" lại để thiết kế:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu được vai trò sinh tử của Phân tích và Thiết kế Hệ thống (Analysis & Design): Chuyển hóa Tài liệu Yêu cầu (SRS / Use Cases) thành một Bản thiết kế (Model) mà các Lập trình viên có thể thực sự hiểu và code được.  
2. Nắm được quy trình 2 bước xây dựng hệ thống: Dựng "khung xương" trước, đắp "da thịt" sau.  
3. Biết cách giải quyết các Yêu cầu Phi chức năng (Non-functional requirements) và Môi trường triển khai (Implementation environment) bằng các Mẫu thiết kế (Design Patterns).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Sự thật phũ phàng về Use Case (Biểu đồ tình huống sử dụng)**

* Khi bạn đi gặp khách hàng và vẽ ra Use Case (ví dụ: "Người dùng đăng nhập", "Hệ thống hiển thị giỏ hàng"), những sơ đồ đó được viết bằng **ngôn ngữ của người dùng**. Nó mang rất nhiều sự mơ hồ (ambiguity).  
* Bạn không thể quăng bản Use Case đó cho một Junior Dev và bảo họ code đi được. Giai đoạn Phân tích & Thiết kế sinh ra để loại bỏ sự mơ hồ đó, dịch mọi thứ sang **ngôn ngữ của Lập trình viên** (quyết định xem sẽ có những Class nào, hàm nào, quan hệ giữa chúng ra sao).

#### **2\. Chiến lược 2 Giai đoạn: "Khung Xương" và "Da Thịt"**

Để không bị ngợp trước một dự án lớn, chúng ta không thiết kế tất cả cùng một lúc:

* **Giai đoạn 1 (Xây dựng Khung xương \- Skeleton):** Thiết lập **Kiến trúc phần mềm (Software Architecture)**. Ở bước này, bạn định hình các khối lớn nhất của hệ thống để tạo ra sự ổn định cốt lõi.  
* **Giai đoạn 2 (Đắp Da thịt \- Growing the system):** Tiến hành phân tích và thiết kế chi tiết (Data analysis & Design). Các Class, các biến, các thuật toán chi tiết sẽ được "đắp" xung quanh cái khung xương ở trên.

#### **3\. Xử lý "Môi trường triển khai" bằng Design Pattern**

Khi lấy yêu cầu, chúng ta thường bỏ qua yếu tố môi trường (VD: Ứng dụng này chạy trên Windows hay Linux? Code bằng Java 8 hay Java 17?). Nhưng đến lúc Thiết kế, bạn bắt buộc phải đối mặt với nó.

* **Ví dụ thực chiến:** Nếu hệ thống của bạn cần đọc/ghi file trên nhiều Hệ điều hành (OS) khác nhau.  
  * *Cách làm tồi (Nhảy vào code luôn):* Viết hàng chục lệnh if (OS \== Windows) thì... else if (OS \== Linux) thì... rải rác khắp nơi. Sau này thêm Mac OS thì sửa code mệt nghỉ.  
  * *Cách làm của Kiến trúc sư (Thiết kế trước):* Tạo ra một Class cầu nối (Bridge class) có tên là FileManager. Mọi logic xử lý file của các OS sẽ nằm gọn trong này. Các hàm nghiệp vụ khác chỉ cần gọi đến FileManager là xong.  
  * Kỹ thuật này gọi là **Bridge Design Pattern** (Mẫu thiết kế Cầu nối) \- thứ giúp code của bạn cực kỳ linh hoạt và dễ bảo trì. (Những pattern thế này chính là "bảo bối" để vượt qua các vòng phỏng vấn Backend tại các ngân hàng hay công ty tài chính lớn đấy).

---

Tóm lại, Thiết kế hệ thống chính là bước bạn tạo ra "Bản vẽ thi công" trước khi đưa cho thợ xây. Bạn đã sẵn sàng để xem cách Thầy Kenneth hướng dẫn dựng "Khung xương" (Architecture) ở bài tiếp theo chưa? Hãy gửi transcript của **Lecture 1-2 Architectural Design and Analysis** lên đây nhé\!

