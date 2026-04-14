**Module 1  : Mở đầu về Kỹ thuật và phần mềm**  
**Module 2 3  : cách vẽ sơ đồ lớp**   
**Module 4 5 6 7 Bức tranh toàn cảnh về thu thập Yêu cầu (Requirements Capture)\! 🎉**  
Để chuẩn bị hành trang đi thi, hoặc tự tin bước vào một dự án thực tế với vai trò Business Analyst (BA) hay Systems Analyst (SA), đây là bức tranh toàn cảnh "chốt hạ" những gì bạn đã học được từ Thầy Kenneth.

---

### **🗺️ BỨC TRANH TOÀN CẢNH: HÀNH TRÌNH TẠO RA SRS**

Mục tiêu tối thượng của toàn bộ chuỗi bài này là đẻ ra được cuốn **SRS (Software Requirements Specification \- Đặc tả Yêu cầu Phần mềm)**. Cuốn sách này được cấu thành từ 3 trụ cột không thể tách rời:

#### **🏛️ Trụ cột 1: DATA REQUIREMENTS (Hệ thống cần lưu gì?)**

* **Câu hỏi cốt lõi:** Dữ liệu nào cần được lưu trữ lâu dài trong cơ sở dữ liệu?  
* **Công cụ sử dụng:** Sơ đồ Domain Model (Mô hình Lĩnh vực / Sơ đồ Lớp mức nghiệp vụ).  
* **Tuyệt chiêu nhận diện (Từ Mô-đun 4):**  
  * **Danh từ:** Trở thành Class.  
  * **Cụm Sở hữu ("của"):** Trở thành Attribute (Thuộc tính).  
  * **Động từ nối 2 Danh từ:** Trở thành Association (Dây liên kết).  
* **Luật "Tử thần" cần nhớ:** Tuyệt đối không đưa "ID" hay các từ ngữ đậm chất kỹ thuật (như "Database", "System") vào bản vẽ.

#### **🏛️ Trụ cột 2: FUNCTIONAL REQUIREMENTS (Người dùng làm được gì?)**

* **Câu hỏi cốt lõi:** Hệ thống cung cấp những chức năng gì cho ai?  
* **Công cụ sử dụng (Mô-đun 5 & 6):**  
  1. **Sơ đồ Use Case:** Bức tranh tổng quan vẽ bằng elip và người que.  
     * *Actor (Người que):* Ai/Cái gì xài hệ thống? (Không bao giờ là thiết bị phần cứng).  
     * *Use Case (Elip):* Bắt đầu bằng Động từ chủ động \+ Danh từ. Phải là một câu chuyện hoàn chỉnh (Complete Story).  
  2. **Đặc tả Use Case (Use Case Specification):** Kịch bản chi tiết bằng chữ cho từng elip.  
     * *Happy Path:* Luồng chạy suôn sẻ.  
     * *Extension Points & Alternative Flows:* Rẽ nhánh xử lý lỗi (Exception) và tùy chọn (Option).  
     * *SubFlow:* Chia nhỏ luồng dài thành S1, S2... để dễ đọc.

#### **🏛️ Trụ cột 3: NON-FUNCTIONAL REQUIREMENTS (Hệ thống chạy tốt đến đâu?)**

* **Câu hỏi cốt lõi:** Ràng buộc về chất lượng, hiệu năng, bảo mật là gì?  
* **Công cụ sử dụng (Mô-đun 7):** Liệt kê bằng văn bản hoặc đưa vào nhóm *Admin Use Cases* nếu cần code giao diện quản trị (như Phân quyền, Backup).  
* **Các nhóm chính:** Performance (Tốc độ), Reliability (Độ tin cậy), Security (Bảo mật), Usability (Độ dễ dùng).

---

### **🕵️ BƯỚC CUỐI CÙNG: VALIDATION (BẮT BUG TRÊN GIẤY)**

Trước khi ký nghiệm thu, bạn phải tự "soi" lại cuốn SRS của mình để đảm bảo nó không dính 4 loại "phốt" kinh điển (Bài 7-2):

1. **Incomplete:** Thiếu trường hợp ngoại lệ / mép biên.  
2. **Inconsistent:** Hai dòng yêu cầu cãi nhau chan chát.  
3. **Unclear:** Dùng từ ngữ mơ hồ, chung chung.  
4. **Incorrect:** Viết sai sự thật, sai kiến thức thực tế.

---

### **🚀 GÓC THỰC CHIẾN: CHIA KHÓA HỌC THÀNH QUY TRÌNH BA**

Nếu ngày mai bạn đi làm công ty phần mềm, sếp giao cho bạn phân tích một dự án mới, hãy mở lại quy trình này ra:

1. Gặp khách hàng, nghe họ kể lể \-\> Viết ra Problem Statement (Mô-đun 4).  
2. Gạch chân các Danh từ \-\> Lọc và vẽ **Domain Model** (Mô-đun 4).  
3. Xác định ai dùng hệ thống \-\> Vẽ **Actors** (Mô-đun 5).  
4. Xác định các luồng nghiệp vụ hoàn chỉnh \-\> Vẽ **Use Case Diagram** (Mô-đun 5).  
5. Ngồi gõ kịch bản chi tiết (Happy path \+ Exceptions) \-\> Viết **Use Case Specification** (Mô-đun 6).  
6. Khai thác ngầm các ràng buộc bảo mật/hiệu năng \-\> Liệt kê **Non-Functional Requirements** (Mô-đun 7).  
7. Đọc rà soát lại toàn bộ, sửa lỗi mâu thuẫn \-\> **Validation** (Mô-đun 7).  
8. Giao cho đội Dev bắt đầu code\!

Bạn đã sẵn sàng bước vào bài kiểm tra tổng hợp cuối cùng của khóa học chưa? Nếu có câu hỏi trắc nghiệm nào hóc búa, cứ gửi lên đây nhé\! Chúc bạn chinh phục xuất sắc chứng chỉ này\!

