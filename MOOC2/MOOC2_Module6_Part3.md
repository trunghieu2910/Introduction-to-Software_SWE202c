# **SubFlow**

Chào mừng bạn đến với bài học cuối cùng của Mô-đun 6\! Bài học này mang đậm tư tưởng **"Clean Code" (Code Sạch)** của dân lập trình, nhưng lại được áp dụng cho... tài liệu văn bản.

Giả sử chức năng \[Thanh toán đơn hàng\] của bạn có quá trình diễn ra tới 50 bước, đọc từ trên xuống dưới chắc chắn khách hàng và cả Developer đều sẽ "tẩu hỏa nhập ma". Thầy Kenneth đã mang đến một giải pháp cứu cánh: **SubFlow (Luồng con)**.

Dưới đây là phần giải mã chi tiết nghệ thuật "Chia để trị" trong viết Đặc tả Use Case:

### **🎯 Mục Tiêu Bài Học (Lesson Objective)**

Bài học này dạy bạn kỹ năng dọn dẹp Luồng sự kiện chính (Basic Flow). Bạn sẽ học cách "đóng gói" một cụm các bước lắt nhắt thành một khối gọn gàng để tài liệu dễ đọc hơn, đồng thời giải quyết triệt để sự nhầm lẫn giữa việc "Tạo Luồng con" và "Tạo Use Case mới".

---

### **🧠 Các Kiến Thức Trọng Tâm (Core Knowledge)**

#### **1\. SubFlow (Luồng con) là gì?**

* **Bản chất:** Nó giống y hệt như việc bạn tạo ra một Hàm (Function/Method) phụ trong lập trình để gọi ra dùng. Nó là một tập hợp các bước (Segment of events) có chung một mục đích rõ ràng và mang tính nguyên tử (Atomic \- làm là làm trọn vẹn).  
* **Quy tắc đặt tên:** Đánh số thứ tự **S1, S2, S3...** kèm theo một cái tên ngắn gọn.  
* **Cách hoạt động:** Trên Luồng chính, thay vì liệt kê từ bước 11 đến bước 20 mô tả cách lưu dữ liệu, bạn chỉ cần ghi 1 dòng ngắn gọn: *"Bước 11: Thực hiện luồng con \[S1: Lưu thông tin lịch học\]"*. Chi tiết S1 gồm những gì sẽ được viết ở một phần riêng biệt bên dưới.

#### **2\. ⛔ Luật cấm "Búp bê Nga" (Excessive Nesting)**

* Bạn tuyệt đối **không được** nhét một SubFlow vào bên trong một SubFlow khác, rồi lại có một SubFlow nhỏ hơn nữa bên trong.  
* *Lý do:* Nó sẽ tạo ra một mê cung đọc không lối thoát (Spaghetti document), đi ngược lại mục đích ban đầu là làm cho tài liệu dễ đọc.

#### **3\. Chân lý cốt lõi: SubFlow KHÔNG PHẢI LÀ MỘT USE CASE TÁCH RỜI**

Đây là phần quan trọng nhất của bài học, nơi Thầy Kenneth lặp lại triết lý "Complete Story" (Câu chuyện hoàn chỉnh) từ Mô-đun 5:

* **Tính Độc Lập của Use Case:** Các Use Case (hình elip trên bản vẽ) **KHÔNG ĐƯỢC GIAO TIẾP / GỌI NHAU**. Chúng phải hoàn toàn độc lập. Bạn không thể bắt người đọc phải cầm Đặc tả của Use Case A lên, đọc đến nửa chừng lại phải đi tìm cuốn Đặc tả của Use Case B để đọc tiếp.  
* **Lỗi chia nhỏ sai lầm:** Thay vì vẽ 4 cái elip nhỏ xíu là \[Chọn đồ\], \[Nhập địa chỉ\], \[Nhập thẻ\], \[Chốt đơn\], hãy gộp tất cả lại thành **1 hình elip duy nhất** là \[Đặt hàng\].  
* **Giải pháp với SubFlow:** Trong cuốn Đặc tả của cái Use Case \[Đặt hàng\] khổng lồ đó, bạn chia nó thành các Luồng con:  
  * Luồng chính gọi \-\> S1: Nhập địa chỉ.  
  * Luồng chính gọi \-\> S2: Xử lý thẻ tín dụng.  
    \=\> **Bản vẽ bên ngoài (Sơ đồ) cực kỳ sạch sẽ, bên trong Đặc tả (Tài liệu) cực kỳ rõ ràng\!**

---

Để rèn luyện tư duy phân định rạch ròi giữa việc "Vẽ thêm một elip mới" (Use Case) hay "Viết thêm một S1" (SubFlow), hãy thử đóng vai một Kiến trúc sư Hệ thống và xử lý tình huống sau nhé:

Cho tôi xem hình ảnh trực quan  
Chúc mừng bạn đã "phá đảo" toàn bộ Mô-đun 6\! Tư duy của bạn hiện tại đã vượt ra khỏi mức độ của một thợ code và đạt tới chuẩn mực của một người thiết kế hệ thống chuyên nghiệp rồi đấy. Bạn muốn tổng hợp từ vựng Mô-đun 6 hay nhảy thẳng sang Mô-đun tiếp theo luôn nào?

