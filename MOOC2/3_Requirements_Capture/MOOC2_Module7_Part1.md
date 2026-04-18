# **Non-Functional Requirements**

(**Hệ thống làm điều đó TỐT ĐẾN MỨC NÀO?**)

Chào mừng bạn đến với chặng cuối cùng của SRS\! Ở Mô-đun 5 và 6, chúng ta đã trả lời câu hỏi **"Hệ thống làm được gì?" (Functional)**. Bây giờ, Giáo sư Kenneth đưa chúng ta đến câu hỏi quyết định sự sống còn của dự án: **"Hệ thống làm điều đó TỐT ĐẾN MỨC NÀO?" (Non-Functional)**.

Thực tế đi làm, khách hàng rất hiếm khi tự nói ra những điều này, họ mặc định bạn phải tự biết\! Nếu code xong mà app chạy rùa bò, bảo mật lỏng lẻo, BA (Business Analyst) sẽ là người bị "gõ đầu" đầu tiên.

Dưới đây là tóm tắt những tinh hoa của Bài 7-1:

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Bài học này giúp bạn thay đổi tư duy: Từ việc chỉ tập trung vào "Tính năng" sang việc rào trước các **"Ràng buộc" (Constraints)** về mặt chất lượng, hiệu năng, nền tảng, và bảo mật của hệ thống.

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

#### **1\. Yêu cầu Phi chức năng (NFRs) là gì?**

* **Bản chất:** Là những điều kiện rành buộc (constraints) ép hệ thống phải tuân theo.  
* Hệ thống có thể chạy đúng logic (Function), nhưng nếu không đạt chuẩn NFR thì vẫn bị coi là sản phẩm lỗi.

#### **2\. Các danh mục NFRs phổ biến (Từ ví dụ "Đồng hồ Set Watch")**

Thầy Kenneth đã bóc tách từng câu chữ của khách hàng để phân loại ra các nhóm rành buộc:

* **Giao diện & Tính khả dụng (Interface / Usability):** *"Bất kỳ ai biết xem đồng hồ điện tử đều dùng được"*. (Phần mềm phải dễ dùng, không cần đào tạo).  
* **Chất lượng Thiết kế (Design Quality):**  
  * **Độ tin cậy (Reliability):** *"Không bao giờ bị sập nguồn/phải reset"*.  
  * **Khả năng hỗ trợ (Supportability):** *"Phải cho phép nâng cấp qua cổng USB"*.  
* **Hiệu năng (Performance):**  
  * **Thời gian phản hồi (Response Time):** *"Cập nhật múi giờ trong vòng 5 phút sau khi có sóng"*.  
  * **Độ chính xác (Accuracy):** *"Sai số không quá 1/100 giây trong 5 năm"*.  
* **Triển khai & Kỹ thuật (Implementation):** *"Phải code bằng ngôn ngữ Java"*. (Khách hàng ép ngôn ngữ/công nghệ).  
* **Bảo mật & Quản lý (Security / Management):** Đảm bảo an toàn dữ liệu, phân quyền truy cập, backup hệ thống.

#### **3\. ⚠️ Ngoại lệ thú vị: "Admin Use Cases"**

Thầy Kenneth chỉ ra một điểm giao thoa rất hay: Có những thứ vốn là Yêu cầu *Phi chức năng* (Ví dụ: "Hệ thống phải bảo mật"), nhưng để code được nó, chúng ta phải biến nó thành các Yêu cầu *Chức năng* (Ví dụ: Tính năng Đăng nhập, Tính năng Backup dữ liệu, Tính năng Cấp quyền).

\-\> Những Use Case sinh ra chỉ để phục vụ hệ thống (chứ không phải cho luồng nghiệp vụ kinh doanh chính) được gọi là **Administration Use Cases (Ca sử dụng Quản trị)**.

---

