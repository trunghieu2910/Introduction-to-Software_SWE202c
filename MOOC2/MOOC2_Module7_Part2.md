# **Validate System Requirements**

Chúc mừng bạn đã đi đến bài giảng "chốt sổ" của toàn bộ quy trình Thu thập Yêu cầu\!

Đến lúc này, chúng ta đã gom đủ 3 trụ cột (Domain Model, Use Case Model, và Non-Functional Requirements) để đóng thành một cuốn Đặc tả Yêu cầu Hệ thống (SRS) dày cộp. Nhưng khoan đem đi code vội\! Ví dụ như khi thiết kế một trang web thương mại điện tử bán quần áo thời trang, dù bạn áp dụng chuẩn mô hình MVC và giao diện mượt mà đến đâu, nếu cái bản thiết kế ban đầu bị sai logic thì code ra cũng đành đập đi xây lại.

Đó là lý do Giáo sư Kenneth dành trọn Bài 7-2 này để hướng dẫn nghệ thuật **"Bắt bug trên giấy" (Validate System Requirements)** trước khi nghiệm thu với khách hàng (Acceptance Test).

Dưới đây là 4 lỗi "ngớ ngẩn" kinh điển nhất mà các kỹ sư phần mềm thường mắc phải khi viết tài liệu:

### **🎯 4 Lỗi Sai Phổ Biến Khi Viết Đặc Tả (Validation Errors)**

**1\. Incomplete (Thiếu sót / Bỏ quên vùng biên)**

* **Bản chất:** Bạn nghĩ ra kịch bản chạy chính, nhưng quên mất xử lý các trường hợp ngoại lệ hoặc các ranh giới mép (Edge cases).  
* *Ví dụ của Thầy (Đồng hồ SatWatch):* Bỏ quên trường hợp người dùng đứng ngay vạch kẻ giới tuyến giữa 2 múi giờ. Nếu không quy định rõ, cái đồng hồ sẽ nhảy loạn xạ giữa giờ Việt Nam và giờ Thái Lan liên tục mỗi giây\!  
* *Cách sửa:* Bổ sung luật: "Đồng hồ chỉ được phép đổi múi giờ tối đa 5 phút 1 lần".

**2\. Inconsistent (Mâu thuẫn / "Tự vả")**

* **Bản chất:** Yêu cầu số 1 nói một đằng, yêu cầu số 10 lại nói một nẻo. Lập trình viên đọc xong không biết đường nào mà lần.  
* *Ví dụ của Thầy:* Câu trên ghi "Phần mềm hoàn hảo, không bao giờ cần cập nhật". Câu dưới lại ghi "Phần mềm hỗ trợ cập nhật dễ dàng qua cổng USB".  
* *Cách sửa:* Bắt buộc phải họp lại với khách hàng để xóa bỏ hoặc sửa đổi 1 trong 2 câu.

**3\. Unclear (Mơ hồ / Tối nghĩa)**

* **Bản chất:** Dùng những từ ngữ chung chung khiến mỗi người đọc lại hiểu theo một hướng khác nhau.  
* *Ví dụ của Thầy:* "Đồng hồ phải hỗ trợ các múi giờ". Viết như vậy rất mập mờ, lập trình viên sẽ thắc mắc: "Thế có cần hỗ trợ Giờ Mùa Hè (Daylight Saving Time) không?".  
* *Cách sửa:* Làm rõ định nghĩa (Refine & Clarify).

**4\. Incorrect (Sai sự thật / Sai thực tế đời sống)**

* **Bản chất:** Yêu cầu đi ngược lại với chân lý khoa học hoặc thực tế kinh doanh ngoài đời.  
* *Ví dụ của Thầy:* "Đồng hồ hỗ trợ đúng 24 múi giờ". Sai bét\! Thực tế trên thế giới hiện nay có tới hơn 38 múi giờ (do có những vùng bù trừ 30 phút hoặc 45 phút).  
* *Cách sửa:* Sửa lại cho đúng với kiến thức thực tế (Domain Knowledge).

---

