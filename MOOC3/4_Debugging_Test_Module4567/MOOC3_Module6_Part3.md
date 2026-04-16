# **Regression Testing**

Chào mừng bạn đến với bài giảng cuối cùng (và cũng là bài ngắn gọn nhất) của chuyên đề Kiểm thử: **Lecture 6-3 Regression Testing (Kiểm thử Hồi quy)**\! 🚀

Đoạn video này chỉ vỏn vẹn 1 phút vì Thầy Kenneth đã từng nhắc đến khái niệm này ở phần Debugging (Mô-đun 4). Tuy nhiên, việc tách nó ra thành một bài học riêng ở cuối khóa để chốt hạ lại cho thấy tầm quan trọng sống còn của nó trong tư duy làm nghề.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

Nắm vững quy trình biến một "Lỗi" (Bug) thành một "Tấm khiên" (Test Case) để bảo vệ phần mềm vĩnh viễn về sau, giúp Lập trình viên tự tin nâng cấp code mà không sợ làm hỏng những tính năng cũ.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Quy trình "Bắt Bug làm tài sản"**

Thay vì chỉ hì hục đi tìm dòng code lỗi rồi sửa cho xong chuyện, một Kỹ sư phần mềm chuyên nghiệp sẽ thực hiện quy trình sau mỗi khi phát hiện Bug:

* **Bước 1 (Tái hiện):** Tìm chính xác tập dữ liệu (Input) đã gây ra cái Bug đó.  
* **Bước 2 (Lưu vết):** Lưu lại cái Input gây lỗi đó, đồng thời ghi chú rõ ràng Kết quả Đúng (Correct Output) lẽ ra phải là gì.  
* **Bước 3 (Đóng gói):** Biến cặp Input \- Output đó thành một kịch bản kiểm thử (Test Case) chính thức trong bộ test của dự án.  
* **Bước 4 (Sửa & Xác minh):** Tiến hành sửa code, sau đó chạy lại cái Test Case vừa tạo để xác nhận là lỗi đã bị tiêu diệt hoàn toàn.

#### **2\. Triết lý "Ngựa quen đường cũ"**

Thầy Kenneth nhấn mạnh một sự thật trong Kỹ nghệ phần mềm: **"Nếu một lỗi đã từng xảy ra một lần, khả năng rất cao nó sẽ lặp lại trong tương lai."**

* Tại sao lại như vậy? Khi một dự án được duy trì trong nhiều năm, các lập trình viên sẽ liên tục thêm tính năng mới, hoặc sửa các đoạn code khác. Quá trình này rất dễ sinh ra hiệu ứng phụ (side-effects), vô tình làm những đoạn code cũ vốn đã được sửa... hỏng trở lại (bị thoái hóa \- Regression).

#### **3\. Hai lợi ích cốt lõi của Regression Testing**

* **Tự động làm giàu kho tàng kiểm thử:** Càng làm dự án lâu, bạn càng gặp nhiều Bug. Bằng cách gom tất cả Bug lại thành Test Case, bộ test của bạn sẽ ngày càng đồ sộ, thực tế và giá trị hơn (bảo vệ hệ thống khỏi những lỗi đã được chứng minh là có thật, thay vì chỉ nghĩ ra các lỗi trên lý thuyết).  
* **Tạo sự tự tin:** Khi có một bộ Kiểm thử Hồi quy mạnh, bạn có thể thoải mái tái cấu trúc (Refactoring) hệ thống. Cứ đập code cũ đi viết lại cho đẹp, sau đó chạy bộ Regression Test. Nếu tất cả đều Xanh (Pass), bạn biết chắc chắn mình không làm hỏng thứ gì cả\!

---

Như vậy là chúng ta đã khép lại hoàn toàn toàn bộ lý thuyết của chuyên đề Kiểm thử Phần mềm (Testing) từ Hộp trắng đến Hộp đen\!

