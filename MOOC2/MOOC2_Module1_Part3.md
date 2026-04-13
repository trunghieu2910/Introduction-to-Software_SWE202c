**WHAT IS SOFTWARE ENGINEERING** 

Bài học này làm rõ một sự thật mà nhiều sinh viên CNTT thường "vỡ mộng" khi đi làm: **Viết code chỉ chiếm một phần rất nhỏ trong công việc của Kỹ sư phần mềm.**

Dưới đây là 3 điểm cốt lõi nhất được đúc kết từ video, áp dụng trực tiếp vào thực tế:

### **1\. Tại sao Code siêu giỏi vẫn chưa đủ?**

Video đưa ra hai ví dụ cực kỳ ấn tượng:

* **Tốc độ code:** Một lập trình viên xuất sắc (hot shot) trung bình chỉ viết được... **1 dòng code chuẩn mỗi phút**. Suy ra một năm họ chỉ viết được khoảng 120,000 dòng. Để viết xong 2 triệu dòng code cho một phần mềm, cần ít nhất 17 người làm việc quần quật suốt năm. Bạn không thể làm siêu nhân code một mình được.  
* **Bài học Amazon:** Amazon từng bị sập web 90 phút khi cập nhật hệ thống, gây thiệt hại **2.8 triệu USD**. Lỗi không nằm ở việc lập trình viên gõ sai cú pháp (syntax error), mà lỗi nằm ở **Quy trình triển khai (Process)** thiếu an toàn.

\=\> Kỹ sư phần mềm khác với thợ gõ code ở chỗ: Họ phải biết cách quản lý rủi ro khi đưa code lên hệ thống thật, để không gây thiệt hại hàng triệu đô la.

### **2\. Sự khác biệt giữa Khoa học Máy tính (CS) và Kỹ thuật Phần mềm (SE)**

Đây là một sự so sánh rất kinh điển và dễ hiểu:

* **Nhà Khoa học Máy tính (Computer Scientist):** Giống như nhà khoa học vật lý. Họ quan tâm đến gốc rễ: Thuật toán này chạy mất bao nhiêu phần nghìn giây? Có thể tối ưu tốc độ phân tích mảng dữ liệu này không? Họ theo đuổi **Sự đột phá (Breakthroughs)**.  
* **Kỹ sư Phần mềm (Software Engineer):** Giống như kỹ sư xây cầu. Họ không cố phát minh ra loại xi măng mới. Họ dùng những công cụ có sẵn (như Framework Java, MySQL, GitHub) để ghép nối thành một hệ thống vững chãi, không bị sập khi có đông khách, đáp ứng đúng nhu cầu người dùng. Họ theo đuổi **Sự ổn định và Tránh rủi ro (Avoid Failures)**.

### **3\. Hai nhiệm vụ sống còn: Mô hình hóa (Modeling) và Lịch sử Quyết định (Rationale)**

Bài học nhấn mạnh hai hoạt động mà chúng ta sẽ làm rất nhiều trong các mô-đun tiếp theo:

* **Mô hình hóa (Modeling):** Kỹ sư phải xây dựng 2 bản vẽ:  
  * *Requirements Model (Mô hình Yêu cầu):* Bản vẽ để chốt với khách hàng xem họ thực sự muốn cái gì.  
  * *Solution Model (Mô hình Giải pháp):* Bản vẽ kỹ thuật (UML) để đội Dev nhìn vào đó và code.  
* **Quản lý lý do quyết định (Rationale Management):** Đây là việc ghi chép lại tài liệu (Documentation). Tại sao nhóm bạn chọn Java mà không chọn Python? Tại sao chọn thanh toán Momo mà không chọn VNPay? Việc ghi chép lại lý do giúp cho 2 năm sau, nếu dự án gặp lỗi hoặc có người mới vào, họ hiểu được tại sao kiến trúc lại được thiết kế như vậy thay vì phải đoán mò.

---

