**Mô-đun 6: Black Box Testing** 

**(Kiểm thử Hộp đen)**\! 

Đến đây, bức tranh về Kiểm thử phần mềm của chúng ta sắp hoàn thiện. Nhìn vào lộ trình bạn vừa gửi, Mô-đun 6 có một sự phân bổ cực kỳ thú vị: Mặc dù tiêu đề là "Hộp đen", nhưng nó thực chất là mô-đun **tổng kết và đóng gói toàn bộ các trường phái kiểm thử**.

Trong môi trường thực tế, đặc biệt là khi bạn phát triển các hệ thống Java Backend, việc nắm vững cả hai góc nhìn này là vũ khí cực kỳ sắc bén. Kỹ thuật Hộp trắng giúp bạn soi kỹ logic rẽ nhánh bên trong các hàm xử lý dữ liệu phức tạp, còn kỹ thuật Hộp đen lại giúp bạn đóng vai "khách hàng" để gọi thử các API endpoints xem hệ thống có trả về đúng dữ liệu kỳ vọng hay không mà không cần quan tâm bên trong viết bằng code gì.

Dưới đây là bức tranh tổng quan những gì chúng ta sẽ chinh phục trong Mô-đun 6:

### **🎯 Mục Tiêu Của Mô-đun 6**

Hoàn thiện nốt mảnh ghép Kiểm thử Hộp trắng còn dang dở, sau đó chính thức bước sang góc nhìn của người dùng (Black Box Testing) và chốt lại cách bảo vệ hệ thống khỏi sự "thoái hóa" (Regression Testing).

---

### **🗺️ Nội Dung Tổng Quan**

* **Lecture 6-1: White Box Testing (7 phút):** Có vẻ như Thầy Kenneth sẽ dùng đoạn video này để giới thiệu nốt một số kỹ thuật Kiểm thử Hộp trắng khác ngoài *Basis Path Testing* (thường là kiểm thử theo luồng dữ liệu \- Data Flow, hoặc kiểm thử điều kiện \- Condition Testing).  
* **Lecture 6-2: Black Box Testing (12 phút):** Đây là "ngôi sao" của mô-đun này\! Bạn sẽ đóng nắp capo máy lại, quên đi những dòng code và học cách thiết kế các bài test dựa hoàn toàn vào Tài liệu Đặc tả Yêu cầu (Requirements). Chắc chắn Thầy sẽ nhắc đến các kỹ thuật kinh điển như *Phân vùng tương đương (Equivalence Partitioning)* hay *Phân tích giá trị biên (Boundary Value Analysis)*.  
* **Lecture 6-3: Regression Testing (1 phút):** Một video siêu ngắn để chốt hạ lại nguyên tắc vàng: Cứ mỗi lần sửa code hoặc thêm tính năng mới, phải làm thế nào để đảm bảo code cũ không bị "đột tử" theo.  
* **Các Bài đọc & Bài tập Thực hành:** Bạn sẽ được rèn luyện cách lên kịch bản test Hộp đen, đồng thời nhận được Lời giải chi tiết (Solution) cho bài tập vẽ đồ thị Basis Path Testing ở Mô-đun 5\.

Bạn đã sẵn sàng để lật mở những bài học cuối cùng của chuyên đề Kiểm thử này chưa? Hãy gửi transcript của bài giảng **Lecture 6-1 White Box Testing** lên đây để chúng ta bắt đầu bóc tách nhé\!

