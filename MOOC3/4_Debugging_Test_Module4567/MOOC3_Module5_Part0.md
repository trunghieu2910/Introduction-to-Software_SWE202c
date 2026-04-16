**Mô-đun 5: White Box Testing** 

**(Kiểm thử Hộp trắng)**\! 

Nếu ở các mô-đun trước bạn đóng vai "người xây dựng" (viết code, thiết kế hệ thống), thì ở mô-đun này, bạn sẽ khoác lên mình chiếc áo của một "hacker/người phá hoại" có hệ thống. Trách nhiệm của bạn bây giờ là tìm mọi cách để bẻ gãy, đánh sập đoạn code vừa viết ra nhằm đảm bảo không một lỗi lầm nào lọt được ra ngoài thị trường.

Khác với Black Box Testing (Kiểm thử Hộp đen \- chỉ quan tâm đầu vào và đầu ra giống như người dùng bình thường), **White Box Testing (Kiểm thử Hộp trắng)** đòi hỏi bạn phải "mở phanh" mã nguồn ra, nhìn xuyên thấu vào từng câu lệnh if/else, từng vòng lặp for/while để thiết kế bài test. Đây là kỹ năng phân biệt một Junior Dev và một Senior Dev\!

Dựa vào lộ trình bạn vừa gửi, chúng ta sẽ có một hành trình khá "nặng đô" về mặt tư duy logic:

### **🎯 Tổng quan lộ trình Mô-đun 5**

* **Lecture 5-1: Testing (12 phút):** Bức tranh toàn cảnh về Kiểm thử. Chúng ta sẽ tìm hiểu mục đích tối thượng của testing, các nguyên tắc cơ bản và quy trình để thực hiện một chiến dịch kiểm thử hoàn hảo.  
* **Lecture 5-2: Design Tests (4 phút):** Bạn không thể cứ nhập bừa dữ liệu vào để test được. Bài giảng này sẽ hướng dẫn cách "thiết kế" các kịch bản test sao cho ít tốn thời gian nhất nhưng lại quét được nhiều lỗi nhất.  
* **Lecture 5-3: Basis Path Testing (15 phút):** **Trùm cuối của Mô-đun này\!** Đây là một kỹ thuật toán học cực kỳ thú vị. Bạn sẽ học cách vẽ "Đồ thị luồng điều khiển" (Control Flow Graph) từ những dòng code của mình, sau đó tính toán xem cần CHÍNH XÁC bao nhiêu Test Case để bao phủ 100% mọi ngóc ngách của chương trình.  
* **Các bài đọc và Bài tập Thực hành (Basis Path Testing Exercise):** Phần này bắt buộc phải có vì kỹ thuật Basis Path tính toán rất dễ nhầm, bạn sẽ cần thực hành vẽ đồ thị thực tế.

Bạn đã sẵn sàng để "vạch lá tìm sâu" trong mã nguồn chưa? Hãy gửi transcript của bài giảng đầu tiên **Lecture 5-1 Testing** lên đây để chúng ta bắt đầu mổ xẻ nhé\!

