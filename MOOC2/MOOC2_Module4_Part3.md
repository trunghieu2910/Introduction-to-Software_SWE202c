# **Domain Modeling \- Evaluating Associations and Attributes**

Tiếp tục guồng quay học tập nào\! Nếu Bài 4-2 giúp bạn tìm ra các viên gạch (Classes), thì Bài 4-3 này sẽ dạy bạn cách trát vữa (Associations) và sơn màu (Attributes) sao cho ngôi nhà không bị sập hay rối mắt.

Dưới đây là phần bóc tách nội dung theo đúng "chuẩn" bạn yêu cầu:

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Mục tiêu của bài này là học nghệ thuật **"Tỉa cành" (Refining & Eliminating)**. Thầy Kenneth muốn bạn nhận ra rằng: Không phải cứ gạch chân được bao nhiêu động từ/danh từ là nhét hết vào bản vẽ. Bạn phải biết đường liên kết nào bị thừa, thuộc tính nào bị đặt sai chỗ, và đặc biệt là cách xử lý "vòng lặp" (Cycle) trong sơ đồ để Domain Model trở nên gọn gàng, sát với thực tế kinh doanh nhất.

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

Giáo sư chia việc "tỉa cành" ra làm hai bộ lọc lớn:

#### **1\. Bộ lọc cho Mối liên kết (Evaluating Associations)**

Khi bạn có các sợi dây nối giữa các Class, hãy tự hỏi:

* **Có phải là Hành động (Operation) không?** Nếu sợi dây tên là Tính\_Tổng\_Tiền, nó là một hàm (method) của Class chứ không phải sợi dây liên kết \-\> *Xóa.*  
* **Có phải liên kết 3 ngôi (Ternary) không?** Đứng giữa 3 Class cùng lúc rất rối rắm \-\> *Nên bẻ gãy thành các liên kết 2 ngôi (Binary) cho dễ đọc.*  
* **⚠️ Vòng lặp thừa (Derived) vs Vòng lặp có ý nghĩa (Meaningful):** Đây là kiến thức quan trọng nhất bài\!  
  * *Luật chung:* Nếu đi từ A \-\> B, và đi từ A \-\> C \-\> B mà **ra cùng một lượng thông tin y hệt nhau**, thì 1 trong 2 đường là đồ thừa \-\> *Xóa bớt 1 đường.*  
  * *Cái bẫy kinh điển (Ví dụ của Thầy):* Sơ đồ có Vòng tròn giữa Khách hàng \- Tài khoản \- Giao dịch.  
    * *Đường 1:* Giao dịch \-\> Tài khoản \-\> Khách hàng (Cho biết tiền đi ra/đi vào từ ví của ai).  
    * *Đường 2:* Khách hàng \-\> Giao dịch (Cho biết ai là người cầm điện thoại bấm nút chuyển tiền).  
    * *Kết luận:* Khi A chuyển tiền cho B, Đường 1 không thể cho biết A hay B là người chủ động bấm chuyển. Do đó, Đường 2 mang **ý nghĩa hoàn toàn khác** \-\> **BẮT BUỘC GIỮ CẢ HAI ĐƯỜNG.**

#### **2\. Bộ lọc cho Thuộc tính (Evaluating Attributes)**

Khi rà soát các biến (variables) nằm trong Class:

* **Nó có gắn kết chặt chẽ với Class không?** Nếu không \-\> *Xóa hoặc đẩy sang Class khác.*  
* **Nó có bị kẹt giữa 2 người không?** (Ví dụ: Điểm thi nằm ở đâu? Không thể nằm ở Sinh viên, cũng không thể nằm ở Môn học) \-\> *Tạo ra một Association Class để chứa nó.*  
* **⛔ QUY TẮC TỬ THẦN (Loại bỏ toàn bộ ID):** Trong bước thiết kế Domain Model, bạn phải **XÓA SẠCH** mọi loại ID (Ví dụ: StudentID, OrderID).  
  * *Lý do:* ID là thứ nhân tạo (Artificial numbers) do cơ sở dữ liệu đẻ ra để dễ quản lý. Nó KHÔNG PHẢI là đặc tính thật của thực thể ngoài đời. (Con người đẻ ra có Tên, Tuổi, chứ không ai đẻ ra có sẵn mã thẻ CCCD in trên trán cả).

---

