# **Defensive Programming**

Chào mừng bạn đến với chiến trường thực sự của Kỹ sư Phần mềm: **Viết code an toàn\!**

Trong bài giảng này, Thầy Kenneth không dạy bạn cú pháp lập trình (vì bạn đã biết code Java/C++ rồi), mà Thầy dạy bạn **tư duy sinh tồn** khi viết code.

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung cốt lõi của Lecture 3-1:

### **🎯 Mục Tiêu Bài Học**

Sau bài học này, bạn sẽ nắm được:

1. Bản chất của giai đoạn **Implementation** (Triển khai/Lập trình).  
2. Nắm vững triết lý **Defensive Programming** (Lập trình Phòng vệ) để bảo vệ hệ thống khỏi những dữ liệu "rác" từ người dùng.  
3. Biết cách sử dụng **Assertions** (Câu lệnh xác nhận) và kỹ năng **Suy luận ngược (Backward Reasoning)** để khoanh vùng và tiêu diệt Bug tận gốc.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Tổng quan về Implementation (Giai đoạn Lập trình)**

Viết code không phải là viết một lèo từ dòng 1 đến dòng 10.000. Chúng ta phải tổ chức code thành các khối:

* **Module:** Là một khối code vật lý, có thể thay thế được (Ví dụ: một file mã nguồn, một đoạn script, một file thực thi .exe).  
* **Subsystem (Hệ thống con):** Là một tập hợp gồm nhiều Module gom lại với nhau cho dễ quản lý.  
* Nhiệm vụ của Dev trong giai đoạn này là: Viết thuật toán cho từng class \-\> Gán class vào các Module \-\> Tích hợp (Integrate) các Module lại thành một hệ thống chạy được. (Tất nhiên phải dùng Git/Version Control để quản lý).

#### **2\. Lập trình Phòng vệ (Defensive Programming)**

* **Triết lý tối thượng:** *Tự bảo vệ mình mọi lúc, mọi nơi và KHÔNG TIN TƯỞNG BẤT KỲ AI (đặc biệt là người dùng).*  
* Người dùng luôn có xu hướng nhập sai (vô tình hoặc cố ý phá hoại). Nếu bạn lấy thẳng dữ liệu họ nhập (từ GUI, form web, command line) nhét thẳng vào thuật toán cốt lõi, phần mềm chắc chắn sẽ sập (crash).  
* **Giải pháp \- Barricade Classes (Lớp rào chắn):** Giống như bảo vệ ở cửa quán bar. Mọi dữ liệu (như Student ID, Email) trước khi được đưa vào "hệ thống nội bộ" (Internal classes) đều phải đi qua các lớp rào chắn này để "tắm rửa sạch sẽ" (kiểm tra định dạng, độ dài, tính hợp lệ). Nếu dữ liệu bẩn, rào chắn sẽ chặn lại ngay.

#### **3\. Assertions (Câu lệnh Xác nhận)**

Assertion là những dòng code bạn chèn vào giữa chương trình để **ép** một điều kiện nào đó phải đúng. Nếu sai, chương trình sẽ báo lỗi ngay lập tức tại dòng đó.

* **Pre-condition (Tiền điều kiện):** Assertion đặt *trước* khi chạy code. (VD: Kiểm tra mẫu số phải khác 0 trước khi làm phép chia).  
* **Post-condition (Hậu điều kiện):** Assertion đặt *sau* khi chạy code để đảm bảo kết quả tính toán ra đúng như kỳ vọng.  
* Những thứ nên dùng Assertion để check: Dữ liệu đầu vào, đầu ra, con trỏ có bị null không, mảng có bị tràn (out of bound) không, file đã đóng chưa...  
* ⛔ **Quy tắc vàng:** TUYỆT ĐỐI KHÔNG để các câu lệnh thực thi làm thay đổi dữ liệu (executable code) vào bên trong Assertion.

#### **4\. Kỹ năng Suy luận (Reasoning) để đặt Assertion**

Làm sao để biết đặt Assertion như thế nào cho chuẩn? Có 2 cách tư duy:

* **Forward Reasoning (Suy luận Tiến):**  
  * *Cách làm:* Đọc code từ trên xuống dưới. Biết biến đầu vào \-\> Tính nhẩm xem sau mỗi dòng lệnh biến đó thay đổi thành bao nhiêu.  
  * *Đặc điểm:* Rất tự nhiên, dễ hiểu. Nhưng nhược điểm là nó sinh ra rất nhiều thông tin thừa, lan man, làm mất thời gian khi project lớn.  
* **Backward Reasoning (Suy luận Lùi \- Đỉnh cao của Debug):**  
  * *Cách làm:* Bạn đi ngược từ dưới lên\! Bạn biết kết quả cuối cùng (Post-condition), sau đó suy ngược lên từng dòng code phía trên để tìm xem **Đầu vào (Pre-condition) bắt buộc phải là bao nhiêu** thì mới ra được kết quả đó.  
  * *Đặc điểm:* Cực kỳ hiệu quả để tìm Bug (lỗi). Khi khách hàng báo một lỗi, bạn nhìn vào lỗi đó (kết quả cuối), dùng suy luận lùi để biết chính xác người dùng đã nhập cái gì để gây ra lỗi này (tạo Test Case tái hiện lỗi).

---

### **📊 Thực hành: Phân loại Kỹ thuật Phòng vệ**

Để thực sự ngấm triết lý của Thầy Kenneth, bạn hãy thử áp dụng các khái niệm trên vào các tình huống thực tế của một Kỹ sư phần mềm:

Đang xác định các bước nội bộ  
Ở bài tiếp theo, chúng ta sẽ xem cách các Senior Dev "bắt giò" nhau qua hoạt động **Code Review**. Sẵn sàng chưa nào?

