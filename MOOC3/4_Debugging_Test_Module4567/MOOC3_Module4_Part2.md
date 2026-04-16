# **Configuration Management**

Chúc mừng bạn đã đi đến bài giảng cuối cùng của phần Triển khai (Implementation)\!

Nếu bạn đã từng code nhóm và gặp thảm cảnh "đứa này copy đè lên file của đứa kia", hoặc làm tính năng mới khiến tính năng cũ bị hỏng mà không biết cách lấy lại code ngày hôm qua, thì bài giảng **Lecture 4-2: Configuration Management (Quản lý Cấu hình)** chính là vị cứu tinh của bạn.

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung cốt lõi của bài học:

### **🎯 Mục Tiêu Bài Học**

Bạn sẽ hiểu được cách các công ty công nghệ quản lý sự thay đổi của một dự án phần mềm khổng lồ. Cách tổ chức mã nguồn, cách kiểm duyệt yêu cầu thay đổi từ khách hàng, và cách quản lý các phiên bản (version) để hàng chục lập trình viên có thể làm việc song song mà không dẫm chân lên nhau.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Configuration Management (Quản lý Cấu hình) là gì?**

* **Định nghĩa:** Là việc quản lý, kiểm soát và theo dõi sự thay đổi của tất cả các "Artifacts" (Tạo tác) trong vòng đời dự án.  
* **Lưu ý cực kỳ quan trọng:** Artifacts ở đây **không chỉ là Source Code**\! Nó bao gồm toàn bộ Tài liệu thiết kế (Documentation), Sách hướng dẫn sử dụng (User Manual), Kịch bản kiểm thử (Test cases)... Tất cả đều phải được quản lý sự thay đổi.  
* Một phần tử cụ thể được đưa vào diện theo dõi và quản lý sự thay đổi được gọi là một **Configuration Item** (Hạng mục Cấu hình).

#### **2\. Cấu trúc của Thư viện Phần mềm (Software Library)**

Để quản lý tốt, mã nguồn và tài liệu không được ném lung tung mà phải chia làm 3 cấp độ (giống hệt tư duy của Git/GitHub hiện đại):

1. **Developer's Workspace (Không gian của Dev):** Nơi một lập trình viên duy nhất cày cuốc, sửa code và test hàng ngày (Tương đương với máy tính cá nhân \- Local machine).  
2. **Master Directory (Thư mục Chính):** Nơi chứa các phiên bản đã tương đối ổn định để các lập trình viên khác có thể tải về làm nền tảng làm việc chung (Tương đương với nhánh dev hoặc main trên GitHub).  
3. **Software Repository (Kho lưu trữ):** Nơi chứa những phiên bản CỰC KỲ ỔN ĐỊNH, đã sẵn sàng để phát hành (Release) cho người dùng cuối.

#### **3\. Khái niệm Baseline (Đường cơ sở / Phiên bản chốt)**

* **Định nghĩa:** Là một thời điểm trong dự án mà hệ thống được "đóng băng" (freeze) lại sau khi hoàn thành một cột mốc quan trọng.  
* Khi hệ thống đạt đến Baseline, nó được coi là ổn định. Kể từ giây phút đó, bất kỳ ai muốn sửa đổi dòng code nào cũng KHÔNG ĐƯỢC tự ý sửa, mà phải làm **giấy tờ xin phép chính thức (Formalized)**.  
* Để một tài liệu/code được đưa vào Baseline, nó phải vượt qua bài kiểm tra và được duyệt (Formal review procedures).

#### **4\. Quy trình Xử lý Thay đổi (Change Management Process)**

Khi khách hàng yêu cầu đổi một tính năng, team không được nhảy vào code luôn mà phải đi theo quy trình chuẩn:

1. **Submit Request:** User hoặc Dev gửi yêu cầu thay đổi.  
2. **Evaluate:** Ban kiểm soát đánh giá xem việc thay đổi này tốn bao nhiêu chi phí và ảnh hưởng thế nào đến hệ thống.  
3. **Approve:** Quản lý quyết định cho phép làm (Issue a change order).  
4. **Check-out & Change:** Lập trình viên lấy code từ thư viện ra và bắt đầu sửa.  
5. **SQA & Check-in:** Đội QA/Tester kiểm tra lại xem code sửa có chạy đúng không và có làm hỏng thứ khác không. Nếu OK thì cho Check-in (đưa code trở lại thư viện).  
6. **Auditing & Reporting:** Kiểm toán lại và tạo báo cáo ghi rõ: Ai đã sửa? Sửa khi nào? Tại sao lại sửa?

#### **5\. Version Management (Quản lý Phiên bản)**

Trong một dự án thực tế, các lập trình viên thường làm việc **song song (Parallel Development)**, dẫn đến việc sinh ra nhiều hướng đi của mã nguồn:

* **Codeline (Dòng mã):** Sự tiến hóa tuyến tính (Bản 1.0 \-\> Bản 1.1 \-\> Bản 1.2).  
* **Branches (Nhánh):** Khi 2 team cùng phát triển 2 tính năng khác nhau cùng lúc, code sẽ rẽ ra 2 nhánh riêng biệt.  
* **Merge (Hợp nhất):** Sau khi làm xong, các nhánh này sẽ được ghép ngược trở lại vào dòng mã chính (Mainstream).  
* **Variants (Biến thể):** Phần mềm có nhiều cấu hình chạy song song (Ví dụ: Một bản cài cho Windows, một bản cài cho Linux).

