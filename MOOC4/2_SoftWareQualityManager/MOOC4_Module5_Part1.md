# **Achieving Software Quality**

Chào mừng bạn đến với bài học đầu tiên của Mô-đun 5: **Lecture 5-1: Achieving Software Quality (Đạt được Chất lượng Phần mềm)**.

Việc chuyển hướng sang tư duy Đảm bảo chất lượng (SQA) trước là một bước đi cực kỳ chiến lược. Khi điều phối một nhóm phát triển phần mềm gồm nhiều thành viên xây dựng các hệ thống như trang web thương mại điện tử, việc thiết lập các tiêu chuẩn ngay từ đầu sẽ giúp quá trình làm việc trơn tru hơn rất nhiều so với việc chỉ cắm cúi vào gõ code rồi sửa lỗi sau.

Dưới đây là phần bóc tách chi tiết bài giảng của Thầy Kenneth:

### **🎯 Mục Tiêu Bài Học**

1. **Hiểu rõ SQA không chỉ là Kiểm thử (Testing):** Nhận thức được SQA là một quá trình xuyên suốt từ đầu đến cuối dự án.  
2. **Nắm bắt 3 hoạt động cốt lõi của quy trình chất lượng:** Đảm bảo chất lượng (QA), Lập kế hoạch chất lượng (Quality Planning), và Kiểm soát chất lượng (QC).  
3. **Hiểu sức mạnh của Tiêu chuẩn (Standards) và Độ đo (Metrics):** Biết cách áp dụng và đo lường để cải tiến quy trình làm phần mềm.  
4. **Nhận diện 4 chữ P:** Project (Dự án), Process (Quy trình), People (Con người), và Product (Sản phẩm).

---

### **🧠 Nội Dung Chi Tiết (Core Content)**

#### **1\. Định nghĩa chuẩn xác về SQA**

Rất nhiều người lầm tưởng: *"Cứ code xong, đưa cho Tester test thật kỹ là sẽ ra phần mềm chất lượng"*. Thầy Kenneth khẳng định điều này là **SAI**.

* SQA (Software Quality Assurance) bao gồm các quy trình, kỹ thuật và công cụ được áp dụng **xuyên suốt toàn bộ vòng đời phát triển dự án**.  
* Mục đích là để đảm bảo sản phẩm đáp ứng hoặc vượt qua các tiêu chuẩn đã định ra từ trước.

#### **2\. Ba Trụ Cột của Quy Trình Chất Lượng**

Để đạt được chất lượng, tổ chức phải thực hiện theo trình tự 3 bước:

* **Quality Assurance (Đảm bảo chất lượng):** Định nghĩa ra bộ "Luật chung" (Organizational standards) mà tất cả mọi người trong công ty phải tuân theo.  
* **Quality Planning (Lập kế hoạch chất lượng):** Lựa chọn và "cắt cúp" (tailor) các tiêu chuẩn chung đó sao cho phù hợp với đặc thù của một dự án cụ thể.  
* **Quality Control (Kiểm soát chất lượng):** Theo dõi và giám sát để đảm bảo mọi người thực sự làm đúng theo những tiêu chuẩn đã thống nhất trong suốt quá trình chạy dự án.

#### **3\. Nguyên lý Chi phí Sửa lỗi (Cost of Defect)**

Đây là biểu đồ kinh điển trong kỹ nghệ phần mềm.

* Nếu bạn phát hiện và sửa một lỗi sai ngay từ khâu Lấy yêu cầu hoặc Thiết kế, chi phí cực kỳ rẻ (chỉ tốn vài phút sửa tài liệu).  
* Nhưng nếu cái lỗi đó lọt qua được khâu Code, lọt qua khâu Test, và đến tay Khách hàng (Production) mới phát nổ, chi phí để sửa nó sẽ **đắt gấp hàng chục đến hàng trăm lần** (bao gồm việc dừng hệ thống, sửa code, đền bù thiệt hại, mất uy tín...). SQA sinh ra để phát hiện lỗi càng sớm càng tốt.

#### **4\. Công thức "4 chữ P" để Đạt được Chất lượng**

Chất lượng không tự sinh ra, nó là kết quả của sự kết hợp 4 yếu tố:

* **Project (Dự án):** Cần một bản kế hoạch dự án tốt ngay từ vạch xuất phát và phải được giám sát liên tục.  
* **Process (Quy trình):** Cần những quy trình làm việc chuẩn mực (ví dụ: quy tắc quản lý code chung) để mọi thành viên trong nhóm có thể phối hợp nhịp nhàng.  
* **People (Con người):** Các thành viên cần được đào tạo, hướng dẫn và có kỹ năng tốt.  
* **Product (Sản phẩm):** Thực hiện kiểm thử (testing) kỹ lưỡng ở khâu cuối để đảm bảo đầu ra sạch lỗi.

#### **5\. Đo lường và Cải tiến Liên tục**

* Bạn phải đặt ra các **Thuộc tính chất lượng (Quality Attributes)** ngay từ đầu làm mục tiêu thiết kế.  
* Trong quá trình làm, phải liên tục **Đo lường (Measure)** xem sản phẩm có đang đi đúng hướng không.  
* Cuối cùng, những tiêu chuẩn hay công thức nào thành công ở dự án này sẽ được **Tái sử dụng (Reuse)** để làm nền tảng phát triển cho các dự án trong tương lai.

---

