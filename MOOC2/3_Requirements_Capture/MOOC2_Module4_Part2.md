

# **Domain Modeling \- Evaluating Classes**

Chào mừng bạn đến với giai đoạn cực kỳ thú vị của Kỹ nghệ Phần mềm\! Ở bài học này, chúng ta sẽ cất các công cụ vẽ sang một bên để học cách **"đọc hiểu tâm lý khách hàng"**.

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Mục tiêu cốt lõi của bài 4-2 là dạy bạn kỹ năng **Trích xuất (Extraction) và Đánh giá (Evaluation)**. Bạn sẽ học cách cầm một đoạn văn bản yêu cầu dài ngoằng của khách hàng, đọc lướt qua nó, và biết chính xác từ nào sẽ trở thành Class, từ nào là Thuộc tính, và từ nào là "từ rác" cần phải vứt bỏ khỏi bản thiết kế.

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

Giáo sư Kenneth đã đưa ra một bộ quy tắc cực kỳ thực chiến giúp bạn "phiên dịch" ngôn ngữ đời thường sang ngôn ngữ UML:

#### **1\. Quy tắc Ánh xạ Từ vựng (Vocabulary Mapping)**

Khi đọc tài liệu yêu cầu (Prompt statement), hãy cầm bút dạ quang và gạch chân theo quy luật sau:

* **Danh từ (Nouns) & Cụm danh từ:** Đây chính là các "ứng cử viên" sáng giá để biến thành **Class (Lớp)**.  
  * *Lưu ý:* Luôn đổi chúng sang dạng số ít (Singular) khi vẽ UML (Ví dụ: Đọc thấy "Students", khi vẽ Class phải ghi là "Student").  
* **Động từ (Verbs) & Cụm động từ:** Đây chính là các **Association (Mối liên kết)** giữa các Class.  
  * *Lưu ý:* Dùng thể chủ động (Active form) cho dễ đọc (Ví dụ: Dùng "Đăng ký" thay vì "Được đăng ký bởi").  
* **Cụm từ Sở hữu (Possessive phrases):** Các danh từ đi kèm với sự sở hữu thường là **Attribute (Thuộc tính)**.  
  * *Ví dụ:* "Password **of** student" (Mật khẩu của sinh viên) \-\> Password là thuộc tính của Class Student.

#### **2\. Nguyên lý "Không có đáp án đúng duy nhất"**

Giáo sư nhấn mạnh: **Domain Modeling phụ thuộc vào kinh nghiệm và sự phán đoán của kỹ sư.**

Sẽ không có một cái sơ đồ UML nào gọi là "đáp án chuẩn xác 100%" cho một yêu cầu của khách hàng. Việc bạn chọn thiết kế sơ đồ theo hướng A hay hướng B hoàn toàn là lựa chọn thiết kế (Design choice). Miễn sao nó giải quyết được bài toán\!

#### **3\. Bộ lọc "Nhặt Sạn" (Evaluating Classes)**

Bạn sẽ gạch dưới được hàng tá danh từ, nhưng **KHÔNG PHẢI danh từ nào cũng được làm Class**. Dưới đây là 7 màng lọc để bạn loại bỏ các Class "rác":

1. **Irrelevant (Không liên quan):** Nhắc đến cho vui, không cần lưu trữ trong hệ thống \-\> *Loại bỏ.*  
2. **Vague (Mơ hồ):** Những từ quá chung chung như "Thông tin" (Information), "Dữ liệu" (Data) \-\> *Loại bỏ hoặc phải làm rõ ra (Ví dụ: Thông tin gì? Thông tin cá nhân hay Thông tin thanh toán?).*  
3. **Redundant (Trùng lặp):** Hai danh từ cùng chỉ một thứ. Ví dụ khách hàng vừa dùng chữ "Lớp học" (Classes) vừa dùng chữ "Khóa học" (Courses) \-\> *Gộp lại, chỉ giữ một từ mô tả chuẩn nhất.*  
4. **Should be Attribute (Bản chất là Thuộc tính):** Nó là một mảnh dữ liệu nhỏ thuộc về một vật khác chứ không thể đứng độc lập \-\> *Biến nó thành Thuộc tính (Attribute).*  
5. **Should be Role (Bản chất là Vai trò):** Từ này mô tả vai trò của một đối tượng trong một mối quan hệ \-\> *Ghi nó lên sợi dây liên kết làm Role Name, không vẽ thành Class.*  
6. **Operations/Actions (Bản chất là Hành động):** Một số danh từ thực chất ám chỉ một chức năng/hành động \-\> *Biến nó thành Hàm (Method) hoặc vứt bỏ.*  
7. **Implementation Constructs (Cấu trúc triển khai):** Ví dụ điển hình nhất là từ **"Hệ thống" (System)**. Khách hàng hay nói "Hệ thống phải lưu...", nhưng bạn ĐỪNG BAO GIỜ vẽ một Class tên là "System" vào sơ đồ UML. Vì toàn bộ bản vẽ của bạn chính là cái System đó rồi\! \-\> *Loại bỏ.*

---

