KEY WORD

| Nhóm | Thuật ngữ (Tiếng Anh) | Tiếng Việt | Bản chất / Ý nghĩa cốt lõi | Cách vẽ UML / Code Java |
| :---: | :---: | :---: | :---: | :---: |
|  Nền tảng | UML | Ngôn ngữ mô hình hóa | Ngôn ngữ trực quan để vẽ bản thiết kế phần mềm, không phải ngôn ngữ lập trình. | N/A |
|  | Requirement Model | Mô hình Yêu cầu | Bản vẽ mô tả "Nghiệp vụ thực tế", dùng ngôn ngữ tự nhiên để chốt với Khách hàng. | Bỏ qua kiểu dữ liệu, bỏ qua từ khóa kỹ thuật. |
|  | Solution Model | Mô hình Giải pháp | Bản vẽ kỹ thuật chi tiết dùng cho Lập trình viên để gõ code. | Chứa kiểu dữ liệu, tầm vực (+/-), class cấu hình. |
| Sơ đồ Sơ đồ Sơ đồ | Class Diagram | Sơ đồ Lớp | Biểu diễn cấu trúc Dữ liệu, các Lớp và mối liên hệ giữa chúng. | Hình chữ nhật chia 3 ngăn (Tên, Thuộc tính, Thao tác). |
|  | Use-case Diagram | Sơ đồ Use-case | Biểu diễn Chức năng hệ thống từ góc nhìn của người dùng. | Hình người (Actor) và các hình bầu dục (Use case). |
|  | State Machine Diagram | Sơ đồ Trạng thái | Biểu diễn Vòng đời và sự biến đổi trạng thái của một đối tượng cụ thể. | Các nút trạng thái (tròn/vuông) và mũi tên luồng. |
| Cấu trúc Lớp  | Classification | Sự phân loại | Hành động gom nhóm các đối tượng cụ thể có chung đặc điểm thành 1 bản thiết kế. | (Kỹ năng tư duy thiết kế) |
|  | Classifier | Bộ phân loại | "Cái khuôn" trừu tượng dùng để chứa hoặc đúc ra thực thể (Class, Association). | N/A |
|  | Class | Lớp | Bản thiết kế/Cái khuôn quy định thuộc tính và hành vi chung. | public class TenLop { ... } |
|  | Instance / Object | Thực thể / Đối tượng | Một đối tượng có thật được "đúc" ra từ Class (VD: Class là Khách, Object là ông A). | TenLop obj \= new TenLop(); |
|  | Attribute | Thuộc tính | Dữ liệu, đặc điểm lưu trữ bên trong một Class. | private String ten; |
|  | Operation | Thao tác | "Chữ ký" của hàm (Tên hàm, Tham số, Kiểu trả về). Chỉ là khai báo. | \+ tinhToan(x: int): int |
|  | Method | Phương thức | Ruột code logic thực sự nằm bên trong thao tác đó. | Code nằm trong ngoặc { ... } |
| Quan hệ  | Link | Liên kết | Sợi dây kết nối cụ thể giữa 2 đối tượng thật ngoài đời. | N/A |
|  | Association | Kết hợp | Mối quan hệ phổ biến nhất, gom nhóm các Links. Thể hiện sự tương tác. | Nét liền (Không mũi tên). Code: Biến thuộc tính. |
|  | Navigability | Tính điều hướng | Quy định luồng tương tác một chiều (A biết B, nhưng B không biết A). | Mũi tên chỉ một hướng. Code: Khai báo biến 1 bên. |
|  | Role Name | Tên vai trò | Nhãn (Danh từ) ở 2 mút sợi dây. Chính là Tên Biến khi gõ code. | Ví dụ: \-chuSoHuu \-\> Code: private User chuSoHuu; |
|  | Multiplicity | Bản số | Luật số lượng Cận dưới \- Cận trên (Ví dụ: 0..1, 1..\*). | Code: Biến đơn lẻ (nếu max=1) hoặc biến List (nếu max=\*). |
|  | Aggregation | Tập hợp | Quan hệ "Toàn thể \- Bộ phận" lỏng lẻo. Xóa Mẹ, Con vẫn sống. | Nét liền \+ Hình thoi rỗng. Code: Nhận Con từ Constructor. |
|  | Composition | Cấu thành | Quan hệ "Toàn thể \- Bộ phận" sinh tử. Xóa Mẹ, Con chết theo. | Nét liền \+ Hình thoi đặc. Code: Tự new Con bên trong. |
|  | Dependency | Phụ thuộc | Quan hệ "Sử dụng tạm thời", lỏng lẻo nhất. Dùng xong là bỏ. | Nét đứt \+ Mũi tên chữ V. Code: Truyền làm Tham số hàm. |
|  | Inheritance | Kế thừa | Quan hệ "Là một" (Is-a). Con thừa hưởng mọi thứ của Cha. | Nét liền \+ Tam giác rỗng. Code: Từ khóa extends. |
|  | Realization | Hiện thực hóa | Class cam kết viết code thực thi các hàm rỗng trong Interface. | Nét đứt \+ Tam giác rỗng. Code: Từ khóa implements. |

