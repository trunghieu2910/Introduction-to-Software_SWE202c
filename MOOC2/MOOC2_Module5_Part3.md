# **Use Case Modeling Example**

Bài 5-3 này là một màn thực chiến cực kỳ quan trọng\! Thầy Kenneth không dạy thêm hình vẽ mới, mà thầy dạy bạn cách **"gom rác" và "nâng cấp"** một bản nháp lộn xộn thành một bản vẽ Use Case chuẩn mức Kiến trúc sư phần mềm.

Dưới đây là 3 bài học xương máu được đúc kết từ ví dụ "Hệ thống Đăng ký môn học ASU" của Giáo sư:

### **🎯 1\. Quy tắc "Bức tranh toàn cảnh" (Complete Story)**

* **Lỗi sai kinh điển:** Sinh viên thường đọc từng câu trong yêu cầu, thấy động từ nào là vẽ ngay một cái Use Case.  
  * Ví dụ: Thấy "Xem môn học", "Thêm môn", "Xóa môn", "Đổi lịch" \-\> Vẽ ra 4 cái elip. Điều này làm cho sơ đồ nhìn như một bát mì spaghetti\!  
* **Quy tắc của Thầy:** Một Use Case tốt phải là một **CÂU CHUYỆN HOÀN CHỈNH từ đầu đến cuối**.  
  * Hãy tự hỏi: "Tại sao sinh viên lại phải thêm/xóa/xem môn học?" \-\> À, vì mục đích cuối cùng của họ là *Đăng ký học*.  
  * **Cách giải quyết:** Gom toàn bộ 4 hành động lắt nhắt kia thành **MỘT Use Case duy nhất** mang tên `Đăng ký môn học (Register for courses)`. Các hành động nhỏ kia sẽ được giấu đi và viết chi tiết trong tài liệu Đặc tả (Specification).

### **🔍 2\. Kỹ năng "Đào bới" Actor ẩn (Hidden Actors)**

* Đôi khi, khách hàng viết yêu cầu ở thể bị động: *"Khóa học sẽ được tạo ra và quản lý trên hệ thống."*  
* Bất kỳ lúc nào bạn thấy một hành động mà không thấy ai làm, bạn phải đi hỏi chuyên gia (Domain Expert): *"Ai là người tạo ra khóa học này?"*  
* Từ đó, Thầy Kenneth đã phát hiện thêm một Actor bị giấu kín là `Registrar` (Phòng Đào tạo) để chịu trách nhiệm cho Use Case `Quản lý thông tin môn học`.

### **🔀 3\. Nét liền (Link) vs Mũi tên (Arrow)**

Đứng giữa Actor và Use Case là sợi dây liên kết. Thầy phân biệt rất rõ 2 loại nét vẽ này:

* **Mũi tên (Arrow \-\>):** Thể hiện **Sự khởi xướng (Initiation)**.  
  * *Ví dụ:* Mũi tên trỏ từ `Sinh viên` \-\> `Đăng ký môn`. Có nghĩa là: Sinh viên là người chủ động bấm nút bắt đầu quá trình này.  
* **Nét liền trơn (Line \-):** Thể hiện **Sự trao đổi thông tin (Communication)** nhưng KHÔNG chủ động bắt đầu.  
  * *Ví dụ:* Nét trơn nối từ Use Case `Đăng ký môn` \- `Hệ thống hóa đơn`. Có nghĩa là: Hệ thống hóa đơn nằm im chờ. Chỉ khi nào sinh viên đăng ký xong, dữ liệu mới được đẩy sang cho Hệ thống hóa đơn. Nó bị động nhận dữ liệu chứ không khởi xướng.

---

### **⛔ Cảnh báo cuối bài: Generalization trong Use Case**

Giống như Class, Actor và Use Case cũng có thể áp dụng quan hệ Kế thừa (Mũi tên tam giác rỗng).

* **Kế thừa Actor (ĐƯỢC KHUYÊN DÙNG):** Rất tốt. Vẽ Actor chung là `Nhân viên`, rồi chia ra thành Actor con là `Quản lý` và `Thu ngân`. (Quản lý sẽ làm được mọi thứ của Thu ngân).  
* **Kế thừa Use Case (CẤM KỴ):** Thầy Kenneth khuyên chân thành: **Tránh xa nó ra\!** Nó rất dễ bị dùng sai và làm sơ đồ trở nên khó hiểu. Không cần nó, bạn vẫn thiết kế được hệ thống hoàn hảo.

