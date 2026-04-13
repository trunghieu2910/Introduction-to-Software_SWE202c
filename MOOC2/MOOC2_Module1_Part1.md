              Introduction Software Engineering  
 Bài giảng đầu tiên của Giáo sư Kenneth thực sự giống như một "gáo nước lạnh" tạt vào những ai có suy nghĩ: *"Làm phần mềm chỉ đơn giản là mở máy tính lên và gõ code"*.  
Bài học này mang nhiệm vụ đập bỏ tư duy của một "thợ gõ code" (Coder) để bắt đầu xây dựng tư duy của một **Kỹ sư phần mềm (Software Engineer)**.

### **1\. Sự ảo tưởng về việc "Vừa nghĩ, vừa Code" (Bottom-up)**

- Khi mới học lập trình, chúng ta thường làm các bài tập nhỏ. Bạn có thể mở máy lên, gõ từ dòng 1 đến dòng 100 là xong chương trình. Đó gọi là lập trình từ dưới lên (Bottom-up).  
- Nhưng với các hệ thống lớn (như Windows có 15 triệu dòng code, hay hệ thống máy bay Boeing có 14 triệu dòng code), việc "vừa nghĩ vừa code" là **bất khả thi**. Bạn bắt buộc phải có bản vẽ thiết kế tổng thể từ trên xuống (Top-down) trước khi đặt tay gõ dòng code đầu tiên.

### **2\. Sự phức tạp không đến từ Code, mà đến từ... Con người**

Giáo sư chỉ ra 3 "thủ phạm" chính làm cho việc phát triển phần mềm trở nên vô cùng phức tạp:

* **Sự mù mờ về Nghiệp vụ (Application Domain):** Lập trình viên rất giỏi viết vòng lặp for, lệnh if/else, nhưng lại mù tịt về kiến thức chuyên ngành.  
  *Ví dụ:* Khi nhóm bạn làm trang web thương mại điện tử bán quần áo thời trang, các bạn rất giỏi Java, nhưng chưa chắc các bạn đã hiểu rõ quy trình quản lý tồn kho, cách tính chiết khấu marketing, hay logic của các cổng thanh toán. Sự lệch pha này rất dễ dẫn đến việc code xong nhưng hệ thống chạy sai thực tế.  
* **Sự rào cản Giao tiếp (Communication):** Khách hàng dùng ngôn ngữ kinh doanh, lập trình viên dùng ngôn ngữ kỹ thuật. Khách hàng bảo: *"Tôi muốn lưu số tiền"*. Bạn là Dev, bạn sẽ đau đầu tự hỏi: *"Lưu kiểu Integer hay kiểu Float? Có lưu số thập phân không?"*. Ngôn ngữ con người vốn dĩ rất mơ hồ, dẫn đến việc truyền đạt sai yêu cầu.  
* **Sự phức tạp trong Quản lý (Management):** Một dự án có hàng chục người cùng làm. Ai làm phần Database? Ai làm phần giao diện? Ghép code của người này với người kia thế nào để không bị "đụng" nhau?

### **3\. Hậu quả tàn khốc của việc Code không có Thiết kế**

Nếu coi thường sự phức tạp này, hậu quả để lại không chỉ là "chạy bị lỗi", mà đôi khi là thảm họa thực sự:

* **Hậu quả về chất lượng (Quality):** Giáo sư lấy ví dụ về việc tên lửa Ariane 5 nổ tung chỉ vì một dòng code lỗi, hay hệ thống Xe cứu thương ở London (Anh) bị sập khiến người bệnh tử vong vì không gọi được xe.  
* **Hậu quả về dự án (Development Problems):** Nhẹ hơn một chút thì dự án của bạn sẽ rơi vào cảnh: **Trễ tiến độ (Over schedule)**, **Đội vốn (Over budget)**, hoặc tệ nhất là đập đi làm lại từ đầu (như hệ thống Sàn giao dịch chứng khoán London mất 5 năm phát triển rồi bị vứt bỏ).

**Tóm tắt lại thông điệp của bài học:** Làm phần mềm cực kỳ phức tạp. Đừng vội vàng lao vào code ngay. Hãy dành thời gian để giao tiếp, phân tích nghiệp vụ, vẽ thiết kế (UML) và quản lý tiến độ. Đó mới là việc của một Kỹ sư\!

---

