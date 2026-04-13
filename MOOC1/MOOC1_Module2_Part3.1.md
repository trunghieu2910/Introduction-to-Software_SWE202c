Mở rộng về các khái niệm 

Đây là hai "công thần" đời đầu đã giúp các gã khổng lồ như Google, Facebook, hay Yahoo xử lý được lượng dữ liệu khổng lồ (Big Data).

Để dễ hiểu nhất, bạn hãy quên máy tính đi và tưởng tượng chúng ta đang có một bài toán thực tế: **Bạn có một thư viện chứa 1 triệu cuốn sách và bạn cần đếm xem từ "Tình yêu" xuất hiện tổng cộng bao nhiêu lần trong toàn bộ thư viện.**

Nếu làm theo cách truyền thống (Database thông thường): Bạn sẽ thuê 1 thủ thư, bắt anh ta đọc từ cuốn số 1 đến cuốn số 1.000.000. Anh ta sẽ mất khoảng... 100 năm để làm xong.

Đây là lúc **Hadoop** và **MapReduce** xuất hiện để giải cứu\!

### **1\. Hadoop: "Nhà kho phân tán" (Chỗ chứa dữ liệu)**

Hadoop thực chất là một hệ sinh thái mã nguồn mở, trong đó thành phần nổi tiếng nhất là hệ thống lưu trữ **HDFS** (Hadoop Distributed File System).

* **Cách nó hoạt động:** Thay vì mua một siêu máy tính khổng lồ (và cực kỳ đắt đỏ) để chứa 1 triệu cuốn sách, Hadoop cho phép bạn mua 1.000 cái máy tính tính bình thường, rẻ tiền. Nó sẽ băm nhỏ 1 triệu cuốn sách kia ra và rải đều vào 1.000 máy tính đó.  
* **Điểm hay ho:** Nếu 1 máy tính bị cháy ổ cứng, sách vẫn không mất vì Hadoop luôn tự động copy dự phòng (backup) dữ liệu sang các máy khác.

### **2\. MapReduce: "Chiến thuật chia để trị" (Cách xử lý dữ liệu)**

Dữ liệu đã nằm gọn trong 1.000 máy tính của Hadoop. Bây giờ làm sao để đếm chữ "Tình yêu" nhanh nhất? MapReduce chính là một thuật toán chia bài toán lớn thành 2 giai đoạn: **Map (Phân bổ)** và **Reduce (Thu gọn)**.

* **Giai đoạn 1 \- MAP (Chia việc):** Thay vì bắt 1 người đọc hết, Tổng chỉ huy sẽ ra lệnh cho 1.000 máy tính (đang chứa sách) *cùng lúc* tự đếm số từ "Tình yêu" trong chính máy của mình.  
  * *Máy số 1 báo cáo:* "Tôi tìm thấy 50 chữ Tình yêu".  
  * *Máy số 2 báo cáo:* "Tôi tìm thấy 120 chữ Tình yêu".  
  * ... 1.000 máy cùng làm việc song song, nên thời gian đếm xong thay vì 100 năm giờ rút xuống chỉ còn 1 tháng\!  
* **Giai đoạn 2 \- REDUCE (Gom kết quả):** Sau khi 1.000 máy đếm xong phần của mình, chúng đẩy các con số báo cáo (50, 120, 80...) về cho một nhóm máy tính khác làm nhiệm vụ "Reduce". Máy tính Reduce chỉ việc làm phép cộng đơn giản: 50 \+ 120 \+ 80 \+ ... \= Kết quả cuối cùng.

**Tóm lại:**

* **Hadoop** là cái kệ sách khổng lồ giúp bạn cất giữ dữ liệu ở khắp mọi nơi một cách an toàn.  
* **MapReduce** là chiến thuật rải quân đi làm việc song song, giúp một công việc tốn 100 năm có thể giải quyết trong vài chục phút.

---

Để bạn có thể "nhìn thấy" MapReduce hoạt động bên trong hệ thống như thế nào, mình đã tạo một mô phỏng bên dưới. Bạn hãy thử nhập một đoạn văn bản có nhiều từ lặp lại và xem thuật toán băm nhỏ, đếm song song và gộp lại ra sao nhé:

