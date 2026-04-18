**Software Quality Assurance Activities**.

Nếu bài trước thiết lập tư duy "Tại sao phải làm SQA", thì bài này Thầy Kenneth sẽ đi thẳng vào thực tế: **"Làm SQA là cụ thể làm những việc gì?"**. Trong đó, Thầy nhấn mạnh vào hai vũ khí tối thượng của mọi công ty công nghệ: **Standards (Tiêu chuẩn)** và **Metrics (Độ đo)**.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Nắm được danh sách các hoạt động thực tế để đảm bảo chất lượng phần mềm (Reviews, SCM, Testing, v.v.).  
2. Phân biệt được sự khác nhau giữa **Tiêu chuẩn Sản phẩm (Product Standards)** và **Tiêu chuẩn Quy trình (Process Standards)**.  
3. Hiểu được tầm quan trọng của việc lượng hóa chất lượng bằng **Độ đo (Metrics)** thay vì chỉ "đoán mò".

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Tổng quan các Hoạt động SQA (SQA Activities)**

Để tạo ra một phần mềm chất lượng, bạn không thể phó mặc cho sự may rủi. Bạn phải thực hiện các hoạt động sau:

* Thiết lập **Tiêu chuẩn (Standards)** để mọi người cùng tuân theo.  
* Thiết lập **Độ đo (Metrics)** để đánh giá mức độ đạt tiêu chuẩn.  
* Sử dụng **Công cụ (Tools)** tốt để hỗ trợ phát triển (ví dụ: IDE như IntelliJ, VS Code mà bạn đang dùng).  
* Thực hiện **Đánh giá (Reviews)** thường xuyên để bắt lỗi sớm.  
* Quản lý **Cấu hình phần mềm (Software Configuration Management \- SCM)** (ví dụ: dùng Git/GitHub để quản lý phiên bản code, tránh việc code đè lên nhau).  
* Thực hiện **Kiểm thử (Testing)** đầy đủ.

#### **2\. Tiêu chuẩn (Standards) là gì?**

Đó là những quy định, tiêu chí kỹ thuật chuẩn mực được lập ra để ép mọi người làm việc theo một "form" chung. Có 2 loại chính:

* **Product Standards (Tiêu chuẩn Sản phẩm):** Tập trung vào *KẾT QUẢ*. Nó định nghĩa sản phẩm đầu ra phải trông như thế nào.  
  * *Ví dụ:* Code Java phải viết theo quy tắc đặt tên CamelCase (e.g., calculateTotal), tài liệu yêu cầu (SRS) phải có đầy đủ sơ đồ Use Case.  
* **Process Standards (Tiêu chuẩn Quy trình):** Tập trung vào *CÁCH LÀM*. Nó định nghĩa các bước mà team phải trải qua để làm ra sản phẩm đó.  
  * *Ví dụ:* Trước khi gộp code (merge) vào nhánh main trên GitHub, bắt buộc phải có 1 người khác vào Review (đọc chéo) code và duyệt (Approve).

**Tại sao Tiêu chuẩn lại quan trọng?**

* **Ngăn ngừa sai lầm:** Vì nó đúc kết những phương pháp tốt nhất (best practices) của những người đi trước.  
* **Giảm thời gian học việc (Onboarding):** Người mới vào team chỉ cần đọc cuốn sổ tay tiêu chuẩn (Standard Handbook) là biết team đang làm việc theo style nào.  
* **Tính linh hoạt:** Không phải dự án nào cũng dùng chung một bộ tiêu chuẩn. Với mỗi dự án mới, Leader (như bạn) sẽ phải quyết định xem tiêu chuẩn nào giữ nguyên, tiêu chuẩn nào cần bỏ, hoặc cần tạo thêm mới cho phù hợp.

#### **3\. Độ đo (Metrics) là gì?**

"Bạn không thể quản lý thứ mà bạn không thể đo lường được". Thay vì nói *"Code của em phức tạp lắm"*, SQA yêu cầu bạn phải có con số chứng minh.

* **Định nghĩa:** Metric là bất kỳ phép đo lường nào liên quan đến sản phẩm, quy trình, hoặc tài nguyên phần mềm.  
* **Công dụng 1 \- Kiểm soát quy trình:** Đo lường effort (công sức), thời gian, và ngân sách để biết dự án có đang chạy đúng tiến độ hay không.  
* **Công dụng 2 \- Dự đoán chất lượng:** Thầy Kenneth đưa ra một ví dụ kinh điển: **Độ phức tạp Cyclomatic (Cyclomatic Complexity)**.  
  * Nếu một hàm của bạn chứa quá nhiều vòng lặp for lồng nhau và các lệnh rẽ nhánh if/else, chỉ số Cyclomatic sẽ rất cao.  
  * Nhìn vào chỉ số này, kỹ sư QA có thể *dự đoán* ngay: "Hệ thống này sau này sẽ cực kỳ khó bảo trì và rất dễ sinh ra bug ẩn".

Tóm lại, bài học này rèn cho bạn tư duy: Làm việc phải có quy tắc (Standards) và đánh giá phải dựa trên con số (Metrics) chứ không dựa trên cảm tính.

Bạn đã sẵn sàng để xem Thầy Kenneth hướng dẫn cách áp dụng những tiêu chuẩn này để tạo ra một Sản phẩm (Product) cụ thể trong bài tiếp theo **Lecture 5-3 Achieving Product Quality** chưa?

