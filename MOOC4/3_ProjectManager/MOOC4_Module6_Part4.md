Dưới đây là bảng tổng hợp các thuật ngữ cốt lõi của Mô-đun 6 và bảng bài tập đã được làm sạch (loại bỏ hoàn toàn các đoạn text cảnh báo của hệ thống) kèm theo đáp án chi tiết.

*Lưu ý nhỏ: Trong 5 câu hỏi bạn gửi, có một vài câu (như câu 1, 2, 4\) thực chất là kiến thức ôn tập tổng hợp từ các mô-đun trước (Thiết kế hệ thống và Kiểm thử). Mình vẫn sẽ giải quyết triệt để giúp bạn nhé\!*

### **Bảng 1: Tổng hợp Thuật ngữ Mô-đun 6 (Managing Software Development)**

| Thuật ngữ (Tiếng Anh) | Tên Tiếng Việt | Giải thích / Ý nghĩa cốt lõi |
| :---- | :---- | :---- |
| **SDP (Software Development Plan)** | Bản Kế hoạch Phát triển Phần mềm | Tài liệu "sống" định nghĩa toàn bộ dự án: phạm vi, nguồn lực, ngân sách, lịch trình và các sản phẩm sẽ bàn giao. |
| **WBS (Work Breakdown Structure)** | Cấu trúc Phân rã Công việc | Kỹ thuật "chia để trị" \- bẻ nhỏ dự án thành các giai đoạn, module, và các task nhỏ hơn để dễ phân công và kiểm soát. |
| **Gantt Chart** | Biểu đồ Gantt | Biểu đồ thanh ngang hiển thị lịch trình dự án trên trục thời gian (Task nào làm từ ngày nào đến ngày nào). |
| **PERT Chart** | Biểu đồ PERT | Biểu đồ dạng mạng lưới (network) thể hiện sự *phụ thuộc* giữa các task (task nào phải xong trước mới được làm task sau). |
| **Critical Path** | Đường găng | Chuỗi các task dài nhất từ đầu đến cuối dự án trên biểu đồ PERT. Bất kỳ task nào trên đường này bị trễ, toàn bộ dự án sẽ trễ. |
| **Deliverables** | Sản phẩm bàn giao | Bất cứ thứ gì phải giao nộp trong dự án (source code, tài liệu spec, file thiết kế, thư viện, dịch vụ cài đặt...). |
| **KLOC (Kilo Lines of Code)** | Hàng ngàn dòng code | Độ đo kích thước dự án dựa trên số lượng dòng code. (Thường thiếu chính xác do phụ thuộc vào phong cách code của mỗi người). |
| **Function Points (FP)** | Điểm chức năng | Độ đo kích thước dự án khách quan hơn, dựa trên số lượng tính năng, inputs, outputs và giao diện kết nối (interfaces). |
| **Delphi Technique** | Kỹ thuật Delphi | Phương pháp ước lượng bằng cách thu thập dự đoán từ nhiều chuyên gia độc lập, sau đó lấy trung bình để ra con số chính xác nhất. |
| **PERT Estimation (3-point)** | Ước lượng 3 điểm | Kỹ thuật tính thời gian dựa trên 3 kịch bản: Lạc quan (O), Khả dĩ nhất (M), và Bi quan (P). Công thức: (O \+ 4M \+ P) / 6. |
| **Brooks's Law** | Định luật Brooks | Nghịch lý quản lý: *"Thêm người vào một dự án đang trễ hạn sẽ chỉ làm nó trễ hạn thêm"* (do tốn thời gian đào tạo và giao tiếp). |

---

### **Bảng 2: Bài tập trắc nghiệm (Quiz)**

| Câu hỏi | Các lựa chọn |
| :---- | :---- |
| 1\. In system analysis and design, an entity class represents | \- information about a user of the system.- information that is persistent.- system dependencies on actors.- information that is transient.- coordination, sequencing, transactions and control of other objects. |
| 2\. System analysis and design distributes the functionality of a use case into boundary, entity and control classes because | \- these are the only kinds of classes available to us.- these classes are easier to test.- we want to isolate specific types of changes to specific types of classes.- state machine diagrams use these classes.- object interaction is more easily described using these classes. |
| 3\. Which of the following CANNOT be shown on a Gantt chart? | \- the task dependencies- the time estimates for each task- the resource assignment for each task- the tasks that lie on the critical path- the progress of each task |
|  4.One of the required inputs for a program that does room scheduling for a public venue is the day of the week, which is input as Sunday, Monday, etc. When testing this program for the input day of the week, what are the minimum number of test values that you would use? | \- 5 \- 7 \- 8 \- 9 \- 10 |
| 5\. What would be most effective in reducing the complexity of designing a software system? | \- having clear design goals- having refined work breakdown structure- having right level of communication- having sufficient budget- having timely administrative support |

