# Lý Thuyết Trò Chơi (phần 2) 
### 2. Giải trò chơi và khái niệm điểm cân bằng (tiếp theo) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Trực giác đằng sau những cân bằng* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một cách lý giải về điểm cân bằng trong các trò chơi như *Qua cầu* là lý giải tiến hóa. Nếu thợ săn và người chạy trốn/tổ tiên của họ thường xuyên chơi các trò chơi có cấu trúc tương tự trong quá khứ thì sức ép từ những thói quen/văn hóa/sinh học là thứ đưa cả 2 tới việc chơi các chiến lược NE và duy lý hóa hành động đó (sẽ nói rõ hơn khi thảo luận về *"Lý thuyết trò chơi tiến hóa"*). Cách hiểu như vậy rất phù hợp với các mô hình xã hội quy mô lớn, đặc biệt trong kinh tế học, nơi mà một hệ thống kinh tế được diễn giải như mạng lưới của các mối quan hệ nhân quả, thường nằm trong sự cân bằng và chỉ bị xáo trộn khi có sự can thiệp của một lực lượng ngoại sinh. Nhưng một số người lại coi LTTC là một lý thuyết về suy lý chiến lược đơn thuần mà với họ, lời giải của trò chơi phải là một kết quả dự đoán được bằng cách sử dụng duy nhất các cơ chế tính toán duy lý. Các lý thuyết gia này phải đối mặt với những vướng mắc đã đề cập ***cuối mục 0/***. Vấn đề sẽ được giải quyết nếu ta thừa nhận rằng tính duy lý trong LTTC có thể do người chơi tự tính toán hoặc được bao hàm trong những cấu trúc hành vi hình thành bởi sự chọn lọc kinh tế, văn hóa hoặc tự nhiên. <br>
### 3. Tinh chỉnh cân bằng Nash <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bộ lọc cân bằng Nash* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi các đặc tính của NE, nếu trò chơi chỉ có 1 kết quả NE thì nó phải là lời giải duy nhất. Tuy nhiên, ở các trò chơi có nhiều NE, không phải tất cả các NE đều trông hợp lý. Hãy xem trò chơi sau <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/69634713-e24f-4ee9-8d01-2d2e7dce72a1)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi này có 2 NE với chiến lược thuần túy: $\left( {{s_1},{t_1}} \right),\left( {{s_2},{t_2}} \right)$  và 1 NE với chiến lược hỗn hợp: $\left( {\frac{1}{{11}}{s_1} + \frac{{10}}{{11}}{s_2},\frac{1}{{11}}{t_1} + \frac{{10}}{{11}}{t_2}} \right)$ (Player I phân phối xác suất cho ${s_1},{s_2}$ lần lượt là $\frac{1}{{11}}$ và $\frac{10}{{11}}$ ; tương tự với Player II <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu NE là khái niệm giải pháp duy nhất thì 3 kết quả này đều phải được coi là lời giải của trò chơi. Nhưng có điều gì đó đã bị bỏ quên: những người chơi duy lý và có đầy đủ thông tin chắc chắn sẽ hội tụ vào $\left( {{s_1},{t_1}} \right)$   ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xem tiếp ví dụ sau:
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/889e17dd-b9f9-4ecf-a30d-21864ae45095)
</div>

Trò chơi có các NE là: 
```math
\left\{ \begin{array}{l}
\left( {{s_1},{t_2}} \right)\
\left( {r{s_1} + \left( {1 - r} \right){s_2},{\rm{ }}{t_1}} \right)
\end{array} \right.  ,{\rm{      }} \text{      } r \le \frac{1}{3}
```
&nbsp;&nbsp;&nbsp;&nbsp;Không có chiến lược nào thống trị / bị thống trị nghiêm ngặt. Tuy nhiên, hàng $s_1$ "thống trị yếu" $s_2$ , nghĩa là phần thưởng của Player I khi chơi $s_1$ luôn lớn hơn hoặc ít nhất cũng bằng phần thưởng khi chơi $s_2$ dù Player II chơi bất cứ cột nào. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy chúng ta có nên xóa đi hàng $s_2$ bị thống trị yếu để cho $\( s_{1} ; t_{2} \)$ trở thành NE duy nhất không? Để kiểm chứng, ta thử thay đổi các khoản tiện ích của trò chơi một chút (qua *ví dụ* mới dưới đây). <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/67ffa881-7779-460f-b040-0cc9ace973a6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nhận thấy $s_2$ vẫn bị thống trị yếu, nhưng NE $\( s_{2} ; t_{1} \)$  giờ đây là hấp dẫn nhất đối với cả 2 người chơi. Vậy thì tại sao các nhà phân tích lại muốn loại bỏ nó? Lý lẽ cho việc loại bỏ các chiến lược bị thống trị yếu là ở chỗ Player I có thể sợ rằng Player II *không hoàn toàn duy lý* - chơi $t_2$ bằng một xác suất dương. Vì vậy Player I muốn tránh kết quả tệ nhất của mình, $\( s_{2} ; t_{2} \)$ , và cái giá cho sự đảm bảo này là giảm tiện ích từ 10 xuống 5. Player II-biết Player I nghĩ gì, sẽ có động cơ để chơi $t_2$ ; và thế là Player I-biết Player II biết mình nghĩ gì, càng tin vào quyết định chơi $s_1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, có thể nghĩ về kịch bản 2 người chơi đã giao tiếp với nhau trước khi chơi và đồng ý chơi các chiến lược dẫn đến $\( s_{2} ; t_{1} \)$ , bằng cách loại bỏ sự không chắc chắn về đối phương <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Qua 3 ví dụ trên, phần nào minh họa một sự thật rằng NE là một ***<ins>khái niệm giải pháp tương đối yếu</ins>***, thường không dự đoán được các kết quả nhạy cảm về mặt trực giác vì nếu áp dụng đơn độc, nó sẽ không cho người chơi sử dụng các nguyên tắc lựa chọn mà nếu không dựa trên tính duy lý thì ít nhất cũng không phải là phi lý. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bất cứ nguyên tắc nào giải quyết các trò chơi bằng cách loại bỏ 1 hoặc nhiều NE khỏi sự xem xét thì đều được coi là bộ lọc của NE. Trong trường hợp ở ảnh 3 thì việc loại bỏ các chiến lược bị thống trị yếu chính là một bộ lọc vì nó giữ lại duy nhất NE $\( s_{1} ; t_{2} \)$  và lọc đi tất cả các NE khác, và song song là một bộ lọc khác, giữ lại mỗi NE $\( s_{2} ; t_{1} \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy thì bộ lọc nào thích hợp hơn với vai trò là một khái niệm giải pháp? Ưu khuyết của chúng và một số lượng lớn các bộ lọc khác đều cần phải bàn thêm. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Sự cân bằng hoàn hảo của trò chơi con* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta xét 2 ví dụ tương ứng với 2 trò chơi như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 1:</ins>* Cho hình vẽ sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ad99b231-ad32-422e-ac04-b8fd42bfe1fe)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Áp dụng *thuật toán Zermelo*, ta tìm được lời giải cho trò chơi là $\( LR, RL \)$ . (Player I chơi chiến lược $LR$ , Player II chơi chiến lược $RL$ ). Mỗi người chơi có 2 nút thông tin, mỗi nút có 2 lựa chọn hành động, nên tổng cộng mỗi người có 4 chiến lược. Chữ cái đầu tiên/thứ 2 trong mỗi chiến lược là điều mà người chơi sẽ làm khi họ ở nút thông tin đầu tiên/thứ 2. $\( LR, RL \)$ có nghĩa là Player I chơi $4L$ và $7R$ , Player II chơi $5R$ và $6L$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ảnh bên phải vẫn là trò chơi này nhưng được biểu diễn ở dạng chuẩn tắc. Quan sát ma trận này, ta phát hiện ra $\( LL, RL \)$ cũng là NE. Có gì đó không đúng ở đây, nhìn lại dạng mở rộng, tại sao Player I lại muốn chơi $7L$ trong khi chơi $7R$ đem lại mức thưởng cao hơn? <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Phép phân tích NE bỏ qua điều này vì nó không quan tâm đến những diễn biến bên ngoài cuộc chơi-tức là lựa chọn của Player I ở nút 7, điều sẽ không bao giờ xảy ra khi Player I đã chọn $4L$ . Tuy nhiên đó lại là điều ta phải xem xét đến khi phân tích trò chơi, vì nó là động lực cho những gì xảy ra trong cuộc chơi: hành động của Player I ở nút 7 quyết định hành động của Player II ở nút 6, và đó lại là nguyên nhân cho hành động của Player I ở nút 4. Chúng ta sẽ vứt bỏ lượng thông tin quan trọng này nếu chỉ phân tích NE theo lối đơn thuần. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Việc thuật toán Zermelo chọn $\( LR, RL \)$ là lời giải duy nhất của trò chơi cho thấy nó đạt được một khái niệm cân bằng trên cả NE. Thực tế thì nó đang tạo ra sự cân bằng hoàn hảo của trò chơi con ***<ins>(SPE-subgame perfect equilibrium)</ins>*** . Một NE của trò chơi là SPE khi nó là NE trong mọi trò chơi con của trò chơi đó (định nghĩa trò chơi con: cho một cây trò chơi, nếu giữ lại 1 nút thông tin cùng tất cả các nhánh đi xuống xuất phát từ nó, và xóa bỏ toàn bộ phần còn lại của cây trò chơi, ta thu được một trò chơi mới là trò chơi con của trò chơi ban đầu). <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 2:</ins>* Cho hình vẽ sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/f29f9a1e-a30c-4dca-a49c-7cf11b19dbde)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi giữa 2 người chơi C và D, được biểu diễn ở cả 2 dạng: mở rộng (trái) và chuẩn tắc (phải). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong 3 NE được đánh dấu (*) ở dạng chuẩn tắc, chỉ có NE $\( E, EB \)$ - đánh dấu (**)-là SPE, có thể xác định bằng thuật toán Zermelo. Ta thấy $\( B, EE \)$ cũng là một NE, nhưng nó không thể được chấp nhận là lời giải của trò chơi. Tại kết quả $\( B, EE \)$ , C chơi B bởi vì D "đe dọa" sẽ chơi E nếu C chơi E, nhưng nếu C chơi E thật thì D chắc chắn sẽ không làm thế-chơi B rõ ràng có lợi cho D hơn $\left( {l > 0} \right)$ , do đó đây là một lời đe doạ "không đáng tin". Các NE bất hợp lý này giống như một lỗi kỹ thuật phát sinh khi ta chuyển trò chơi từ dạng mở rộng về dạng chuẩn tắc (do một phần thông tin về trò chơi đã bị giấu đi, khiến cho 2 người chơi trông như là đang đưa ra quyết định đồng thời). Nếu một NE không phải là SPE, nó là bất hợp lý và không thể là lời giải của trò chơi. Ở đây *thuật toán Zermelo* có vai trò như một bộ lọc vậy, nó loại bỏ tất cả các NE không phải là SPE. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Những bàn tay run* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Những vấn đề ở trên mở ra một rắc rối liên quan tới nền tảng logic của LTTC. Quay lại trò chơi ở ***ví dụ 1*** , lời giải là $\( LR, RL \)$ được tìm ra bởi *qui nạp ngược* . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cụ thể: Player I chơi $4L$ vì anh ta biết Player II là người duy lý-sẽ chơi $5R$ và $6L$ . Player II chơi 6L vì biết Player I là người duy lý - sẽ chơi $7R$ . Nhưng lại xuất hiện một nghịch lý, trò chơi chỉ đến được nút 6 nếu Player I không duy lý! Nếu Player I không duy lý thì Player II không thể chắc chắn rằng Player I sẽ chơi $7R$ , vì vậy chưa chắc là Player II sẽ chơi $6L$ , và nếu Player II chơi $6R$ thì Player I sẽ có phần thưởng tốt hơn nếu chơi $4R$ . Cả 2 tay chơi phải sử dụng lối qui nạp ngược đòi hỏi rằng mỗi người chơi là duy lý và biết người kia cũng duy lý, nhưng đồng thời họ phải giả định đối thủ hành động phi lý. Mâu thuẫn này được gọi là "nghịch lý qui nạp ngược". <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cách chuẩn mực nhất để giải quyết nghịch lý này là viện đến khái niệm "bàn tay run" của Selten [1975]. Tư tưởng này cho rằng một hành động phi lý có thể gắn với một xác suất dương vô cùng bé. Nghĩa một tay chơi có thể mắc lỗi khi thực hiện hành động-với một khả năng rất nhỏ. Vậy là không còn mâu thuẫn nào khi sử dụng lý lẽ qui nạp ngược nữa. Trong ví dụ của chúng ta, Player II có thể nghĩ về lựa chọn ở nút 6 dựa vào định đề rằng Player I muốn chọn $4L$ , nhưng sau đó đã "lỡ tay" chọn $4R$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khái niệm này cũng củng cố tính hợp lý của các bộ lọc đã thảo luận ở ***phần 3/, a/*** . Nếu "bàn tay" đối thủ của tôi có thể "run", thì tôi có lý do chính đáng để tránh cái chiến lược bị thống trị yếu $s_2$ trong hình mục ***phần 3/, b/*** . Đối thủ của tôi có thể cam kết chơi $t_1$ và tôi có thể tin vào lời hứa của anh ta. Nhưng nếu sau đó anh ta "run tay" và chơi $t_2$ , thì tôi phải nhận một kết quả tồi tệ nhất. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Cân bằng tuần tự* <br>















