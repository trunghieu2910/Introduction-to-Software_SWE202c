# **Code Review**

Bài giảng này tuy ngắn (chỉ 2 phút) nhưng lại đề cập đến một trong những "nghi thức" thiêng liêng nhất của ngành công nghiệp phần mềm. Đặc biệt trong các môi trường đòi hỏi tính bảo mật và chuẩn mực cao như hệ thống công nghệ của các ngân hàng hay tổ chức tài chính, **Code Review (Đánh giá Mã nguồn)** là lớp khiên bảo vệ sống còn.

Dưới đây là phần bóc tách chi tiết Lecture 3-2:

### **🎯 Mục Tiêu Bài Học**

Hiểu được bản chất, mục đích thực sự và cách thức tiến hành Code Review. Bạn sẽ nhận ra đây không phải là một buổi "đấu tố" tìm lỗi, mà là một hoạt động hợp tác nghệ thuật để nâng cao chất lượng phần mềm và gắn kết đội ngũ.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Code Review là gì?**

* Thầy Kenneth định nghĩa: Code Review là **"phiên bản offline của Pair-programming"** (Lập trình theo cặp).  
* Thay vì 2 người ngồi chung 1 máy tính cùng gõ code (như Extreme Programming), thì ở đây: Bạn tự viết code xong \-\> Gọi đồng nghiệp ra \-\> Mở máy lên, trình bày và giải thích từng dòng code (step-by-step) cho họ hiểu.

#### **2\. Mục đích TỐI THƯỢNG của Code Review**

Rất nhiều Lập trình viên sợ Code Review vì nghĩ rằng mình đang bị đánh giá. Thầy Kenneth nhấn mạnh:

* **Không phải để "bới lông tìm vết" (Not finding faults):** Mục đích không phải là chê bai người khác viết code dở.  
* **Không dùng để đánh giá KPI (Not assessment of performance):** Sếp không dùng số lượng lỗi tìm thấy trong Code Review để trừ lương.  
* **Mục đích thực sự là Sự hợp tác (Collaboration):** Cùng nhau làm cho chương trình ổn định và tốt hơn. Trách nhiệm là *chia đều* (Accountability is both). Nếu một đoạn code đã được review mà sau này phát sinh lỗi, cả người viết code (Author) và người review (Reviewer) đều phải chịu trách nhiệm.

#### **3\. 5 Lợi ích Vàng của Code Review**

1. Bắt được lỗi (Bug) từ rất sớm trước khi nó phá hỏng hệ thống.  
2. Đảm bảo có **nhiều hơn 1 người** hiểu rõ về một đoạn code (Tránh tình trạng một Dev nghỉ việc là cả team "khóc thét" vì không ai hiểu đoạn code đó viết gì).  
3. Ép người viết code (Author) phải suy nghĩ cẩn thận và viết code sạch sẽ hơn (vì biết chắc chắn ngày mai sẽ có người đọc code của mình).  
4. **Cơ hội "lên trình":** Đây là con đường ngắn nhất để các Fresher/Junior Java Backend học hỏi tư duy xử lý logic và tiêu chuẩn viết code từ các bậc tiền bối (Senior).  
5. Code Review mang tính tự nguyện (Voluntary) giúp xây dựng văn hóa chia sẻ.

#### **4\. Chúng ta Review những gì?**

* Có thể review: Một bộ tài liệu, một Module hoàn chỉnh, hoặc chỉ một đoạn code nhỏ.  
* **Trọng tâm soi lỗi (Focus areas):**  
  * *Error-prone code:* Những đoạn code phức tạp, dễ sinh lỗi (như vòng lặp phức tạp, xử lý đa luồng).  
  * *Security:* Các lỗ hổng bảo mật.  
  * *Coding standards:* Kiểm tra xem code có tuân thủ quy tắc đặt tên biến, tên hàm của công ty không.  
  * Kiểm tra chéo dựa trên Checklist có sẵn.

---

### **💡 Bài học Thực chiến**

Khi bắt đầu đi làm thực tế, bạn sẽ thường xuyên sử dụng các nền tảng như GitHub hoặc GitLab. Quá trình Code Review thường được diễn ra thông qua **Pull Requests (PR)**. Khi bạn làm xong một chức năng, bạn sẽ tạo một PR. Các Senior sẽ vào đọc code của bạn, để lại comment (bình luận) trực tiếp trên từng dòng code cần sửa. Chỉ khi nào tất cả reviewer "Approve" (Chấp thuận), code của bạn mới được phép hòa (Merge) vào nhánh code chính của công ty.

