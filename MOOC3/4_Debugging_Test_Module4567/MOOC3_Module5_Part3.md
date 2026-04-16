# **Basis Path Testing**

Chào mừng bạn đến với kỹ thuật "đỉnh cao" nhất của Kiểm thử Hộp trắng: **Basis Path Testing (Kiểm thử Đường dẫn Cơ sở)**\!

Đây là lúc Toán học và Lập trình giao thoa. Kỹ thuật này sinh ra để trả lời một câu hỏi vô cùng đau đầu của các lập trình viên: *"Hàm này có rất nhiều lệnh if/else rẽ nhánh chằng chịt, vậy tôi phải viết chính xác bao nhiêu Test Case thì mới dám vỗ ngực tự xưng là đã test 100%?"*.

Dưới đây là phần bóc tách chi tiết Mục tiêu và Nội dung cốt lõi:

### **🎯 Mục Tiêu Bài Học**

Bạn sẽ học được quy trình 4 bước để áp dụng Basis Path Testing:

1. Đọc code và vẽ ra **Flow Graph (Đồ thị luồng)**.  
2. Dùng toán học tính toán **Cyclomatic Complexity (Độ phức tạp Cyclomatic)**.  
3. Từ con số tính được, vạch ra các **Independent Paths (Đường đi độc lập)**.  
4. Từ các đường đi đó, tạo ra các Test Cases tương ứng.

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **Bước 1: Vẽ Flow Graph (Đồ thị luồng)**

Thay vì nhìn vào những dòng chữ khô khan, bạn biến code thành một bức tranh gồm các Node (hình tròn) và Edge (mũi tên).

* **Code chạy tuần tự** (A \= 1; B \= 2;): Trở thành các Node nối tiếp nhau trên một đường thẳng.  
* **Câu lệnh rẽ nhánh** (if/else, switch): Trở thành một Node có 2 (hoặc nhiều) mũi tên túa ra các hướng khác nhau. Đây gọi là **Predicate Node (Node vị từ / Node ra quyết định)**.  
* **Vòng lặp** (while, do-while): Trở thành một Node có mũi tên chạy một vòng quay ngược trở lại chính nó.

*(Mẹo của Thầy Kenneth: Hãy gộp các lệnh chạy tuần tự liền nhau thành 1 Node duy nhất để làm cho đồ thị đơn giản và dễ nhìn hơn, nhớ ghi lại bảng mapping để không quên Node đó chứa những dòng code nào).*

#### **Bước 2: Tính toán Cyclomatic Complexity  V(G)** 

Độ phức tạp Cyclomatic là một con số phép thuật. Nó cho bạn biết **GIỚI HẠN TRÊN** của số lượng Test Case bạn cần viết. (Ví dụ: Tính ra V(G) \= 4, nghĩa là bạn cần *tối đa* 4 bài test là sẽ phủ kín đoạn code này).

Có 3 cách để tính  V(G) , bạn dùng cách nào cũng ra cùng một đáp án:

* **Cách 1 (Đếm số Vùng/Regions):** Nhìn vào đồ thị, đếm số "vùng kín" được bao bọc bởi các đường kẻ, CỘNG THÊM 1 vùng không gian mở bên ngoài đồ thị.  
* **Cách 2 (Dùng công thức Toán):** V(G) \= E \- N \+ 2\. Trong đó E là số mũi tên (Edges), N là số vòng tròn (Nodes).  
* **Cách 3 (Nhanh nhất \- Đếm Node rẽ nhánh):** V(G) \= P \+ 1\. Trong đó  P  là số lượng **Predicate Nodes** (những cái vòng tròn có từ 2 mũi tên đi ra trở lên). Cứ lấy số nút rẽ nhánh cộng thêm 1 là xong\!

#### **Bước 3: Vạch ra các "Đường đi Độc lập" (Independent Paths)**

* Định nghĩa: Một con đường được gọi là "Độc lập" nếu nó **đi qua ít nhất MỘT CẠNH (Edge) mới** mà các con đường trước đó chưa từng đi qua.  
* Bạn sẽ cầm bút chì, vẽ dọc theo đồ thị từ đỉnh xuống đáy sao cho tạo ra đủ các đường đi khác nhau (số lượng đường đi không được vượt quá con số  V(G)  vừa tính ở trên).  
* Tập hợp các con đường này tạo thành một **Basis Set (Tập cơ sở)**. *(Lưu ý: Basis Set không phải là duy nhất, 2 lập trình viên có thể vạch ra 2 tập con đường khác nhau nhưng đều đúng).*

#### **Bước 4: Chuyển thành Test Case**

Khi đã có danh sách các đường đi (Ví dụ: Đường 1 là đi qua Node 1-2-3-4; Đường 2 là 1-2-5-4...), bạn sẽ lấy tài liệu code ra, dùng *Backward Reasoning* để tính xem: *"À, muốn đi vào nhánh số 3 thì điều kiện if phải là True, vậy Input x phải lớn hơn 0..."*. Từ đó chốt hạ được Dữ liệu đầu vào cho từng bài Test.

---

### **💡 Lưu ý Thực chiến (The "Real-World" Catch)**

Thầy Kenneth có một dặn dò cực kỳ đắt giá vào cuối video: **Đừng rảnh rỗi mà đi vẽ Flow Graph cho TẤT CẢ các hàm trong hệ thống\!**

Vẽ đồ thị và tính toán rất tốn thời gian. Bạn chỉ nên lôi kỹ năng Basis Path Testing này ra áp dụng cho những **Critical Components (Các hàm cốt lõi, quan trọng nhất)** hoặc những đoạn code có quá nhiều lệnh if/else lồng nhau (Logically complicated). Đối với những hàm đơn giản chỉ chạy tuần tự từ trên xuống dưới, cứ test bình thường là đủ\!