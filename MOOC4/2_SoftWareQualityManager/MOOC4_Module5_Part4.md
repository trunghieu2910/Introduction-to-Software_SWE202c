**Achieving Project-Process-People Quality**.

Bài giảng này đưa góc nhìn của chúng ta từ việc "soi" từng dòng code (ở bài trước) lên tầm nhìn của một Project Manager (Người quản lý dự án) và một CTO (Giám đốc công nghệ). Thầy Kenneth sẽ phân tích "Tam giác Vàng" quyết định thành bại của một tổ chức phần mềm: **Dự án (Project) \- Quy trình (Process) \- Con người (People)**.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu cách kiểm soát rủi ro ở cấp độ **Dự án (Project)** thông qua Reviews và SCM.  
2. Đánh giá sự trưởng thành của **Quy trình (Process)** trong công ty thông qua khung chuẩn **CMMI**.  
3. Đánh giá mức độ đầu tư vào **Con người (People)** của tổ chức thông qua khung chuẩn **PCMM**.  
4. Tổng hợp bức tranh toàn cảnh: Làm sao để xây dựng văn hóa "Chất lượng" cho cả công ty.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Đạt được Chất lượng Dự án (Project Quality)**

Để dự án đi đúng hướng, Thầy Kenneth nhấn mạnh 2 vũ khí bắt buộc:

* **Reviews (Đánh giá chéo) đa tầng:** Đừng chỉ đợi đến lúc có Code mới đem ra Review. Phải Review ngay từ khâu lấy Yêu cầu (Requirements) và Thiết kế (Design).  
  * *Sự thật phũ phàng:* 50-60% số bug của dự án sinh ra từ việc phân tích sai yêu cầu ban đầu. Nếu bạn tổ chức các buổi Review kỹ thuật (Formal Technical Reviews) tốt, bạn có thể "giết chết" 75% số bug này ngay trên giấy trước khi chúng biến thành những dòng code đắt đỏ.  
* **SCM (Software Configuration Management \- Quản lý cấu hình):** Mọi sự thay đổi (từ tài liệu, phiên bản database, đến source code) đều phải được quản lý chặt chẽ. (Ví dụ: Dùng Git, Jira). Nếu không có SCM, dự án sẽ biến thành một mớ hỗn độn khi có 2 người cùng sửa chung một file.

#### **2\. Đạt được Chất lượng Quy trình (Process Quality)**

* **Sự thật về Quy trình:** Quy trình tốt là cần thiết, nhưng nó KHÔNG THỂ sao chép 100%. *"Google dùng Agile thành công, không có nghĩa là công ty tôi copy y hệt quy trình đó thì cũng sẽ thành công."* Quy trình phải phù hợp với văn hóa nội bộ. Nếu thiếu tiền (budget) hoặc thiếu thời gian (time), thì quy trình thần thánh đến mấy dự án cũng sẽ nát.  
* **Thang đo CMMI (Capability Maturity Model Integration):** Đây là thước đo chuẩn quốc tế để chấm điểm "độ trưởng thành" của một công ty phần mềm.  
  * *Level 1 (Ad hoc):* Làm việc bản năng, không quản lý, mạnh ai nấy code.  
  * *Level 2:* Bắt đầu quản lý được thời gian, tiền bạc.  
  * *Level 3:* Quy trình được định nghĩa rõ ràng, ai vào cũng biết phải làm gì.  
  * *Level 4:* Bắt đầu dùng số liệu (Metrics) để đo lường hiệu quả.  
  * *Level 5 (Cao nhất):* Liên tục tối ưu hóa quy trình dựa trên phản hồi.

#### **3\. Đạt được Chất lượng Con người (People Quality)**

Software Engineering là ngành thiết kế sáng tạo, không phải dây chuyền sản xuất cơ khí. Do đó, **Con người & Công nghệ đôi khi còn quan trọng hơn cả Quy trình**.

* **Thang đo PCMM (People CMM):** Thước đo mức độ công ty đầu tư cho nhân viên.  
  * *Level 1:* Vào công ty tự bơi, không ai dạy dỗ.  
  * *Level 2:* Có training cơ bản lúc mới vào (ví dụ: dạy cách dùng tool nội bộ).  
  * *Level 3:* Có lộ trình phát triển tài năng rõ ràng.  
  * *Level 4:* Tập trung xây dựng tinh thần đồng đội (Team building).  
  * *Level 5:* Cá nhân xuất sắc, tập thể xuất sắc, liên tục cải tiến.  
* **Lời khuyên vàng từ Thầy Kenneth:** Khi đi xin việc (như lúc bạn apply vào MBBank hay MCredit), hãy chọn những công ty đạt chuẩn **CMM/PCMM từ Level 3 trở lên**. Ở đó, bạn mới được đào tạo bài bản và phát triển sự nghiệp thực sự.

#### **4\. Tổng kết Bức tranh SQA**

* Chất lượng không từ trên trời rơi xuống. Nó phải được nhúng (built-in) vào quy trình làm việc mỗi ngày.  
* **Testing (Kiểm thử) rất quan trọng, nhưng nó không phải là tất cả.** Testing chỉ là chốt chặn cuối cùng ở cuối dự án. SQA thực thụ phải làm từ đầu để bắt lỗi sớm.  
* Một tổ chức muốn đạt chất lượng cao phải có: **Sổ tay Tiêu chuẩn (Standard Handbook)**, **Kế hoạch Chất lượng (Quality Plan)** cho từng dự án, và sự cam kết thực hiện từ đội ngũ quản lý.

---

