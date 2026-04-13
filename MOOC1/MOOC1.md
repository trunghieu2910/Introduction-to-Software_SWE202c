**MOOC 1  :**

### \---

**PHẦN 1: AI AND BUILDING SOFTWARE (Kỹ năng Lập trình \& Kiến trúc)**

Phần này tập trung vào việc dùng **Generative AI (AI tạo sinh)** như một "trợ lý đắc lực" để tăng tốc độ phát triển phần mềm và thiết kế kiến trúc chuẩn mực.

* **Tư duy cốt lõi:** AI là công cụ khuếch đại năng lực (Assistant), không phải người thay thế (Replacement). Bạn vẫn là người làm chủ ngữ cảnh và quyết định cuối cùng.
* **Làm chủ "Bộ 3 Công cụ":**

  * **ChatGPT:** Người cố vấn (Mentor) giúp lên ý tưởng kiến trúc (như mô hình MVC), viết mã giả (pseudocode) và giải thích logic.
  * **GitHub Copilot:** Đồng nghiệp hỗ trợ gõ code siêu tốc ngay trong IDE (IntelliJ), gợi ý code theo ngữ cảnh thời gian thực.
  * **Amazon Q Developer:** "Kiểm toán viên" giúp giải thích các đoạn code phức tạp, tự động tìm lỗi (bug) và tối ưu hóa hiệu năng.
* **Kỹ năng Prompting (Ra lệnh cho AI):** Đặt câu hỏi cụ thể, yêu cầu AI cung cấp ví dụ, và sử dụng kỹ thuật "Iterative prompting" (ép AI tinh chỉnh code liên tục cho đến khi tối ưu nhất).
* **Thiết kế \& Tối ưu Hệ thống:** Dùng AI để phác thảo cấu trúc thư mục, thiết lập luồng CI/CD, và lên phương án chịu tải (Load Balancer, Caching) cho các hệ thống lớn.
* **Nguyên tắc sống còn:** Luôn **Verify (Kiểm chứng)** mã nguồn AI tạo ra để tránh "ảo giác" (hallucinations) và các lỗ hổng bảo mật.

### \---

**PHẦN 2: AI AND DIGITAL TRANSFORMATION - Decision-Making Models (Tư duy Trí tuệ nhân tạo)**

Nếu Phần 1 là dùng AI để *viết phần mềm*, thì Phần 2 là dạy bạn cách *nhúng AI vào phần mềm* để nó tự động ra quyết định thay con người.

* **Sự dịch chuyển tư duy:** Thay vì viết code if-else cứng nhắc (Lập trình truyền thống), bạn dùng **Machine Learning (Học máy)**. Bạn nạp dữ liệu lịch sử vào, máy tính tự tìm ra quy luật và áp dụng cho tương lai.
* **Thuật toán 1: Decision Trees (Cây quyết định)**

  * *Cách hoạt động:* Đặt ra một chuỗi câu hỏi Có/Không (từ Nút Gốc xuống Nút Lá) để phân loại dữ liệu (VD: Khách có mua hàng không?).
  * *Điểm yếu:* Dễ bị **Overfitting (Học vẹt)** — quá cứng nhắc với dữ liệu cũ và đoán sai dữ liệu mới.
* **Thuật toán 2: Random Forests (Rừng ngẫu nhiên)**

  * *Cách hoạt động:* Giải quyết điểm yếu của Cây quyết định bằng cách tạo ra hàng trăm cái cây độc lập. Mỗi cây chỉ được học một phần dữ liệu ngẫu nhiên (Bagging \& Feature Randomness).
  * *Ra quyết định:* Dùng "Tri thức đám đông". Gom kết quả của tất cả các cây lại và **Bỏ phiếu theo số đông (Majority Vote)** hoặc Tính trung bình.
* **Thuật toán 3: Neural Networks (Mạng Nơ-ron - Deep Learning)**

  * *Cách hoạt động:* Bắt chước não bộ con người, chuyên xử lý dữ liệu phức tạp như hình ảnh, giọng nói.
  * *Cấu trúc 3 lớp:* Lớp đầu vào (Input) -> Các lớp ẩn (Hidden Layers) -> Lớp đầu ra (Output).
  * *Cơ chế toán học:* Các nơ-ron nhận dữ liệu, nhân với **Trọng số (Weights)** để đánh giá độ quan trọng, tính tổng, rồi đưa qua **Hàm kích hoạt (Activation Function - như Sigmoid)** để ra kết quả dạng Xác suất (%).
  * *Học hỏi:* AI tự động đối chiếu kết quả, nếu sai nó sẽ tự động điều chỉnh lại Trọng số (Error Correction) để thông minh hơn.

\---

**Tóm lại:** Khóa học đã trang bị cho bạn đủ "cả văn lẫn võ". Bạn đã biết cách dùng AI để viết code nhanh hơn, sạch hơn; đồng thời hiểu rõ bản chất của các thuật toán ML để sau này có thể tự tin tích hợp các tính năng thông minh (như gợi ý sản phẩm, tìm kiếm bằng hình ảnh) vào nền tảng thương mại điện tử thời trang của mình.

Bạn đánh giá phần kiến thức nào trong lộ trình vừa qua sẽ là "vũ khí" hữu ích nhất để áp dụng ngay vào kỳ làm đồ án PRJ301 sắp tới?

