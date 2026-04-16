# **Project Planning**

Bài học này chính là cẩm nang sinh tồn dành cho những ai đóng vai trò là "Thuyền trưởng" (Trưởng nhóm / Project Manager). Thầy Kenneth đã chỉ ra rằng: Code giỏi chưa chắc dự án đã thành công, nhưng lên kế hoạch tồi thì chắc chắn dự án sẽ thất bại.

Dưới đây là phần bóc tách những kỹ năng lập kế hoạch cốt lõi từ Bài 1-3:

### **🎯 Mục Tiêu Bài Học**

Bạn sẽ học cách biến một mớ yêu cầu hỗn độn thành một kế hoạch tác chiến rõ ràng: Chia việc cho ai, chia như thế nào, làm sao để ước lượng thời gian không bị "hố", và cách quản lý tiến độ từ bức tranh toàn cảnh đến từng chi tiết nhỏ.

---

### **🧠 Nội Dung Trọng Tâm (Core Content)**

Nhận lệnh\! Nếu bạn muốn một bản tóm tắt **"vắt kiệt" từng chữ** của Thầy Kenneth trong Lecture 1-3, mình sẽ bóc tách chi tiết toàn bộ transcript này thành một bản hệ thống kiến thức toàn diện nhất. Không bỏ sót bất kỳ chi tiết nào\!

Dưới đây là **Bản tóm tắt Đầy đủ & Chi tiết nhất** của Lecture 1-3: Project Planning:

---

### **1\. Tổ chức Đội ngũ Dự án (Project Organization)**

Lập kế hoạch không chỉ là chia việc, mà là xếp người. Kế hoạch dự án phải chỉ rõ: Các vai trò, trách nhiệm và số lượng nhân sự cần thiết.

* **Quy tắc "Nhân tố gánh team":** Để tăng tỷ lệ thành công, bắt buộc/nên có ít nhất một thành viên đã từng có kinh nghiệm làm một hệ thống tương tự trong quá khứ.  
* **Chiến lược "Modular" (Chia để trị):** Không dồn một đống người vào làm chung một thứ. Phải chia nhỏ hệ thống phần mềm lớn thành các "mảnh" (pieces/modules) nhỏ hơn.  
  * *Lý do:* Giảm thiểu sự phức tạp trong giao tiếp. Nhóm quá đông sẽ gây nhiễu loạn thông tin.  
* **Phân quyền trách nhiệm:** Giao cho các nhóm nhỏ chịu trách nhiệm thiết kế và code một (hoặc vài) phần cụ thể.  
* **Chỉ định "Đầu tàu" (Person in charge):** Bắt buộc phải có một người chịu trách nhiệm chính cho từng phần nhỏ, và một người chịu trách nhiệm cho TOÀN BỘ hệ thống. Nếu có lỗi xảy ra, bạn biết chính xác cần "nắm đầu" ai.  
* **Chìa khóa thành công:** Đạt được mức độ giao tiếp (communication) vừa đủ và đúng mực trong toàn dự án.

### **2\. Định nghĩa Task (Nhiệm vụ) và Activity (Hoạt động)**

* **Task (Công việc/Nhiệm vụ):** Là một khối lượng công việc được định nghĩa rõ ràng, giao cho đúng MỘT vai trò/người cụ thể.  
* **Activity (Hoạt động):** Là một nhóm (group) bao gồm nhiều Task có liên quan mật thiết với nhau.  
* **Hai trường phái lập kế hoạch:**  
  * *Plan-driven (Truyền thống):* Lên kế hoạch chi tiết từng li từng tí ngay từ lúc bắt đầu dự án.  
  * *Agile (Linh hoạt):* Kế hoạch được bổ sung và điều chỉnh tăng dần trong quá trình làm. (Việc chọn cách nào phụ thuộc vào tính chất dự án, Thầy sẽ dạy kỹ ở bài sau).

### **3\. Lập Lịch trình Dự án (Project Schedule)**

Một lịch trình chuẩn phải bao gồm: Các Task, thứ tự thực hiện (ordering), thời gian ước lượng, người phụ trách (resource assigning), cột mốc (milestones) và sản phẩm bàn giao (deliverables).

Bạn phải quản lý song song **3 cấp độ Lịch trình**:

1. **Master Schedule (Lịch Tổng thể):** Bức tranh toàn cảnh dùng để quản lý cấp cao và báo cáo, giao tiếp với khách hàng.  
2. **Macro-schedule (Lịch Vĩ mô):** Dùng cho quản lý dự án hàng ngày (day-to-day).  
3. **Micro-schedule (Lịch Vi mô):** Dùng để quản lý chi tiết trong nội bộ team code.  
   *(Note: Thầy hé lộ sẽ dạy sử dụng Biểu đồ Burndown và Biểu đồ Gantt để quản lý các lịch này ở các bài sau).*

### **4\. Nghệ thuật Ước lượng (Estimating) \- Nơi chứa nhiều Rủi ro nhất**

→ **Để trả lời khách hàng về thời gian làm dự án**   
Project Manager phải tính toán được: Quy mô dự án, Công sức (effort), Thời lượng (duration), Năng suất (productivity) và Chi phí (cost).

* **Cơ sở để ước lượng:** Dựa vào kinh nghiệm, dữ liệu lịch sử (từ các dự án cũ) hoặc các mô hình toán học. Tuy nhiên, yếu tố *Kinh nghiệm* của nhân sự là quan trọng nhất để ra được con số thực tế.  
* **Ba cách để giảm thiểu Rủi ro ước lượng sai:**  
  1. **Chốt cứng Phạm vi (Scope) ngay từ đầu:** Biết chính xác cái gì phải làm và cái gì KHÔNG làm.  
  2. **Dùng dữ liệu lịch sử:** Ví dụ, dự án cũ làm một app tương tự tốn 10.000 dòng code và 5 người, hãy lấy đó làm hệ quy chiếu.  
  3. **Chia để trị (Divide and Conquer):** Chia dự án lớn thành các mảnh nhỏ \-\> Ước lượng thời gian cho từng mảnh nhỏ \-\> Cộng tổng lại sẽ chính xác hơn là ngồi đoán mò cho cả một cục to.

### **5\. Quy trình (Process) \- Chữ "P" cốt lõi**

* **Định nghĩa:** Là toàn bộ các Hoạt động (activities / workflows) và Trình tự của chúng nhằm biến Yêu cầu (Requirements) thành Sản phẩm (Product).  
* **Đặc tính của Quy trình:**  
  1. Đưa ra các nguyên tắc chỉ đạo mục tiêu cho từng hoạt động.  
  2. Mỗi hoạt động đều có **Tiêu chí Bắt đầu (Entry)** và **Tiêu chí Kết thúc (Exit)** rõ ràng. (Biết khi nào được bắt đầu làm và khi nào được tính là xong).  
  3. Áp dụng các giới hạn, ràng buộc (về thời gian, nhân sự) để kiểm soát.  
* **8 Lý do BẮT BUỘC phải có Quy trình:**  
  1. Giúp quản lý dự án dễ dàng hơn.  
  2. Cho phép phân chia lao động (Division of labor) rõ ràng.  
  3. Thúc đẩy teamwork, hiệu suất cá nhân và giao tiếp.  
  4. **Tái sử dụng (Reuse):** Nếu quy trình này thành công, có thể bế nguyên xi nó sang áp dụng cho dự án mới.  
  5. Dễ dàng đào tạo (Training) nhân sự mới.  
  6. Tăng năng suất (Productivity).  
  7. Tăng chất lượng phát triển phần mềm.  
  8. Ép dự án phải có cấu trúc và tính nhất quán (Consistency).

---

