# **State Machine Diagram**

 **(Sơ đồ Máy trạng thái)**

Nếu bạn đã từng gặp lỗi code kiểu như: *"Tại sao người dùng chưa đăng nhập mà vẫn bấm được nút thanh toán?"* hay *"Tại sao tài khoản ngân hàng âm tiền rồi mà vẫn rút được?"*, thì bài học này chính là "thuốc giải" cho những lỗi logic đau đầu đó.

Thầy Kenneth sẽ hướng dẫn bạn cách vẽ ra "vòng đời" của một đối tượng, kiểm soát chặt chẽ từng trạng thái của nó từ lúc sinh ra đến lúc chết đi.

Dưới đây là phần bóc tách chi tiết:

### **🎯 Mục Tiêu Bài Học**

1. Hiểu bản chất của State Machine Diagram: Mô tả vòng đời và hành vi bên trong của **một đối tượng duy nhất (a single object)**.  
2. Phân biệt được các khái niệm: **State (Trạng thái)** có tính kéo dài, trong khi **Transition (Chuyển đổi)** diễn ra ngay tức khắc.  
3. Nắm vững cú pháp vẽ sơ đồ: Cách khai báo Trạng thái ban đầu, Trạng thái kết thúc, Sự kiện (Event), Điều kiện chắn (Guard) và Hành động (Action/Activity).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Trạng thái (State) là gì?**

* **Định nghĩa:** Là một khoảng thời gian trong vòng đời của đối tượng khi nó thỏa mãn một điều kiện nào đó.  
  * *Ví dụ Tài khoản Ngân hàng:* Trạng thái InCredit (Còn tiền), Overdrawn (Thấu chi/Âm tiền), Frozen (Bị đóng băng), Closed (Đã đóng).  
* **Đặc tính cốt lõi:** Trạng thái **có thời lượng (duration)**. Đối tượng có thể nằm "ngâm" ở một trạng thái trong 1 giây hoặc 10 năm (như tài khoản ngân hàng).  
* **Cách xác định trạng thái:** Thường dựa vào giá trị của thuộc tính (VD: balance \> 0 thì ở trạng thái InCredit) hoặc dựa vào liên kết (VD: Đĩa phim có link tới khách hàng \-\> Trạng thái Rented/Đã cho thuê).

#### **2\. Các Trạng thái Đặc biệt (Special States)**

* **Initial State (Trạng thái bắt đầu):** Ký hiệu bằng một **chấm đen đặc**. Nó đại diện cho khoảnh khắc đối tượng được tạo ra bằng hàm Khởi tạo (Constructor).  
* **Final State (Trạng thái kết thúc):** Ký hiệu bằng một **chấm đen có vòng tròn bao quanh** (giống hồng tâm). Nó đại diện cho lúc đối tượng bị xóa sổ (Destroyed/Deleted).  
* *(Lưu ý: Nếu sơ đồ không có Final State, nghĩa là đối tượng này chạy vòng lặp vô hạn).*

#### **3\. Chuyển đổi (Transition) và Tính Tất định (Deterministic)**

* **Định nghĩa:** Sự nhảy vọt từ trạng thái này sang trạng thái khác.  
* **Đặc tính cốt lõi:** Transition diễn ra **ngay lập tức (zero time)** và **không thể bị ngắt quãng**.  
* **Tại sao phải thiết kế như vậy?** Để đảm bảo tính *Tất định (Deterministic)*. Tại một thời điểm bất kỳ (kể cả thời điểm đang chuyển đổi), đối tượng CHỈ ĐƯỢC PHÉP nằm ở 1 trạng thái duy nhất. Không được phép có chuyện "Nửa nạc nửa mỡ" (Vừa ở trạng thái Còn tiền, vừa ở trạng thái Âm tiền).

#### **4\. Cú pháp của một Transition (Cực kỳ quan trọng)**

| Cấu trúc hoàn chỉnh của một mũi tên chuyển đổi (Transition) luôn là: `Sự kiện [Điều kiện chắn] / Hành động hệ quả` *(Tiếng Anh: `Event [Guard] / Effect`)* Để dễ nhớ, bạn hãy dịch nó ra thành câu nói tiếng Việt theo công thức: 👉 "KHI (Sự kiện) xảy ra, NẾU (Điều kiện) thỏa mãn, THÌ hệ thống tự động (Hành động)."  |
| :---- |

Một mũi tên chuyển đổi hoàn chỉnh có cấu trúc như sau:

**Event\_Trigger \[Guard\_Condition\] / Effect\_List**

* **Event Trigger (Sự kiện kích hoạt):** Cái gì gây ra sự chuyển đổi?  
  * *Call Event:* Ai đó gọi hàm (VD: Gọi hàm withdraw()).  
  * *Change Event:* Một điều kiện tự động đạt ngưỡng (VD: when balance \< 0).  
  * *Time Event:* Hết thời gian (VD: after 3 months).  
* **Guard Condition (Điều kiện chắn \- Nằm trong ngoặc vuông \[ \]):** Sự kiện xảy ra rồi, nhưng CÓ ĐƯỢC PHÉP chuyển trạng thái không? (VD: Khách bấm rút tiền withdraw(), nhưng phải thỏa mãn điều kiện \[balance \>= amount\] thì mới cho rút).  
* **Effect List (Hệ quả \- Nằm sau dấu /):** Hành động tự động phải làm khi chuyển đổi (VD: / updateDatabase()).

#### **5\. Hành vi bên trong Trạng thái (Entry / Exit / Do)**

Khi đối tượng đang nằm "ngâm" trong một trạng thái, nó không hẳn là đứng im. Bạn có thể định nghĩa 3 loại hành vi:

* **Entry activity:** Việc phải làm ngay khoảnh khắc bước chân vào trạng thái. (VD: Vào trạng thái "Nhập mật khẩu" \-\> entry / set dấu sao (\*) cho ký tự).  
* **Exit activity:** Việc phải làm ngay trước khi rời khỏi trạng thái. (VD: Thoát khỏi "Nhập mật khẩu" \-\> exit / hiển thị lại chữ bình thường).  
* **Do activity:** Việc làm lặp đi lặp lại hoặc có thể bị ngắt quãng trong lúc đang ở trạng thái đó (VD: do / chớp tắt con trỏ chuột chờ nhập liệu).

---

