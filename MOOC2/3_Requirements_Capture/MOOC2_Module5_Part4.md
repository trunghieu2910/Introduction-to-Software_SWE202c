KEY WORD 5 

| Nhóm | Thuật ngữ (Tiếng Anh / Tiếng Việt) | Bản chất & Cách áp dụng thực chiến |
| :---- | :---- | :---- |
| Khái niệm cốt lõi | Functional Requirements (Yêu cầu Chức năng) | Trả lời câu hỏi: "Người dùng làm được gì trên hệ thống?". Đây là mục tiêu ra đời của sơ đồ Use Case. |
| Thành phần Sơ đồ | Actor (Tác nhân / Người que) | Đại diện cho một Vai trò (Role) hoặc một Hệ thống bên ngoài (External System) tương tác với phần mềm.⛔ Luật thép: Thiết bị phần cứng (bàn phím, màn hình) KHÔNG BAO GIỜ là Actor. |
| Thành phần Sơ đồ | Use Case (Ca sử dụng / Hình elip) | Một chức năng tổng quát mô tả một Câu chuyện hoàn chỉnh (Complete Story) từ góc nhìn của Actor.⛔ Luật thép: Đặt tên bắt đầu bằng Động từ chủ động \+ Danh từ (VD: Đăng ký môn học). |
| Thành phần Sơ đồ | System Boundary (Ranh giới hệ thống) | Hình chữ nhật bao quanh các Use Case.⛔ Luật thép: Các Actor bắt buộc phải đứng bên ngoài hình chữ nhật này. |
| Thành phần Sơ đồ | Initiation Arrow (Mũi tên khởi xướng: \-\>) | Nối từ Actor đến Use Case, chỉ ra rằng Actor là người chủ động bấm nút bắt đầu chức năng đó. |
| Thành phần Sơ đồ | Communication Line (Đường giao tiếp: \-) | Nét liền trơn nối Actor và Use Case, chỉ ra sự trao đổi dữ liệu, nhưng Actor này không phải là người bắt đầu (thường dùng cho các Hệ thống bên ngoài đứng đợi nhận dữ liệu). |
| Phân biệt rạch ròi | Scenario (Kịch bản cụ thể) | Là một trường hợp sử dụng chi tiết của một cá nhân cụ thể ở một thời điểm cụ thể (VD: Hieu đăng nhập lúc 8h).⛔ Luật thép: KHÔNG vẽ Scenario lên sơ đồ. Sơ đồ chỉ vẽ Use Case. |
| Phân biệt rạch ròi | Normal Sequence (Luồng suôn sẻ / Happy Path) | Quá trình sử dụng không gặp lỗi.⛔ Luật thép: Sơ đồ Use Case CHỈ VẼ luồng này. |
| Phân biệt rạch ròi | Exception / Alternative (Ngoại lệ / Luồng rẽ nhánh) | Các lỗi như sai mật khẩu, thẻ hết tiền, mất mạng...⛔ Luật thép: KHÔNG vẽ lên sơ đồ để tránh rối rắm. Chỉ ghi chú bằng chữ vào tài liệu. |
| Quy tắc Nâng cao | Actor Generalization (Kế thừa Tác nhân) | Dùng mũi tên tam giác rỗng để gom các Actor có quyền giống nhau (VD: Quản lý kế thừa Nhân viên). \-\> Khuyên dùng. |
| Quy tắc Nâng cao | Use Case Generalization (Kế thừa Use Case) | Cho một Use Case này kế thừa Use Case khác. \-\> ⛔ Luật thép của Thầy: KHÔNG NÊN DÙNG vì rất dễ sai và làm nát sơ đồ. |
| Tài liệu đính kèm | Use Case Specification (Đặc tả Use Case) | Cuốn tài liệu Word đi kèm sơ đồ. Nơi bạn viết bằng chữ mọi chi tiết: Kịch bản, Lỗi ngoại lệ, Luồng thay thế mà bạn đã giấu đi trên bản vẽ. |

