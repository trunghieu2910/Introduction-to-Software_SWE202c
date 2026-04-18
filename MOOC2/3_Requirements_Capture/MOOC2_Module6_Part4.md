Key word 6 

| Thuật ngữ (Tiếng Anh / Tiếng Việt) | Bản chất & Cách áp dụng thực chiến |
| :---- | :---- |
| Use Case Specification (Đặc tả Use Case) | Cuốn tài liệu văn bản đi kèm với hình vẽ Use Case, dùng để mô tả chi tiết logic chạy của tính năng (từ lúc bắt đầu đến khi kết thúc). |
| Pre-condition (Tiền điều kiện) | Trạng thái BẮT BUỘC hệ thống phải đạt được trước khi chức năng này được phép chạy. (VD: Giỏ hàng phải có đồ). |
| Basic Flow / Happy Path (Luồng sự kiện chính) | Kịch bản mọi thứ diễn ra suôn sẻ, hoàn hảo, không có lỗi gì xảy ra. Ghi theo dạng hội thoại "Ping-Pong" giữa Hệ thống và Người dùng. |
| Post-condition (Hậu điều kiện) | Trạng thái của hệ thống sau khi chức năng này hoàn tất thành công. (VD: Đơn hàng chuyển sang trạng thái "Đã thanh toán"). |
| Alternative Flow (Luồng thay thế / Ngoại lệ) | Kịch bản mô tả các "ngã rẽ": khi người dùng làm sai (sai pass), khi hệ thống lỗi (rớt mạng), hoặc khi có tùy chọn phụ (nhập mã giảm giá). |
| Extension Point (Điểm mở rộng) | Một cái nhãn (label) cắm trên Luồng chính để đánh dấu "ngã rẽ" cho Luồng thay thế nhảy vào. Có 3 loại cắm mốc: |
| \- Single Location (Điểm đơn) | Nhãn chỉ xuất hiện đúng 1 lần ở 1 bước cụ thể. |
| \- Discrete Locations (Điểm rời rạc) | Nhãn xuất hiện ở nhiều bước khác nhau, cách xa nhau trong luồng chính. |
| \- Region (Vùng kéo dài) | Nhãn kẹp một cụm nhiều bước lại với nhau (Từ... đến...). |
| Resume Point / Exit Point (Điểm quay lại) | Khi kết thúc Luồng thay thế, hệ thống phải biết đi đâu tiếp. Có 3 cách hạ cánh: Quay lại đúng chỗ vừa rẽ, Quay lại một chỗ trước đó, hoặc Kết thúc luôn Use Case. |
| SubFlow (Luồng con) | Nhóm một cụm các bước (Segment of events) trên Luồng chính lại thành một gói (S1, S2...) để tài liệu dễ đọc.⛔ Luật thép: SubFlow KHÔNG PHẢI là một Use Case tách rời. Và tuyệt đối không được nhét SubFlow lồng vào nhau (Nesting). |

