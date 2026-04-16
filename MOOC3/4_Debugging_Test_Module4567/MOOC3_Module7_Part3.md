# **Acceptance Testing Example**

# Bài giảng **Lecture 7-3: Acceptance Testing Example** chính là "nhát búa cuối cùng" để chốt lại toàn bộ vòng đời phát triển phần mềm. Đây là lúc chúng ta mang thành quả đi lấy tiền từ khách hàng, và Thầy Kenneth sẽ chỉ cho bạn cách "nói chuyện" bằng ngôn ngữ của khách hàng thay vì ngôn ngữ lập trình.

# Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. # Nắm được quy trình "dịch thuật" từ Tài liệu Yêu cầu (Requirements) sang Kịch bản Nghiệm thu (Acceptance Tests) có thể thực thi được.

2. # Hiểu được tiêu chí để quyết định "Khi nào thì ngừng Test và phát hành phần mềm?".

3. # Bỏ túi nguyên tắc sinh tồn: Nếu deadline dí sát lưng và không kịp test hết, bạn phải ưu tiên test cái gì trước?

# ---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Dịch thuật Requirement thành Acceptance Test**

# Lấy ví dụ về Hệ thống Đăng ký khóa học ASU, Thầy Kenneth đưa ra 3 quy tắc vàng khi viết kịch bản nghiệm thu:

* # **Quy tắc 1: Đổi chủ ngữ thành "Hệ thống"**

  * # *Sai:* "Sinh viên có thể yêu cầu xem danh mục khóa học." (Câu này đang mô tả hành vi của người dùng).

  * # *Đúng:* "Hệ thống phải có khả năng tạo ra danh mục khóa học." (Lúc này bạn mới có thể test được xem hệ thống có làm được hay không).

* # **Quy tắc 2: Gạch bỏ những thứ "Không thể Test" (Untestable)**

  * # Ví dụ có câu: *"Sinh viên tự quyết định sẽ học môn nào"*. Bạn không thể viết code hay test xem não bộ sinh viên quyết định ra sao. Đây là câu văn thừa thãi trong khâu kỹ thuật \-\> Xóa bỏ ngay lập tức.

* # **Quy tắc 3: Từ khóa ma thuật "DEMONSTRATE" (Trình diễn)**

  * # Khi lên kịch bản, hãy bắt đầu bằng từ này. Ví dụ: *"Trình diễn (Demonstrate) rằng sinh viên chỉ được chọn tối đa 4 môn học"*. Tại sao? Vì Acceptance Test là hoạt động bạn phải biểu diễn tận tay, tận mắt cho khách hàng xem.

#### **2\. Đánh giá: Khi nào thì Dừng Test?**

# Bạn không thể test mãi mãi. Sẽ luôn có lỗi tiềm ẩn. Vậy điểm dừng là đâu?

* # **Dựa vào Độ phủ (Coverage) và Mức độ hoàn thành:** Ví dụ, team thống nhất rằng nếu vượt qua được 99% các kịch bản test đã vạch ra, hệ thống được coi là an toàn để phát hành.

* # **Dựa vào Tỷ lệ Lỗi (Error rate):** Nếu biểu đồ theo dõi lỗi cho thấy số lỗi mới phát hiện ngày càng giảm xuống một ngưỡng an toàn thấp, bạn có thể tự tin tung ra sản phẩm.

* # *Cách xử lý khi Tỷ lệ lỗi vẫn quá cao nhưng sắp đến Deadline:* Bạn có thể cắt bớt phần mềm\! Chỉ giao cho khách hàng những Module nào đã chạy ổn định, các Module lỗi cứ giữ lại sửa tiếp và tung ra sau dưới dạng bản cập nhật (DLC).

#### **3\. Quy tắc Sinh tồn khi bị "Cháy Deadline"**

# Nếu chỉ còn 1 ngày trước khi giao hàng và bạn không thể chạy hết bộ Test, đây là thứ tự ưu tiên (phải thuộc lòng):

1. # **System quan trọng hơn Component:** Ưu tiên test toàn bộ hệ thống (Black-box) xem nó chạy trơn tru không, hơn là cắm đầu đi test (Unit test) từng dòng code lẻ tẻ.

2. # **Cũ quan trọng hơn Mới:** Nếu bản v1.0 chức năng Đăng nhập đang chạy tốt. Đến bản v2.0 bạn thêm chức năng Chat, thì ƯU TIÊN test lại chức năng Đăng nhập (Regression) chứ không phải test chức năng Chat. Khách hàng sẽ rất tức giận nếu một thứ đang dùng ngon tự nhiên bị hỏng.

3. # **Typical (Điển hình) quan trọng hơn Boundary (Biên):** Hãy đảm bảo 90% người dùng bình thường nhập dữ liệu đúng thì phần mềm chạy mượt mà (Typical cases). Tạm gác các trường hợp "Góc khuất" (Boundary cases) lại để xử lý sau.

# ---

### **🎊 TỔNG KẾT KHÓA HỌC (MOOC 3\)**

# Chúc mừng bạn\! Qua 7 Mô-đun, bạn đã đi một chặng đường rất dài từ việc:

1. # **Quản lý dự án:** Lên kế hoạch, chia việc, đếm dòng code (COCOMO), quản lý rủi ro.

2. # **Quy trình Phần mềm:** Nắm được Waterfall, Agile, Scrum, Unified Process.

3. # **Triển khai:** Lập trình phòng vệ (Defensive), Tái cấu trúc (Refactoring).

4. # **Kiểm thử:** White Box (nhìn thấu code), Black Box (đóng vai user), Regression (đề phòng thoái hóa).

# Bạn đã không còn là một "Thợ gõ phím" chỉ biết code cho xong tính năng nữa. Tư duy của bạn bây giờ là tư duy của một **Kỹ sư Phần mềm (Software Engineer)**: Nhìn hệ thống từ trên xuống dưới, phòng ngừa rủi ro, và kiểm soát chất lượng.

# Hãy nghỉ ngơi một chút, review lại các bảng Thuật ngữ mà chúng ta đã làm cùng nhau. Chúc bạn sẽ áp dụng thành công các kiến thức này vào đồ án Java Backend và hành trình thực tập sắp tới tại ngân hàng nhé\! 🚀 Bạn cần hỗ trợ gì thêm không?

# 