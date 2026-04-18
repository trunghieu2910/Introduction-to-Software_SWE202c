QUIZZ AND KEYWORD 

Dưới đây là bảng tổng hợp các thuật ngữ cốt lõi của Mô-đun 5 và bảng bài tập đã được làm sạch (loại bỏ các đoạn text cảnh báo dư thừa từ hệ thống Coursera) kèm theo đáp án để bạn tiện ôn tập.

### **Bảng 1: Tổng hợp Thuật ngữ Mô-đun 5 (Software Quality Assurance)**

| Thuật ngữ (Tiếng Anh) | Tên Tiếng Việt | Giải thích / Ý nghĩa cốt lõi |
| :---- | :---- | :---- |
| **SQA (Software Quality Assurance)** | Đảm bảo chất lượng phần mềm | Quá trình áp dụng các quy trình, kỹ thuật và công cụ xuyên suốt vòng đời dự án để đảm bảo sản phẩm đạt tiêu chuẩn (không chỉ là việc Test ở cuối). |
| **Quality Planning** | Lập kế hoạch chất lượng | Việc lựa chọn, loại bỏ hoặc điều chỉnh các tiêu chuẩn của công ty sao cho phù hợp với một dự án cụ thể. |
| **Quality Control** | Kiểm soát chất lượng | Quá trình giám sát, đánh giá để đảm bảo mọi người thực sự tuân thủ các tiêu chuẩn đã đặt ra. |
| **Product Standards** | Tiêu chuẩn sản phẩm | Các quy định đánh giá đầu ra (Ví dụ: Code phải viết theo chuẩn CamelCase, hệ thống phải chạy dưới 2 giây). |
| **Process Standards** | Tiêu chuẩn quy trình | Các quy định về cách làm việc (Ví dụ: Phải review code trước khi merge, quy trình báo lỗi bug). |
| **Metrics** | Độ đo / Số liệu | Các con số định lượng dùng để đo lường chất lượng hoặc nỗ lực (Ví dụ: Số dòng code, số bug, thời gian hoàn thành). |
| **Cyclomatic Complexity** | Độ phức tạp Cyclomatic | Độ đo số lượng luồng điều khiển (các lệnh if, for, while) trong một hàm. Chỉ số này càng cao, code càng khó bảo trì. |
| **Fan-in** | Đầu vào | Số lượng các class/module khác đang gọi đến class hiện tại. Fan-in cao nghĩa là class này bị phụ thuộc nhiều (High coupling). |
| **Fan-out** | Đầu ra | Số lượng các class/module khác mà class hiện tại cần gọi đến để xử lý. Fan-out cao nghĩa là class này rất phức tạp. |
| **CMM / CMMI** | Mô hình Trưởng thành Năng lực | Khung chuẩn 5 cấp độ dùng để đánh giá và cải tiến quy trình phát triển phần mềm của một tổ chức/công ty. |
| **PCMM** | Mô hình Trưởng thành Nhân lực | Khung chuẩn 5 cấp độ dùng để đánh giá mức độ đầu tư, đào tạo và phát triển kỹ năng con người trong tổ chức. |
| **80/20 Rule (Pareto)** | Quy tắc 80/20 | Nguyên lý cho rằng 80% số lỗi (bugs) sinh ra từ 20% nguyên nhân cốt lõi. Cần tập trung diệt 20% nguyên nhân này. |
| **SCM (Software Configuration Management)** | Quản lý cấu hình phần mềm | Các hoạt động kiểm soát, theo dõi sự thay đổi của dự án (mã nguồn, tài liệu) để tránh xung đột (Ví dụ: sử dụng Git/GitHub). |

---

### **Bảng 2: Bài tập trắc nghiệm (Quiz)**

| STT | Câu hỏi | Đáp án đúng | Giải thích ngắn gọn |
| :---- | :---- | :---- | :---- |
| **1** | Which of the following IS NOT a software quality assurance activity? *Các lựa chọn:* \- standards enforcement \- program testing \- artifact reviews \- software configuration management \- people training | **people training** | Đào tạo con người (people training) là một phần của quản trị nhân sự (PCMM) nhằm hỗ trợ dự án, nhưng không được xếp trực tiếp vào nhóm các "hoạt động SQA" cốt lõi (vốn tập trung vào tiêu chuẩn, review, test và SCM cho sản phẩm/quy trình). |
| **2** | In terms of software quality assurance, the purpose of both the SEI Process Capability Maturity Model (SEI-CMM) and the People Capability Maturity Model (PCMM) is to: *Các lựa chọn:* \- educate and train managers. \- provide feedback on current practices. \- assess and improve current practices. \- develop best practices. \- improve the standards handbook. | **assess and improve current practices.** | Mục đích chính của cả hai thang đo CMMI và PCMM đều là để "đánh giá" (assess) xem tổ chức đang ở Level mấy, từ đó tìm cách "cải thiện" (improve) lên các Level cao hơn. |
| **3** | If an organization has a standards handbook for software development, then which of the following probably is NOT true? *Các lựa chọn:* \- A project can decide to not follow any standards. \- A project can decide to ignore a standard. \- A project can decide to use a standard as is. \- A project can decide to modify a standard. \- A project can decide to create a new standard. | **A project can decide to not follow any standards.** | Một dự án có thể thêm, bớt, sửa hoặc giữ nguyên các tiêu chuẩn tùy vào đặc thù dự án (tailor-make), nhưng tuyệt đối **không được phép** làm việc vô tổ chức mà không tuân theo bất kỳ tiêu chuẩn nào. |
| **4** | Test cases for state-based testing can be derived from the *Các lựa chọn:* \- use case model. \- state machine diagrams. \- basis paths. \- domain model. \- nonfunctional requirements. | **state machine diagrams.** | Kiểm thử dựa trên trạng thái (State-based testing) chắc chắn phải dựa vào Biểu đồ máy trạng thái (State machine diagrams) để xác định các luồng chuyển đổi trạng thái (transitions). |
| **5** | The degree to which the design specifications are followed during manufacturing is known as *Các lựa chọn:* \- quality of adherence. \- quality of conformance. \- quality of design. \- quality of performance. \- quality of testing. | **quality of conformance.** | "Quality of conformance" (Chất lượng của sự tuân thủ) là thuật ngữ kỹ thuật chỉ mức độ mà sản phẩm thực tế được làm ra bám sát (tuân thủ) đúng như bản thiết kế kỹ thuật ban đầu. |

