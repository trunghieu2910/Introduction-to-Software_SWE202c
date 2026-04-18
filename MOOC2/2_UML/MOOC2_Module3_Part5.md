Các thuật ngữ 

| Tiêu chí phân biệt | Ràng buộc Kế thừa (Coverage Constraint) | Ràng buộc Nghiệp vụ (Business Constraints) |
| :---- | :---- | :---- |
| **Bản chất** | Là **Luật phân loại**. Quy định một đối tượng thuộc "chủng loại" nào trong cây gia phả. | Là **Luật vận hành**. Quy định cách các đối tượng tương tác, hoặc điều kiện để dữ liệu hợp lệ. |
| **Trả lời câu hỏi** | *"Tôi mang thân phận gì?"* (Tôi là ai?) | *"Tôi được phép làm gì / Tương tác như thế nào?"* |
| **Vị trí trên bản vẽ** | Ghi ở cạnh **Mũi tên Kế thừa** (Tam giác rỗng). | Ghi trên **Sợi dây Liên kết (Association)** hoặc ghi chú cạnh Thuộc tính/Class. |
| **Các nhãn (Tags) UML** | {disjoint} (Tách biệt) {overlapping} (Giao nhau) {complete} (Trọn vẹn) {incomplete} (Chưa trọn vẹn) | {ordered} (Có thứ tự) {subset} (Tập con) {xor} (Độc quyền con đường) {điều\_kiện\_logic} (VD: {age \>= 18}) |
| **Ví dụ trong dự án E-commerce** | Khách hàng chỉ có thể là Cá nhân hoặc Doanh nghiệp. {disjoint} | Đơn hàng chỉ được chọn Giao tận nhà HOẶC Lấy tại quầy. {xor} |
| **Cách triển khai trong Code Java** | Thể hiện qua **Cấu trúc Class**: Dùng từ khóa extends hoặc implements. | Thể hiện qua **Logic & Cấu trúc Dữ liệu**: Dùng lệnh if/else, throw Exception, hoặc chọn đúng kiểu List/Set/Queue. |

→ ràng buộc kế thừa chỉ được viết trên đường kế thừa và đường association thì chỉ được viết ràng buộc nghiệp vụ

| Nhóm kiến thức | Thuật ngữ (Tiếng Anh / Tiếng Việt) | Bản chất & Cách sử dụng thực tế |
| :---- | :---- | :---- |
| **Lớp Kết Hợp** (Bài 3.1) | **Association Class** (Lớp kết hợp) | Class sinh ra để "bám" vào sợi dây nối giữa 2 Class, dùng để chứa dữ liệu trung gian (VD: Điểm khi Sinh viên đăng ký Khóa học). |
|  | **Unique Link Rule** (Luật độc quyền) | Giữa 2 đối tượng cụ thể (Ông A, Môn B) **chỉ được tồn tại 1 sợi dây nối**. Cố nối thêm sẽ bị ghi đè dữ liệu. |
|  | **Offering Pattern** (Lớp Phiên bản) | Kỹ thuật chèn Class trung gian (VD: Lớp mở theo học kỳ) để lách Luật độc quyền, giúp lưu trữ lịch sử lặp lại (Học lại, mua lại). |
| **Kế Thừa** (Bài 3.2) | **Generalization** (Tổng quát hóa) | Mối quan hệ **IS-A (Là một)**. Gom điểm chung lên Lớp Cha, hoặc chẻ Lớp Cha thành các Lớp Con. (Nét liền \+ Tam giác rỗng). |
|  | **Overriding** (Ghi đè hàm) | Lớp Con viết lại code cho hàm của Lớp Cha. Khi chạy, hệ thống **ưu tiên code của Lớp Con**. |
|  | **Abstract Class** (Lớp trừu tượng) | "Bản thiết kế gốc" cho họ hàng. **Không bao giờ được dùng new** để tạo đối tượng trực tiếp. Tên Class viết *in nghiêng*. |
| **Ràng buộc Kế thừa** (Bài 3.2)  | **{disjoint}** (Tách biệt) | Một đối tượng **chỉ được chọn 1** Lớp Con duy nhất. |
|  | **{overlapping}** (Giao nhau) | Một đối tượng có thể đóng vai trò ở **Nhiều** Lớp Con cùng lúc. |
|  | **{complete}** (Trọn vẹn) | Sơ đồ đã vẽ **đủ 100%** các loại có thật ngoài đời. |
|  | **{incomplete}** (Chưa trọn vẹn) | Ngoài đời **vẫn còn loại khác** chưa được vẽ vào sơ đồ. |
| **Ràng buộc Nghiệp vụ** (Bài 3.3) | **Constraint** (Ràng buộc logic) | Quy tắc kinh doanh ép hệ thống phải theo (thường viết trong { }). VD: {Số dư \>= 100k}. |
|  | **{ordered}** (Có thứ tự) | Dữ liệu trên sợi dây liên kết không được lộn xộn, phải được sắp xếp (VD: Hàng đợi First-in-First-out). |
|  | **{subset}** (Tập con) | Đối tượng ở sợi dây này BẮT BUỘC phải được chọn từ danh sách đối tượng ở sợi dây kia. |
|  | **{xor}** (Độc quyền XOR) | Đứng giữa ngã ba, một đối tượng **chỉ được chọn 1 trong 2 con đường**, tuyệt đối không chọn cả hai. |

