# **Unified Process**

UP chính xác  là một **Framework (Khung làm việc) được xây dựng bằng cách "đánh cắp" những Tinh hoa (Best Practices) tốt nhất của các quy trình đi trước.**

| Hãy tưởng tượng các quy trình trước đó giống như các môn phái võ lâm, mỗi phái có một điểm mạnh riêng nhưng cũng có điểm yếu chí mạng. Ba vị giáo sư (những người tạo ra UML) đã ngồi lại, chọn lọc những chiêu thức xịn nhất của từng phái và đúc kết thành Unified Process (UP). Cụ thể, UP đã "kế thừa" những gì? Từ Waterfall (Thác nước): UP lấy đi sự kỷ luật. Nó cũng chia dự án thành các Giai đoạn (Phases: Inception, Elaboration...) rất rõ ràng để dễ quản lý và báo cáo. Từ Spiral (Xoắn ốc): UP lấy đi tư duy Đánh giá rủi ro. Trong UP, những rủi ro khó nhằn nhất (về kiến trúc, công nghệ) luôn được ưu tiên giải quyết ngay ở những vòng lặp đầu tiên. Từ Agile / Prototyping: UP lấy đi trái tim của sự linh hoạt: Iterative & Incremental (Lặp và Tăng dần). UP không bắt khách hàng chờ 1 năm mới thấy sản phẩm, mà liên tục tung ra các bản release sau mỗi vòng lặp. Từ Mô hình Hướng đối tượng (MOOC 2): UP lấy Use Case làm trung tâm (Use-case driven) để dẫn dắt mọi hoạt động từ lấy yêu cầu đến lập trình và kiểm thử. |
| :---- |

Dưới đây là phần bóc tách chi tiết mục tiêu và nội dung của bài giảng này:

### **🎯 Mục Tiêu Bài Học**

1. **Tổng kết cẩm nang chọn quy trình:** Cung cấp cho bạn (dưới vai trò Project Manager) một "kim chỉ nam" để quyết định chọn mô hình nào dựa trên đặc thù của dự án.  
2. **Nắm vững bộ khung UP (Unified Process):** Hiểu được 4 pha (Phases) cốt lõi của Quy trình Hợp nhất. Thầy Kenneth nhấn mạnh: *Từ các bài học sau trở đi, toàn bộ khóa học sẽ bám chặt vào vòng đời của quy trình UP này\!*

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **Phần 1: Cẩm nang "Nhìn bệnh bốc thuốc" (Process Selection Guide)**

### **💡 TÓM LẠI: BÍ QUYẾT CHỌN QUY TRÌNH (The Ultimate Cheat Code)**

#### Khi đi làm, bạn chỉ cần nhớ quy luật sinh tồn này:

* #### Yêu cầu RÕ RÀNG 100%, không được phép sai: Dùng Waterfall / UP.

* #### Yêu cầu MƠ HỒ, chắc chắn sẽ đổi ý: Dùng Agile / Prototyping.

* #### Hệ thống RẤT TO, muốn xài từng phần: Dùng Phased-Release / Incremental.

* #### Hệ thống RẤT MỚI & NGUY HIỂM: Dùng Spiral

**Cẩm nang chọn quy trình chi tiết** 

| Nhóm dự án | Bản chất | Đặc điểm (Dấu hiệu nhận biết) | Bốc thuốc (Quy trình) |
| :---- | :---- | :---- | :---- |
| **1\. "SAI LÀ ĐI TÙ"(Formality & Discipline)** | Liên quan đến sinh mạng, an ninh quốc gia hoặc hệ thống tài chính cốt lõi (VD: Hàng không, Y tế, Lõi ngân hàng). | Yêu cầu chốt cứng 100% từ đầu, cấm thay đổi. Cần giấy tờ, phê duyệt khắt khe, tính kỷ luật thép ở từng bước. | Đơn giản: Waterfall (Thác nước).  Phức tạp: Spiral (Xoắn ốc). |
| **2\. "VỪA ĐI VỪA DÒ ĐƯỜNG"(Anticipation of Change)** | Làm sản phẩm mới (VD: Startup app gọi xe, mạng xã hội), chưa rõ thị hiếu người dùng, ý tưởng ban đầu cực kỳ mơ hồ. | Yêu cầu thay đổi xoành xoạch. Cần làm nhanh để đưa khách hàng dùng thử và lấy phản hồi ngay lập tức để quay xe nếu cần. | Phát triển tính năng: Agile / Scrum.  Mơ hồ giao diện: Prototyping. |
| **3\. "CHIA ĐỂ TRỊ"(Modularity)** | Hệ thống phần mềm cực kỳ đồ sộ nhưng có thể cắt nhỏ thành các khối độc lập (VD: Hệ thống Quản lý trường Đại học). | Khách hàng không muốn chờ 2 năm. Họ muốn hệ thống xong khối nào (ví dụ: Quản lý tuyển sinh) thì mang ra dùng thật luôn khối đó. | Phased-Release (Phát hành theo Giai đoạn). |
| **4\. "CƯỢC MẠNG VÀO CÔNG NGHỆ"(Risk Assessment)** | Làm một thứ vô tiền khoáng hậu, áp dụng công nghệ quá mới mà team chưa ai có kinh nghiệm thực chiến (AI, Blockchain...). | Rủi ro sập dự án hoặc cạn vốn cực cao. Cần liên tục có các "trạm dừng" để chuyên gia đánh giá rủi ro trước khi code tiếp. | Spiral Model (Mô hình Xoắn ốc \- Vua trị rủi ro). |

#### 

#### **Phần 2: Unified Process (UP) \- Kẻ kế thừa tinh hoa**

Thay vì phải cãi nhau xem mô hình nào tốt nhất, giới công nghệ sinh ra **Unified Process (UP)**.

* **Bản chất:** UP không phải là một mô hình mới tinh. Nó là một **Framework tổng quát (General framework)** được chắt lọc từ những "Thực hành tốt nhất" (Best practices) của tất cả các quy trình đi trước.  
* **Đặc tính:** UP luôn tuân thủ nguyên tắc **Lặp và Tăng dần (Iterative and Incremental)**. Mỗi vòng lặp sẽ tạo ra một phần mềm chạy được (working product), và mỗi phần tăng dần sẽ thiết lập một nền tảng cơ sở (baseline) cho hệ thống.

#### **Phần 3: Vòng đời của UP (4 Pha sinh tử)**

Bất kể bạn code bằng ngôn ngữ gì, dự án chạy theo quy trình UP bắt buộc phải đi qua 4 mốc thời gian (Phases) sau:

1. **Inception (Khởi tạo):** Thu thập các yêu cầu ban đầu. Nhiệm vụ quan trọng nhất ở bước này là "Double-check" tính khả thi: Nếu khả thi (Feasible) thì làm tiếp, nếu thấy "no hope" thì dũng cảm hủy dự án ngay để đỡ tốn tiền.  
2. **Elaboration (Trau chuốt / Thiết kế kiến trúc):** Dựa trên yêu cầu, bắt đầu phác thảo ra các bản Thiết kế (như Sơ đồ Lớp, Sơ đồ Use Case) làm bản lề cho bước lập trình.  
3. **Construction (Xây dựng):** Đây là lúc Lập trình viên trực tiếp gõ code (Implement) và test phần mềm.  
4. **Transition (Chuyển giao):** Triển khai (Deploy) hệ thống đưa cho khách hàng sử dụng và tiến hành bảo trì (Maintain).

#### **Phần 4: Các Hoạt động (Activities) chạy dọc suốt dự án**

Đi kèm với 4 Pha thời gian ở trên là các Đầu việc chuyên môn (Activities) luôn phải diễn ra:

* *Kỹ thuật:* Thu thập Yêu cầu (Requirements) \-\> Phân tích (Analysis) \-\> Thiết kế (Design) \-\> Lập trình (Implementation) \-\> Kiểm thử (Test).  
* *Quản trị:* Đảm bảo Chất lượng Phần mềm (Software Quality Assurance \- SQA) và Quản lý Dự án (Project Management).

---

