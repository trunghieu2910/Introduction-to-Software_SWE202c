# **Software Development Plan**

Bài giảng **Lecture 6-2: Software Development Plan (SDP)** chính là "trái tim" và là bài học nặng đô nhất của toàn bộ khóa Quản lý dự án này. Đây là nơi bạn chuyển hóa từ những ý tưởng mơ hồ thành một bản thiết kế hành động thực tế.

Trong vai trò là một Leader, việc nắm vững các kỹ thuật lập kế hoạch này sẽ giúp bạn điều phối công việc cho một nhóm khoảng 6 thành viên một cách nhịp nhàng, đảm bảo ai cũng có việc phù hợp (ví dụ: người lo UI, người lo Database) mà không bị chồng chéo hay ngồi chờ đợi lẫn nhau.

Dưới đây là phần bóc tách chi tiết bản đồ chiến thuật này:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu rõ cấu trúc của một **Bản Kế hoạch Phát triển Phần mềm (SDP)**.  
2. Nắm vững kỹ thuật **WBS (Work Breakdown Structure)** để "chia để trị" công việc.  
3. Biết cách trực quan hóa tiến độ bằng biểu đồ **Gantt** và **PERT**, đặc biệt là tìm ra **Đường găng (Critical Path)**.  
4. Nắm được các công thức toán học và kỹ thuật để ước lượng thời gian, chi phí (LOC, Function Points, Delphi).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Lõi của SDP & Sản phẩm bàn giao (Deliverables)**

Lập SDP là bài toán **"Tối ưu hóa trong điều kiện thiếu dữ liệu"** (bạn phải tính toán mọi thứ khi dự án còn chưa bắt đầu).

* Bạn phải chốt hạ **Deliverables (Sản phẩm bàn giao)**: Không chỉ là code chạy được, mà còn là tài liệu phân tích, bản thiết kế (Design specs), thư viện mã nguồn, và thậm chí là dịch vụ hướng dẫn cài đặt.  
* **Môi trường & Công cụ:** Việc chọn dùng VS Code hay IntelliJ, dùng Maven hay Ant cũng phải được chốt trong bản kế hoạch này.

#### **2\. Cấu trúc Phân rã Công việc (Work Breakdown Structure \- WBS)**

Tuyệt chiêu lớn nhất của người quản lý là **Chia để trị (Divide and Conquer)**.

* Bạn chia dự án lớn thành các module, module chia thành các task, task chia thành các sub-task nhỏ hơn (như rễ cây).  
* **Nguyên tắc vàng:** Task không được chia quá to (rất khó kiểm soát tiến độ), nhưng cũng không được quá nhỏ lắt nhắt (dẫn đến sa đà vào tiểu tiết (micromanagement)). Mỗi "nhánh cây" cuối cùng phải dễ dàng gán cho đúng một người chịu trách nhiệm.

#### **3\. Lên Lịch Trình (Scheduling): Gantt và PERT**

Sau khi chặt nhỏ công việc, bạn phải ráp chúng lên trục thời gian:

* **Gantt Chart:** Biểu đồ ngang cực kỳ trực quan giúp nhìn tổng thể dự án. Task nào kéo dài từ ngày nào đến ngày nào đều hiện rõ.  
* **PERT Chart:** Biểu đồ dạng mạng lưới (network). Nó thể hiện tính *phụ thuộc* (Ví dụ: Phải code xong Database thì mới làm được giao diện).  
  * ⚠️ **Critical Path (Đường găng):** Đây là khái niệm quan trọng nhất\! Nó là **con đường dài nhất** từ lúc bắt đầu đến lúc kết thúc dự án. Bất kỳ một task nào nằm trên đường găng này bị chậm tiến độ, **toàn bộ dự án sẽ bị trễ deadline**.

#### **4\. Nghệ thuật Ước lượng (Estimation Techniques)**

Thầy Kenneth giới thiệu cách chấm dứt việc "đoán mò" thời gian/chi phí bằng các phương pháp khoa học:

* **Lines of Code (KLOC):** Đo bằng số dòng code. (Điểm yếu: Mỗi lập trình viên có một văn phong code khác nhau, người code dài chưa chắc đã làm nhiều việc hơn người code ngắn).  
* **Function Points (FP):** Đo bằng số lượng tính năng, số lượng Input/Output, số lượng API giao tiếp với bên ngoài. Cách này khách quan và chính xác hơn.  
* **Ước lượng đa chiều:** Không bao giờ để 1 người đoán. Hãy dùng **Delphi Technique** (hỏi nhiều chuyên gia rồi lấy trung bình) hoặc **PERT Estimation** (ước lượng theo 3 kịch bản: Lạc quan, Khả dĩ nhất, Bi quan).

#### **5\. Quản trị Rủi ro & Ngân sách (Risk & Budget)**

* Phải luôn tự hỏi: *"Điều tồi tệ nhất nào có thể xảy ra?"* (Thiếu người, lỗi server, khách đổi yêu cầu...). Từ đó lên phương án B (Contingency plans).  
* **Quy tắc ngân sách:** Luôn phải giữ lại **10% \- 15% quỹ dự phòng (extra reserve)**. Đừng bao giờ vung tay quá trán ngay từ tháng đầu tiên.

---

### **🧮 Trạm thực hành: Máy tính Ước lượng PERT**

Để ứng dụng ngay cách tính toán thời gian cho một task khó nhằn mà không bị "hớ" khi cam kết với sếp, Thầy Kenneth khuyên dùng kỹ thuật ước lượng 3 điểm (PERT Estimation) với công thức: $E \= (O \+ 4M \+ P) / 6$.

Hãy thử nhập thời gian bạn dự tính cho một task vào công cụ mô phỏng dưới đây để xem thời gian thực tế bạn nên báo cáo là bao nhiêu:

Cho tôi xem hình ảnh trực quan  
Việc áp dụng công thức PERT này vào lúc chia task sẽ giúp team lập trình của bạn bớt bị "ngộp" vì deadline ảo.

Bạn đã sẵn sàng để xem cách quản lý và "chữa cháy" khi dự án thực sự đi vào hoạt động trong bài **Lecture 6-3 Project Tracking and Control** chưa?

