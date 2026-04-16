# **Agile Philosophy**

Chào mừng bạn đến với **Agile** \- triết lý làm việc đang thống trị ngành công nghiệp phần mềm hiện nay\! Nếu bạn ứng tuyển vào bất kỳ công ty công nghệ nào, từ startup cho đến tập đoàn lớn, 99% họ sẽ hỏi bạn: *"Em có biết làm việc theo mô hình Agile/Scrum không?"*

Dưới đây là phần bóc tách chi tiết bài giảng siêu quan trọng này của Thầy Kenneth:

### **🎯 Mục Tiêu Bài Học**

Bạn sẽ hiểu được cốt lõi của triết lý Agile (Linh hoạt) và phân biệt được nó với các mô hình truyền thống (như Waterfall). Trọng tâm lớn nhất của bài là giúp bạn nắm vững các thuật ngữ, vai trò và cách vận hành của framework **Scrum** \- một trong những biến thể phổ biến nhất của Agile.

---

### **🧠 Nội Dung Trọng Tâm & Chi Tiết**

#### **1\. Triết lý Agile (Bản Tuyên Ngôn Agile)**

Agile không phải là một công thức cứng nhắc, nó là một "tư duy" dựa trên việc đánh đổi các ưu tiên:

* **Coi trọng Cá nhân và Tương tác** HƠN LÀ Quy trình và Công cụ.  
* **Coi trọng Phần mềm chạy được (Working software)** HƠN LÀ Tài liệu đồ sộ.  
* **Coi trọng Hợp tác với khách hàng** HƠN LÀ Đàm phán hợp đồng.  
* **Coi trọng Phản hồi sự thay đổi (Responsiveness)** HƠN LÀ Bám sát kế hoạch ban đầu.  
  *(Lưu ý: Agile không vứt bỏ quy trình hay tài liệu, nó chỉ ưu tiên sự linh hoạt và sản phẩm thực tế hơn).*

#### **2\. Các phương pháp (Practices) chung của Agile**

Thầy Kenneth giới thiệu 3 phương pháp làm việc đặc trưng của giới Agile:

* **Planning Poker:** Dùng các lá bài để cả team cùng "bỏ phiếu" ước lượng thời gian cho 1 tính năng.  
* **Pair Programming (Lập trình theo cặp):** Hai dev ngồi chung 1 máy tính. Một người gõ code, một người nhìn màn hình soi lỗi ngay lập tức để tránh sai sót.  
* **Test Driven Development (TDD):** Viết kịch bản test (bài kiểm tra) TRƯỚC khi viết code. Code sao cho vượt qua bài test đó là xong.

#### **3\. Các Mô hình (Frameworks) thuộc trường phái Agile**

Trong bài, Thầy đề cập đến 3 quy trình cụ thể áp dụng tư duy Agile:

**A. Extreme Programming (XP \- Lập trình Cực hạn)**

Quy trình XP chia làm 2 giai đoạn cực kỳ rạch ròi về mặt trách nhiệm:

**1\. Giai đoạn Lấy yêu cầu và Phân tích (Requirements and analysis)**

* **Developer (Lập trình viên):** Đóng vai trò là thợ xây. Họ nhìn vào hệ thống để xác định xem cần làm những tính năng (features) nào, sau đó đưa ra **ước lượng (estimates) về thời gian và chi phí** cho từng tính năng đó. *(Khác với Waterfall là BA đi lấy yêu cầu, ở đây Dev làm trực tiếp).*  
* **Client (Khách hàng):** Đóng vai trò là người chi tiền. Dựa trên bảng báo giá và thời gian của Dev, khách hàng sẽ có quyền **chọn lựa tính năng nào** được nhét vào vòng lặp (iteration) sắp tới để làm trước.

**2\. Giai đoạn Thực thi (Implementation)**

* Sau khi khách hàng chốt tính năng, **Developer** sẽ "băm nhỏ" vòng lặp đó ra thành các đầu việc nhỏ hơn (**Tasks**).  
* Các Tasks này có thể được chia cho nhiều người làm **song song (parallel)**.  
* Điểm "cực hạn" (Extreme) của quy trình này nằm ở 3 nguyên tắc Dev bắt buộc phải tuân thủ cho **MỖI TASK**:   
  1\. **Thiết kế Test Cases trước (TDD):** Chưa cần biết code ra sao, phải viết kịch bản bắt lỗi trước.  
  2 .**Code bằng Pair Programming:** Hai Dev cùng ngồi một máy để code cái task đó.  
  3\. **Tích hợp (Integrates):** Làm xong task nào là phải ghép ngay đoạn code đó vào sản phẩm chung hiện tại (khá giống với tinh thần của Continuous Integration).

→ lập trình cực hạn chỉ làm việc với 2 vai trò là dev và khách hàng

**B. Continuous Integration (CI \- Tích hợp Liên tục)**

* Đặc trưng: Lập trình viên không ôm code trên máy mình cả tháng. Mỗi ngày, cứ làm xong một đoạn nhỏ là đẩy ngay lên kho chứa chung (Shared Repository).  
* Hệ thống máy chủ CI (CI Server) sẽ tự động ghép code và chạy test. Nếu code mới làm hỏng hệ thống, nó báo lỗi ngay lập tức. Giúp giảm thiểu "địa ngục tích hợp" vào cuối dự án.

**C. Scrum (Ngôi sao của bài học)**

Đây là quy trình Agile phổ biến nhất thế giới. Bạn phải thuộc nằm lòng các thuật ngữ sau:

**3 Vai Trò (Roles) trong Scrum:**

1. **Product Owner (Chủ Sản phẩm):** Thường là khách hàng hoặc người đại diện khách hàng. Người đưa ra yêu cầu, xếp hạng mức độ ưu tiên tính năng và nghiệm thu sản phẩm.  
2. **Scrum Master (Điều phối viên):** Tương đương Project Manager. Người giữ nhịp dự án, tổ chức các cuộc họp, và "dọn dẹp chướng ngại vật" để team dev yên tâm code. (Không tham gia code).  
3. **Development Team:** Những người trực tiếp làm ra sản phẩm (Dev, Tester, UI/UX...).

**3 Tài Liệu (Artifacts) trong Scrum:**

1. **Product Backlog:** Danh sách (Wish-list) TOÀN BỘ các tính năng cần làm của dự án.  
2. **Sprint Backlog:** Danh sách các tính năng được bốc ra từ Product Backlog để làm trong một khoảng thời gian ngắn (Sprint).  
3. **Burndown Chart:** Biểu đồ "Đốt cháy công việc". Đường biểu diễn đi xuống dốc, thể hiện số lượng công việc CÒN LẠI theo từng ngày. Nhìn vào biểu đồ là biết team đang đi đúng tiến độ hay bị trễ.

**Cách Scrum vận hành (Sự kiện \- Events):**

* **Sprint:** Một vòng lặp ngắn hạn (thường từ 2 \- 4 tuần). Mục tiêu là cuối mỗi Sprint phải ra được một chức năng hoàn chỉnh có thể chạy được (Ship-ready state). *Luật thép: Không được phép đổi yêu cầu khi Sprint đang chạy.*  
* **Sprint Planning Meeting:** Họp đầu Sprint để bốc tính năng từ Product Backlog vào Sprint Backlog.  
* **Daily Scrum (Stand-up meeting):** Họp đứng 15 phút mỗi sáng. Mọi người trả lời 3 câu hỏi: Hôm qua làm gì? Hôm nay làm gì? Có gặp khó khăn gì không?

#### **4\. Ưu và Nhược điểm của Agile**

* **Ưu điểm:** Cực kỳ thích ứng với thay đổi. Đưa sản phẩm ra thị trường nhanh (Fast to market). Chất lượng cao vì lỗi được dọn sạch sau mỗi Sprint. Khách hàng vui vì được nhìn thấy sản phẩm liên tục.  
* **Nhược điểm:** Đòi hỏi khách hàng phải cực kỳ nhiệt tình (suốt ngày phải họp với team). Tài liệu sơ sài (vì mải lo code). Rất dễ bị "Scope Creep" (Khách hàng thấy hay quá nên đòi nhét thêm tính năng vô tội vạ). Các cuộc họp hàng ngày đôi khi gây mệt mỏi cho team.

---

→ Agile là 1 trường phái trong đó bao gồm nhiều khung phát triển và khi khung phát triển triển khai thực tế thì gọi là quy trình phát triển

