# **Use Cases**

Nếu Actor (Hình người que) là những "diễn viên", thì **Use Case (Hình elip)** chính là "kịch bản hành động" mà họ sẽ thực hiện trên sân khấu hệ thống của bạn.

Giáo sư Kenneth đã chuyển trọng tâm sang việc định nghĩa các chức năng của hệ thống. Dưới đây là "giải mã" các nguyên tắc sống còn của Bài 5-2:

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Bài học này giúp bạn hiểu rõ cách "gói ghém" một tính năng phần mềm vào trong một hình elip. Bạn sẽ học được quy luật đặt tên chuẩn mực và cách phân biệt rạch ròi giữa một Chức năng tổng quát (Use Case) với một hành động cụ thể của một cá nhân (Scenario).

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

Để vẽ các hình elip (Use Case) đúng chuẩn kỹ sư phần mềm, bạn phải tuân thủ 4 quy luật sau:

#### **1\. Nguyên lý "Phát súng hiệu lệnh" (Initiation)**

* **Bản chất:** Một Use Case mô tả tương tác giữa hệ thống và Actor.  
* **Quy luật:** Bất kỳ Use Case nào cũng **bắt buộc phải được khơi mào (initiated) bởi một Actor**. Hệ thống máy tính là một khối sắt vô tri, nó không tự nhiên thức dậy làm việc nếu không có ai đó (hoặc một hệ thống khác) "đánh thức" nó.

#### **2\. Quy tắc Đặt tên (Naming Conventions)**

Tương tự như cách bạn đặt tên Hàm (Method) trong lập trình Java:

* Bắt đầu bằng một **Động từ chỉ hành động** ở thể chủ động (Active voice), thì hiện tại.  
* Kèm theo một **Danh từ** (Vocabulary từ ứng dụng).  
* *Ví dụ ĐÚNG:* Đăng ký môn học, Thanh toán giỏ hàng, Hủy đơn.  
* *Ví dụ SAI:* Việc đăng ký (thiếu động từ), Hóa đơn được in (bị động), Quản lý dữ liệu (quá mơ hồ).

#### **3\. Phân biệt Use Case và Scenario (Giống hệt Class & Object trong OOP)**

Thầy Kenneth lại một lần nữa dùng tư duy Hướng đối tượng để giải thích:

* **Use Case (Bản thiết kế chung):** Đại diện cho một nhóm các kịch bản giống nhau. (Nó là một *Class*). Ví dụ: Rút tiền.  
* **Scenario (Kịch bản cụ thể):** Là một câu chuyện chi tiết, mô tả chính xác 1 người cụ thể, làm 1 việc cụ thể ở 1 thời điểm. (Nó là một *Instance/Object*). Ví dụ: *"Thầy Kenneth đăng nhập hệ thống lúc 8h sáng và chấm điểm cho sinh viên A"*.  
* \-\> **Kết luận:** Trên sơ đồ, ta **chỉ vẽ Use Case**, KHÔNG vẽ Scenario.

#### **4\. Quy tắc "Bức tranh màu hồng" (Happy Path)**

Khi vẽ biểu đồ Use Case, chúng ta **chỉ vẽ luồng hoạt động bình thường, suôn sẻ (Normal sequence)**.

* KHÔNG vẽ các Use Case cho lỗi (Exceptions) hay các luồng phụ (Alternatives) lên mặt sơ đồ để tránh làm rác bản vẽ.  
* Ví dụ: Chỉ vẽ elip Đăng nhập. Không vẽ thêm elip Nhập sai mật khẩu 3 lần hay Mất kết nối mạng. Những lỗi này sẽ được giấu đi và viết bằng chữ vào cuốn tài liệu Đặc tả (Use Case Specification).

---

