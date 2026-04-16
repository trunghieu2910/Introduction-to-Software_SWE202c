# **Debugging**

Chào mừng bạn đến với nỗi ám ảnh lớn nhất của mọi Lập trình viên: **Debugging (Gỡ lỗi)**\!

Thầy Kenneth đã mở đầu bài giảng bằng một sự thật phũ phàng: Debugging luôn đau khổ và tốn thời gian. Do đó, tư duy đúng đắn nhất không phải là "làm sao để debug nhanh", mà là "làm sao để không phải debug".

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung cốt lõi của Lecture 4-1:

### **🎯 Mục Tiêu Bài Học**

Sau bài học này, bạn sẽ:

1. Phân biệt rõ ràng ranh giới giữa Testing (Kiểm thử) và Debugging (Gỡ lỗi).  
2. Nắm vững 3 chiến lược phòng thủ để lỗi không thể sinh ra ngay từ khâu thiết kế.  
3. Bỏ túi các kỹ thuật khoanh vùng (localize) để cô lập và tiêu diệt Bug khi nó lỡ xuất hiện.  
4. Biết cách xử lý khi gặp những Bug quá "cứng đầu".

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Testing khác Debugging như thế nào?**

*"Testing là để chứng minh lỗi **CÓ TỒN TẠI**. Còn Debugging là để tìm ra lỗi **NẰM Ở ĐÂU** và **TẠI SAO**."*

* **Testing (Kiểm thử):** Là hành động đi tìm xem chương trình CÓ TỒN TẠI VẤN ĐỀ hay không.  
* **Debugging (Gỡ lỗi):** Sau khi Testing báo là có lỗi, Debugging là quá trình đi tìm **VỊ TRÍ CHÍNH XÁC** của lỗi đó nằm ở dòng code nào, và tìm ra **NGUYÊN NHÂN** tại sao nó lại xảy ra.  
* *Sự thật thú vị:* Từ "Bug" (con bọ) ra đời vào ngày 9/9/1947 khi người ta tìm thấy một con bọ kẹt trong phần cứng máy tính làm sập toàn bộ hệ thống.

#### **2\. Chiến lược phòng thủ (Defend against bugs)**

Vì debug rất khổ, hãy cố gắng áp dụng 3 nguyên tắc sau để ngăn bug xuất hiện:

* **Cách 1: Biến lỗi thành "Không thể xảy ra" nhờ Thiết kế (Impossible by design):**  
  * Chọn công cụ/ngôn ngữ phù hợp (VD: Dùng Java sẽ không bao giờ bị lỗi ghi đè bộ nhớ, dùng Java BigInteger sẽ tránh được lỗi tràn số).  
  * Đặt ra các luật lệ (Conventions) và kỷ luật tuân theo: Cấm dùng đệ quy (tránh lặp vô hạn), dùng cấu trúc dữ liệu bất biến (immutable).  
* **Cách 2: Cố gắng làm đúng ngay từ đầu:**  
  * *Quy tắc:* Hãy nghĩ trước khi code, đừng code trước khi nghĩ\!  
  * Không dùng Trình biên dịch (Compiler) làm cái nạng đỡ. Compiler chỉ bắt được lỗi cú pháp (chấm phẩy, viết sai tên lệnh), chứ không bao giờ bắt được lỗi logic (semantic errors).  
* **Cách 3: Giữ sự đơn giản (Simplicity):**  
  * Chia nhỏ hệ thống (Modularity). Viết đặc tả (Specifications) và giao diện (Interfaces) rõ ràng cho từng Module.

#### **3\. Kỹ thuật Khoanh vùng Bug (Localize bugs)**

Khi bug đã xảy ra, bạn đừng đọc cả 10.000 dòng code. Hãy thu hẹp phạm vi lại:

* **Chiến thuật Lắp ghép:** Bắt đầu với một chương trình trống trơn \-\> Bỏ dần từng mảnh code vào chạy thử \-\> Mảnh nào vừa bỏ vào mà lỗi xuất hiện thì bug nằm ở đó.  
* **Tìm kiếm Nhị phân (Binary Search):** Chia chương trình làm 2 nửa. Nếu nửa sau bị lỗi, tiếp tục lấy nửa sau chia làm 2... Cứ thế sẽ tìm ra chính xác dòng code lỗi rất nhanh.  
* **Sử dụng Assertion:** Đặt các "trạm kiểm soát" để check điều kiện (như đã học ở bài 3-1).  
  * *Lưu ý:* Có nên để Assertion trong code giao cho khách hàng (Production code) không? **Tùy ngữ cảnh**. Nếu phần mềm điều khiển y tế sai là chết người \-\> CẦN ĐỂ LẠI để bắt nó dừng ngay lập tức. Nếu là game giải trí \-\> KHÔNG NÊN ĐỂ, vì lỡ lỗi thì game vẫn nên chạy tiếp thay vì văng ra ngoài.

#### **4\. Các "Lỗi ngớ ngẩn" (Stupid Mistakes) cần check đầu tiên**

Đôi khi bạn debug cả ngày không ra vì những lỗi rất ngớ ngẩn:

* Viết sai thứ tự tham số truyền vào hàm.  
* Viết sai chính tả tên biến.  
* **Trong Java:** Dùng \== (chỉ so sánh địa chỉ bộ nhớ) thay vì dùng .equals() (để so sánh nội dung bên trong object).  
* Quên khởi tạo giá trị ban đầu cho biến.  
* Sao chép nông (Shallow copy \- chỉ copy địa chỉ) thay vì Sao chép sâu (Deep copy \- copy dữ liệu).

#### **5\. Kiểm thử Hồi quy (Regression Test)**

* Khi bạn tìm ra và sửa xong 1 Bug, **HÃY LƯU LẠI CÁI BUG ĐÓ LÀM BÀI TEST CA (Test Case)**.  
* Tại sao? Vì khi bạn sửa lỗi mới, rất dễ vô tình làm hệ thống sinh ra lại cái lỗi cũ. Việc lưu lại bài test này để đảm bảo lỗi cũ không bao giờ có cơ hội quay lại phá hoại (Quá trình này gọi là Regression Test).

#### **6\. Bí kíp sinh tồn khi Debug quá bế tắc**

Làm sao khi nhìn code mãi không thấy lỗi?

* **Nghi ngờ mọi giả định:** Lỗi có thể do bạn đổi Hệ điều hành? Do ổ cứng đầy? Đừng chỉ nhìn vào code. (Lưu ý: Debug vào code chứ đừng debug vào những dòng comment).  
* **Vẽ lại tài liệu (Documenting):** Để hiểu lại luồng chạy của chương trình.  
* **Hỏi đồng nghiệp (Get help):** Nhờ người có kinh nghiệm review hộ.  
* **BỎ ĐI CHỖ KHÁC (Walk away):** Đừng cố debug lúc 2 giờ sáng. Hãy đi ngủ, não bộ minh mẫn vào sáng hôm sau sẽ giúp bạn tìm ra bug chỉ trong 5 phút\!

