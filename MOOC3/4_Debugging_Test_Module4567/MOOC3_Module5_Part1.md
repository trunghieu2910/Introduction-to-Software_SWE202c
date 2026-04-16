# **Testing**

Chào mừng bạn chính thức bước vào thế giới của những "kẻ phá hoại" mã nguồn hợp pháp\!  
Thầy Kenneth đã mở đầu bài giảng bằng một sự thật khá thú vị: **Kiểm thử (Testing) là một hoạt động mang tính hủy diệt (Destructive activity)**. Thay vì cố gắng chứng minh code của mình chạy đúng, nhiệm vụ của bạn bây giờ là làm mọi cách để chứng minh code của mình... sai.

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung cốt lõi của **Lecture 5-1**:

### **🎯 Mục Tiêu Bài Học**

Sau bài học này, bạn sẽ nắm được:

1. Mục đích thực sự của Kiểm thử (và tại sao Dev hay lười viết Test).  
2. Sự khác biệt sống còn giữa **Validation** (Xác nhận giá trị) và **Verification** (Xác minh tính đúng đắn).  
3. Tại sao chúng ta không thể test 100% mọi trường hợp (Exhaustive testing).  
4. Chiến thuật "Khoanh vùng dữ liệu" (Partitioning/Sub-domains) để tìm ra bộ Test Case nhỏ nhất nhưng tóm được nhiều Bug nhất.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Căn bệnh "Lười Test" và Hậu quả Tỷ đô**

Lập trình viên thường có rất nhiều lý do để ngụy biện cho việc không viết Test: *"Viết test làm chậm tiến độ", "Code của tôi là hoàn hảo", "Kiểm thử là việc của bọn gà mờ không biết code"*...

Tuy nhiên, hậu quả của việc thiếu kiểm thử là vô cùng tàn khốc. Thầy Kenneth đưa ra 2 ví dụ kinh điển:

* **Tên lửa Ariane 5 (Thiệt hại 1 tỷ USD):** Nổ tung sau 37 giây chỉ vì một lỗi ép kiểu dữ liệu từ số thực 64-bit sang số nguyên có dấu 16-bit gây tràn bộ nhớ.  
* **Sàn giao dịch chứng khoán Vancouver (1992):** Chỉ số chứng khoán tụt từ 1000 xuống 520 sau 22 tháng. Lý do cực kỳ ngớ ngẩn: Lập trình viên đã dùng hàm cắt bỏ phần thập phân (Truncated) thay vì hàm làm tròn (Rounded).  
* 👉 *Bài học thực chiến:* Đặc biệt khi bạn xây dựng các hệ thống backend tài chính hoặc ngân hàng, nơi giao dịch diễn ra liên tục với khối lượng khổng lồ, một lỗi làm tròn số lẻ cực nhỏ cũng có thể tích tụ thành sai lệch hàng tỷ đồng. Code càng quan trọng, càng phải test gắt gao.

#### **2\. Validation vs. Verification (Khái niệm Sinh tử)**

Khi đi làm, bạn bắt buộc phải phân biệt được hai thuật ngữ này:

* **Validation (Xác nhận giá trị):** Trả lời câu hỏi *"Chúng ta có đang xây dựng ĐÚNG CÁI SẢN PHẨM mà khách hàng cần không?"* (Build the right product). Tập trung vào việc đáp ứng nhu cầu thực tế của user.  
* **Verification (Xác minh tính đúng đắn):** Trả lời câu hỏi *"Chúng ta có đang xây dựng sản phẩm MỘT CÁCH ĐÚNG ĐẮN không?"* (Build the product right). Tập trung vào việc check xem code có lỗi không, thuật toán chạy có đúng logic không. **Hầu hết các bài Test của Developer đều nhắm vào Verification.**

#### **3\. Tại sao không thử "mọi trường hợp" (Exhaustive Testing)?**

Giả sử bạn có một hàm nhận vào 3 biến x, y, z (từ 1 đến 10.000). Nếu bạn muốn test mọi trường hợp, bạn phải chạy 10.000^3 kịch bản. Điều này là **bất thi (impractical)**.

**Mục tiêu tối thượng của Testing:** Không phải là test mọi thứ. Mục tiêu là tìm ra một **tập hợp Test Case NHỎ NHẤT** nhưng có **XÁC SUẤT tìm ra lỗi CAO NHẤT** trong thời gian ngắn nhất.

*(Lưu ý: Testing KHÔNG THỂ chứng minh phần mềm sạch bóng 100% lỗi, nó chỉ có thể chứng minh là có lỗi đang tồn tại).*

#### **4\. Chiến thuật "Chia để trị" (Partitioning / Sub-domains)**

Để tìm ra bộ Test case "nhỏ mà có võ" đó, chúng ta dùng thủ thuật gom nhóm dữ liệu. Thay vì test số 1, 2, 3, 4, 5... ta chia chúng thành các nhóm có hành vi giống hệt nhau, rồi rút ra đúng 1 số đại diện ở mỗi nhóm để test.

Có 2 cách gom nhóm:

* **Cách 1: Theo luồng thực thi (Execution Equivalence)**  
  * Ví dụ code có đoạn: if (x \< 0\). Ta chia làm 2 nhóm: Nhóm số âm (chọn đại số \-3) và Nhóm số dương (chọn đại số 3). Tập Test Case: **{-3, 3}**.  
  * *Rủi ro:* Nếu code bị viết sai thành if (x \< \-2), việc bạn thử số \-3 và 3 vẫn cho ra kết quả đúng\! Bạn không thể phát hiện ra cái bug \<-2 này.  
* **Cách 2: Theo kết quả Đúng/Sai (Sub-domains) \- Hiệu quả hơn\!**  
  * Với đoạn code lỗi if (x \< \-2) ở trên, ta chia theo kết quả:  
    * Nhóm luôn cho kết quả ĐÚNG: x \<= \-3 và x \>= 0\. (Chọn đại số \-3)  
    * Nhóm cho kết quả SAI (phát hiện được bug): x \= \-1 và x \= \-2. (Chọn đại số \-1).  
  * Vậy tập Test Case tối ưu nhất là: **{-3, \-1}**. Nó cực kỳ nhỏ gọn nhưng lại tóm gọn được cái Bug ẩn giấu kia.

Việc vận dụng các chiến thuật gom nhóm dữ liệu (Heuristics) này đòi hỏi bạn phải đọc được mã nguồn. Và đó chính là sự lợi hại của White Box Testing\!

