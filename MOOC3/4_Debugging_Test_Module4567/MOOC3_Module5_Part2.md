# **Design Tests**

Chào mừng bạn đến với phần tiếp theo của hành trình "phá hoại có hệ thống". Ở bài giảng **Lecture 5-2: Design Tests**, Thầy Kenneth đã chính thức đưa ra các định nghĩa chuẩn mực nhất về các loại hình kiểm thử và giải thích lý do tại sao tư duy "code chạy qua hết các dòng là được" lại cực kỳ nguy hiểm.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Nắm vững định nghĩa và 5 bước vòng đời chuẩn để thực thi một **Test Case (Kịch bản kiểm thử)**.  
2. Phân biệt rạch ròi 3 trường phái kiểm thử: Hộp trắng (White Box), Hộp đen (Black Box) và Hồi quy (Regression).  
3. Hiểu được rào cản tư duy đầu tiên của White Box Testing: Tại sao việc chạy qua toàn bộ các dòng lệnh (Statement Coverage) vẫn chưa đủ để kết luận code an toàn?

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Định nghĩa và Vòng đời của một Test Case**

Khi bạn thiết kế bài test, bạn phải viết ra các **Test Cases**. Một Test Case được định nghĩa là *một cách/một kịch bản cụ thể* để thử nghiệm hệ thống, trong đó ghi rõ: Test cái gì? Điều kiện môi trường ra sao? Dữ liệu đầu vào là gì?

**5 Bước thực thi một Test Case chuẩn:**

1. **Chọn Input:** Đưa dữ liệu đầu vào hoặc cấu hình phần mềm cần test.  
2. **Định nghĩa Expected Output:** Xác định trước kết quả KỲ VỌNG (Nếu code đúng thì nó phải ra cái gì?).  
3. **Thực thi (Run):** Chạy chương trình với cái Input đó.  
4. **Ghi nhận (Record):** Lấy kết quả THỰC TẾ (Actual Output) mà chương trình vừa nhả ra.  
5. **So sánh (Compare):** Lấy Thực tế so với Kỳ vọng. Nếu giống nhau \-\> **PASS** (Qua). Nếu khác nhau \-\> **FAIL** (Trượt, có Bug).

#### **2\. Ba Trường phái Kiểm thử Kinh điển**

Trong Kỹ nghệ phần mềm, có 3 loại hình test chính:

* **White Box Testing (Kiểm thử Hộp trắng):**  
  * Được gọi là *Testing in the small* (Kiểm thử vi mô).  
  * Mục tiêu: Xác minh tính logic của thuật toán, luồng dữ liệu, vòng lặp.  
  * Điều kiện bắt buộc: **Phải có mã nguồn (Source code)**.  
* **Black Box Testing (Kiểm thử Hộp đen):**  
  * Được gọi là *Testing in the large* (Kiểm thử vĩ mô).  
  * Mục tiêu: Xác minh xem chức năng của phần mềm có chạy đúng như tài liệu yêu cầu không, chỉ quan tâm Input và Output.  
  * Điều kiện: **Không cần biết mã nguồn** bên trong viết bằng ngôn ngữ gì hay chạy ra sao.  
* **Regression Testing (Kiểm thử Hồi quy):**  
  * Như đã học ở phần Debugging, mỗi khi tìm ra một Bug, bạn lấy ngay cái Input gây ra lỗi đó lưu lại thành một Test Case. Lần sau sửa code xong thì lôi nó ra test lại. Có thể áp dụng bằng cả kỹ thuật Hộp trắng lẫn Hộp đen.

#### **3\. Cạm bẫy của Kiểm thử Hộp trắng: Phủ dòng lệnh (Statement) vs. Phủ đường đi (Path)**

Mục tiêu của Hộp trắng là phải kiểm tra được mọi câu lệnh logic, mọi vòng lặp và mọi cấu trúc dữ liệu bên trong. Thầy Kenneth đã đặt ra một câu hỏi cực kỳ sát sườn:

*"Nếu chúng ta viết Test Case sao cho mọi dòng lệnh (every single statement) trong chương trình đều được chạy qua ít nhất 1 lần, thì đã đủ để tìm ra lỗi chưa?"*

Câu trả lời là: **KHÔNG ĐỦ\!**

**Ví dụ chứng minh:**

Giả sử bạn có một đoạn mã với điều kiện if (A and B). Bên dưới lệnh if này là một loạt các thao tác tính toán.

* Nếu bạn thiết kế một Test Case với A \= true và B \= true, chương trình sẽ chui vào trong block if và thực thi toàn bộ các dòng lệnh bên trong đó. Bạn tự tin nghĩ rằng: *"Tuyệt vời, 100% dòng lệnh đã được chạy qua\!"*.  
* Nhưng chuyện gì xảy ra nếu bạn cho A \= false? Lệnh if bị bỏ qua và rẽ sang một nhánh khác. Nếu ở nhánh ẩn đó (nhánh false) có một phép tính **chia cho 0 (divided by 0\)**, chương trình của bạn sẽ sập ngay lập tức\!

**Kết luận sống còn:** Chỉ test để chạy qua hết các dòng lệnh là một sự ngộ nhận nguy hiểm. Bạn bắt buộc phải test được **Tất cả các Nhánh (Branches)** hoặc **Tất cả các Đường đi độc lập (Independent Paths)**.

Khái niệm "Đường đi độc lập" này chính là cánh cửa dẫn thẳng vào kỹ thuật **Basis Path Testing (Kiểm thử Đường dẫn Cơ sở)** \- một phương pháp toán học giúp bạn vẽ sơ đồ code và tính ra chính xác cần bao nhiêu Test Case để "quét sạch" mọi rẽ nhánh.

