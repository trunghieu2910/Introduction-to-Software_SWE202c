# **Perform Tests**

Chào mừng bạn đến với chặng đường cuối cùng của phần Kiểm thử\!

Ở bài giảng **Lecture 7-1: Perform Tests**, Thầy Kenneth đã gom tất cả các mảnh ghép từ Hộp trắng, Hộp đen, Gỡ lỗi lại với nhau để tạo thành một "Dây chuyền" kiểm thử hoàn chỉnh. Đây chính là bức tranh toàn cảnh mà bất kỳ Kỹ sư Phần mềm nào cũng phải nằm lòng.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu được tầm quan trọng của việc **Tự động hóa kiểm thử (Test Automation)** để tiết kiệm sức lực.  
2. Nắm vững quy trình thực thi và theo dõi kết quả của một chiến dịch kiểm thử.  
3. Phân biệt được sự đối lập thú vị: Quá trình Phát triển đi theo hướng **"Từ ngoài vào trong" (Outside-in)**, trong khi quá trình Kiểm thử lại đi theo hướng **"Từ trong ra ngoài" (Inside-out)**.  
4. Phân chia rõ ràng trách nhiệm: Ai sẽ là người thực hiện Unit Test, Integration Test, System Test và Acceptance Test?

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Triển khai và Tự động hóa Kiểm thử**

* Việc con người tự tay nhập từng Input, bấm nút, rồi ghi chép lại kết quả ra giấy là vô cùng tẻ nhạt, mất thời gian và dễ sai sót.  
* Giải pháp của các Lập trình viên là **viết ra một chương trình để đi test một chương trình khác** (Ví dụ như khi bạn viết các class kiểm thử tự động bằng JUnit trong dự án Java Backend của mình, cứ mỗi lần chạy là nó tự động quét qua hàng loạt hàm xử lý).  
* Các công cụ tự động sẽ giúp: Ghi lại thao tác, đẩy hàng loạt dữ liệu (từ file Excel hoặc Database) vào phần mềm, và tự động so sánh kết quả để báo Xanh (Pass) hoặc Đỏ (Fail).

#### **2\. Quy trình Thực thi Kiểm thử và Lên kế hoạch**

* **Vòng lặp Test \- Debug:** Cài đặt môi trường \-\> Đưa Input \-\> Lấy Kết quả thực tế \-\> So sánh với Kỳ vọng \-\> Nếu sai thì quay về Debug \-\> Sửa xong thì **bắt buộc phải chạy lại Test** để xác nhận \-\> Ghi nhận kết quả vào file theo dõi.  
* **Nỗi đau Deadline:** Lên kế hoạch kiểm thử cực kỳ khó vì bạn không thể lường trước việc "bắt một con Bug sẽ mất bao lâu". Do đó, khâu Testing thường hay bị dồn rập vào sát ngày Deadline của dự án.

#### **3\. Tư duy "Inside-out" (Từ trong ra ngoài)**

Thầy Kenneth chỉ ra một sự tương phản rất hay giữa làm code và test code:

* **Khi Xây dựng (Outside-In):** Bạn bắt đầu từ bên ngoài (Lấy yêu cầu của khách hàng) \-\> Đi dần vào trong (Thiết kế kiến trúc) \-\> Đi vào lõi (Viết từng dòng code).  
* **Khi Kiểm thử (Inside-Out):** Bạn bắt đầu từ trong lõi (Test từng dòng code) \-\> Đi dần ra ngoài (Ghép các module lại) \-\> Đi ra ngoài cùng (Trình diễn giao diện cho khách hàng dùng thử).

#### **4\. Bốn Cấp độ Kiểm thử Kinh điển**

Quá trình "Inside-out" được chia làm 4 nấc thang, quy định rõ ai làm việc gì và dùng kỹ thuật nào:

* **Bậc 1: Unit Testing (Kiểm thử Mức Đơn vị)**  
  * **Mục tiêu:** Test từng hàm, từng class riêng lẻ (cái lõi nhỏ nhất).  
  * **Kỹ thuật chủ đạo:** Hộp trắng (White-box).  
  * **Người thực hiện:** Chính Lập trình viên (Developer).  
* **Bậc 2: Integration Testing (Kiểm thử Tích hợp)**  
  * **Mục tiêu:** Ghép các class hoặc các module lại với nhau xem chúng có "nói chuyện" được với nhau không (Ví dụ: Module Giỏ hàng gọi sang Module Thanh toán).  
  * **Kỹ thuật chủ đạo:** Kết hợp cả Hộp trắng và Hộp đen.  
  * **Người thực hiện:** Lập trình viên hoặc Đội Test (Testing Team).  
* **Bậc 3: System Testing (Kiểm thử Hệ thống)**  
  * **Mục tiêu:** Test toàn bộ hệ thống phần mềm đã được lắp ráp hoàn chỉnh.  
  * **Kỹ thuật chủ đạo:** Hoàn toàn là Hộp đen (Black-box). Lúc này không ai nhìn vào code nữa.  
  * **Người thực hiện:** Đội Test chuyên nghiệp (Testing Team).  
* **Bậc 4: Acceptance Testing (Kiểm thử Nghiệm thu)**  
  * **Mục tiêu:** Chứng minh cho khách hàng thấy phần mềm đáp ứng đúng yêu cầu hợp đồng (Validation) để chốt dự án.  
  * **Kỹ thuật chủ đạo:** Hộp đen (Black-box).  
  * **Người thực hiện:** Khách hàng (Client) hoặc Người dùng cuối (Users).

