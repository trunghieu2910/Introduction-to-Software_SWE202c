KEY WORD

| Chủ đề | Thuật ngữ gốc (Tiếng Anh) | Thuật ngữ Tiếng Việt | Giải thích ngắn gọn (Bản chất) |
| :---- | :---- | :---- | :---- |
| 1\. NGUỒN GỐC CỦA SỰ PHỨC TẠP | Application Domain | Lĩnh vực Nghiệp vụ | Ngành nghề thực tế mà phần mềm phục vụ (Ví dụ: Y tế, Bán lẻ, Ngân hàng). Dev thường không hiểu rõ cái này. |
|  | Stakeholders | Các bên liên quan | Bất kỳ ai có liên quan đến dự án: Khách hàng, Lập trình viên, Người dùng cuối, Quản lý. |
|  | Communication barrier | Rào cản giao tiếp | Sự hiểu lầm do ngôn ngữ con người mơ hồ hoặc do khách hàng dùng từ ngữ khác với lập trình viên. |
| 2\. CÁCH "TRỊ" SỰ PHỨC TẠP | Design Goals | Mục tiêu thiết kế | Ưu tiên hàng đầu của hệ thống (nhanh, bảo mật, hay dễ dùng). Phải chọn 2-3 cái vì không thể có tất cả. |
|  | Divide and Conquer | Chia để trị | Chiến thuật chẻ một hệ thống khổng lồ thành nhiều mảnh nhỏ để dễ quản lý và phân chia công việc. |
|  | Modularity | Tính Mô-đun | Kết quả của việc "Chia để trị", hệ thống được tách thành các khối độc lập (Ví dụ: Khối Giỏ hàng, Khối Thanh toán). |
|  | Incremental Development | Phát triển tăng dần | Không làm tất cả cùng lúc. Làm xong mô-đun nào, ráp vào và chạy thử mô-đun đó. |
|  | Information Hiding | Che giấu thông tin | Nguyên tắc không cho phép các mô-đun chọc sâu vào code của nhau, chỉ được giao tiếp qua bề mặt. |
|  | Interface | Giao diện / Cổng giao tiếp | "Bản hợp đồng" quy định cách các mô-đun gọi hàm của nhau. |
|  | Abstraction | Trừu tượng hóa | Bỏ qua các chi tiết thừa. Khi dùng một hàm, chỉ cần biết hàm đó làm gì (qua Interface), không cần biết nó được code thế nào. |
|  | Encapsulation | Đóng gói | Khoanh vùng sự thay đổi. Sửa code nát bét bên trong một mô-đun cũng không làm hỏng các mô-đun khác đang gọi nó. |
| 3\. BẢN CHẤT NGHỀ NGHIỆP | Programming-in-the-small | Lập trình vi mô | Chỉ đơn thuần là viết code, gõ phím. (Công việc của Coder). |
|  | Programming-in-the-large | Lập trình vĩ mô | Vẽ kiến trúc, thiết kế hệ thống, quản lý tài liệu, giao tiếp. (Công việc của Software Engineer). |
|  | Requirements Model | Mô hình Yêu cầu | Bản vẽ/Tài liệu mô tả những gì hệ thống phải làm (để chốt với khách hàng). |
|  | Solution Model | Mô hình Giải pháp | Bản vẽ kỹ thuật (như UML) mô tả hệ thống được xây dựng như thế nào (để team Dev nhìn vào code). |
|  | Rationale Management | Quản lý lý do quyết định | Việc ghi chép lại tài liệu giải thích TẠI SAO lại đưa ra một quyết định kỹ thuật nào đó để sau này xem lại. |
|  | Computer Scientist | Nhà Khoa học Máy tính | Người tìm hiểu sâu về lý thuyết, thuật toán để tạo ra những sự đột phá (breakthroughs). |
|  | Software Engineer | Kỹ sư Phần mềm | Người áp dụng các công cụ có sẵn để xây dựng sản phẩm chất lượng, với mục tiêu tránh rủi ro/thất bại (avoid failures). |

