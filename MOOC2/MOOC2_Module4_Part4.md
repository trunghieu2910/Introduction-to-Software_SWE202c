KEY WORD 

| Nhóm kiến thức | Thuật ngữ (Tiếng Anh / Tiếng Việt) | Bản chất & Cách áp dụng thực tế |
| :---- | :---- | :---- |
|  Yêu cầu (Reqs) | Requirements Capture (Thu thập yêu cầu) | Quá trình đi tìm chữ "WHAT" (Phần mềm cần làm gì?), tuyệt đối không bàn đến "HOW" (Sẽ code nó như thế nào?). |
|  | SRS Document (Đặc tả Yêu cầu) | Cuốn tài liệu hợp đồng quy định 100% tính năng hệ thống. Gồm 3 trụ cột: Data, Functional, và Non-functional. |
|  | Functional Req. (Yc. Chức năng) | Những hành động người dùng có thể thao tác trên hệ thống (VD: Đăng nhập, Thanh toán, Thêm sửa xóa). |
|  | Non-functional Req. (Yc. Phi chức năng) | Các tiêu chuẩn chất lượng ép hệ thống phải đạt được (VD: Load web dưới 2 giây, chịu tải 1000 user, bảo mật cao). |
|  | Data Req. (Yc. Dữ liệu) | Danh sách những thông tin cốt lõi bắt buộc phải được lưu trữ lâu dài trong hệ thống. |
| Mô hình hóa | Domain Model (Mô hình Lĩnh vực) | Một phiên bản Sơ đồ Lớp (Class Diagram) thuần túy về mặt kinh doanh. Không chứa các yếu tố kỹ thuật hay code. |
| Ánh xạ Từ vựng  | Noun / Noun Phrase (Danh từ) | Dấu hiệu nhận biết để tạo ra Class. Luôn chuyển sang dạng số ít (Singular) khi vẽ. |
|  | Verb / Verb Phrase (Động từ) | Dấu hiệu nhận biết để vẽ Association (Dây liên kết). Nên dùng thể chủ động cho dễ đọc. |
|  | Possessive Phrase (Cụm từ sở hữu) | Dấu hiệu nhận biết để tạo Attribute (Thuộc tính). Đi theo cấu trúc "A của B" (VD: Mật khẩu của Sinh viên). |
|  Bộ Lọc Class | Irrelevant / Vague (Không liên quan / Mơ hồ) | Các từ nhắc đến cho vui, hoặc quá chung chung (VD: "Thông tin", "Dữ liệu"). \-\> BẮT BUỘC LOẠI BỎ. |
|  | Redundant (Trùng lặp) | Nhiều từ đồng nghĩa cùng chỉ một đối tượng. \-\> Gộp lại, chỉ giữ từ chuẩn xác nhất. |
|  | Implementation Construct (Từ chỉ kiến trúc/triển khai) | Các từ ám chỉ cấu trúc kỹ thuật máy tính (VD: "Hệ thống", "Database"). \-\> TUYỆT ĐỐI KHÔNG vẽ làm Class. |
|  Bộ Lọc Liên Kết | Ternary Association (Liên kết 3 ngôi) | Một sợi dây nối cùng lúc 3 Class với nhau. \-\> Nên Chia nhỏ (Decompose) thành các dây 2 ngôi cho dễ quản lý. |
|  | Derived Association (Dây dẫn xuất/Vòng lặp thừa) | Hiện tượng sơ đồ có vòng tròn, trong đó đường đi tắt và đường vòng mang lại cùng một thông tin y hệt nhau. \-\> Xóa bớt 1 đường. |
| Bộ Lọc Thuộc tính | Object Identifier / ID (Mã định danh nhân tạo) | Các mã do máy tính tự đẻ ra để phân biệt (VD: StudentID, OrderID). \-\> XÓA SẠCH khỏi Domain Model vì nó không phải là đặc tính thật ngoài đời. |

