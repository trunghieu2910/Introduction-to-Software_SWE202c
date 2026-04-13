# **Dealing with the Complexity**

Thay vì hoảng sợ trước hàng triệu dòng code, bài học này cung cấp cho chúng ta bộ 3 "vũ khí" tư duy cốt lõi để trị sự phức tạp. Hãy cùng áp dụng thẳng những lý thuyết này vào dự án web thương mại điện tử bằng Java của nhóm bạn để thấy nó thực tế như thế nào nhé:

### **1\. Chọn Mục tiêu thiết kế (Design Goals) & Chấp nhận sự đánh đổi**

Khi làm dự án, ai cũng muốn web của mình phải chạy siêu nhanh (Efficient), bảo mật tuyệt đối (Secure), nhiều tính năng (Feature-rich), và giao diện tuyệt đẹp.

* **Thực tế phũ phàng:** Bạn bị giới hạn bởi thời gian (deadline nộp đồ án) và nguồn lực (chỉ có vài thành viên). Bạn không thể có tất cả.  
* **Cách giải quyết:** Ngay từ đầu, nhóm phải ngồi lại và ưu tiên 2-3 mục tiêu quan trọng nhất. Nếu trang web của bạn tập trung vào việc xử lý hàng ngàn đơn hàng dịp Flash Sale, bạn phải ưu tiên **Hiệu suất (Efficiency)**. Nếu nó lưu trữ thẻ tín dụng, **Độ tin cậy (Reliability)** là số 1\. Việc chốt hạ mục tiêu này giúp nhóm không bị lan man trong quá trình code.

### **2\. Chia để trị (Modularity & Incremental Development)**

Đừng bao giờ cố gắng viết một hệ thống lớn trong một vài file Java khổng lồ.

* **Modularity (Tính mô-đun):** Hãy băm nhỏ trang web thời trang ra thành các khối (module) độc lập: Khối Quản lý Người dùng, Khối Giỏ hàng, Khối Thanh toán, Khối Quản lý Kho.  
* Lợi ích là nhóm bạn có thể chia việc rất dễ: Người A code Giỏ hàng, Người B code Thanh toán. Tiến độ công việc sẽ rõ ràng và ít bị "giẫm chân" lên nhau.

### **3\. "Bức tường bí mật" (Information Hiding)**

Đây là trái tim của Lập trình Hướng đối tượng (OOP) và là phần quan trọng nhất của bài học. Nó được tạo nên bởi hai khái niệm cực kỳ hay bị nhầm lẫn:

* **Abstraction (Trừu tượng hóa \- "Bỏ qua chi tiết"):** Khi Khối Giỏ Hàng cần tính tiền, nó chỉ cần gọi hàm `processPayment()` từ Khối Thanh toán. Khối Giỏ Hàng **không cần biết** Khối Thanh toán gọi API của ngân hàng nào, mã hóa bằng chuẩn gì. Nó chỉ quan tâm đến "Giao diện" (Interface) để giao tiếp.  
  → Tạo ra các hàm tại abstract ban đầu để việc chia ra từng nhóm nhỏ code các tính năng song song với nhau   
* **Encapsulation (Đóng gói \- "Khoanh vùng ảnh hưởng"):** Nếu tháng sau, nhóm quyết định đổi từ thanh toán Momo sang thanh toán ZaloPay, bạn chỉ cần sửa code **bên trong** Khối Thanh toán. Nhờ sự đóng gói này, code của Khối Giỏ Hàng hoàn toàn không bị ảnh hưởng, không bị sập, vì "Giao diện" gọi hàm vẫn giữ nguyên.

![Văn bản thay thế](image/Screenshot%202026-04-09%20124627.png)
