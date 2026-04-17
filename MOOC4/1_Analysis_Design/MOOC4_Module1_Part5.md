KEY AND QUIZ  
Dưới đây là hai bảng tổng hợp toàn bộ các thuật ngữ cốt lõi của **MOOC 4 \- Mô-đun 1** và danh sách 5 câu hỏi Quiz đã được dọn dẹp sạch sẽ các đoạn cảnh báo hệ thống của Coursera.

*(Lưu ý nhỏ: Đọc nội dung 5 câu hỏi này thì có vẻ đây là bài Quiz tổng kết của chuyên đề Kiểm thử \- MOOC 3 trước đó, chứ không phải câu hỏi của phần Thiết kế Hệ thống. Mình vẫn tổng hợp đầy đủ và sạch sẽ cho bạn tiện ôn tập nhé).*

### **Bảng 1: Từ điển Thuật ngữ Kỹ thuật (MOOC 4 \- Mô-đun 1: Phân tích & Thiết kế)**

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **System Analysis and Design** *(Phân tích và Thiết kế hệ thống)* | Quá trình chuyển đổi Tài liệu yêu cầu (ngôn ngữ người dùng) thành Bản vẽ/Mô hình (ngôn ngữ lập trình viên) trước khi bắt tay vào viết code. |
| **Subsystem** *(Hệ thống con)* | Một phần nhỏ được cắt ra từ hệ thống lớn (chia để trị). Nó che giấu cách hoạt động bên trong (Information hiding) và cung cấp dịch vụ ra bên ngoài. |
| **Architectural Pattern** *(Mẫu Kiến trúc)* | Bản thiết kế tiêu chuẩn chỉ ra cách tổ chức và kết nối các hệ thống con lại với nhau (VD: MVC, Client-Server). |
| **Analysis Class** *(Lớp Phân tích)* | Bản nháp mang tính khái niệm của một Class, được dùng trong lúc phân tích Use Case, chưa gắn với ngôn ngữ lập trình cụ thể nào. |
| **Boundary Class** *(Lớp Biên)* | Lớp đại diện cho Giao diện (UI) hoặc cổng kết nối. Nơi hệ thống giao tiếp với Actor (người dùng hoặc hệ thống bên ngoài). |
| **Entity Class** *(Lớp Thực thể)* | Lớp chứa dữ liệu có tính chất sống thọ (persistent data), thường được map với các bảng trong Database. |
| **Control Class** *(Lớp Điều khiển)* | Lớp chứa Business Logic, đóng vai trò là "bộ não" điều phối luồng chạy và làm trung gian giao tiếp giữa Boundary và Entity. |
| **Design Class** *(Lớp Thiết kế)* | Bản nâng cấp của Lớp phân tích, đã được gắn chặt với ngôn ngữ lập trình cụ thể (Java), quy định rõ kiểu dữ liệu, hàm và tầm vực (public/private). |
| **Active Class** *(Lớp Chủ động)* | Một class đặc biệt sở hữu luồng thực thi (thread of control) của riêng nó, thường dùng để chạy ngầm hoặc lắng nghe sự kiện liên tục. |
| **Cohesion** *(Độ gắn kết)* | Thước đo xem một class tập trung vào **mấy nhiệm vụ**. *High Cohesion (Gắn kết cao)* nghĩa là class chỉ làm đúng 1 việc \-\> Rất tốt. |
| **Coupling** *(Độ liên kết)* | Thước đo xem một class **phụ thuộc vào bao nhiêu class khác**. *Loose Coupling (Liên kết lỏng lẻo)* nghĩa là ít phụ thuộc \-\> Rất tốt. |
| **God Class** *(Lớp Chúa tể)* | Một "anti-pattern" (mẫu xấu) chỉ một class bị dồn quá nhiều chức năng (Low Cohesion), ôm đồm mọi việc, cực kỳ khó bảo trì và dễ sinh lỗi. |

---

### **Bảng 2: Câu hỏi trắc nghiệm Ôn tập (Kiểm thử Phần mềm)**

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **The purpose of an acceptance test plan is to**  *(Mục đích của kế hoạch kiểm thử nghiệm thu là để...)* | • verify the acceptability of the code structure. • specify the criteria for determining whether the system is finished. • list all the requirements for the system. • define the scope of the system development. • define the goals of the system. |
| **2** | **The cyclomatic complexity of a program can tell us something about which of the following external attributes (design goals) of software quality?**  *(Độ phức tạp Cyclomatic của một chương trình có thể cho chúng ta biết điều gì về thuộc tính bên ngoài (mục tiêu thiết kế) nào sau đây của chất lượng phần mềm?)* | • usability \- how easy it is to use • learnability \- how easy it is to learn how to us • safety \- how likely it is to be error free • integrity \- how well it prevents unauthorized access • installability \- how easy it is to install |
| **3** | **Integration testing focuses on**  *(Kiểm thử tích hợp tập trung vào...)* | • the flow of control in a component. • the logical conditions in a component. • validating user requirements. • the interaction among the components. • integrating a database with the software system. |
| **4** | **Which statement is true about system testing and acceptance testing?**  *(Nhận định nào sau đây là đúng về kiểm thử hệ thống và kiểm thử nghiệm thu?)* | • System testing is done after acceptance testing. • System testing is done by the developers; acceptance testing is done by the client. • System testing is done at the client's site; acceptance testing is done at the developer's site. • System testing is done by the client; acceptance testing is done by the developers. • None of the above is true. |
| **5** | **Behavioral testing is**  *(Kiểm thử hành vi là tên gọi khác của...)* | • black box testing • white box testing • red box testing • green box testing • blue box testing |

