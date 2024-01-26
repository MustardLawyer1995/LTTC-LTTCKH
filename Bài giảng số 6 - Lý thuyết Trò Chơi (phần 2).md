# Lý Thuyết Trò Chơi (phần 2) 
### 2. Giải trò chơi và khái niệm điểm cân bằng (tiếp theo) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Trực giác đằng sau những cân bằng* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một cách lý giải về điểm cân bằng trong các trò chơi như *Qua cầu* là lý giải tiến hóa. Nếu thợ săn và người chạy trốn/tổ tiên của họ thường xuyên chơi các trò chơi có cấu trúc tương tự trong quá khứ thì sức ép từ những thói quen/văn hóa/sinh học là thứ đưa cả 2 tới việc chơi các chiến lược NE và duy lý hóa hành động đó (sẽ nói rõ hơn khi thảo luận về *"Lý thuyết trò chơi tiến hóa"*). Cách hiểu như vậy rất phù hợp với các mô hình xã hội quy mô lớn, đặc biệt trong kinh tế học, nơi mà một hệ thống kinh tế được diễn giải như mạng lưới của các mối quan hệ nhân quả, thường nằm trong sự cân bằng và chỉ bị xáo trộn khi có sự can thiệp của một lực lượng ngoại sinh. Nhưng một số người lại coi LTTC là một lý thuyết về suy lý chiến lược đơn thuần mà với họ, lời giải của trò chơi phải là một kết quả dự đoán được bằng cách sử dụng duy nhất các cơ chế tính toán duy lý. Các lý thuyết gia này phải đối mặt với những vướng mắc đã đề cập ***cuối mục 0/***. Vấn đề sẽ được giải quyết nếu ta thừa nhận rằng tính duy lý trong LTTC có thể do người chơi tự tính toán hoặc được bao hàm trong những cấu trúc hành vi hình thành bởi sự chọn lọc kinh tế, văn hóa hoặc tự nhiên. <br>
### 3. Tinh chỉnh cân bằng Nash <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bộ lọc cân bằng Nash* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi các đặc tính của NE, nếu trò chơi chỉ có 1 kết quả NE thì nó phải là lời giải duy nhất. Tuy nhiên, ở các trò chơi có nhiều NE, không phải tất cả các NE đều trông hợp lý. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.1:</ins>* Hãy xem trò chơi sau<br> 
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/69634713-e24f-4ee9-8d01-2d2e7dce72a1)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi này có 2 NE với chiến lược thuần túy: $\left( {{s_1},{t_1}} \right),\left( {{s_2},{t_2}} \right)$  và 1 NE với chiến lược hỗn hợp: $\left( {\frac{1}{{11}}{s_1} + \frac{{10}}{{11}}{s_2},\frac{1}{{11}}{t_1} + \frac{{10}}{{11}}{t_2}} \right)$ (Player I phân phối xác suất cho ${s_1},{s_2}$ lần lượt là $\frac{1}{{11}}$ và $\frac{10}{{11}}$ ; tương tự với Player II <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu NE là khái niệm giải pháp duy nhất thì 3 kết quả này đều phải được coi là lời giải của trò chơi. Nhưng có điều gì đó đã bị bỏ quên: những người chơi duy lý và có đầy đủ thông tin chắc chắn sẽ hội tụ vào $\left( {{s_1},{t_1}} \right)$   ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.2:</ins>* Hãy xem tiếp trò chơi sau<br> 
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/889e17dd-b9f9-4ecf-a30d-21864ae45095)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi có các NE là: 
```math
\left\{ \begin{array}{l}
\left( {{s_1},{t_2}} \right)\
\left( {r{s_1} + \left( {1 - r} \right){s_2},{\rm{ }}{t_1}} \right)
\end{array} \right.  ,{\rm{      }} \text{      } r \le \frac{1}{3}
```
&nbsp;&nbsp;&nbsp;&nbsp;Không có chiến lược nào thống trị / bị thống trị nghiêm ngặt. Tuy nhiên, hàng $s_1$ "thống trị yếu" $s_2$ , nghĩa là phần thưởng của Player I khi chơi $s_1$ luôn lớn hơn hoặc ít nhất cũng bằng phần thưởng khi chơi $s_2$ dù Player II chơi bất cứ cột nào. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy chúng ta có nên xóa đi hàng $s_2$ bị thống trị yếu để cho $\( s_{1} ; t_{2} \)$ trở thành NE duy nhất không? Để kiểm chứng, ta thử thay đổi các khoản tiện ích của trò chơi một chút (qua *ví dụ* mới dưới đây). <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.3:</ins>* Hãy xem trò chơi sau<br> 
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
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.4:</ins>* Cho hình vẽ sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ad99b231-ad32-422e-ac04-b8fd42bfe1fe)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Áp dụng *thuật toán Zermelo*, ta tìm được lời giải cho trò chơi là $\( LR, RL \)$ . (Player I chơi chiến lược $LR$ , Player II chơi chiến lược $RL$ ). Mỗi người chơi có 2 nút thông tin, mỗi nút có 2 lựa chọn hành động, nên tổng cộng mỗi người có 4 chiến lược. Chữ cái đầu tiên/thứ 2 trong mỗi chiến lược là điều mà người chơi sẽ làm khi họ ở nút thông tin đầu tiên/thứ 2. $\( LR, RL \)$ có nghĩa là Player I chơi $4L$ và $7R$ , Player II chơi $5R$ và $6L$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ảnh bên phải vẫn là trò chơi này nhưng được biểu diễn ở dạng chuẩn tắc. Quan sát ma trận này, ta phát hiện ra $\( LL, RL \)$ cũng là NE. Có gì đó không đúng ở đây, nhìn lại dạng mở rộng, tại sao Player I lại muốn chơi $7L$ trong khi chơi $7R$ đem lại mức thưởng cao hơn? <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Phép phân tích NE bỏ qua điều này vì nó không quan tâm đến những diễn biến bên ngoài cuộc chơi-tức là lựa chọn của Player I ở nút 7, điều sẽ không bao giờ xảy ra khi Player I đã chọn $4L$ . Tuy nhiên đó lại là điều ta phải xem xét đến khi phân tích trò chơi, vì nó là động lực cho những gì xảy ra trong cuộc chơi: hành động của Player I ở nút 7 quyết định hành động của Player II ở nút 6, và đó lại là nguyên nhân cho hành động của Player I ở nút 4. Chúng ta sẽ vứt bỏ lượng thông tin quan trọng này nếu chỉ phân tích NE theo lối đơn thuần. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Việc thuật toán Zermelo chọn $\( LR, RL \)$ là lời giải duy nhất của trò chơi cho thấy nó đạt được một khái niệm cân bằng trên cả NE. Thực tế thì nó đang tạo ra sự cân bằng hoàn hảo của trò chơi con ***<ins>(SPE-subgame perfect equilibrium)</ins>*** . Một NE của trò chơi là SPE khi nó là NE trong mọi trò chơi con của trò chơi đó (định nghĩa trò chơi con: cho một cây trò chơi, nếu giữ lại 1 nút thông tin cùng tất cả các nhánh đi xuống xuất phát từ nó, và xóa bỏ toàn bộ phần còn lại của cây trò chơi, ta thu được một trò chơi mới là trò chơi con của trò chơi ban đầu). <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.5:</ins>* Cho hình vẽ sau: <br>
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
&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta hãy xem xét trò chơi tay 3 với thông tin không hoàn hảo dưới đây - được gọi là ***"Con ngựa Selten"*** *(tên người tạo ra trò chơi, được giải Nobel, Reinhard Selten)* thông qua hình sau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.6:</ins>* <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/7702ea00-3a1f-4f23-b8e5-be0b8befec8a)
</div>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi có các NE là: <br>

```math
\left\{ \begin{array}{l}
\left( {L,{\rm{ }}s{l_2} + \left( {1 - s} \right){r_2},{\rm{ }}{l_3}} \right),s \le \frac{1}{2}{\rm{ }}\
\left( {R,{\rm{ }}{r_2},{\rm{ }}t{l_3} + \left( {1 - t} \right){r_3}} \right),s \le \frac{1}{3}
\end{array} \right. 
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;lần lượt ứng với kết quả $\( 4;4;4 \)$ và $\( 3;3;0 \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nhưng ta không thể lọc chúng bằng thuật toán Zermelo. Vì các nút 13 và 14 cùng nằm trong một tập thông tin chung nên Con ngựa Selten chỉ có 1 trò chơi con - là toàn bộ trò chơi, dẫn đến việc tất cả các NE đều là SPE. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hãy để ý rằng khi đưa ra lựa chọn, tay chơi (III) chỉ biết là mình đang ở tập thông tin chung nhưng không rõ là nút 13 hay 14, nên anh ta phải gán các xác suất cho mỗi nút. Các xác suất này-có vai trò như hệ thống niềm tin của (III), là cái mà (III) băn khoăn, mặt khác (I) và (II) cũng phải phỏng đoán về nó để lựa chọn chiến lược phù hợp. <br> <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Từ đây ta có một khái niệm mới: ***<ins>cân bằng tuần tự (SE-sequential equilibrium)</ins>***. Một SE gồm 2 phần: (1) tập chiến lược mà các tay chơi lựa chọn; (2) một hệ thống niềm tin cho các tay chơi, nó ấn định cho mỗi tập thông tin $h$ một phân phối xác suất lên các nút trong $h$ , được lý giải là niềm tin của tay chơi sở hữu $h$ về việc anh ta đang ở nút nào trong $h$ . Một SPE là SE khi chiến lược của mỗi tay chơi là tối ưu và nhất quán đối với niềm tin của các tay chơi khác. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta sẽ áp dụng khái niệm này cho trò chơi ***Con ngựa Selten*** . Giả sử (III) ấn định $q$ là xác suất anh ta đang ở nút 13 (và $1-q$ là xác suất của nút 14). (III) đưa ra lựa chọn để tối đa hóa tiện ích của mình theo $q$ . Tiện ích trung bình của (III) khi chơi $l_3$ và $r_3$ lần lượt là $4q$ và $2-q$ , nên (III) sẽ: chơi $l_3$ khi $q > \frac{2}{5}$ ; chơi $r_3$ khi $q < \frac{2}{5}$ ; chơi chiến lược tùy ý khi $q = \frac{2}{5}$ . (I) và (II) phải chơi các chiến lược nhất quán với niềm tin của (III), tức là họ sẽ hành động sao cho xác suất mà (III) đang ở nút 13 đúng là $q$ . Đây là các xác suất có điều kiện (dựa trên sự kiện đã xảy ra là (III) đang ở trong tập thông tin {13,14}) nên theo quy tắc Bayes, ta đánh giá được: <br>
<div align="center">

$$q = \frac{p\( L \)}{p\( L \)+p\( R \) \times p\( l_{2} \)}$$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;trong đó $p\( x \)$ là xác suất mà chiến lược $x$ được sử dụng, $p\( L \)+p\( R \) = 1$ ). Đồng thời, chiến lược mà (I) và (II) lựa chọn phải là tối ưu theo $q$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét NE $\left( {L,{\rm{ }}s{l_2} + \left( {1 - s} \right){r_2},{l_3}} \right),s \le \frac{1}{2}$ , (III) chơi $l_3 \text{     } \( q \ge \frac{2}{5} \)$  nhất quán với $p\( L \) = 1 \text{     } \( q=1 \)$ ; nhưng nếu trò chơi đến được nút 12, (II) sẽ phải chơi $l_2$ , bởi vì (II) biết (III) sẽ chơi $l_3$ theo niềm tin $q=1$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ $\left( {L,{\rm{ }}s{l_2} + \left( {1 - s} \right){r_2},{l_3}} \right),s \le \frac{1}{2}$ không phải là SE. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét NE $\left( {R,{r_2},t{l_3} + \left( {1 - t} \right){r_3}} \right),t \le \frac{1}{3}$ , (III) chơi chiến lược hỗn hợp $t{l_3} + \left( {1 - t} \right){r_3}$ $\text{     } \( q \ge \frac{2}{5} \)$ nhất quán với $p\( L \) = p\( l_{2} \) = 0$ ( $q=\frac{0}{0}$ , giá trị bất định, nghĩa là (III) có thể ấn định $q$ bằng bao nhiêu cũng được); và chiến lược của (I),(II) đã là tối ưu theo lựa chọn của (III) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ $\left( {R,{r_2},t{l_3} + \left( {1 - t} \right){r_3}} \right),t \le \frac{1}{3}$ là SE. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có một cách hiểu trực giác đằng sau việc kết quả hấp dẫn $\( 4;4;4 \)$ không phải là SE, đó là (III) hoàn toàn không biết những gì xảy ra ở các nút 11 và 12, nên một khi trò chơi đã đi đến tập thông tin {13,14}, (III) sẽ luôn hành động theo cùng một kiểu, phụ thuộc vào cái niềm tin của anh ta-đã được ấn định ngay vào lúc bắt đầu trò chơi. Vì thế nếu (I) "run tay" và chơi $R$ (dù anh ta định chơi $L$ ), thì (II) sẽ không ngần ngại chơi $l_2$ để tăng tối đa tiện ích của mình. Ở đây lại một lần nữa ta phải viện đến khái niệm "bàn tay run". 
#### &nbsp;&nbsp;&nbsp;&nbsp; *e. Cân bằng hoàn hảo của bàn tay run* <br>
Trong ví dụ Con ngựa Selten, khi tập thông tin $\{13,14 \}$ nhận xác suất là 0, ta thấy một điểm trái khoáy là xác suất q có thể nhận giá trị tùy ý, tức là (III) có thể tin vào bất kỳ điều gì xảy ra ở tập thông tin {13,14}. Để hóa giải mâu thuẫn này, ta phải cho rằng mọi tay chơi đều sử dụng chiến lược *hỗn hợp hoàn toàn* - tất cả các chiến lược thuần túy đều được gán xác suất dương, ta ngầm hiểu là các chiến lược thuần túy không được sử dụng đều bị gán xác suất $ε \( ε→0⁺ \)$. Điều này cũng tương đương với định đề "tất cả các bàn tay đều run" vậy! Nếu một SE tồn tại ở trạng thái như thế, thì nó là một ***cân bằng hoàn hảo của bàn tay run (THPE-trembling hand perfect equilibrium)*** . Có thể nhận ra ngay các NE thu được bằng cách loại bỏ chiến lược bị thống trị yếu đã nói ở mục 3/,a/ cũng là các THPE, nếu ta biểu diễn các trò chơi ở ***ví dụ 3.2 và 3.3*** của mục đó về dạng mở rộng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.7:</ins>* Cho hình vẽ sau<br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ef10d2de-ff00-48c1-b35f-400bea9290f5)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Bởi vì (III) sẽ luôn chơi $l_3$ , trò chơi xem như đã bị rút gọn về dạng 2 người chơi. Dùng các kỹ thuật đã học, ta tìm được các SPE lần lượt là:  

```math
\left\{ \begin{array}{l}
\left( {L,s{l_2} + \left( {1 - s} \right){r_2},{l_3}} \right),s \ge \frac{1}{4}\
\left( {\frac{4}{5}M + \frac{1}{5}R,\frac{1}{6}{l_2} + \frac{5}{6}{r_2},{l_3}} \right),{\rm{ }}\left( {R,{\rm{ }}{r_2},{\rm{ }}{l_3}} \right)
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;Không khó để nhận ra tất cả chúng đều là SE, niềm tin của (II) ấn định cho các nút 15, 16 xác suất lần lượt là $q$ , $1-q$ , (II) sẽ chơi: $l_2$ khi $q > \frac{4}{5}$ , $r_2$ khi $q < \frac{4}{5}$ , chiến lược tùy ý nếu $q = \frac{4}{5}$ . Tuy nhiên, mọi chuyện sẽ khác nếu ta tính đến sự “run tay” của (III) - chơi $l_3$ và $r_3$ với xác suất lần lượt là $1- \varepsilon$ và $\varepsilon$ . Ở SE thứ nhất ta có $q \ge \frac{4}{5}$ , nếu $q > \frac{4}{5}$ thì (II) sẽ chơi $l_2$ , nếu $q = \frac{4}{5}$ , tiện ích của (II) khi chơi $l_2$ và $r_2$ lần lượt là:

```math
\left\{ \begin{array}{l}
\frac{4}{5} \times 2 + \frac{1}{5} \times 4 = \frac{{12}}{5}\
\frac{4}{5} \times 1 + \frac{1}{5} \times \left( {8\left( {1 - \varepsilon } \right) + 2\varepsilon } \right) = \frac{1}{5}\left( {12\varepsilon  - 6} \right)
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ (II) sẽ chơi $l_2$ và khi đó ta thu được THPE  $\left( {L,{\rm{ }}{l_2},{\rm{ }}{l_3}} \right)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tương tự ở SE thứ 2, $q = \frac{4}{5}$ $\Longrightarrow$ (II) cũng sẽ chơi $l_2$ $\Longrightarrow$ SE $\left( {\frac{4}{5}M + \frac{1}{5}R,\frac{1}{6}{l_2} + \frac{5}{6}{r_2},{l_3}} \right)$ không phải là THPE <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ở SE cuối cùng, dễ thấy độ run tay của cả 3 tay chơi đều không ảnh hưởng tới chiến lược của họ, nên $\left( {R,{\rm{ }}{r_2},{\rm{ }}{l_3}} \right)$ là THPE. Ta thấy rằng, dù SPE, SE đã mang ý niệm về “bàn tay run”, song chúng chưa áp dụng định đề này một cách nhất quán. Tại sao ta lại cho rằng tay chơi (I) có thể run tay - đưa trò chơi vào tập thông tin $\{ 15,16 \}$ , nhưng tay chơi (III) thì không ? <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *f. Cân bằng thích hợp* <br>
&nbsp;&nbsp;&nbsp;&nbsp;THPE gán cho mỗi hành động phi lý của người chơi một xác suất dương tiệm cận 0, nhưng lờ đi sự so sánh xác suất của 2 hành động phi lý. Điều này có lẽ cũng không phản trực giác lắm, bởi vì ta không có thói quen so sánh 2 giá trị vô cùng bé, và nếu 2 hành động đều sinh ra từ sự lỡ tay của người chơi, thì chẳng lẽ họ lại còn phân phối xác suất cho nó? Tuy nhiên, có những căn nguyên rất hợp lý để cho rằng, giữa 2 hành động phi lý, người chơi sẽ thực hiện hành động đem lại thiệt hại lớn hơn (tiện ích thấp hơn) với xác suất nhỏ hơn rất nhiều: <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi đó ta có: <br> 
<div align="center">

$${u_k}\left( {{s_k}^\prime ,s} \right) < {u_k}\left( {{s_k},s} \right) \to \frac{{{p_k}\left( {{s_k}^\prime ,s} \right)}}{{{p_k}\left( {{s_k},s} \right)}} = \varepsilon $$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;trong đó $s_k$ là chiến lược của tay chơi $k$ , $s$ là tập chiến lược mà các tay chơi còn lại lựa chọn, $u_{k} \( s_{k};s \)$ là tiện ích của tay chơi $k$ ứng với kết quả đó và $p_{k} \( s_{k};s \)$ là xác suất mà anh ta gán cho $s_k$ khi những người còn lại chơi $s$ ). Một THPE đạt được điều kiện trên là một ***<ins>cân bằng thích hợp (PE-proper equilibrium)</ins>*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.8:</ins>* Cho hình vẽ sau<br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ea7ea034-3f85-4bc2-aa13-f69e9628a578)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi giữa 2 người chơi (I) và (II) (hình trên) có các nút 2 và 3 cùng nằm trong một tập thông tin chung (ký hiệu bằng đường đứt đoạn thay vì hình oval). Trò chơi có vô hạn NE: (I) chắc chắn sẽ chơi $L$ - chiến lược thống trị nghiêm ngặt, và (II) có thể làm bất cứ cái gì. Tất cả NE đều là THPE, vì (II) có thể ấn định bất cứ niềm tin nào cho tập thông tin $\\{ 2,3 \\}$ (nguyên lý của THPE cho phép tỉ số $\frac{p\( M \)}{p\( R \)}$ nhận giá trị tùy ý khi chúng đều là các xác suất tiệm cận $0$ ). Nhưng chỉ có 1 PE duy nhất là $\left( {L,{\rm{ }}\frac{3}{5}l + \frac{2}{5}r} \right)$ . Lấy THPE $\( L,r \)$ làm ví dụ, rõ ràng (II) chỉ chơi $r$ nếu anh ta tin rằng $q_{2} \le \frac{2}{3}$ (với $q_2$ là xác suất (II) ở nút 2 khi trò chơi đã đi vào tập thông tin $\\{ 2,3 \\}$ ), nhưng lúc này (I) lại ấn định $\frac{p\( R \)}{p\( M \)} = \varepsilon$ (với (I) nhận được 0 khi chơi $R$ và 3 khi chơi $M$ ), đồng nghĩa: 

```math
{q_2} = \frac{{{p_M}}}{{{p_R} + {p_M}}} = {\left. {\frac{1}{{1 + \varepsilon }}} \right|_{\varepsilon  \to {0^ + }}} \to {1^ - }
```
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Khi ấy ta kết luận $\( L, r \)$ không phải là PE <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta nhận ra là tại kết quả PE, (II) phải chơi các chiến lược giống như trong một NE của trò chơi con bắt đầu từ nút $1'$ ở hình dưới. Thật vậy, (II) sẽ chơi chiến lược tối ưu theo niềm tin của mình $\( q_{2};q_{3} \)$ vốn phụ thuộc vào $\frac{p\( M \)}{p\( R \)}$ , ngược lại, (I) cũng tối đa hóa tiện ích của mình tại tập $\\{ 2,3 \\}$ bằng cách điều chỉnh $\frac{p\( M \)}{p\( R \)}$ theo chiến lược của (II). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Điều này hóa ra lại rất có sức thuyết phục, nó tạo nên "tính bất biến của lời giải" - một lời giải bền vững với các cách biểu diễn khác nhau của cùng một trò chơi. PE trong trò chơi ban đầu (trên) là SPE duy nhất trong một dị bản của nó (dưới) - về bản chất vẫn giống với trò chơi gốc. Hành động $T$ tương đương với "không chọn $L$", ở nút $1'$ , (I) bắt đầu suy nghĩ về việc chọn $M$ hay $R$ sau khi lỡ tay bỏ phí kết quả hấp dẫn $\( 4,0 \)$ . Lời giải hợp lý nhất là PE, vì nó làm cho trò chơi con xuất phát từ nút $1'$ cũng đạt được NE. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dù vẫn còn các tranh cãi xung quanh định đề "tối thiểu hóa thiệt hại do run tay", hãy nghĩ về lời giải này như một phản ứng tối ưu của (II) cho tình huống (I) lỡ tay đưa trò chơi vào tập thông tin $\\{ 2,3 \\}$ . <br>
### 4. Trò chơi có thông tin không đầy đủ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Người chơi tự nhiên* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Sinh viên $B$ đến thư viện để chuẩn bị cho bài thi môn LTTC vào ngày mai thì gặp $A$ - một tay ngang đến tìm sách nhập môn về LTTC, họ chưa từng biết nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có 2 loại sách cho $A$ chọn là cơ bản (M) và nâng cao (E) (giả sử $A$ chỉ có đủ thời gian để đọc trọn vẹn 1 quyển). $B$ có thể: ở lại thư viện ôn thi qua đêm (L) hoặc mượn sách về nhà (H). Từ cuộc trò chuyện với thủ thư về $A$ - người hay đến đây đọc sách, $B$ biết $A$ thuộc 1 trong 2 kiểu người: xuất chúng $A_1$ -xác suất 0.7 hoặc bình thường $A_2$ - xác suất 0.3 (ta cũng giả định $A$ biết $B$ đã nắm được bao nhiêu thông tin về $A$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các mức tiện ích của $A$ : 1 _đọc sách không phù hợp với khả năng; 2 _đọc sách phù hợp; 3 _đọc sách không phù hợp nhưng được học cùng với $B$ ; 4 _đọc sách phù hợp và học cùng $B$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các mức tiện ích của $B$ : 1 _ở lại và học cùng $A_1$ (đạt điểm cao); 0 _ôn thi ở nhà (điểm thi trung bình); -1 _ở lại học cùng và mất thời gian với $A_2$ (điểm thấp). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tình huống trên là một trò chơi có thông tin hoàn hảo ( $A$ hành động trước $B$ , $B$ thấy rõ hành động của $A$ ) nhưng không đầy đủ vì $B$ không biết chính xác các tiện ích của mình và của đối phương ở mỗi kết quả. Harsanyi (đồng giải Nobel với Nash và Selten, 1994) giải quyết khó khăn này bằng cách thêm vào 1 người chơi ảo gọi là "Tự nhiên" ( $N$ - nature), điều này sẽ được diễn giải chi tiết bằng *ví dụ* nêu sau đây. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 4.1:</ins>* Cho hình vẽ sau<br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/c82df17e-77ba-409e-b863-e3ac91780ac4)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Bằng cách quy ước 1 người chơi ảo là $N$ , ta có thể biểu diễn trò chơi về dạng mở rộng, trong đó $N$ đi nước đầu tiên để ấn định $A$ là $A_1$ hay $A_2$ , với chiến lược hỗn hợp $0.7{a_1} + 0.3{a_2}$ . $N$ đặc biệt so với các người chơi khác ở chỗ: không có tiện ích và luôn phân phối xác suất cho các chiến lược theo một cách cố định - tất cả người chơi đều biết phân phối đó (thông tin chung). Dĩ nhiên khi hành động thì $A$ đã biết mình là ai ( $A_1$ và $A_2$ ở 2 nút thông tin tách biệt, có thể đưa ra quyết định khác nhau). Ngược lại, các nút 17,18 thuộc cùng một tập thông tin ( $19,20$ cũng vậy) bởi $B$ không biết hành động của $A$ đến từ nút $A_1$ hay $A_2$ . Cách biểu diễn này đã biến trò chơi có thông tin không đầy đủ thành trò chơi có thông tin không hoàn hảo (nhưng đầy đủ), từ đây nó có thể được giải theo cách thông thường. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi thuộc dạng này được gọi là trò chơi Bayes và các NE của nó được gọi là ***<ins>BNE (bayesian nash equilibrium)</ins>***. Trò chơi Thư viện của chúng ta có các BNE là: <br>

```math
\left\{ \begin{array}{l}
\left( {EE,{\rm{ }}L\left( {rL + \left( {1 - r} \right)H} \right)} \right),r \le \frac{1}{2}\
\left( {MM,{\rm{ }}\left( {sL + \left( {1 - s} \right)H} \right)L} \right),s \le \frac{1}{2}
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp; $B$ chơi $LH$ nghĩa là $B$ chơi $L$ ở tập thông tin $\\{ 17,18 \\}$ và chơi $H$ ở $\\{ 19,20 \\}$ ; $A$ chơi $EM$ nghĩa là $A$ sẽ chơi $E$ nếu là $A_1$ và chơi $M$ nếu là $A_2$. Cần lưu ý rằng $A_1$ và $A_2$ về bản chất không phải là cùng 1 người, do đó các tiện ích của họ là riêng biệt, $A_1$ không quan tâm đến tiện ích của $A_2$ và ngược lại. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Cân bằng Bayes hoàn hảo* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trước khi đi sâu vào lời giải cho trò chơi *Thư viện* , ta nói qua một chút về ***<ins>cân bằng Bayes hoàn hảo (PBE-perfect bayesian equilibrium)</ins>***. Một PBE cũng gồm 2 phần: chiến lược và niềm tin-như một SE. Một BNE là PBE khi niềm tin của mỗi tay chơi là nhất quán với chiến lược của những tay chơi khác. Khác với SE, PBE không yêu cầu chiến lược của mỗi tay chơi phải là tối ưu đối với niềm tin của tay chơi khác, điều này có thể dẫn đến những tình huống như ở *Con ngựa Selten*. Do đó PBE là một bộ lọc mạnh hơn SPE nhưng yếu hơn SE, nó thường chỉ được sử dụng trong trò chơi Bayes (dù về nguyên tắc có thể áp dụng cho bất cứ trò chơi mở rộng nào). Cũng có thể dùng SE và các cân bằng mạnh hơn SE đã nêu ở ***mục 3/*** để lọc các PBE trong trò chơi Bayes. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 4.2:</ins>* Cho thư viện hình vẽ sau<br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/0d041873-8ba4-4e2d-aaf2-eb70d65b9c15)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ở trò chơi Bayes trong hình, $N$ ấn định xác suất cho 2 kiểu người chơi $A_{1} , A_{2}$ là $p$ và $1-p$ , trò chơi luôn có các BNE sau với mọi $p$ : $\left( {LL,{\rm{ }}l} \right),{\rm{ }}\left( {RR,{\rm{ }}tl + \left( {1 - t} \right)r} \right),t \le \frac{1}{2}$ . Niềm tin của $B$ tại tập thông tin $\\{ 21,22 \\}$ ấn định xác suất cho các nút 21,22 là $q,1-q$ . $B$ sẽ điều chỉnh các chiến lược của mình tối ưu theo $q$ . Tuy nhiên tiện ích trung bình của $B$ khi chơi $l$ và $r$ lần lượt là: $1 \times q + 0 \times \left( {1 - q} \right) = q$ và $0 \times q + \left( { - 1} \right) \times \left( {1 - q} \right) = q - 1$ $\Longrightarrow$   $B$ sẽ luôn chơi $l$ trong mọi tình huống. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ BNE $\left( {RR,{\rm{ }}tl + \left( {1 - t} \right)r} \right),t \le \frac{1}{2}$ không phải là PBE, bởi vì chiến lược $\left( {tl + \left( {1 - t} \right)r} \right),t \le \frac{1}{2}$ của $B$ không phù hợp với bất cứ niềm tin nào mà anh ta có thể có tại $\\{ 21,22 \\}$ . Ở đây ta thấy một logic tương tự SPE nhưng được áp dụng lên 1 tập thông tin thay vì 1 nút thông tin đơn lẻ: $B$ đe doạ sẽ chơi $\left( {tl + \left( {1 - t} \right)r} \right),t \le \frac{1}{2}$ khi trò chơi đi vào tập thông tin $\\{ 21,22 \\}$ nhưng nếu điều đó thật sự xảy ra thì $B$ lại không làm thế, đây là một lời đe dọa không đáng tin. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Vậy trò chơi chỉ có duy nhất 1 PBE là $\( LL, l \)$ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Tiêu chuẩn trực quan* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Rất dễ để nhận ra tất cả BNE trong trò chơi Thư viện đều là PBE, thậm chí là PE nếu ta loại đi 2 PBE ứng với $r=\frac{1}{2}$ và $s=\frac{1}{2}$ . “Cho & Kreb” [1987] đề xuất bộ lọc ***<ins>Tiêu chuẩn trực quan (IC-intuitive criterion)</ins>***, cho phép loại bỏ “PBE - $\sigma$ ” nếu ở đó tồn tại kiểu người chơi $\theta$ có lợi khi đi chệch khỏi $\sigma$ (thu được tiện ích cao hơn so với ở $\sigma$ ) miễn là những người chơi khác giữ niềm tin với xác suất $0$ cho mọi hành động đi chệch khỏi $\sigma$ của kiểu người chơi $T$ mà không có lợi cho $T$ trong bất kỳ trường hợp nào. Ở trò chơi Thư viện, IC loại bỏ PBE $\left( {MM,{\rm{ }}\left( {sL + \left( {1 - s} \right)H} \right)L} \right),s \le \frac{1}{2}$ . Thật vậy, $A_2$ chẳng có lợi gì khi đi chệch khỏi PBE này cả ( $A_2$ chơi $E$ nhận được 3 hoặc 1, đều thấp hơn 4 khi chơi $M$ ), nếu tại $\\{ 17,18 \\}$ , $B$ ấn định xác suất $0$ cho $A=A_{2}$ thì $B$ sẽ chơi $L$ , khi đó $A_1$ có lợi nếu chơi $E$ - đi chệch khỏi PBE ban đầu $\( 4>3 \)$ . Ngược lại, PBE $\left( {EE,{\rm{ }}L\left( {rL + \left( {1 - r} \right)H} \right)} \right),r \le \frac{1}{2}$ không bị lọc bởi IC, mặc dù $A_1$ không có lợi gì khi thay đổi chiến lược từ $E$ sang $M$ $\( 1<4, 3<4 \)$ nhưng $A_2$ cũng vậy nếu $B$ giữ niềm tin $A=A_{2}$ và chơi $H$ tại $\\{ 19,20 \\}$ $\( 2<3 \)$ . Kết hợp định đề của PE, ta thu được PBE $\left( {EE,{\rm{ }}L\left( {rL + \left( {1 - r} \right)H} \right)} \right),r \le \frac{1}{2}$ vừa là PE vừa thỏa mãn IC. Vậy là $A$ sẽ lấy sách nâng cao dù $A$ là $A_1$ hay $A_2$  trước mặt $B$ , và $B$ chọn ở lại thư viện qua đêm để học cùng $A$ . <br> 
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Quy nạp ngược và quy nạp xuôi* <br>
&nbsp;&nbsp;&nbsp;&nbsp;IC đã gây nhiều tranh cãi trong giới hàn lâm. Khác với các bộ lọc ở ***mục 3/*** dựa trên nền tảng là *quy nạp ngược* - giả định người chơi luôn hành động duy lý trong tương lai ngay cả khi anh ta đã mắc sai lầm trong quá khứ *(bàn tay run)*, IC dựa trên *quy nạp xuôi* - giả định hành động trong quá khứ của người chơi là duy lý. Ở trò chơi Thư viện, tại PBE bị lọc bởi IC, việc $B$ ấn định xác suất để $A=A_{2}$ tại $\\{ 17,18 \\}$ là $0$ tương đương với việc $B$ tin $A_2$ sẽ chơi $E$ với xác suất $0$ và $A_1$ chơi $E$ với xác suất dương, vì $A_2$ chẳng có lợi gì khi chơi $E$ , còn $A_1$ thì có. Quy nạp xuôi diễn giải hành động đi chệch khỏi cân bằng ( $A$ chơi $E$ ) là động thái để đạt được lợi ích lớn hơn ( $A$ chỉ có thể là $A_1$ - đang cố nhắm tới tiện ích 4 ở nút $17L$ ), trái với *quy nạp ngược* chỉ coi đó là một sai lầm của người chơi ( $A_2$ có thể lỡ tay chơi $E$ với xác suất dương). Bởi sự mâu thuẫn này, rất khó để áp dụng đồng thời *quy nạp ngược và xuôi*. Cũng không thể bắt chước logic của PE để nói rằng xác suất $A_2$ chơi $E$ rất nhỏ so với $A_1$ chơi $E$ , bởi vì $A_1$ và $A_2$ không phải là cùng 1 người. <br>
### 5. Bản chất tiện ích, đạo đức, và hiệu quả <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bản chất tiện ích* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có thể xác định nhanh chóng hàm tiện ích ở những tình huống mà lợi ích quy ra giá trị rõ ràng (tiền bạc, vật chất, ...). Nhưng thường thì mọi chuyện không đơn giản như thế, bởi tiện ích liên quan tới các biến số tâm lý rất khó để đo lường (niềm vui sướng chẳng hạn). Ở trò chơi Qua cầu, nếu tất cả những gì người chạy trốn quan tâm là sự sống chết của mình chứ không phải cách thức chết, và tất cả những gì thợ săn quan tâm là ngăn người chạy trốn thoát được thì cách thiết lập hàm tiện ích ở ***1/ a/*** là phù hợp (để ý rằng tiện ích của người chạy trốn chính là xác suất sống sót của anh ta, còn xác suất chết của anh ta là tiện ích của thợ săn). Giờ hãy giả định: Thợ săn thích nhất là tự tay kết liễu người chạy trốn, và thích người chạy trốn chết vì đá rơi/rắn cắn hơn là để anh ta thoát; người chạy trốn thích một cái chết chóng vánh bằng 1 phát đạn hơn là bị đá đè hoặc nỗi kinh hoàng khi bị rắn cắn (dĩ nhiên thích nhất vẫn là trốn thoát). Không thể giải trò chơi này nếu chỉ biết thứ tự sở thích của mỗi tay chơi, vì cường độ của mỗi sở thích giờ đây sẽ liên quan đến các chiến lược của họ. Vậy phải xây dựng hàm tiện ích như thế nào, khi đã biết dãy thứ tự các kết quả: ${L_1},{\rm{ }}{L_2},{\rm{ }}{L_3},{\rm{ }}...,{\rm{ }}{L_n}$ sắp xếp theo độ ưa thích tăng dần của tay chơi $P$ ? <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ *Von Newmann & Morgenstern* giải quyết chuyện này bằng cách ấn định 2 giá trị tùy ý cho tiện ích ứng với $L_1$ và $L_n$  thỏa mãn $u\( L_{1} \) < u\( L_{n} \)$ . Tiện ích của kết quả $L_k$ là $u\( L_{k} \) = qu\( L_{n} \) + (1-q)u\( L_{1} \)$ (với $0<q<1$) sao cho $P$ hoàn toàn trung lập (không thích cái nào hơn) giữa $L_k$ và một kết quả chưa biết có xác suất $q$ rơi vào $L_n$ và xác suất $1-q$ rơi vào $L_1$ . <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Tính đạo đức và hiệu quả* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong trò chơi ở ***Mục 3/ b/ (phần 2, ví dụ 3.4)***, chắc chắn các tay chơi cũng thấy $\\( 4,5 \\)$ là kết quả cao hơn về phương diện xã hội và đạo đức. Tuy nhiên, các động lực trong trò chơi ngăn cản nó xảy ra. Giống như ở PD game, 2 tay chơi đáng lẽ đều đã nhận được tiện ích cao hơn nếu hợp tác với nhau. Có lẽ bạn đã nghĩ sự éo le này đơn giản nảy sinh từ tính ích kỷ và bệnh hoang tưởng của những tay chơi: từ đầu họ đã không quan tâm đến thiện chí về phương diện xã hội và sau đó thì bội ước! Đây là một cách hiểu rất lệch lạc về LTTC. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các phúc lợi xã hội được thể hiện bằng khái niệm *"hiệu quả Pareto"* . Trạng thái o là ưu thế Pareto so với trạng thái d nếu ít nhất 1 tay chơi có tiện ích tăng và không tay chơi nào bị giảm tiện ích khi chuyển từ o sang d. Kết quả (-1,-1)-thể hiện sự hợp tác trong mô hình PD rõ ràng là ưu thế Pareto so với $\\( -5,-5 \\)$ - cùng phản bội. Thất bại trong việc đạt được $\\( -1,-1 \\)$ thể hiện sự phân phối tiện ích thiếu hiệu quả vì sự tồn tại của nó cho thấy một tiện ích nào đó đang bị bỏ phí tại $\\( -5,-5 \\)$ , điều này thật đáng tiếc. Tuy nhiên, thiếu hiệu quả không đồng nghĩa với "phi đạo đức". Hàm tiện ích của một tay chơi thể hiện điều mà anh ta ưa thích, nó có thể là bất cứ thứ gì. 2 tù nhân của chúng ta thực sự chỉ quan tâm đến bản án tù riêng của mình, nhưng đó không phải điểm cốt lõi. Cái duy nhất làm cho một tình huống trở thành PD game chỉ là cấu trúc tiện ích của nó. Câu chuyện dân gian về 2 anh em nông dân nghèo yêu thương nhau, rình lúc đêm đến bỏ 1 bó lúa sang nhà nhau..chính là một trò chơi đối xứng, mỗi người có tiện ích như sau: 3 _gửi lúa cho người kia mà họ không trả lại; 2 _cả hai đều không làm gì; 1 _cả hai gửi lúa cho nhau, họ đều thấy tệ vì đã làm việc vô ích mà còn khiến cho người kia thấy tệ nữa; 0 _thấy tội lỗi khi nhận lúa của người kia-cũng nghèo như họ. Vậy là 2 anh em tốt bụng đã tham gia một PD game, dù họ không nghĩ đến bản thân mà chỉ quan tâm đến sự no đủ của người còn lại. Nếu các khoản tiện ích của họ thay đổi thì họ sẽ chơi một trò chơi khác không phải PD. Điều đó chỉ ra rằng các kết quả thiếu hiệu quả không liên quan gì đến tính vị kỷ. Logic của tình huống PD, chứ không phải tâm lý của những tay chơi, là thứ đánh bẫy họ trong một kết quả thiếu hiệu quả. <br>
### 6. Những trò chơi kéo dài vô tận <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Trò chơi lặp lại* <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Trò chơi dài vô tận nhưng có kích thước hữu hạn* <br>
### 7. Lý thuyết trò chơi tiến hóa <br>


















