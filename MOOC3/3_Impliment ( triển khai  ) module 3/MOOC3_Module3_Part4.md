KEY WORD AND QUIZ 

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **Implementation** *(Triển khai/Lập trình)* | Giai đoạn biến các bản thiết kế (Design) thành mã nguồn có thể thực thi được (Executable code). |
| **Defensive Programming** *(Lập trình Phòng vệ)* | Tư duy viết code không tin tưởng bất kỳ ai. Luôn kiểm tra và chặn các dữ liệu đầu vào không hợp lệ để ngăn chương trình bị sập (crash). |
| **Barricade Classes** *(Lớp rào chắn)* | Các lớp (classes) được dùng để "tắm rửa" và lọc dữ liệu bẩn từ người dùng/bên ngoài trước khi đưa vào xử lý ở các lớp nội bộ. |
| **Assertion** *(Câu lệnh xác nhận)* | Một biểu thức logic chèn vào code để ép một điều kiện phải đúng. Dùng để kiểm tra lỗi ngay trong lúc chương trình đang chạy. |
| **Forward Reasoning** *(Suy luận Tiến)* | Đọc code từ trên xuống dưới để đoán xem trạng thái của biến/chương trình sẽ thay đổi như thế nào ở cuối đoạn code. |
| **Backward Reasoning** *(Suy luận Lùi)* | Đi ngược từ kết quả mong muốn (hoặc từ lỗi) lên trên để tìm xem đầu vào bắt buộc phải là bao nhiêu. Cực kỳ hiệu quả để Debug. |
| **Code Review** *(Đánh giá Mã nguồn)* | Hoạt động hợp tác nơi lập trình viên trình bày và giải thích code của mình cho đồng nghiệp xem để cùng tìm lỗi và học hỏi (Offline Pair-programming). |
| **Refactoring** *(Tái cấu trúc Mã nguồn)* | Hành động dọn dẹp, cải thiện cấu trúc bên trong của code (cho dễ đọc, dễ bảo trì) MÀ KHÔNG làm thay đổi chức năng bên ngoài của nó. |
| **Code Rot** *(Mã nguồn mục nát)* | Hiện tượng code trở nên lộn xộn, chắp vá và khó bảo trì theo thời gian nếu chỉ cắm đầu thêm tính năng mà không chịu dọn dẹp (Refactor). |
| **God Class** *(Lớp Chúa tể)* | Một "anti-pattern" (mẫu thiết kế tồi) nơi một Class bị nhồi nhét quá nhiều chức năng và làm mọi thứ trong hệ thống. Cách giải quyết là phải "xẻ thịt" nó ra. |

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **An interface abstracts a module. Abstraction helps most in reducing the complexity of:**  *(Một giao diện trừu tượng hóa một mô-đun. Sự trừu tượng hóa giúp ích nhiều nhất trong việc giảm độ phức tạp của việc:)* | • designing the system. • building the system. • maintaining the system. • cost and time estimates for developing the system. • understanding the system. |
| **2** | **An interface encapsulates a module. Encapsulation helps most in reducing the complexity of:**  *(Một giao diện đóng gói một mô-đun. Sự đóng gói giúp ích nhiều nhất trong việc giảm độ phức tạp của việc:)* | • designing the system. • building the system. • maintaining the system. • cost and time estimates for developing the system. • understanding the system. |
| **3** | **In software engineering, we build models of a software system to:**  *(Trong kỹ nghệ phần mềm, chúng ta xây dựng các mô hình của một hệ thống phần mềm để:)* | • reduce the workload of the project team. • help us deal with the complexity of a problem. • reduce the amount of communication with users. • know which people to hire into the project team. • know which language to use for implementation. |
| **4** | **Defensive programming means that you**  *(Lập trình phòng vệ có nghĩa là bạn:)* | • do not let anyone else read your code • do not let input data crash your program • do not let anyone else change your code • do not use object-oriented programming languages • do not let anyone else test your code |
| **5** | **The primary purpose of refactoring code is to**  *(Mục đích chính của việc tái cấu trúc mã nguồn là để:)* | • reduce the number of input parameters. • isolate bugs by rewriting the code. • add assertions to the code. • improve the internal structure of the code. • improve the interaction among components. |

