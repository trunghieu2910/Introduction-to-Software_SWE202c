# **Introduction to Software Development**

(Phạm vi toàn bộ SDLC tổng quan )

Dưới đây là phần tổng hợp chi tiết Mục tiêu và Nội dung trọng tâm của **Bài 1-1: Nhập môn Phát triển Phần mềm**, được đúc kết từ bài giảng của Thầy Kenneth:

### **🎯 Mục Tiêu Bài Học (Learning Objectives)**

Sau khi hoàn thành bài học này, bạn sẽ:

* Hiểu được cách một phần mềm được lên kế hoạch, quản lý và phát triển trong thực tế.  
* Nắm bắt được các loại hình dự án phần mềm khác nhau mà một Kỹ sư phần mềm (Software Engineer) sẽ gặp phải khi đi làm.  
* Nắm được Vòng đời Phát triển Phần mềm (SDLC) và các thành phần cấu tạo nên một quy trình phát triển tốt (chuẩn bị cho các bài học về mô hình Agile/Iterative sau này).

---

### **🧠 Nội Dung Trọng Tâm (Core Content)**

#### **1\. Bản chất đặc thù của dự án Phần mềm**

Phát triển phần mềm rất khác biệt so với các ngành kỹ thuật truyền thống (như sản xuất ô tô hay xây nhà) vì 4 đặc tính:

* **Vô hình (Intangible):** Rất khó để hình dung toàn bộ chi tiết dự án khi mới bắt đầu (không giống như việc có thể làm mô hình sa bàn cho một ngôi nhà).  
* **Dễ nhân bản (Easy to mass-produce):** Sản phẩm cuối cùng là mã nguồn (source code), việc sao chép ra hàng triệu bản gần như không tốn chi phí.  
* **Thâm dụng lao động (Labor-intensive):** Tài nguyên tốn kém nhất và quan trọng nhất không phải là máy móc, mà là sức lực và chất xám của Lập trình viên.  
* **Không hao mòn (Does not wear out):** Code không bị rỉ sét hay mòn đi theo thời gian sử dụng như các cỗ máy vật lý.

#### **2\. Phân loại Phần mềm**

Thầy Kenneth chia phần mềm thành 3 loại chính:

* **Phần mềm đại trà (Generic software / COTS):** Làm cho thị trường chung (vd: Windows, MS Office).  
* **Phần mềm nhúng (Embedded software):** Code nạp vào phần cứng/vi điều khiển (vd: phần mềm trong DVD player).  
* **Phần mềm tùy chỉnh (Custom software):** Viết riêng cho một khách hàng/doanh nghiệp. Trọng tâm của khóa học nằm ở loại này vì khâu thu thập yêu cầu cực kỳ phức tạp và dễ gây thất bại.  
+ **Phần mềm trong Hệ thống xử lý dữ liệu (Data processing system):** phục vụ cho công tác quản trị,các nghiệp vụ , kinh doanh và ra quyết định. ⇒ chủ yếu là các thao tác CRUD   
+ **Phần mềm trong Hệ thống thời gian thực (Real-time processing system):** Là hệ thống mà tính đúng đắn của nó không chỉ phụ thuộc vào kết quả tính toán chính xác, mà còn phụ thuộc tuyệt đối vào việc kết quả đó phải được đưa ra trong một giới hạn thời gian cực kỳ nghiêm ngặt.  
+ **Phần mềm trong Hệ thống kỹ thuật (Technical system):** Là phần mềm được thiết kế để tự động thực hiện các nhiệm vụ cơ học, vật lý hoặc tính toán thuần túy, hoạt động dựa trên các nguyên lý kỹ thuật khách quan.  
+ **Phần mềm trong Hệ thống kỹ thuật \- xã hội (Socio-technical system):** Là hệ thống phức hợp giữa các phần mềm (Hệ thống kỹ thuật, Hệ thống thời gian thực, Hệ thống kỹ thuật )  hệ thống trên và các quy tắc của xã hội, gắn kèm với con người   
* **Phân biệt phần mềm của hệ thống Kỹ Thuật và phần mềm hệ thống nhúng  ?** 

→ Phần mềm của hệ thống kỹ thuật mang tính chất là server quản lý các phần mềm hệ thống nhúng . Lúc này phần mềm của hệ thống kỹ thuật đóng vai trò là server / master còn phần mềm hệ thống nhúng đóng vai trò là client / slave . Hệ thống kỹ thuật ra lệnh cho hệ thống nhúng. .

#### **3\. Phân loại Dự án (Điều sẽ gặp khi đi làm)**

* **Green field project:** Xây dựng mọi thứ lại từ đầu (từ con số 0).  
* **Evolutionary project (Dự án tiến hóa):** Tiếp nhận một đống code có sẵn (legacy system) và được yêu cầu sửa lỗi (fix bugs), thêm tính năng mới, hoặc nâng cấp công nghệ. *Thầy Kenneth nhấn mạnh: Đây là loại dự án phổ biến nhất mà bạn sẽ gặp khi đi làm thực tế.*  
* **Framework-based:** Lấy một bộ khung (framework) có sẵn và đắp thêm các tính năng đặc thù của khách hàng lên đó.

#### **4\. Khái niệm Vòng đời và "Nguyên tắc 4 chữ P"**

Mỗi dự án đều phải trải qua một vòng đời (Life-cycle) bao gồm các pha: Xác định tính khả thi \-\> Thiết kế \-\> Xây dựng \-\> Triển khai \-\> Bảo trì cho đến khi khai tử. Để quản lý vòng đời này, một Project Manager phải kiểm soát được **4 chữ P**:

1. **Problem (Vấn đề):** Phải thu thập và hiểu rõ mọi yêu cầu từ lĩnh vực ứng dụng (Application domain).  
2. **People (Con người):** Quản lý các bên liên quan như Khách hàng, Người dùng cuối và Đội ngũ Kỹ sư.  
3. **Process (Quy trình):** Tập hợp các hoạt động, khuôn mẫu làm việc của team.  
4. **Product (Sản phẩm):** Kết quả đạt được (bao gồm Code, các sơ đồ UML, sách hướng dẫn...).

#### **5\. Nhiệm vụ tối thượng của người Quản lý Dự án**

Khi bắt đầu, công việc đầu tiên không phải là mở máy lên code, mà là:

* Xác định rõ **Phạm vi (Scope)**: Cái gì làm, cái gì KHÔNG làm.  
* Xác định **Mục tiêu (Objectives)** và **Ràng buộc (Constraints \- thường là Thời gian và Ngân sách)**.  
* Chốt các mục tiêu thiết kế (Design goals).  
* Phân tích yêu cầu (dùng Domain Model và Use Case Model đã học ở MOOC 2).  
* Ước lượng thời gian và công sức (Estimate timing and effort).

