**"Đặc tả Use Case" (Use Case Specification)\!**

Nếu ở bài trước, chúng ta cãi nhau xem nên vẽ elip hay mũi tên thế nào cho đúng, thì bài này Thầy Kenneth đã khẳng định: Sơ đồ chỉ là cái bìa sách, còn cuốn "Đặc tả Use Case" mới là nội dung bên trong.

Dưới đây là phần bóc tách cấu trúc của một tài liệu Đặc tả Use Case chuẩn mực mà một BA (Business Analyst) phải viết:

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Bài học này giúp bạn nắm được **Bộ khung 6 phần (Template)** bắt buộc phải có khi viết mô tả cho bất kỳ một chức năng nào. Mục tiêu là viết sao cho cả khách hàng (người không biết code) đọc cũng hiểu phần mềm chạy thế nào, và lập trình viên (người code) đọc cũng biết chính xác phải lập trình luồng logic (if-else) ra sao.

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

Một bản Đặc tả Use Case (Use Case Specification) hoàn chỉnh luôn gồm các phần sau:

#### **1\. Thông tin cơ bản (Header)**

* **Tên Use Case:** Phải khớp 100% với tên cái hình elip trên bản vẽ (Ví dụ: *Rút tiền*).  
* **Mô tả ngắn (Brief Description):** Một câu tóm tắt chức năng này dùng để làm gì.  
* **Tác nhân (Participating Actors):** Liệt kê ai là người được phép dùng chức năng này.

#### **2\. Tiền điều kiện (Pre-conditions)**

* **Bản chất:** Hệ thống phải ở trong trạng thái như thế nào thì người dùng mới được phép bấm nút "Bắt đầu" chức năng này?  
* *Lưu ý:* Chỉ ghi KẾT QUẢ, không ghi CÁCH LÀM.  
* *Ví dụ của Thầy:* Để rút tiền ATM, Tiền điều kiện là Số dư trong thẻ \>= 100k. Thầy nhấn mạnh: Chúng ta chỉ ghi điều kiện, chứ không quan tâm làm cách nào khách hàng nạp được số tiền đó vào thẻ.  
* *Ví dụ khác:* Để chức năng Mua hàng chạy, Tiền điều kiện là Giỏ hàng phải có ít nhất 1 sản phẩm.

#### **3\. Luồng sự kiện chính (Basic Flow / Happy Path)**

* **Bản chất:** Đây là kịch bản hoàn hảo nhất, nơi mọi thứ đều suôn sẻ, không có lỗi gì xảy ra.  
* **Cách viết:** Viết theo dạng kịch bản đối thoại "Ping-Pong" giữa Actor và System. Có thể dùng giả mã (pseudo-code) như IF... THEN... hoặc vòng lặp FOR/WHILE.  
* *Ví dụ mô phỏng Ping-Pong:*  
  1. Actor chọn nút "Rút tiền".  
  2. System hiển thị màn hình nhập số tiền.  
  3. Actor nhập 500k và bấm "Enter".  
  4. System nhả ra 500k và in biên lai.

#### **4\. Luồng thay thế / Ngoại lệ (Alternative Flows / Exceptions)**

* **Bản chất:** Nơi xử lý những cú "quay xe" của người dùng hoặc các lỗi hệ thống.  
* Đây là lý do bản Đặc tả này tồn tại\! Sơ đồ không vẽ được chỗ này, nên ta phải viết ra chữ.  
* *Ví dụ:* Tại bước 3 của Luồng chính, NẾU Actor nhập số tiền lớn hơn số dư \-\> System báo lỗi "Số dư không đủ" và kết thúc.

#### **5\. Hậu điều kiện (Post-conditions)**

* **Bản chất:** Sau khi thực hiện xong chức năng (và thành công), trạng thái của hệ thống thay đổi như thế nào?  
* *Lưu ý:* Nó giúp các chức năng khác biết được tình hình hiện tại.  
* *Ví dụ của Thầy:* Hậu điều kiện của Rút tiền là Số dư thẻ \>= 0. (Bạn không thể rút âm tiền được).  
* *Ví dụ khác:* Hậu điều kiện của Thêm vào giỏ là Tổng số lượng hàng trong giỏ tăng lên 1.

#### **6\. Yêu cầu phi chức năng (Non-functional Reqs \- Tùy chọn)**

* Nếu có yêu cầu đặc biệt về tốc độ hay bảo mật cho riêng chức năng này. (Ví dụ: Quá trình trừ tiền phải hoàn tất trong vòng 3 giây).

---

