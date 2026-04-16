KEYWORD & QUIZ 

### **Bảng 1: Từ điển Thuật ngữ Kỹ thuật (Mô-đun 4\)**

| Từ khóa (Tiếng Anh / Tiếng Việt) | Bản chất & Ý nghĩa |
| :---- | :---- |
| **Testing** *(Kiểm thử)* | Quá trình chạy chương trình để **tìm xem có tồn tại** lỗi (bug) hay không. |
| **Debugging** *(Gỡ lỗi)* | Quá trình đi tìm **vị trí chính xác** và **nguyên nhân** của lỗi sau khi Testing đã phát hiện ra nó. |
| **Binary Search** *(Tìm kiếm nhị phân)* | Một chiến thuật khoanh vùng lỗi nhanh chóng bằng cách chia đôi chương trình: test nửa này, nếu không có lỗi thì khoanh vùng nửa kia, tiếp tục chia đôi cho đến khi tìm ra dòng code hỏng. |
| **Regression Test** *(Kiểm thử hồi quy)* | Việc chạy lại các bài test cũ (đặc biệt là test case của các bug vừa sửa xong) để đảm bảo việc sửa code mới không làm các lỗi cũ quay trở lại. |
| **Configuration Management** *(Quản lý Cấu hình \- CM)* | Quá trình quản lý, kiểm soát và theo dõi sự thay đổi của tất cả các tạo tác (artifacts) trong suốt vòng đời dự án. |
| **Artifacts** *(Tạo tác)* | Bất kỳ sản phẩm nào được tạo ra trong dự án (Mã nguồn, Tài liệu, Sách hướng dẫn, Kịch bản test...). |
| **Configuration Item** *(Hạng mục cấu hình)* | Bất kỳ một Artifact nào được đưa vào diện phải theo dõi và kiểm soát sự thay đổi. |
| **Baseline** *(Đường cơ sở / Bản chốt)* | Một thời điểm mà hệ thống đã đạt được độ ổn định nhất định và được "đóng băng" lại. Bất kỳ ai muốn thay đổi thứ gì sau Baseline đều phải xin phép chính thức. |
| **Change Management** *(Quản lý thay đổi)* | Quy trình đánh giá chi phí, tác động và phê duyệt các yêu cầu thay đổi tính năng từ khách hàng/lập trình viên trước khi cho phép sửa code. |
| **Version Management** *(Quản lý phiên bản)* | Việc theo dõi và lưu trữ nhiều phiên bản khác nhau của cùng một hạng mục (Ví dụ: code bản 1.0, bản 1.1). |
| **Codeline** *(Dòng mã)* | Một chuỗi các phiên bản mã nguồn nối tiếp nhau, bản sau kế thừa từ bản trước. |
| **Branch & Merge** *(Nhánh & Hợp nhất)* | **Branch:** Tách mã nguồn ra nhiều nhánh để các team làm việc song song. **Merge:** Ghép các nhánh đó trở lại thành một phiên bản thống nhất. |

---

### **Bảng 2: Câu hỏi trắc nghiệm Ôn tập (Mô-đun 4\)**

*Lưu ý: Bộ câu hỏi này dường như bao gồm cả kiến thức ôn tập lại của các phần trước (UML) và mào đầu cho phần Kiểm thử (Testing) sắp tới.*

| STT | Câu hỏi (Question) | Các lựa chọn đáp án (Options) |
| :---- | :---- | :---- |
| **1** | **In the UML the multiplicity of an association specifies**  *(Trong UML, đa số (multiplicity) của một mối quan hệ chỉ định:)* | • which classes can be related to each other. • how many classes participate in the association. • the navigability of the association. • the number of objects that must/can be related. • whether role names are required. |
| **2** | **Could reviews or inspections be considered part of testing?**  *(Đánh giá (reviews) hoặc thanh tra (inspections) có thể được coi là một phần của kiểm thử không?)* | • No, because they are normally applied before testing. • Yes, because both help detect faults and improve quality. • Yes, because testing includes all non-constructive activities. • No, because they do not apply to the test documentation. • No, because they are beyond the development plan. |
| **3** | **The cost of fixing a fault**  *(Chi phí để sửa một lỗi...)* | • can never be more than 5% of the total development cost. • is more expensive if found in requirements than functional design. • can be estimated by performing a SWOT analysis. • increases as we move the product towards live use. • decreases as we move the product towards live use. |
| **4** | **Which of the following statement about early test design is false?**  *(Phát biểu nào sau đây về thiết kế bài kiểm thử sớm là SAI?)* | • Faults found during early test design are less expensive to fix. • Early test design can prevent fault multiplication. • Early test design can find faults. • Early test design takes more effort. • Early test design can cause changes to the requirements. |
| **5** | **Which of the following is NOT a configuration management activity?**  *(Hành động nào sau đây KHÔNG PHẢI là một hoạt động Quản lý Cấu hình?)* | • change management • version management • risk management • release management • system building |

