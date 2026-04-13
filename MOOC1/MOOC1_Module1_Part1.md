1. # **Introduction to generative artificial intelligence  Gen AI** 

- Discriminative AI  (AI phân loại đánh giá )  
- Generative AI  (AI tạo sinh )  
- How to Generative AI work  ?   
- →  Cachs GenAI học và sáng tạo  :    
+ Nguyên Liệu (Data) : GenAI đc ane hàng petabyte nguyên liệu code Java từ khắp nơi trên thế giới  
+ Quy Luật (Patterns) AI không học thuộc mà nó phân tích các quy luật tổ chức code .   
+ Sáng tạo (Generation) khi bạn đưa ra 1 prompt AI sẽ nhào nặn các quy luật để tạo ra code mới 

  \=\> Nguyên Lý bất biến (Consistency vs Variance) Code sinh ra có thể khác nhau nhưng kết quả phải nhất quán  

- GenAI in software Development   
+ GenAI tham gia vào SDLC   
* **Lên kế hoạch (Planning):** Phân tích tài liệu yêu cầu của khách hàng, gợi ý mẫu thiết kế kiến trúc (Design Patterns).  
* **Phát triển (Development):** Tự động sinh ra các đoạn code nhàm chán (như hàm get/set, khởi tạo biến), hoặc gợi ý cách viết thuật toán phức tạp.  
* **Kiểm thử (Testing):** Tự động sinh ra các kịch bản kiểm thử (Test cases) để tìm lỗi.  
* **Triển khai & Bảo trì (Deploy & Maintenance):** Dò tìm bug, tự động viết tài liệu giải thích code.  
+ Mặt tối (Phần này rất hay có trong đề thi)  
* Missing edge(ngoại lệ ) case :  nó thường quên xử lý các ngoại lệ như  :  *1 sản phẩm chỉ còn 1 chiếc 2 người cùng mua thì sao  ?  /  Nếu giỏ hàng trống thì sao? Nếu giá tiền bị làm tròn sai thì sao? Bạn phải là người tự test các trường hợp này.*  
* Copyright Violations   
* Thui chột kỹ năng cá nhân   
- Ethical Consideration (Cân nhắc) and impact   
+ Ethical Implications   
* Data privacy  : vấn đề về dò rỉ dữ liệu thông tin cá nhân   
* Bias : AI mang theo những định kiến của con người   
* Nội dung độc hại & Deepfake : AI có thể bị lợi dụng để viết mã độc (malware) fake new , deepfake  giả giọng nói khuôn mặt   
+ Societal Impact :   
* Job market :  tước đi cơ hội việc làm của các lập trình viên Junior hoặc Tester mới vào nghề.  
* Copyright : Code do AI sinh ra hoàn toàn có thể vô tình "sao chép" nguyên xi một thuật toán đã được đăng ký bản quyền của công ty khác.   
* regulation   : Các cường quốc đang bắt đầu ra luật (như EU AI Act, US AI Bill of Rights) để siết chặt việc phát triển và ứng dụng AI  
- thông điệp của Coursera rất rõ ràng: **Viết code nhanh là tốt, nhưng viết code có trách nhiệm mới làm nên một kỹ sư giỏi.**  
2. **Thuật Ngữ** 

| Pattern  (Khuôn mẫu / Quy luật) | Hiểu đơn giản đó là cấu trúc code , thói quen khi viết code  → Bản châts AI không tự nghĩ ra code từ con số 0  . Mà nó nhận diện với bài toán này thì lập trình viên dùn pattern nào rồi nó viết theo  .  vd : nếu muốn viết code cho rỏ hàng thì nó biết rằng cần dùng 1 list sau đó lưu vào cookie  ..   |
| :---- | :---- |
| **Variance  (Sự biến thiên , đa dạng trong viết code )** | Gen AI là 1 hệ thống xác xuất , cùng 1 vấn đề nhưng có nhiều cách giải quyết khác nhau , nhiều cách triển khai logic khác nhau  → Ví dụ cùng 1 hàm nhưng có nhiều cách viết khác nhau |
| **Consistency   Tính nhất quán về kết quả**  |  Dù code sinh ra có sự Variance (khác nhau về mặt hình thức), nhưng kết quả hoạt động cuối cùng bắt buộc phải Consistent (Nhất quán, không đổi). |
| **SDLC** | **Software Development Life Cycle** |

| Thuật ngữ | Giải thích |
| :---- | :---- |
| **Generative AI (GenAI)** | Trí tuệ nhân tạo tạo sinh, có khả năng sáng tạo ra nội dung mới (text, code, hình ảnh) dựa trên những quy luật đã học từ dữ liệu. |
| **Discriminative AI** | Trí tuệ nhân tạo phân loại, chuyên dùng để đánh giá, phân loại hoặc dự đoán tính chất của dữ liệu cũ (ví dụ: nhận diện ảnh, phát hiện thư rác). |
| **Prompt / Prompt Engineering** | Câu lệnh / Kỹ năng viết câu lệnh rõ ràng, cung cấp đủ ngữ cảnh để điều khiển AI sinh ra đúng đoạn code mong muốn. |
| **Pattern** | Quy luật, cấu trúc mã nguồn hoặc thói quen lập trình mà AI đúc kết được từ hàng tỷ dòng dữ liệu huấn luyện. |
| **Variance** | Sự đa dạng (biến thiên) trong cách AI viết code. Cùng một câu lệnh, AI có thể sinh ra nhiều đoạn code có hình thức và cú pháp khác nhau sau mỗi lần hỏi. |
| **Consistency** | Tính nhất quán về kết quả. Dù code được viết theo cách nào (Variance), chức năng và kết quả trả về của hệ thống phải luôn chính xác và không thay đổi. |
| **SDLC (Software Development Life Cycle)** | Vòng đời phát triển phần mềm, gồm 6 bước chuẩn mực: Phân tích yêu cầu \-\> Thiết kế \-\> Lập trình \-\> Kiểm thử \-\> Triển khai \-\> Bảo trì. |
| **Boilerplate Code** | Những đoạn mã "rập khuôn", lặp đi lặp lại ở nhiều nơi nhưng ít logic phức tạp (ví dụ: khai báo class, hàm getter/setter). Đây là phần AI xử lý rất tốt. |
| **Rule-based Chatbot** | Bot trò chuyện hoạt động hoàn toàn dựa trên các quy tắc logic định sẵn do lập trình viên viết (if-else, switch-case), không tự "chế" ra câu trả lời. |
| **Session Management** | Kỹ thuật quản lý phiên làm việc, giúp hệ thống web "nhớ" được ngữ cảnh hiện tại của người dùng (ví dụ: nhớ người dùng đang hỏi về quốc gia nào, hoặc đang có gì trong giỏ hàng). |
| **Edge Cases** | Các trường hợp ngoại lệ, các tình huống sử dụng hiếm gặp hoặc sai chuẩn mà hệ thống cần phải xử lý nhưng AI thường hay bỏ sót khi tự động sinh code. |
| **Human Oversight** | Sự giám sát của con người. Nguyên tắc bắt buộc kỹ sư phần mềm phải đọc, kiểm chứng và chịu trách nhiệm với những đoạn code do AI tạo ra. |
| **Data Privacy / Anonymization** | Quyền riêng tư dữ liệu / Quá trình ẩn danh hóa dữ liệu (xóa tên, số thẻ...) trước khi đưa vào huấn luyện để tránh AI làm rò rỉ thông tin nhạy cảm. |
| **AI Bias** | Thiên kiến (định kiến) của AI, xảy ra khi AI đưa ra các kết quả thiếu công bằng hoặc phân biệt đối xử do học từ dữ liệu huấn luyện bị lệch lạc. |
| **Intellectual Property (IP)** | Sở hữu trí tuệ. Trong lập trình, đây là nguy cơ vi phạm bản quyền khi AI tự động sinh ra đoạn code sao chép y hệt thuật toán độc quyền của tổ chức khác. |
| **Deepfakes** | Công nghệ sử dụng AI để tạo ra các nội dung giả mạo siêu thực (hình ảnh, video, giọng nói) nhằm mục đích thao túng thông tin hoặc lừa đảo. |
| **Job Displacement** | Sự thay thế việc làm, hiện tượng người lao động (như lập trình viên junior, tester) bị mất vị trí do AI đã tự động hóa các công việc cơ bản của họ. |

