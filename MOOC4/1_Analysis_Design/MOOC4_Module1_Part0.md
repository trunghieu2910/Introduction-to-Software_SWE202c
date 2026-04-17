 **System Analysis and Design** 

Nếu ở MOOC 3, chúng ta đã "thực chiến" với code và test, thì ở Mô-đun 1 này, chúng ta sẽ lùi lại một bước để nhìn bức tranh lớn hơn. Đây là giai đoạn **"Vẽ kiến trúc trước khi xây nhà"**.

Việc phân tích và thiết kế hệ thống tốt sẽ giúp bạn tránh được cảnh "đập đi xây lại" code – nỗi ác mộng của mọi Software Engineer. Đặc biệt là với các hệ thống yêu cầu độ ổn định cao như tại MBBank hay MCredit mà bạn đang hướng tới, khâu này cực kỳ quan trọng.

Dưới đây là lộ trình chúng ta sẽ cùng đi qua trong Mô-đun 1:

---

### **🗺️ Tổng quan lộ trình Mô-đun 1**

* **Lecture 1-1: Introduction to System Design and Analysis (4 phút):** Bài mở đầu giúp bạn hiểu rõ khái niệm Phân tích (Analysis) khác với Thiết kế (Design) như thế nào. Bạn sẽ thấy tại sao chúng ta cần dành thời gian ngồi "vẽ vời" sơ đồ thay vì nhảy vào code ngay.  
* **Lecture 1-2: Architectural Design and Analysis (12 phút):** Đây là bài học về "Cấp độ cao nhất". Bạn sẽ học về các cấu trúc lớn của hệ thống (như Client-Server, Layered Architecture...). Nó giúp bạn quyết định xem hệ thống Java Backend của bạn sẽ kết nối với Database và Mobile app như thế nào cho tối ưu.  
* **Lecture 1-3: Use Case Analysis (10 phút):** Quay trở lại với "Yêu cầu của người dùng". Ở đây chúng ta sẽ đào sâu hơn cách chuyển từ một cái Use Case (người dùng muốn làm gì) sang cấu trúc hệ thống bên trong.  
* **Lecture 1-4: Class Design (3 phút):** Cụ thể hóa các Class. Bạn sẽ học cách xác định các thuộc tính, phương thức sao cho đúng tinh thần hướng đối tượng (OOP) nhất.  
* **Bài tập Thực hành (System Design Optimization):** Bạn sẽ được thử sức tối ưu hóa một bản thiết kế có sẵn. Đây là kỹ năng phân biệt giữa một người biết code và một người biết thiết kế hệ thống tốt.

---

### **💡 Gợi ý tư duy cho bạn:**

Trong quá trình học mô-đun này, hãy luôn liên tưởng đến dự án **"Smart Access Control"** (Kiểm soát ra vào thông minh) mà bạn đã làm.

* **Analysis:** Là lúc bạn xác định: "Hệ thống cần nhận diện vân tay, mở khóa và ghi log".  
* **Design:** Là lúc bạn quyết định: "Dùng ESP32 làm trung tâm, kết nối với cảm biến vân tay qua cổng Serial, và gửi dữ liệu lên server qua Wi-Fi".

