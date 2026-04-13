**II. GenAI programming tool**

1. # **Nền tảng cốt lõi**

- AI hỗ trợ cho ngôn ngữ Java   
+ Boilerplate Code  (Code dập khuôn) 

| Trong Java, việc tạo ra các class đối tượng (POJO) rất mất thời gian vì phải gõ đi gõ lại các hàm constructor, getter, setter, toString(). Cách Alex làm: Thay vì tự gõ, anh ấy ra lệnh (Prompt): *"Create a basic item class with ID and name"*. Kết quả: Amazon Q tự động sinh ra class `Item` chuẩn chỉnh với đầy đủ các hàm lặt vặt đó. Áp dụng: Khi bạn làm website bán áo quần, bạn chỉ cần ra lệnh: *"Tạo class Product cho Java với các thuộc tính: id, name, price, size, color, kèm theo getter/setter"*, AI sẽ làm xong trong 2 giây. |
| :---- |

+ Tư duy “Chia để trị ” khi viết prompt 

| Alex không bắt AI viết toàn bộ phần mềm bằng một câu lệnh dài ngoằng. Anh ấy chia nhỏ ra từng bước rất khoa học: Bước 1: Khởi tạo `Main class` để chạy thử (In ra lời chào). Bước 2: Tạo `Item class` (Cấu trúc dữ liệu đơn lẻ). Bước 3: Tạo `ItemManager class` (Xử lý logic nghiệp vụ \- CRUD). Ở bước này, Prompt của Alex rất rõ ràng: *"Thêm chức năng... thêm, sửa, xóa các item từ một ArrayList*". Nhờ việc chỉ định rõ cấu trúc dữ liệu là `ArrayList`, AI viết code chuẩn xác hơn hẳn. Bước 4: Để AI tự động gợi ý code test nghiệm thu trong hàm `main`  |
| :---- |


- Cách viết prompt( 6 kĩ thuật và  5 nguyên tắc khi Viết prompt )   
+ 6 Kỹ thuật khi viết prompt   
* Instruction-based prompt   
* Zero-Shot prompting  
* Few-Shot Prompting  
* Chain-of-throught Prompting  
* Role-based Prompting  
* Contextual Prompting

+ 5 nguyên tắc  
* Rõ ràng cụ thể   
* Cung cấp ngữ cảnh   
* Dùng ví dụ   
* Thử nghiệm & lặp lại    
* Ngắn gọn    
- Chi tiết Về 6 kĩ thuật  Prompt Engineering

| Phân loại | Bản chất | Ví dụ |
| :---- | :---- | :---- |
| **Instruction-based Prompts (Chỉ thị trực tiếp)** | Ra lệnh rõ ràng, thẳng thắn, không vòng vo. Đi thẳng vào mục tiêu cụ thể cần thực hiện. | *"Viết một phương thức Java sử dụng thư viện java.util.Collections để sắp xếp một danh sách các sản phẩm theo giá tăng dần."* |
| **Zero-Shot Prompting (Không cần ví dụ)** | Yêu cầu AI làm việc ngay lập tức mà không cần cung cấp trước đoạn code mẫu nào. Phù hợp cho các tác vụ cơ bản và phổ thông. | *"Tạo một class Java có tên là Product với các thuộc tính cơ bản."* |
| **Few-Shot Prompting (Cung cấp mẫu)** | Đưa ra 1-2 ví dụ mẫu để ép AI sinh ra code theo đúng định dạng, chuẩn mực (coding convention) mà dự án đang dùng. | *"Đây là cách tôi viết class User: public class User { private int id; private String username; }. Dựa theo định dạng này, hãy viết class Order."* |
| **Chain-of-Thought Prompting (Chuỗi tư duy)** | Yêu cầu AI suy luận và giải quyết vấn đề logic phức tạp theo từng bước một thay vì in ra kết quả cuối cùng ngay lập tức. | *"Để tính tổng tiền, bước 1: Lấy giá nhân số lượng. Bước 2: Trừ % giảm giá. Bước 3: Cộng 10% VAT. Hãy viết hàm Java thực hiện logic từng bước này."* |
| **Role-based Prompting (Nhập vai)** | Ép AI đóng vai một chuyên gia cụ thể (giáo viên, senior dev...) để thay đổi giọng văn, mức độ chuyên sâu và góc nhìn đánh giá. | *"Hãy đóng vai một Senior Software Engineer 10 năm kinh nghiệm. Đánh giá đoạn code SQL này và chỉ ra các rủi ro bảo mật tiềm ẩn."* |
| **Contextual Prompts (Cung cấp ngữ cảnh)** | Đưa ra bức tranh toàn cảnh (ngành nghề, quy mô dự án) để AI hiểu rõ hệ thống và đưa ra giải pháp sát với thực tế nhất. | *"Tôi đang xây website e-commerce bán quần áo bằng Spring Boot. Cần thiết kế bảng Database quản lý sản phẩm có nhiều size và màu sắc. Hãy gợi ý thiết kế."* |


- Chi tiết về 5 Nguyên tắc vàng


| Quy tắc | Bản chất | Ví dụ |
| :---- | :---- | :---- |
| **Rõ ràng & Cụ thể (Be clear and specific)** | Đưa ra chỉ thị chính xác về những gì bạn muốn, không dùng từ ngữ mơ hồ. AI không thể đọc được suy nghĩ của bạn, bạn mô tả càng chi tiết thì code sinh ra càng chuẩn. | *"Thay vì nói: Viết hàm tính tiền. Hãy nói: Viết một phương thức Java trả về kiểu double để tính tổng tiền của một danh sách chứa các đối tượng Item."* |
| **Cung cấp ngữ cảnh (Provide context)** | Cung cấp thông tin nền tảng về dự án, công nghệ đang dùng hoặc mục đích sử dụng. Nhờ đó, AI sẽ điều chỉnh kiến trúc và thư viện cho khớp với dự án thực tế của bạn. | *"Thay vì nói: Tạo bảng lưu sản phẩm. Hãy nói: Tôi đang làm dự án e-commerce bán quần áo bằng Spring Boot và MySQL, hãy gợi ý cấu trúc bảng lưu thông tin sản phẩm."* |
| **Dùng ví dụ (Use examples)** | Đưa ra các mẫu đầu vào (input) và đầu ra (output) mong muốn. Đây là cách nhanh nhất và hiệu quả nhất để ép AI xuất ra đúng định dạng bạn cần. | *"Tôi muốn tạo mã đơn hàng tự động theo định dạng ví dụ sau: ORD-2026-001. Hãy viết hàm Java thực hiện việc này."* |
| **Thử nghiệm & Lặp lại (Experiment and iterate)** | Không nên mong đợi AI viết đúng 100% ngay lần đầu. Hãy xem câu trả lời đầu tiên là bản nháp, sau đó liên tục phản hồi để AI sửa lỗi hoặc tối ưu hóa. | *"Đoạn code bạn vừa viết chạy đúng logic nhưng hơi dài. Hãy tối ưu lại bằng cách sử dụng Stream API của Java 8 cho ngắn gọn và hiện đại hơn."* |
| **Ngắn gọn (Be concise)** | Giữ cho câu lệnh tập trung vào mục tiêu chính, loại bỏ các câu giao tiếp lịch sự thừa thãi hoặc thông tin râu ria làm AI bị phân tâm. | *"Thay vì nói: Chào AI, hôm nay tôi mệt quá, bạn giúp tôi sửa lỗi này nhé. Hãy nói: Hãy tìm và sửa lỗi NullPointerException trong đoạn code Java dưới đây."* |

     

2. #  **Vũ khí chủ lực Amazon Q develope**

| Dưới đây là 3 sức mạnh thực chiến của công cụ này mà bạn cần ghi nhớ để chuẩn bị cho phần thực hành sắp tới: 1\. Xử lý "Boilerplate Code" siêu tốc Thay vì phải tự tay gõ từng ký tự cho public static void main hay khởi tạo các biến lặp đi lặp lại, bạn chỉ cần gõ vài từ khóa đầu tiên hoặc viết một câu Prompt ngắn. Q Developer sẽ tự động sinh ra khung chương trình. Khi bạn cần chương trình nhận dữ liệu đầu vào động (Dynamic input), AI sẽ ngay lập tức hiểu ngữ cảnh và gợi ý khởi tạo đối tượng Scanner. 2\. Nhắc nhở Best Practices (Thực hành chuẩn) Đây là tính năng biến Q Developer thành một "người hướng dẫn" chứ không chỉ là công cụ tự động điền (autocomplete): Quản lý tài nguyên: Nếu bạn dùng Scanner để đọc dữ liệu nhưng quên đóng lại ở cuối hàm, AI sẽ nhắc bạn thêm dòng scanner.close() để tránh rò rỉ bộ nhớ (memory leak). Tự động Import: Nếu bạn gọi class Scanner mà quên khai báo thư viện, công cụ sẽ tự động thêm dòng import java.util.Scanner; lên đầu file Java của bạn. 3\. Trám lỗ hổng bằng Edge Cases (Trường hợp ngoại lệ Bạn còn nhớ khái niệm Edge Cases ở các bài đọc trước chứ? Trong ví dụ tạo máy tính, thao tác chia (Division) tiềm ẩn một lỗi cực kỳ kinh điển trong lập trình: Chia cho 0. Nếu người dùng cố tình nhập số chia là 0, chương trình sẽ bị văng lỗi (crash \- ArithmeticException). Q Developer đủ thông minh để phát hiện rủi ro này trong lúc bạn đang gõ và gợi ý thêm khối lệnh điều kiện if (divisor \== 0\) để bắt lỗi, giúp hệ thống không bị sập.Làm việc với GenAI trong môi trường lập trình giống như bạn luôn có một Senior Developer ngồi cạnh để "nhắc tuồng" (Pair Programming), giúp bạn viết code vừa nhanh vừa an toàn. Để chuẩn bị "thực chiến" cho bài Lab 45 phút tiếp theo, bạn đã cài đặt và kích hoạt thành công plugin Amazon Q Developer trên IntelliJ chưa, hay có bước nào bị vướng cần mình hướng dẫn luôn không |
| :---- |

   

3. # **ChatGPT & Github copilot**

- **ChatGPT Introduction**   
+ Gia sư lý thuyết và giải thích các khái niệm   
+  Chuyên gia gỡ lỗi Debugging  
+ Sức mạnh dòng chảy (Conversational Flow ) → đây chính là điểm “ ăn tiền nhất của Chat GPT  ⇒ Có thể yêu cầu nó tinh chỉnh code dựa trên kết quả cũ  

			⇒ CẠM BẪY  :  Nếu câu lệnh quá chung chung thì nó                                         sẽ đưa ra các outdated solutions các giải pháp lỗi thời ) 

- Hand-on with Chat GPT   
+ Ba vũ khí lợi hại của Chat GPT với java    
* Giải thích kn  
* Cung cấp code Snippet (Đoạn mã mẫu)  
* Bắt bệnh lỗi (Debugging)  
+ 5 bộ bí kíp giúp AI trả lời xuất sắc   
* Provide Context : cung cấp ngữ cảnh câu hỏi    
* Be precise tính chính xác và cụ thể  : yc rõ ràng ngôn ngữ lập trình , phiên bản  …   
* Request Clarification (Yêu cầu làm rõ )  nếu AI trả lời mà dùng các thuật ngữ chuyên ngành thì yêu cầu giải thích thêm   
* Build ôn answers  : xây dựng các chuỗi hội thoại và hỏi đào sâu thêm   
* Test and modify   : không copy code mù quáng mà hãy copy vào trong IntelliJ để chạy thử các edge( ngoại lệ  )   
  Nếu coi Chat GPT là nguwoif thầy giải thích cặn  kẽ và tìm ra lỗi sai cho bạn thì Github Copilot là người đồng nghiệp ( pair programmer)  cực kì hiểu ý của bạn   
- Github Copilot Introduction    
+ Nổi tiếng với khả năng đọc hiểu ngữ cảnh dự án và đưa ra các gợi ý chính xác    
+ 4 “ phép thuật  “  thực chiến của GitHub Copilot    
* Phím tab quyền lực  : khi khai báo 1 hàm nó sẽ tự động đọc đc mục đích bạn viết hàm đó và tự động đưa ra các đề xuất logic mờ ở trong . Công việc của bạn là đọc logic và bấm phím tab để nhận hàm    
* Viết code bằng comment : bạn chỉ cần viết 1 comment bàng tiếng anh hơacj tiếng việt thì nó sẽ tự động xổ ra 1 hàm ở bên dưới   
* Tự động sinh ra các kịch bản kiểm thử  : chỉ cần viết comment yêu cầu tạo ra các unit test case để test hàm là nó sẽ tạo ra các hàm vưới tha số đầu vào để test   
* Bắt bệnh và sửa lỗi tại chỗ  : mở khung chat ẩn  và ra lệnh để nó tự debugging   
- dfg

4. # **Đúc kết rút ra điểm mạnh yếu của các công cụ bằng cách so sanhs các công cụ**  

   \- Định vị lại 3 ông lớn   
+  ChatGPT (Người Thầy/Cố vấn) :  Tuyệt vời nhất khi bạn cần học một khái niệm mới, phân tích các lỗi phức tạp, hoặc cần thiết kế kiến trúc hệ thống (như Design Patterns)  
+ **GitHub Copilot (Người Đồng nghiệp gõ máy nhanh):** Tích hợp thẳng vào IDE (IntelliJ/VS Code). Sức mạnh cốt lõi của nó là tốc độ. Nó dự đoán bạn sắp gõ gì và tự động hoàn thành code, sinh ra các đoạn code rập khuôn (boilerplate) hoặc test cases trong chớp mắt.  
+ **Amazon Q Developer (Chuyên gia Tối ưu & Bảo mật):** Cũng nằm ngay trong IDE, những điểm mạnh của nó là kiểm duyệt và tối ưu theo thời gian thực, đặc biệt xuất sắc với Java và các dịch vụ AWS  . Nó đóng vai trò như một người rà soát, cảnh báo ngay khi bạn quên đóng kết nối Database hoặc viết một vòng lặp chạy quá chậm.

| Thay vì phải tự bỏ tiền tỷ ra mua dàn máy chủ vật lý, cắm điện và thuê người canh gác, AWS cho phép bạn "thuê" máy chủ và các dịch vụ phần mềm của họ qua Internet. Dùng bao nhiêu, trả tiền bấy nhiêu (giống như trả tiền điện, tiền nước). |
| :---- |

  \- Bảng so sánh : 

| Tính năng | Amazon Q Developer | ChatGPT | GitHub Copilot |
| :---- | :---- | :---- | :---- |
| **Môi trường hoạt động** | Tích hợp sâu vào IDE (IntelliJ, VS Code) | Nền tảng Web độc lập | Tích hợp sâu vào IDE |
| **Thế mạnh Code** | Gợi ý theo ngữ cảnh, tối ưu hóa code | Sinh code theo yêu cầu chi tiết của người dùng | Tự động hoàn thành code (Auto-complete) thời gian thực |
| **Bắt lỗi (Error Detection)** | **Tự động, rà soát ngay lúc đang gõ** | Phụ thuộc vào việc bạn copy lỗi đưa cho nó | Hạn chế hơn trong việc chủ động bắt lỗi |
| **Giải thích khái niệm** | Ngắn gọn, tập trung vào đoạn code hiện tại | **Chi tiết, chuyên sâu, kèm ví dụ thực tế** | Giải thích ngắn gọn về code |
| **Mục tiêu chính** | Best practices (Viết code chuẩn), Bảo mật | Học hỏi, Debug logic, Lên ý tưởng | Tốc độ, Xử lý tác vụ lặp đi lặp lại |

5. Các thuật ngữ   
   

| Thuật ngữ | Giải thích |
| :---- | :---- |
| **Amazon Q Developer** | Trợ lý AI tích hợp trực tiếp vào IDE, chuyên kiểm tra lỗi và tối ưu hóa code theo thời gian thực (real-time). Rất mạnh trong việc nhắc nhở thực hành chuẩn (best practices) và làm việc với hệ sinh thái AWS. |
| **ChatGPT** | Trợ lý AI hoạt động qua giao diện nền web. Rất xuất sắc trong việc đóng vai trò "gia sư", giải thích các khái niệm phức tạp, hỗ trợ tư duy thuật toán và phân tích nguyên nhân gây lỗi chi tiết. |
| **GitHub Copilot** | Trợ lý AI tích hợp trong IDE (xây dựng trên mô hình Codex). Nổi tiếng với tốc độ tự động hoàn thành code (autocomplete) cực nhanh và khả năng dịch từ ngôn ngữ tự nhiên (comment) sang code. |
| **Prompt Engineering** | Kỹ nghệ viết câu lệnh. Là kỹ năng thiết kế, định hình cấu trúc câu hỏi/mệnh lệnh để điều khiển AI sinh ra kết quả chính xác và tối ưu nhất. |
| **Instruction-based Prompts** | Kỹ thuật viết câu lệnh mang tính chỉ thị trực tiếp, đi thẳng vào mục tiêu cụ thể cần thực hiện mà không vòng vo. |
| **Zero-Shot Prompting** | Kỹ thuật ra lệnh cho AI xử lý công việc ngay lập tức mà không cần mồi trước hoặc cung cấp bất kỳ đoạn code mẫu nào. |
| **Few-Shot Prompting** | Kỹ thuật cung cấp 1-2 ví dụ mẫu (input \- output) vào câu lệnh để ép AI sinh ra kết quả tuân theo đúng định dạng và phong cách code mong muốn. |
| **Chain-of-Thought Prompting** | Kỹ thuật "chuỗi tư duy". Thay vì yêu cầu kết quả cuối cùng, bạn ép AI phải suy luận logic và giải quyết bài toán phức tạp theo từng bước một. |
| **Role-based Prompting** | Kỹ thuật "nhập vai". Yêu cầu AI đóng vai một chuyên gia cụ thể (ví dụ: Senior Java Developer, Giảng viên) để thay đổi góc nhìn, mức độ chuyên sâu và giọng văn. |
| **Contextual Prompts** | Kỹ thuật cung cấp ngữ cảnh. Bổ sung thông tin nền tảng về dự án, môi trường hoặc công nghệ đang dùng để AI đưa ra giải pháp sát thực tế nhất. |
| **IDE (Integrated Development Environment)** | Môi trường phát triển tích hợp (như IntelliJ IDEA, Visual Studio Code). Đây là phần mềm chuyên dụng để lập trình viên viết code, và cũng là nơi các plugin như Amazon Q hay Copilot "trú ngụ". |
| **Code Snippet** | Một đoạn mã mẫu ngắn gọn, hoàn chỉnh, được thiết kế để thực hiện một chức năng cụ thể (ví dụ: đoạn code đảo ngược chuỗi). |
| **NullPointerException (NPE)** | Lỗi kinh điển trong Java xảy ra khi chương trình gọi đến một đối tượng chưa được khởi tạo (mang giá trị null). Đây là ví dụ phổ biến để kiểm tra khả năng bắt lỗi của AI. |
| **Inline Debugging / Inline Chat** | Tính năng cho phép bạn chat trực tiếp với AI hoặc nhận gợi ý sửa lỗi ngay tại dòng code đang hiển thị trên IDE, không cần chuyển sang trình duyệt web. |
| **Test Cases / Unit Test** | Các kịch bản kiểm thử mức đơn vị. Đây là những đoạn code phụ được viết ra nhằm mục đích tự động kiểm tra xem hàm chức năng chính có hoạt động đúng logic với các số liệu đầu vào khác nhau hay không. |
| **Refactoring** | Quá trình tinh chỉnh, sắp xếp và viết lại mã nguồn (để code chạy nhanh hơn, dễ đọc hơn) mà không làm thay đổi chức năng hiển thị bên ngoài của hệ thống. |

   