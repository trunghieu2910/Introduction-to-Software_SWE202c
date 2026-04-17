**State Machine Diagram (Sơ đồ Máy trạng thái)**

Nếu ở Mô-đun 1, bạn đã học cách thiết kế "thể xác" của hệ thống (các Class tĩnh), thì ở Mô-đun 2 này, Thầy Kenneth sẽ hướng dẫn bạn cách thổi "linh hồn" vào đó. Phần mềm thực tế luôn vận động và biến đổi liên tục dựa trên các tác động từ bên ngoài.

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung của mô-đun này dựa trên lộ trình bạn đã cung cấp:

### **🎯 Mục Tiêu Của Mô-đun 2**

1. **Chuyển đổi tư duy từ Tĩnh sang Động:** Hiểu được rằng một đối tượng (Object) không chỉ có thuộc tính và phương thức, mà còn có một "vòng đời" với nhiều trạng thái khác nhau.  
2. **Làm chủ công cụ State Machine Diagram:** Học cách vẽ sơ đồ để kiểm soát chặt chẽ các hành vi của hệ thống, bao gồm các khái niệm cốt lõi: Trạng thái (State), Sự kiện kích hoạt (Event), Sự chuyển đổi (Transition), và Điều kiện chắn (Guard).  
3. **Phòng chống lỗi Logic:** Sử dụng sơ đồ này để đảm bảo hệ thống không bao giờ bị kẹt ở một trạng thái "chết" (Deadlock) hoặc thực hiện những hành vi vô lý (ví dụ: giỏ hàng đang trống nhưng lại cho phép bấm nút thanh toán).

---

### **🗺️ Nội Dung Chi Tiết (Core Content)**

Dựa vào danh sách bài học, chúng ta sẽ đi qua các phần sau:

* **Lecture 2-1: State Machine Diagram (Video • 11 phút):** Đây là bài học lý thuyết nền tảng. Bạn sẽ được làm quen với các ký hiệu UML chuẩn mực để vẽ Sơ đồ Máy trạng thái và cách định nghĩa các quy tắc chuyển đổi.  
* **Lecture 2-2: State Machine Diagram Example (Video • 11 phút):** Thầy Kenneth sẽ trực tiếp áp dụng lý thuyết vừa học vào một bài toán thực tế (rất có thể là hệ thống quen thuộc \- Đăng ký khóa học) để bạn thấy cách một trạng thái biến đổi như thế nào khi có sự kiện xảy ra.  
* **Lecture 2 \- System Analysis and Design (Bài đọc • 1h):** Tài liệu đọc chuyên sâu giúp bạn củng cố lại mối liên kết giữa Phân tích hệ thống (Mô-đun 1\) và Thiết kế trạng thái (Mô-đun 2).  
* **Lecture 2 \- State Machine Diagram Exercise (Bài đọc • 1h):** Phần thực hành tối quan trọng. Bạn sẽ tự tay phân tích một Use Case và vẽ ra vòng đời của nó.  
* **Lecture 2 \- State Machine Diagram Exercise (Solution) (Bài đọc • 1h):** Đối chiếu kết quả thiết kế của bạn với đáp án chuẩn của chuyên gia.

---

### **💡 Liên hệ thực tế với dự án của bạn:**

Hãy nhớ lại dự án **Smart Access Control (Kiểm soát ra vào thông minh)** mà Team 2 đã làm. Cánh cửa của bạn chính là một "Máy trạng thái" kinh điển:

* Trạng thái 1: **LOCKED** (Đang khóa).  
* Sự kiện: Người dùng đặt tay lên cảm biến (Fingerprint detected).  
* Trạng thái 2: **AUTHENTICATING** (Đang xác thực).  
* Điều kiện (Guard): *Nếu vân tay đúng* \-\> Chuyển sang Trạng thái 3: **UNLOCKED** (Mở khóa). *Nếu vân tay sai* \-\> Trở về trạng thái **LOCKED** và kêu còi báo động.

Việc vẽ sơ đồ này trước khi code C++ cho mạch ESP32/Arduino sẽ giúp bạn nhắm mắt cũng code được rành mạch mà không sợ lỗi logic.

Bạn đã sẵn sàng đi sâu vào lý thuyết chưa? Hãy ném transcript của **Lecture 2-1 State Machine Diagram** lên đây để chúng ta bắt đầu "mổ xẻ" nhé\!

