**Achieving Product Quality**.

Bài giảng này đưa chúng ta vào một bài toán cực kỳ hóc búa của kỹ sư phần mềm: *Làm sao để biết code mình viết ra có "chất lượng" hay không khi mà dự án còn chưa code xong?* Thầy Kenneth sẽ hướng dẫn bạn cách "cân đo đong đếm" những khái niệm trừu tượng (như tính bảo trì) thành những con số toán học cụ thể. Đây là tư duy khác biệt hoàn toàn giữa một Coder và một Software Engineer.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu được ranh giới và cách ánh xạ giữa **External Attributes (Thuộc tính bên ngoài)** và **Internal Attributes (Thuộc tính bên trong)**.  
2. Làm quen với các công thức đo lường độ phức tạp kiến trúc: **Fan-in, Fan-out**.  
3. Biết đến các công cụ đo lường mức độ phức tạp của code (Ví dụ: Halstead's Software Science, McCabe's Cyclomatic Complexity).  
4. Áp dụng quy tắc **80-20 (Pareto)** trong việc sửa lỗi (bug).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Bài toán Đo lường Chất lượng Trừu tượng**

Mục tiêu thiết kế (Design Goals) thường là những thứ rất "chung chung" và chỉ khách hàng mới cảm nhận được (gọi là *External Attributes*). Ví dụ: *Hệ thống này phải dễ bảo trì (Maintainability)* hoặc *Hệ thống này phải dễ dùng (Usability)*.

**Vấn đề:** Đang code dở dang thì làm sao biết nó có "dễ bảo trì" không?

**Giải pháp:** Các Kỹ sư phải ánh xạ (map) những mục tiêu chung chung đó thành các *Internal Attributes* (Những thứ bên trong source code có thể đếm được).

* *Khách hàng muốn "Dễ bảo trì"?* Kỹ sư sẽ đếm: Số dòng code (Lines of code), số lượng tham số trong 1 hàm (Parameters), Độ phức tạp (Cyclomatic complexity). Code càng dài, hàm càng nhiều tham số \-\> Càng khó bảo trì.  
* *Khách hàng muốn "Dễ sử dụng"?* Kỹ sư sẽ đếm: Số lượng thông báo lỗi (Error messages) bắn ra, độ dài của cuốn Hướng dẫn sử dụng.

#### **2\. Đo lường Kiến trúc: Fan-in và Fan-out**

Khi thiết kế các Class, làm sao biết kiến trúc đó có tốt không? Thầy Kenneth đưa ra 2 khái niệm cốt lõi:

* **Fan-in (Đầu vào):** Có bao nhiêu Class khác đang *gọi đến* Class này?  
  * *Đánh giá:* Fan-in quá cao nghĩa là Class này đang bị quá nhiều nơi phụ thuộc vào (High Coupling). Nếu sửa Class này, nguy cơ làm chết hàng loạt tính năng khác là rất lớn.  
* **Fan-out (Đầu ra):** Class này đang phải *gọi đến* bao nhiêu Class khác để hoàn thành công việc của nó?  
  * *Đánh giá:* Fan-out quá cao nghĩa là Class này đang ôm đồm quá nhiều việc, dẫn đến độ phức tạp (Complexity) cực kỳ lớn.

👉 **Công thức kinh điển:** Complexity \= Component\_Length \* (Fan-in \* Fan-out)^2. Nếu chỉ số này cao, chứng tỏ bạn cần rất nhiều nhân lực (effort) để code và test module này.

#### **3\. Đo lường Mức Code (Implementation Level)**

Khi bắt tay vào gõ code thực tế, Thầy Kenneth giới thiệu một số chỉ số báo động đỏ:

* **McCabe's Cyclomatic Complexity:** Đếm số lượng đường dẫn (path) đi qua một hàm. Cứ có 1 vòng lặp for, hoặc 1 lệnh rẽ nhánh if/else, điểm số sẽ tăng lên. Điểm càng cao, hàm càng dễ sinh ra bug ẩn.  
* **Depth of conditional nesting:** Mức độ lồng nhau của các điều kiện. Ví dụ: if lồng trong for, rồi lại lồng trong while, rồi lại switch. Càng lồng sâu, code càng rác và không thể đọc nổi.  
* **Length of identifiers:** Tên biến/tên hàm quá dài dòng cũng làm code trở nên rối rắm.

#### **4\. Quy tắc 80-20 trong sửa lỗi (The 80-20 Rule)**

Đây là "kim chỉ nam" cho dân QA/QC: **80% số lỗi (bugs) sinh ra từ 20% nguyên nhân gốc rễ.**

Thay vì hì hục đi sửa từng cái bug lặt vặt tốn hàng tháng trời, hãy nhóm chúng lại, phân tích nguyên nhân gốc. Chỉ cần diệt được 20% nguyên nhân lõi đó, hệ thống của bạn sẽ tự động biến mất 80% số bug.

---

