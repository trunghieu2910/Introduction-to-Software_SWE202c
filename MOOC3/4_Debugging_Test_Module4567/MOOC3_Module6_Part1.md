# **White Box Testing**

Chào mừng bạn đến với phần "vét lưới" của Kiểm thử Hộp trắng\!

Trước khi chúng ta đóng mã nguồn lại để chuyển sang góc nhìn của người dùng (Hộp đen), Thầy Kenneth đã bổ sung thêm 3 "chiêu thức" Hộp trắng cực kỳ sắc bén. Các kỹ thuật này đặc biệt hữu dụng khi bạn viết các hàm xử lý logic Backend trong Java, nơi chứa vô vàn các biểu thức điều kiện và vòng lặp duyệt dữ liệu phức tạp.

Dưới đây là phần bóc tách chi tiết 3 kỹ thuật này:

### **🎯 Mục Tiêu Bài Học**

Bổ sung thêm 3 công cụ vào kho vũ khí White Box Testing để xử lý triệt để 3 nơi dễ sinh ra lỗi (bug) nhất trong mã nguồn: Câu lệnh điều kiện (Condition), Vòng lặp (Loop) và Biến dữ liệu (Data Flow).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Condition Testing (Kiểm thử Điều kiện)**

Lập trình viên rất hay viết sai các phép toán logic (sai dấu \<, \>, \=, nhầm AND thành OR, hoặc thiếu dấu ngoặc đơn). Kỹ thuật này ép bạn phải test kỹ từng ngóc ngách của các lệnh if/else.

* **Xử lý Điều kiện kép (Compound Condition):** Nếu bạn có lệnh if (A && B), đừng chỉ coi nó là 1 điểm rẽ nhánh. Hãy tách nó ra thành 2 điều kiện đơn giản (6a cho A, 6b cho B) trên Đồ thị luồng. Bạn phải test các trường hợp: Cả 2 cùng Đúng, A Đúng B Sai, A Sai (lúc này B không cần chạy).  
* **Domain Testing (Kiểm thử Miền giá trị):** Nếu điều kiện là một biểu thức quan hệ, ví dụ x \> 4. Bạn KHÔNG ĐƯỢC test bừa. Bạn bắt buộc phải chọn 3 giá trị đại diện cho 3 trạng thái:  
  * Nhỏ hơn (Ví dụ: x \= 2)  
  * Bằng (Ví dụ: x \= 4)  
  * Lớn hơn (Ví dụ: x \= 6)

#### **2\. Loop Testing (Kiểm thử Vòng lặp)**

Vòng lặp (for, while) là mỏ vàng của lỗi (đặc biệt là lỗi lặp vô hạn hoặc dừng sớm 1 nhịp). Giả sử vòng lặp của bạn thiết kế để chạy tối đa n lần, bạn phải thiết kế Test Case quét qua các mốc sau:

* Chạy **0 lần** (Bỏ qua vòng lặp ngay lập tức \- ví dụ mảng rỗng).  
* Chạy **1 lần**, **2 lần**.  
* Chạy số lần trung bình **m lần** (với $m \< n$).  
* Chạy cận trên: **n-1 lần**, **n lần** (đúng mốc tối đa), và **n+1 lần** (để xem nó có báo lỗi/thoát đúng cách khi vượt giới hạn không).

**Xử lý các loại vòng lặp phức tạp:**

* **Vòng lặp lồng nhau (Nested loops):** Test từ trong ra ngoài. Ép vòng lặp bên ngoài chạy ít nhất (0 hoặc 1 lần) để tập trung test kỹ vòng lặp trong cùng. Xong xuôi thì mới lùi ra test vòng bên ngoài.  
* **Vòng lặp nối tiếp (Concatenated loops):** Nếu chúng độc lập thì test riêng từng cái. Nếu chúng phụ thuộc nhau thì test như vòng lặp lồng nhau.  
* **Vòng lặp lộn xộn/Vô cấu trúc (Unstructured loops):** Quy tắc vàng của Thầy Kenneth: ĐỪNG TEST\! Hãy đi **Refactor** (Tái cấu trúc) lại đoạn code đó cho đàng hoàng rồi mới test.

#### **3\. Data Flow Testing (Kiểm thử Luồng dữ liệu)**

Kỹ thuật này không test theo đường đi của lệnh, mà test theo **Vòng đời của Biến**.

* **Chuỗi Định nghĩa \- Sử dụng (Definition-Use chain):** Bạn khoanh vùng thời điểm một biến được sinh ra/gán giá trị (Define) và theo dõi nó cho đến thời điểm nó được mang ra tính toán/tiêu thụ (Use).  
* *Mục tiêu:* Đảm bảo rằng KHÔNG có đường đi nào mà biến bị mang ra sử dụng khi chưa được khởi tạo, hoặc biến được gán giá trị xong rồi... vứt đó không bao giờ xài tới. Kỹ thuật này thường được kết hợp chung với Basis Path Testing.

---

Như vậy là kho tàng White Box đã khép lại. Bây giờ, hãy tưởng tượng bạn không còn nhìn thấy bất kỳ dòng code nào nữa. Bạn đã sẵn sàng để gửi transcript của **Lecture 6-2: Black Box Testing** lên đây để chúng ta chuyển đổi góc nhìn chưa?

