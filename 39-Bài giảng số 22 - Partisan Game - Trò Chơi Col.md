# Partisan Game - Trò Chơi Col
### 1. Tổng quan về trò chơi.
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Col</ins>*** là một trò chơi mà 2 người chơi sẽ lần lượt tô màu các khu vực trong một bản đồ theo quy tắc: 2 khu vực liền kề (chung đường biên giới) không được phép có cùng màu. Người chơi không thể thực hiện nước đi hợp lệ ở lượt của mình sẽ thua. Trò chơi được mô tả và phân tích bởi John Conway, người đã gán nó cho Colin Vout. <br>
<div align="center">

![image](https://github.com/user-attachments/assets/b9d72cd4-537f-4eb7-a200-c9a76fea919f)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi kết thúc bởi vì tô bất cứ màu nào lên các vùng đất còn lại của bản đồ cũng đều phạm luật. Trong tình huống này ai vừa thực hiện nước đi cuối cùng là người chiến thắng (mà có lẽ bạn cũng nhận ra đó là Đỏ rồi, vì có 4 vùng đã tô đỏ và 3 vùng tô xanh, đây lại là một trò chơi mà 2 người đi lần lượt). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Như mọi partisan game khác, Col có thể được giải bằng Lý thuyết trò chơi kết hợp (xem lại các bài giảng trước) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giải thuật của Col không có gì đặc biệt bởi vì: Tất cả các giá trị xuất hiện trong trò chơi đều có dạng $n$ hoặc $n+\ast$ , với $n$ là số (do đó tổng của chúng có thể được tính toán dễ dàng).  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có một chứng minh đơn giản cho điều này: Chỉ ra bất đẳng thức sau đúng với mọi game $G$ trong trò chơi Col: $GL + \ast \le G \le GR + \ast$ . <br>
### 2. Chứng minh giải thuật. 
&nbsp;&nbsp;&nbsp;&nbsp;Trước hết ta có hình vẽ như sau: <br>
<div align="center">

![image](https://github.com/user-attachments/assets/2c866573-edab-413d-aa6c-fb612e11aeda)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ giản lược hóa bản đồ bằng cách biểu diễn các vùng đất như các điểm (nút đồ thị), còn biên dưới giữa 2 vùng đất là đường nối giữa 2 điểm (cạnh đồ thị). Có 4 loại nút trong đồ thị được ký hiệu như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.	• là vùng đất mà ai cũng có thể tô màu lên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.	◙ là vùng đất chỉ Trái (Xanh) có thể tô màu lên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.	◘ là vùng đất chỉ Phải (Đỏ) có thể tô màu lên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.	⊗ là vùng đất mà không ai sử dụng được. <br>
&nbsp;&nbsp;&nbsp;&nbsp;(*) Theo quy tắc trò chơi là 2 nút liền kề nhau không được có cùng màu, có các nhận xét sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tô xanh ở 1 nút (chỉ thực hiện được ở •,◙) sẽ làm các nút liền kề với nó: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.	◘,• đều trở thành ◘ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.	◙,⊗ đều trở thành ⊗ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-  Tô đỏ ở 1 nút (chỉ thực hiện được ở •,◘) sẽ làm các nút liền kề với nó: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.	◙,• đều trở thành ◙  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.	◘,⊗ đều trở thành ⊗ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ chứng minh $GR + \ast \ge G$ bằng cách chỉ ra: Phải luôn thua khi đi trước trong $GR + \ast -G$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Xét một game $G$ bất kỳ trong trò chơi Col, một nước đi của Phải sẽ đưa $G$ về $GR$ . Nước đi này chắc chắn sẽ là chơi 1 nút • hoặc ◘ (theo định nghĩa của các ký hiệu này). Không mất tính tổng quát, giả định nút đó là • (trường hợp ◘ có thể được chứng minh theo cách hoàn toàn tương tự), nút này sẽ liên kết với 3 loại nút khác là •, ◙, ◘, nút ⊗ có thể bỏ qua vì nó không có ý nghĩa trong trò chơi. Sau khi Phải chơi nút trên (tô màu đỏ), nó trở thành ⊗ (và có thể loại bỏ khỏi đồ thị), với 3 loại nút liên kết với nó: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • trở thành ◙      ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ◙ giữ nguyên       ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ◘ trở thành ⊗     ; <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\to$  đồ thị $G$ trở thành đồ thị $GR$ , từ đó ta có game $GR + \ast -G$ được mô tả như trong hình, với lưu ý rằng: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1) Nút • đứng độc lập có giá trị là $\ast$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2) Bởi dấu - đằng trước game $G$ , các nước đi của 2 người chơi tại đây sẽ bị đảo ngược lại, Phải (Trái) sử dụng các nước đi của Trái (Phải) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3) Miền tô đậm (tạm gọi là $K$ ) là không gian còn lại của đồ thị mà các nút và cạnh không được biểu diễn cụ thể ra. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu Phải đi trước trong $GR + \ast -G$ , có các trường hợp sau đây tùy theo nước đi đầu tiên của Phải: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 1:</ins>*** chơi ở * (nút •) $\to$ game trở thành $GR-G \parallel > 0$ , Trái đi tiếp và thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 2:</ins>*** chơi 1 nút trong miền $K$ của đồ thị $GR(G)$ , Trái chơi ở nút tương ứng trên đồ thị $GR(G)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 3:</ins>*** chơi ở nút • không gắn với $K$ trong $G$ (tô xanh), Trái chơi ở  $\ast$ . Áp dụng ( $\ast$ ) để xác định các thay đổi sau 2 nước đi, dễ thấy trong game mới tạo ra (Phải đi trước): 6 nút được biểu thị không thể được sử dụng bởi Phải trong các lượt tiếp, nếu Trái thực hiện các thao tác như ở trường hợp 2, Trái sẽ là người đi nước sau cùng và thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 4:</ins>*** chơi ở nút • (gắn với $K$ ) hoặc ◙ trong $G$ (tô xanh), Trái chơi ở vị trí tương ứng trên $GR$ (tô xanh). Trong game mới tạo ra: nút • không gắn với $K$ ở $G$ trở thành ◘ (chỉ có thể được chơi bởi Trái), nếu Phải chơi $\ast$ thì Trái chơi nút này, nếu Phải chơi bất cứ nút nào trên $GR(G)$ thì Trái chơi ở vị trí tương ứng trên $G(GR)$ $\to$ Trái sẽ là người đi nước sau cùng và thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Từ các trường hợp trên suy ra Phải luôn thua khi đi trước trong $GR + \ast -G$ $\Leftrightarrow$ $GR + \ast -G \ge 0$ $\rightarrow$ $GL + \ast \le G$ (do tính đối xứng) $\to$ $GL + \ast \le G \le GR + \ast$ (đpcm). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy suy ra: $Gl \le GR$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt giả thiết quy nạp rằng: $GL,GR \in \\{ {n,{\rm{ }}n + \ast {\rm{ }}:n \in \mathbb{R}} \\}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $GL=GR$ thì $G = \\{ {n|n} \\} = n + \ast$ hoặc $G = \\{ {n + \ast|n + \ast} \\} = n$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $GL<GR$ thì $GR-GL=d$ hoặc $d + \ast {\rm{ }} \( {d \in {\mathbb{R}^+}} \)$ . Suy ra: $\exists d' \in \mathbb{R} {\rm{ }}:0 < d' < d$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\to$ $GL < GL + d' < GR$ và $GL < GL + d' + \ast < GR$ với 1 trong 2 giá trị $GL + d',{\rm{ }}GL + d' + \ast$ là số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $G = \\{ {GL|GR} \\}$ là số (xem lại ***Số siêu thực mục 6, hệ quả của 3.3, bài giảng số 17d***) <br>

&nbsp;&nbsp;&nbsp;&nbsp;Từ đây ta kết luận: $G \in \\{ {n,{\rm{ }}n + \ast {\rm{ }}:n \in \mathbb{R}} \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***giải thuật*** trên. <br>









