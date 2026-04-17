# **State Machine Diagram Example**

Chào mừng bạn đến với bài học **Lecture 2-2: State Machine Diagram Example**.  
Ở bài trước, chúng ta đã nắm được "ngữ pháp" của Sơ đồ Máy trạng thái. Trong bài này, Thầy Kenneth sẽ đưa chúng ta vào phần "thực hành", áp dụng ngay vào dự án Hệ thống Đăng ký Khóa học ASU, đồng thời mở khóa những kỹ năng nâng cao như trạng thái lồng nhau (Inception-style).

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Biết cách trích xuất các Trạng thái (States) và Chuyển đổi (Transitions) từ một kịch bản/yêu cầu thực tế.  
2. Hiểu và áp dụng được **Trạng thái phức hợp (Composite State)** để xử lý các logic lồng ghép nhau.  
3. Phân biệt được sự khác nhau giữa thực thi Tuần tự (Sequential), thực thi Đồng thời (Concurrent) và khái niệm Đồng bộ hóa (Synchronization).  
4. Nắm được nguyên tắc tối ưu: Khi nào thì KHÔNG CẦN vẽ sơ đồ này.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Thực hành: Vòng đời của một Lớp học (Section Class)**

Thầy Kenneth đặt ra 3 câu hỏi cốt lõi trước khi vẽ: *Lớp học có những trạng thái nào? Cái gì quyết định trạng thái đó? Sự kiện nào kích hoạt sự thay đổi?*

Từ đó, ta vẽ được vòng đời của một Lớp học (Section) như sau:

* **Khởi tạo:** Lớp học được tạo ra với số lượng sinh viên (enrolled) \= 0 \-\> Trạng thái **Available (Khả dụng)**.  
* **Chuyển đổi 1:** Sinh viên đăng ký liên tục. Khi enroll \== 40 (Change Event) \-\> Chuyển sang trạng thái **Full (Đầy)**.  
* **Chuyển đổi 2:** Một sinh viên rút môn học (Call Event: dropStudent) \-\> Từ **Full** quay ngược lại **Available**.  
* **Đóng đăng ký (Registration Closed):** Lúc này số phận lớp học sẽ rẽ làm 2 hướng (dựa vào Guard condition):  
  * *Nếu students \>= 10:* Lớp học chuyển sang trạng thái **Offered (Được mở)**.  
  * *Nếu students \< 10:* Lớp học bị chuyển sang trạng thái **Cancelled (Bị hủy)**.

#### **2\. Trạng thái Phức hợp (Composite States)**

Đây là kỹ thuật "vẽ sơ đồ bên trong một sơ đồ khác" (Nested states), dùng khi một trạng thái lớn chứa quá nhiều hành vi phức tạp.

* **Trạng thái Phức hợp Tuần tự (Sequential):** Tại một thời điểm, đối tượng chỉ nằm ở 1 trạng thái con duy nhất.  
  * *Ví dụ:* Một chiếc xe có trạng thái lớn là **Chạy tiến (Forward)**. Bên trong trạng thái Forward này lại có các trạng thái con là *Số 1*, *Số 2*, *Số 3*. Khi bạn phanh xe lại, dù đang ở số nào, mũi tên chuyển đổi cũng sẽ kéo bạn về lại *Số 1*.  
* **Trạng thái Phức hợp Đồng thời (Concurrent):** Trạng thái lớn được chia làm nhiều "phân vùng" (regions). Đối tượng phải thực hiện nhiều trạng thái ở các vùng khác nhau CÙNG MỘT LÚC.  
  * *Ví dụ:* Trạng thái **Chưa Hoàn Thành Môn Học (Incomplete)**. Bên trong nó chia làm 3 vùng độc lập: (1) Làm Lab, (2) Làm Đồ án, (3) Thi cuối kỳ. Sinh viên phải hoàn thành cả 3 vùng này cùng lúc (vùng Lab ở trạng thái Xong, vùng Đồ án ở trạng thái Xong...) thì mới thoát khỏi Incomplete để sang trạng thái **Passed (Qua môn)**.

#### **3\. Thanh Đồng bộ hóa (Synchronization Bar)**

Khi xử lý các trạng thái Đồng thời (Concurrent), chúng ta dùng một ký hiệu đặc biệt là **Thanh ngang đậm (Bar)**.

* **Tách luồng (Fork):** Một mũi tên đi vào thanh ngang, và nhiều mũi tên bắn ra từ thanh ngang đó chỉ vào các trạng thái khác nhau. Ý nghĩa: *Buộc các trạng thái này phải bắt đầu CÙNG MỘT LÚC.*  
* **Gộp luồng (Join):** Nhiều mũi tên từ các trạng thái khác nhau cùng đi vào một thanh ngang. Ý nghĩa: *Phải chờ cho tất cả các trạng thái đó hoàn thành xong xuôi thì mới được phép đi tiếp bước tiếp theo.*  
* *(Lưu ý: Nếu không có thanh ngang này, sơ đồ Máy trạng thái mang tính Tất định (Deterministic) \- nghĩa là nó buộc bạn chỉ được phép chọn rẽ 1 nhánh duy nhất, không có chuyện thực hiện 2 nhánh cùng lúc).*

#### **4\. Lời khuyên Thực chiến từ Kiến trúc sư**

* **Có cần vẽ Sơ đồ Trạng thái cho MỌI Class không?**  
  * **KHÔNG.** Trong một dự án có hàng trăm class, nếu bạn ngồi vẽ hết thì dự án sẽ... phá sản vì chậm tiến độ.  
  * Chỉ vẽ sơ đồ này cho những class có **hành vi động phức tạp (significant dynamic behavior)**, chứa nhiều logic rẽ nhánh có nguy cơ gây lỗi cao (như chức năng Thanh toán, Giỏ hàng, Khóa cửa thông minh, v.v.). Các class dữ liệu đơn giản (chỉ chứa hàm Get/Set) thì hãy bỏ qua.

---

