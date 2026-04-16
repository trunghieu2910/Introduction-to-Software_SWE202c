# **Black Box Testing**

Chào mừng bạn đến với kỹ thuật "Hóa thân thành Khách hàng": **Black Box Testing (Kiểm thử Hộp đen)**\!

Nếu ở các bài học trước, bạn phải căng mắt ra đọc từng dòng code để vẽ đồ thị rẽ nhánh, thì ở bài học này, Thầy Kenneth sẽ cho phép bạn... nhắm mắt lại. Bạn không cần (và không được phép) nhìn vào mã nguồn. Bạn chỉ có trong tay một bản Đặc tả yêu cầu (Requirements) và một giao diện phần mềm để nhập dữ liệu.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu được nguyên lý của Black Box Testing: Dựa hoàn toàn vào Input và Output để tìm lỗi.  
2. Nắm vững 2 kỹ thuật kinh điển nhất để chọn dữ liệu đầu vào: **Phân vùng tương đương (Equivalence Partitioning)** và **Phân tích giá trị biên (Boundary Value Analysis)**.  
3. Làm quen với các chiến lược kiểm thử cấp cao: Thread Testing (Kiểm thử luồng sự kiện) và State-based Testing (Kiểm thử dựa trên trạng thái).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Nguyên lý của Black Box Testing**

* **Bản chất:** Bạn coi phần mềm như một chiếc hộp đen thui. Bạn đẩy dữ liệu (Input) vào một lỗ, chờ xem nó nhả kết quả (Output) ra lỗ kia có đúng với Tài liệu mô tả hay không.  
* **Mục đích:** Không phải để tìm lỗi logic dòng lệnh (cái đó Hộp trắng lo rồi), mà để tìm xem phần mềm có bị *thiếu chức năng*, *lỗi giao diện*, *lỗi truy cập database*, hay *lỗi hiệu năng* hay không.  
* **Thách thức:** Bạn không thể nhập bừa mọi con số trên đời để test. Bạn phải chọn ra một bộ Input thông minh nhất.

#### **2\. Phân vùng Tương đương (Equivalence Partitioning)**

*Kỹ thuật này giống hệt khái niệm "Sub-domains" ở Hộp trắng, nhưng áp dụng cho góc nhìn Hộp đen.*

Bạn chia tất cả các dữ liệu đầu vào có thể có thành các "vùng" (partitions). Bất kỳ giá trị nào nằm trong cùng một vùng đều sẽ khiến phần mềm xử lý giống hệt nhau.

* **Ví dụ:** Yêu cầu hệ thống: *"Mã số sinh viên hợp lệ từ 0 đến 9,999"*.  
* **Phân vùng:**  
  * Vùng Hợp lệ (Valid): Từ 0 đến 9,999. (Chọn đại một số để test: 100).  
  * Vùng Không hợp lệ (Invalid) 1: Số âm (\< 0). (Chọn đại: \-5).  
  * Vùng Không hợp lệ (Invalid) 2: Lớn hơn mức cho phép (\> 9,999). (Chọn đại: 10,000).  
* **Kết luận:** Thay vì test 10.000 con số, bạn chỉ cần test đúng 3 số: \-5, 100, và 10,000 là đủ để quét toàn bộ phổ dữ liệu.

#### **3\. Phân tích Giá trị Biên (Boundary Value Analysis \- BVA)**

*Đây là mỏ vàng của lỗi\! Lập trình viên ít khi sai ở những con số nằm giữa, nhưng cực kỳ hay sai ở những con số nằm ngay Ranh giới (Boundary) do hay nhầm lẫn dấu \< với \<=.*

* **Quy tắc:** Đừng chỉ test ở giữa vùng. Hãy nhắm thẳng vào các điểm ranh giới, và các điểm nằm sát sạt ranh giới đó.  
* **Ví dụ:** Vẫn với yêu cầu *"Mã sinh viên từ 0 đến 9,999"*.  
* **Các điểm cần test bằng BVA:**  
  * Xung quanh ranh giới Dưới: \-1, 0, 1.  
  * Xung quanh ranh giới Trên: 9,998, 9,999, 10,000.  
* Việc test như thế này sẽ bắt ngay lập tức các "Lỗi lệch một" (Off-by-one bugs) kinh điển của dân code.

#### **4\. Các Chiến lược Kiểm thử Cấp cao khác (Dành cho Hệ thống Lớn)**

* **Thread Testing (Kiểm thử Luồng):** Dùng để test sự tương tác giữa các Class (đối tượng) với nhau. Ví dụ: Sự kiện "Sinh viên đăng ký khóa học" sẽ gọi đến Object Sinh viên \-\> gọi tiếp đến Object Khóa học \-\> gọi tiếp đến Object Ngân hàng để trừ tiền. Tester phải test toàn bộ một luồng (thread) dài như vậy.  
* **State-based Testing (Kiểm thử Trạng thái):** Một đối tượng có thể đổi trạng thái liên tục. Ví dụ, một Lớp học (Class) có thuộc tính classSize.  
  * Nếu chưa đủ học sinh \-\> Lớp ở trạng thái Available (Mở đăng ký).  
  * Nếu classSize \== 50 \-\> Lớp chuyển sang trạng thái Full (Khóa đăng ký).  
  * Tester phải chủ động "nhồi" dữ liệu để ép Lớp học chuyển trạng thái thành Full, sau đó mới thử đăng ký tiếp xem hệ thống có chửi không. Kỹ thuật này gắn liền với Sơ đồ Máy trạng thái (State Machine Diagram) mà chúng ta sẽ học sau này.

---

