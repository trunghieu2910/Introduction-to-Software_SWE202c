KEYWORD AND QUIZ  
Dưới đây là hai bảng tổng hợp toàn bộ các thuật ngữ cốt lõi của **MOOC 4 \- Mô-đun 2 (State Machine Diagram)** và danh sách 5 câu hỏi Quiz đã được dọn dẹp sạch sẽ các đoạn cảnh báo hệ thống của Coursera.

### **Bảng 1: Từ điển Thuật ngữ Kỹ thuật (Mô-đun 2: Sơ đồ Máy trạng thái)**

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **State Machine Diagram** *(Sơ đồ Máy trạng thái)* | Sơ đồ mô tả hành vi động và vòng đời của **một đối tượng duy nhất (a single object)** từ lúc sinh ra đến lúc bị hủy. |
| **State** *(Trạng thái)* | Một khoảng thời gian (có duration) trong vòng đời của đối tượng khi nó thỏa mãn một điều kiện nhất định. |
| **Transition** *(Sự chuyển đổi)* | Sự dịch chuyển từ trạng thái này sang trạng thái khác. Quá trình này diễn ra ngay lập tức (zero time) và không thể bị ngắt quãng. |
| **Initial State** *(Trạng thái bắt đầu)* | Dấu chấm đen đặc. Đại diện cho thời điểm đối tượng được tạo ra bằng hàm khởi tạo (Constructor). |
| **Final State** *(Trạng thái kết thúc)* | Dấu chấm đen có vòng tròn bên ngoài. Đại diện cho lúc đối tượng bị xóa khỏi bộ nhớ (Destroyed). |
| **Event** *(Sự kiện)* | Tác nhân gây ra sự chuyển đổi. Có 3 loại chính: **Call Event** (gọi hàm), **Change Event** (thay đổi giá trị điều kiện), **Time Event** (hết thời gian). |
| **Guard Condition** *(Điều kiện chắn)* | Biểu thức logic (nằm trong dấu ngoặc vuông \[ \]) phải trả về True thì mũi tên chuyển đổi mới được phép chạy. |
| **Effect / Action** *(Hệ quả / Hành động)* | Hàm hoặc hành động tự động được thực thi ngay trong quá trình chuyển đổi (nằm sau dấu /). |
| **Entry / Exit / Do Activity** | Các hoạt động diễn ra khi đối tượng nằm trong một trạng thái: lúc mới bước vào (Entry), lúc rời đi (Exit), hoặc làm liên tục trong lúc ở đó (Do). |
| **Composite State** *(Trạng thái phức hợp)* | Một trạng thái lớn chứa một Sơ đồ Máy trạng thái nhỏ ở bên trong nó (Nested state). |
| **Concurrent Composite State** *(Trạng thái phức hợp đồng thời)* | Trạng thái lớn được chia làm nhiều vùng (regions) độc lập, đối tượng tồn tại ở nhiều trạng thái con cùng một lúc. |
| **Synchronization Bar** *(Thanh đồng bộ hóa)* | Ký hiệu thanh ngang đậm dùng để tách luồng (Fork \- bắt đầu cùng lúc) hoặc gộp luồng (Join \- chờ nhau kết thúc cùng lúc). |

---

### **Bảng 2: Câu hỏi trắc nghiệm Ôn tập (Mô-đun 2\)**

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **A state machine diagram describes the behaviour of**  *(Sơ đồ máy trạng thái mô tả hành vi của...)* | • an object. • a use case. • an operation. • an actor. • a class. |
| **2** | **A state machine diagram responds to every event that**  *(Sơ đồ máy trạng thái phản hồi lại mọi sự kiện mà...)* | • occurs • occurs provided it is not processing an activity. • changes a value of the object's attributes. • triggers a transition. • sends a message. |
| **3** | **An event on a state machine diagram can represent**  *(Một sự kiện trên sơ đồ máy trạng thái có thể đại diện cho...)* | • the completion of an activity. • a return from a message send. • exiting a state. • the passage of a designated period of time. • a guard becoming true. |
| **4** | **Which statement is NOT true about a state in a state machine diagram?**  *(Nhận định nào KHÔNG đúng về một trạng thái trong sơ đồ máy trạng thái?)* | • It has duration. • It can be anonymous (unnamed). • It can only be entered by the triggering of an event. • It may be characterized by the value of one or more attributes. • It may be characterized by the existence of a link to another object. |
| **5** | **One purpose of system analysis and design is to**  *(Một trong những mục đích của phân tích và thiết kế hệ thống là để...)* | • determine the cost of developing the system. • determine the time required to implement the system. • capture the system's nonfunctional requirements. • adapt the requirements to the implementation environment. • obtain the client's approval for developing the system. |

