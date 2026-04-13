## **Cây quyết định (Decision Trees)**

### **Giới thiệu**

Cây quyết định là một công cụ học máy giúp phân loại dữ liệu và dự đoán kết quả bằng cách chia nhỏ quá trình ra quyết định thành một chuỗi các câu hỏi đơn giản. Hãy tưởng tượng bạn đang cố gắng dự đoán liệu một khách hàng có mua sản phẩm hay không dựa trên hành vi trực tuyến của họ.

Ví dụ, cây quyết định có thể bắt đầu bằng câu hỏi: “Khách hàng có xem trang sản phẩm không?” Tùy vào câu trả lời, nó sẽ chuyển sang câu hỏi tiếp theo, như: “Họ có thêm sản phẩm vào giỏ hàng không?” Mỗi câu hỏi giúp thu hẹp các khả năng và dẫn đến kết quả cuối cùng, như “có khả năng mua” hoặc “không có khả năng mua”.

Trong phần này, bạn sẽ tìm hiểu cây quyết định là gì, cách hoạt động của chúng và cách sử dụng để dự đoán. Cuối cùng, bạn sẽ có thể giải thích và tự tạo một cây quyết định đơn giản.

---

## **Tree là gì?**

Tree (cây) là một cấu trúc dữ liệu trong khoa học máy tính dùng để tổ chức dữ liệu theo dạng phân cấp. Nó gồm các điểm gọi là **node (nút)**.

Trong khoa học máy tính, cây giống như một cây bị lật ngược:

* Gốc (root) ở trên  
* Lá (leaf) ở dưới

Việc duyệt cây luôn bắt đầu từ **root node** (nút gốc).

### **Các thành phần của cây**

* **Root node (Level 0):** Nút trên cùng, điểm bắt đầu của cây  
* **Child nodes (Level 1):** Các nút con nằm dưới một nút khác  
* **Parent node:** Nút có chứa các nút con  
* **Leaf nodes (Level 2):** Nút lá ở cuối, không có con (kết quả cuối)  
* **Internal nodes:** Nút trung gian, có cả cha và con

### **Lưu ý**

Trong Java, level (cấp) bắt đầu từ 0\. Level thể hiện độ sâu của cây, tức số bước từ root đến một node.

---

## **Cây quyết định là gì?**

Cây quyết định là một loại cây đặc biệt dùng trong học máy để đưa ra quyết định dựa trên dữ liệu đầu vào.

* **Dữ liệu đầu vào (input data):** thông tin để mô hình học hoặc dự đoán  
* Cây quyết định mô phỏng cách con người ra quyết định bằng cách chia dữ liệu theo điều kiện

### **Thành phần trong cây quyết định**

* **Internal nodes:** câu hỏi/điều kiện  
* **Branches:** các câu trả lời  
* **Leaf nodes:** kết quả cuối cùng

---

## **Ví dụ: Dự đoán Pass/Fail**

Điều kiện:

* Học \> 3 giờ  
* Đi học \> 75%

👉 Nếu thỏa cả hai → **Pass**  
👉 Ngược lại → **Fail**

### **Feature (đặc trưng)**

* Study Hours  
* Attendance

Giá trị của chúng gọi là **feature value**

---

## **Mục tiêu của cây quyết định**

Chia dữ liệu thành các tập con (**subsets**) dựa trên feature cho đến khi đưa ra quyết định rõ ràng.

---

## **Cách hoạt động của cây (ví dụ)**

* **Root:** Study Hours \> 3?  
  * No → Fail  
  * Yes → kiểm tra tiếp  
* **Internal node:** Attendance \> 75%?  
  * Yes → Pass  
  * No → Fail

---

## **Tree vs Decision Tree**

| Khía cạnh | Tree | Decision Tree |
| ----- | ----- | ----- |
| Mục đích | Tổ chức dữ liệu | Ra quyết định |
| Node | Đại diện dữ liệu | Đại diện câu hỏi |
| Cấu trúc | Quan hệ cha-con | Chuỗi câu hỏi Yes/No |
| Ví dụ | Cây thư mục | Dự đoán Pass/Fail |

---

## **Độ phức tạp của cây quyết định**

Ví dụ nâng cao: thêm

* Assignment Marks

Điều kiện Pass:

* Study \> 3  
* Attendance \> 75%  
* Assignment \> 50%

Nếu không học \> 3 giờ:

* Có muốn học lại không?  
  * Không → Fail  
  * Có → kiểm tra Assignment

---

## **Duyệt cây**

* Luôn đi từ root → leaf  
* Không thể quay lại (không backtracking)

### **Ưu điểm của hướng một chiều**

1. Luôn có kết quả  
2. Bao phủ mọi trường hợp  
3. Không bị lặp vô hạn

---

## **Số node con trong cây**

### **1\. Binary tree**

* 2 nhánh (Yes/No)

### **2\. Multiway tree**

* Nhiều nhánh (ví dụ Weather: Sunny, Rainy, Cloudy)

### **3\. Continuous feature**

* Giá trị liên tục (Age: 1–100)

### **Discretized feature**

Chia thành nhóm:

* Child  
* Young adult  
* Adult  
* Veteran

---

## **Ưu và nhược điểm**

### **✅ Ưu điểm**

* Dễ hiểu  
* Dùng được nhiều loại dữ liệu  
* Không cần giả định phân phối

### **❌ Nhược điểm**

* Overfitting (quá khớp)  
* Không ổn định  
* Bias với feature nhiều giá trị

---

## **Ứng dụng**

* Y tế: dự đoán bệnh  
* Tài chính: xét duyệt vay  
* Giáo dục: dự đoán kết quả học tập

---

## **Kết luận**

Cây quyết định giúp đơn giản hóa việc ra quyết định bằng cách chia nhỏ thành các câu hỏi.

Nó là cầu nối giữa:  
👉 tư duy con người  
👉 trí tuệ nhân tạo

---

Nếu bạn muốn, mình có thể:

* Vẽ lại cây decision tree cho bạn dễ hiểu 🌳  
* Hoặc viết code Java/Python để bạn áp dụng luôn

