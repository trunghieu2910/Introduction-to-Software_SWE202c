KEY AND QUIZZ 

Dưới đây là hai bảng tổng hợp toàn bộ các thuật ngữ cốt lõi của **Mô-đun 7** và danh sách câu hỏi Quiz đã được dọn dẹp sạch sẽ các đoạn cảnh báo hệ thống của Coursera.

*(Lưu ý: Bạn sẽ thấy bộ câu hỏi Quiz này thực chất là bài ôn tập tổng hợp lại kiến thức của cả Mô-đun 6 và Mô-đun 7).*

### **Bảng 1: Từ điển Thuật ngữ Kỹ thuật (Mô-đun 7 \- Các cấp độ Kiểm thử)**

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **Unit Testing** *(Kiểm thử Đơn vị)* | Mức kiểm thử thấp nhất (Inside-out). Developer tự test từng hàm, từng class (component) độc lập. Chủ yếu dùng White-box. |
| **Integration Testing** *(Kiểm thử Tích hợp)* | Ghép các class/module lại với nhau để kiểm tra lỗi giao tiếp (interface). Dùng kết hợp cả White-box và Black-box. |
| **System Testing** *(Kiểm thử Hệ thống)* | Test toàn bộ hệ thống đã lắp ráp hoàn chỉnh. Do đội Tester thực hiện, hoàn toàn sử dụng Black-box testing. |
| **Acceptance Testing** *(Kiểm thử Nghiệm thu)* | Mức kiểm thử cuối cùng. Khách hàng/Người dùng tự tay test (Black-box) để xác nhận (Validate) phần mềm đáp ứng đúng hợp đồng. |
| **Driver** *(Trình điều khiển / Giả lập cấp trên)* | Một chương trình/hàm giả mạo đóng vai trò làm giao diện (cấp trên) để gọi và truyền Input xuống cho module đang được test. |
| **Stub** *(Mã giả / Giả lập cấp dưới)* | Một class/hàm giả mạo đóng vai trò làm cấp dưới. Thay vì xử lý logic thật, nó luôn nhả ra một kết quả tĩnh để module cấp trên có dữ liệu chạy tiếp. |
| **Top-down Integration** *(Tích hợp Từ trên xuống)* | Ghép code và test từ tầng Giao diện (UI) xuống dần tầng Database. Yêu cầu viết rất nhiều **Stubs**. |
| **Bottom-up Integration** *(Tích hợp Từ dưới lên)* | Ghép code và test từ tầng lõi (Database/Controller) lên dần tầng Giao diện. Yêu cầu viết rất nhiều **Drivers**. |
| **Sandwich Integration** *(Tích hợp Kẹp chả)* | Cách tiếp cận test song song cả từ trên xuống và từ dưới lên cùng một lúc để tiết kiệm thời gian. |
| **Pilot Testing** *(Kiểm thử Thử nghiệm)* | Mời một nhóm người dùng cuối (end-users) vào dùng thử phần mềm trước khi phát hành chính thức. |
| **Alpha Testing** *(Kiểm thử Alpha)* | Người dùng thử nghiệm phần mềm **tại công ty/môi trường của Developer** (có sự kiểm soát và giám sát). |
| **Beta Testing** *(Kiểm thử Beta)* | Người dùng tải phần mềm về và thử nghiệm **tại máy cá nhân của họ** (không có sự giám sát của Developer), lỗi sẽ được report về sau. |

---

### **Bảng 2: Câu hỏi trắc nghiệm Ôn tập (Mô-đun 7\)**

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **Black box testing techniques are mostly used in what type of testing?**  *(Các kỹ thuật kiểm thử hộp đen chủ yếu được sử dụng trong loại kiểm thử nào?)* | • unit • condition • loop • integration • data flow |
| **2** | **Black box testing uses test values at the boundaries of a subdomain because**  *(Kiểm thử hộp đen sử dụng các giá trị kiểm thử ở ranh giới của một miền con (phân tích giá trị biên) bởi vì...)* | • these values are easier for us to figure out. • this will make integrating components easier. • errors are more likely to occur here. • black box testing only works for such values. • these values can be given to us by the users. |
| **3** | **The purpose of data flow testing is to ensure the correctness of values**  *(Mục đích của kiểm thử luồng dữ liệu (Data flow testing) là để đảm bảo tính chính xác của các giá trị...)* | • stored by a program into a database. • that move into and out of a database. • that pass through a user interface. • of program variables. • output by a program. |
| **4** | **When testing a nested loop, we initially test the inner loop while holding the outer loop at**  *(Khi kiểm thử một vòng lặp lồng nhau, ban đầu chúng ta kiểm tra vòng lặp bên trong trong khi giữ nguyên vòng lặp bên ngoài ở...)* | • its minimum value. • its middle value. • its maximum value. • both its minimum and maximum value. • any value. |
| **5** | **When testing a simple loop, what is the minimum number of test cases required?**  *(Khi kiểm thử một vòng lặp đơn giản, số lượng tối thiểu các kịch bản kiểm thử (test cases) cần thiết là bao nhiêu?)*  *(Gợi ý: Nhớ lại quy tắc 0, 1, 2, m, n-1, n, n+1 của Thầy Kenneth).* | • 1 • 3 • 4 • 5 • 7 |

---

Chúc mừng bạn đã hoàn tất toàn bộ lý thuyết và thuật ngữ của **MOOC 3: Software Engineering: Implementation and Testing**. Hành trình từ Quản lý dự án, Triển khai mã nguồn an toàn đến các chiến lược Kiểm thử của bạn đã hoàn thành xuất sắc\!

