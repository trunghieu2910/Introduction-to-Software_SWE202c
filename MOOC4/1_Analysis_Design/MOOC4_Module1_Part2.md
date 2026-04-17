# **Architectural Design and Analysis**

Bài giảng **Lecture 1-2: Architectural Design and Analysis** sẽ đưa bạn lên vị trí "chim bay" (Bird's-eye view) để nhìn xuống toàn bộ hệ thống.

Khi hệ thống quá lớn, bạn không thể nhét tất cả code vào một chỗ. Thầy Kenneth giới thiệu khái niệm cốt lõi: **Subsystem (Hệ thống con)** và cách ứng dụng các **Architectural Patterns (Mẫu kiến trúc)** để "lắp ráp" các hệ thống con này lại với nhau sao cho đáp ứng được các yêu cầu khắt khe về bảo mật, hiệu năng hay bảo trì.

Dưới đây là bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu được nguyên lý "Chia để trị" bằng cách sử dụng các Hệ thống con (Subsystems).  
2. Nắm được cách thiết kế kiến trúc để đáp ứng các **Yêu cầu Phi chức năng** (Non-functional Requirements).  
3. Làm quen với **7 Mẫu Kiến trúc Kinh điển (Architectural Patterns)** thường được sử dụng nhất trong ngành công nghiệp phần mềm.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Hệ thống con (Subsystem) & Nguyên lý che giấu thông tin**

* Thay vì code một khối khổng lồ, ta chia phần mềm thành các "cục" nhỏ hơn gọi là Subsystem (VD: Cục Quản lý user, Cục Thanh toán, Cục Gửi email).  
* **Information Hiding (Che giấu thông tin):** Cục Thanh toán không cần biết Cục User được viết bằng code gì. Nó chỉ cần biết gọi hàm getUser() là sẽ lấy được thông tin. Điều này giúp các team code độc lập mà không dẫm chân lên nhau.

#### **2\. Kiến trúc giải quyết Yêu cầu Phi chức năng như thế nào?**

Kiến trúc bạn chọn sẽ quyết định "tính cách" của phần mềm:

* **Hiệu năng (Performance):** Gom các chức năng chạy nhiều vào chung 1 subsystem để tránh việc phải gọi chéo nhau qua mạng làm chậm tốc độ.  
* **Bảo mật (Security):** Giấu các subsystem chứa dữ liệu nhạy cảm vào sâu bên trong (Inner layers), bắt buộc phải đi qua nhiều lớp kiểm duyệt ở ngoài mới vào được tới nơi.  
* **Bảo trì (Maintainability):** Chia nhỏ hệ thống (Self-contained). Nếu lỗi ở phần thanh toán, chỉ sửa đúng cục Thanh toán, không làm sập cả hệ thống.

#### **3\. Bảy (07) Mẫu Kiến trúc Kinh điển**

Đây là phần "ăn tiền" nhất của bài học. Hãy lưu ý kỹ vì khi đi phỏng vấn Backend, nhà tuyển dụng rất hay hỏi về những mô hình này:

1. **Multi-layer (Kiến trúc phân tầng):** \* Chia hệ thống thành các tầng (VD: Tầng UI \-\> Tầng Logic \-\> Tầng Database).  
   * *Closed layer:* Tầng trên chỉ được gọi trực tiếp xuống tầng ngay sát dưới nó (Bảo mật cao nhưng chậm).  
   * *Open layer:* Tầng trên có thể nhảy cóc gọi xuyên xuống bất kỳ tầng nào bên dưới (Nhanh nhưng khó kiểm soát).  
2. **Repository (Kiến trúc Kho lưu trữ):** \* Mọi client/subsystem đều đổ dồn vào gọi chung một cái kho dữ liệu trung tâm.  
   * *Ví dụ:* Hệ quản trị cơ sở dữ liệu (DBMS). *Nhược điểm:* Cái kho này dễ bị nghẽn cổ chai (Bottleneck) hoặc sập thì đi tong cả hệ thống.  
3. **Client-Server (Kiến trúc Khách \- Chủ):**  
   * Kinh điển của Web App. Nhiều Client (Browser/App) gửi yêu cầu lên 1 Server trung tâm, Server này lại chọc xuống Database để lấy dữ liệu trả về.  
4. **Broker (Kiến trúc Môi giới):**  
   * Dùng khi hệ thống chạy phân tán trên nhiều máy chủ khác nhau. Client không gọi thẳng Server mà gọi qua một thằng "cò" (Broker/Proxy). Thằng cò này sẽ tự biết tìm đến máy chủ nào đang rảnh để xử lý.  
5. **Transaction Processing (Xử lý Giao dịch):**  
   * Có một bộ phận gọi là "Dispatcher" đứng hứng mọi luồng giao dịch, sau đó phân luồng ném cho các Handler xử lý. Ứng dụng nhiều nhất trong Database Engine hoặc hệ thống Ngân hàng.  
6. **Pipe and Filter (Ống nước và Bộ lọc):**  
   * Dữ liệu chảy qua một đường ống. Đi qua trạm A (xử lý xong 1 phần) \-\> nhả ra cho trạm B xử lý tiếp \-\> nhả cho trạm C.  
   * *Ví dụ:* Hệ thống xử lý ảnh (Đổi sang trắng đen \-\> Làm mờ \-\> Cắt viền). Ưu điểm là làm việc song song (Pipelining) rất mượt.  
7. **MVC (Model \- View \- Controller):**  
   * Ngôi sao sáng nhất, đặc biệt quen thuộc với bạn khi làm Java Web\!  
   * Chia làm 3 cục: **Model** (Xử lý Data/Database), **View** (Giao diện UI/HTML), **Controller** (Não bộ điều phối luồng chạy).  
   * *Lợi ích:* Cực kỳ dễ bảo trì. Sửa HTML ở View không làm chết logic truy vấn SQL ở Model.

---

