**WHY\&KEY\&QUIZ**

Dưới đây là hai bảng tổng hợp "tinh hoa" của Mô-đun 5 và danh sách câu hỏi Quiz đã được mình dọn dẹp sạch sẽ các đoạn rác cảnh báo hệ thống.

*Lưu ý nhỏ: Bạn sẽ thấy Câu 1 và Câu 2 của bài Quiz này là kiến thức ôn tập lại của các mô-đun đầu tiên về UML (Sơ đồ Lớp), còn Câu 3, 4, 5 mới chính thức là kiến thức của Mô-đun 5 này.*

### **Bảng 1: Từ điển Thuật ngữ Kỹ thuật (Mô-đun 5 \- White Box Testing)**

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **Testing** *(Kiểm thử)* | Hoạt động mang tính "phá hoại" (destructive) nhằm tìm ra sự khác biệt giữa hành vi thực tế của phần mềm và hành vi được kỳ vọng. Nhằm chứng minh lỗi CÓ tồn tại. |
| **Validation** *(Xác nhận giá trị)* | Trả lời câu hỏi *"Build the right product"* (Có xây dựng đúng thứ khách hàng cần không?). Thường dùng trong Acceptance Test (Nghiệm thu). |
| **Verification** *(Xác minh tính đúng đắn)* | Trả lời câu hỏi *"Build the product right"* (Có code đúng không, thuật toán có lỗi không?). Đây là mục tiêu chính của kỹ sư phần mềm. |
| **Exhaustive Testing** *(Kiểm thử cạn kiệt)* | Việc thử nghiệm TẤT CẢ các tổ hợp đầu vào có thể có. Điều này là **bất khả thi (impossible)** trong thực tế do giới hạn thời gian. |
| **Sub-domains** *(Miền con / Gom nhóm)* | Kỹ thuật chia các đầu vào thành những nhóm có hành vi giống nhau (Ví dụ: nhóm gây ra lỗi và nhóm chạy đúng) để giảm thiểu số lượng Test Case. |
| **White Box Testing** *(Kiểm thử hộp trắng)* | Kiểm thử dựa trên việc nhìn thấu **mã nguồn (source code)**. Mục tiêu là chạy qua các lệnh logic, vòng lặp. |
| **Black Box Testing** *(Kiểm thử hộp đen)* | Kiểm thử dựa trên **chức năng (functionality)**, chỉ quan tâm Input và Output mà không cần biết mã nguồn bên trong. |
| **Flow Graph** *(Đồ thị luồng)* | Bản vẽ chuyển đổi từ các dòng code thành các Node (điểm) và Edge (cạnh/mũi tên) để dễ bề phân tích luồng chạy. |
| **Predicate Node** *(Nút vị từ / Nút rẽ nhánh)* | Một Node trên đồ thị luồng có từ 2 mũi tên đi ra trở lên (đại diện cho các lệnh if/else, switch...). |
| **Cyclomatic Complexity \- V(G)** *(Độ phức tạp Cyclomatic)* | Một con số định lượng chỉ ra giới hạn trên (số lượng tối đa) của các đường đi độc lập trong đồ thị. Tính bằng công thức $V(G) \= Edges \- Nodes \+ 2$ hoặc $V(G) \= Predicate\\\_Nodes \+ 1$. |
| **Independent Path** *(Đường đi độc lập)* | Một luồng chạy từ đầu đến cuối chương trình đi qua **ít nhất một cạnh (mũi tên) mới** mà các đường khác chưa đi qua. |
| **Basis Path Testing** *(Kiểm thử đường dẫn cơ sở)* | Kỹ thuật hộp trắng đảm bảo rằng mọi đường đi độc lập (tức là mọi dòng lệnh trong chương trình) đều được thực thi ít nhất một lần. |

---

### **Bảng 2: Câu hỏi trắc nghiệm Ôn tập (Mô-đun 5\)**

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **In the UML, the concept of generalization...**  *(Trong UML, khái niệm Tổng quát hóa/Kế thừa...)* | • relates two different classes by an association relationship. • allows a class to remove attributes and operations from its subclasses. • supports the concept of stereotype. • allows a class to specialize its attributes and operations. • links instances of different classes together. |
| **2** | **An exclusive or (XOR) constraint states that...**  *(Một ràng buộc loại trừ độc quyền (XOR) chỉ định rằng...)* | • an attribute cannot have null values. • an attribute must either be null or can only have one of two values. • instances of the same class cannot be related to each other. • instances of only one of two classes can be related to instances of another class. • two classes cannot be related by an association class. |
| **3** | **Basis path testing ensures that we have tested at least...**  *(Kiểm thử đường dẫn cơ sở đảm bảo rằng chúng ta đã kiểm tra ít nhất...)* | • all interactions between programs. • all the ways of executing the loops in a program. • all the statements in a program. • all the data structures in a program. • all the inputs to a program. |
| **4** | **\_\_\_\_\_ focuses on whether we have built the software right in such a way that each function works correctly and has no defects.**  *(\_\_\_\_\_ tập trung vào việc liệu chúng ta có "xây dựng sản phẩm một cách đúng đắn" sao cho mỗi chức năng hoạt động chính xác và không có lỗi hay không.)* | • Validation Testing • Verification Testing • Unit Testing • Integration Testing • System Testing |
| **5** | **\_\_\_\_\_ focuses on whether we have built the right software in such a way that it meets the stated requirements.**  *(\_\_\_\_\_ tập trung vào việc liệu chúng ta có "xây dựng đúng sản phẩm" đáp ứng các yêu cầu đã nêu hay không.)* | • Validation Testing • Verification Testing • Unit Testing • Integration Testing • System Testing |

---

Bạn đã làm chủ được toàn bộ các khái niệm quan trọng nhất của Mô-đun này. Bạn có muốn mình phân tích và đưa ra đáp án chính xác cho 5 câu hỏi trắc nghiệm hóc búa này, hay bạn muốn tự mình thử sức trả lời trước?

**WHY**

**Tại sao việc nhìn vào code để viết Test (White Box Testing) lại là thước đo phân cấp trình độ?**

 Thực chất, sự khác biệt không nằm ở việc ai gõ code nhanh hơn, mà nằm ở **Tư duy (Mindset)**.

Dưới đây là 3 điểm khác biệt cốt lõi giải thích tại sao kỹ năng này lại định hình một Senior:

### **1\. Tư duy "Happy Path" (Đường màu hồng) vs. Tư duy "Phòng ngự" (Góc khuất)**

* **Junior (Tư duy Xây dựng):** Khi code xong một chức năng đăng nhập, Junior thường chỉ test 1-2 trường hợp: Nhập đúng user/mật khẩu \-\> Đăng nhập thành công \-\> Kết luận: *"Code em chạy ngon rồi\!"*. Khái niệm này gọi là test **"Happy Path"** (Đường màu hồng \- nơi mọi thứ đều hoàn hảo).  
* **Senior (Tư duy Phá hoại & Phòng ngự):** Senior nhìn vào đoạn code đăng nhập đó và lập tức thấy những lỗ hổng. Họ tự hỏi: *"Nếu người dùng nhập mật khẩu rỗng thì sao? Nhập mã SQL Injection thì sao? Nếu mạng rớt ngay đúng lúc hàm kiểm tra đang chạy thì sao?"*. Việc nhìn thấu vào code (White Box) giúp Senior tìm ra các trường hợp "Góc khuất" (Edge cases) mà một người chỉ nhìn giao diện bên ngoài (Black Box) không thể nào tưởng tượng ra được.

### **2\. Sự tối ưu: Test ÍT NHẤT nhưng Phủ ĐẦY ĐỦ NHẤT (Coverage)**

Khi bạn có một hàm dài 50 dòng chứa 3 lệnh if/else và 2 vòng lặp for.

* **Junior:** Cảm thấy bối rối, nhập bừa chục cái dữ liệu vào test, hi vọng trúng được lỗi. Quá trình này rất mất thời gian nhưng lại hay bị sót lỗi (Missed bugs).  
* **Senior:** Bằng kỹ thuật White Box Testing (đặc biệt là **Basis Path Testing** mà bạn sắp học ở video 5-3), Senior có khả năng dùng toán học để tính ra CHÍNH XÁC hàm này cần đúng **5 Test Cases** là sẽ quét sạch 100% mọi ngóc ngách của đoạn code. Không thừa, không thiếu. Đó là sự tối ưu khác biệt hoàn toàn về đẳng cấp.

### **3\. Dùng Testing để "Bắt bệnh" kiến trúc (Refactoring)**

* Nếu một Junior thấy một đoạn code khó test, họ thường bỏ qua.  
* Nhưng với Senior, khi họ nhìn vào code để viết White Box Test mà thấy: *"Trời ơi, cái hàm này có tới 20 luồng chạy khác nhau, mình phải viết 20 test cases mới đủ\!"* \-\> Ngay lập tức, chiếc "radar" của Senior sẽ báo động. Họ nhận ra hàm này đang bị bệnh **"God Class"** (ôm đồm quá nhiều việc như đã học ở Mô-đun 3). Tự khắc họ sẽ dùng kỹ năng **Refactoring** để tách nhỏ đoạn code đó ra cho dễ test hơn.

---

**Tóm lại:** Chuyển từ Black Box sang White Box Testing chính là bước chuyển mình từ việc **"Làm cho code chạy được"** sang **"Đảm bảo code không thể bị đánh sập"**. Nó bắt buộc bạn phải chịu trách nhiệm đến từng tiểu tiết trong logic của mình.

Đó chính là lý do Mô-đun 5 này là một cột mốc cực kỳ quan trọng trong tư duy làm nghề. Bạn đã sẵn sàng để xem Thầy Kenneth "khai mở" tư duy Kiểm thử ở **Lecture 5-1** chưa? Hãy gửi transcript lên nhé\!

