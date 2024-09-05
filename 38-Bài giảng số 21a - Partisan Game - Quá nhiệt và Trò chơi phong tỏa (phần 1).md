# Partisan Game - Quá nhiệt và Trò chơi phong tỏa (phần 1)
### 1. Tổng quan về trò chơi <br>
&nbsp;&nbsp;&nbsp;&nbsp; ***<ins>"Phong tỏa"</ins>*** là một partisan game với 2 người chơi là Xanh và Đỏ (Xanh thường được quy ước là Trái, và Đỏ là Phải). Chiến trường là một dải ô vuông $n \times 1$ (dải đất), mỗi người chơi khi đến lượt sẽ "xác nhận quyền sở hữu" bằng cách tô màu vào 1 ô (lô đất) trống mà mình chọn. Trò chơi kết thúc khi tất cả các ô đã bị tô màu, số điểm của Trái (Xanh) sẽ là số lượng "cạnh" hình vuông mà được tô màu xanh ở cả 2 phía. Mục đích của Trái là cố gắng tối đa hóa số lượng này, còn Phải cố gắng giảm nó xuống thấp nhất có thể. Như vậy, chỉ có các cặp ô vuông liền kề Trái-Trái (xanh-xanh) mới được tính điểm, các cặp Trái-Phải (xanh-đỏ) và Phải-Phải (đỏ-đỏ) đều không ảnh hưởng đến kết quả, không có điểm số cho người chơi Phải. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi là một phép ẩn dụ về hành vi "phong tỏa" trong kinh doanh bất động sản ngoài đời thực: 2 người chơi là 2 đại lý bất động sản đối địch nhau đang thu mua hết các lô đất trên một con phố, Trái theo chủ nghĩa phân biệt chủng tộc, cố gắng sắp đặt để các khách hàng tương lai của mình là hàng xóm của nhau, còn Phải là người theo chủ nghĩa hợp chủng, cố gắng chia tách họ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đây là một loại trò chơi đặc biệt, 2 người chơi có vai trò khác nhau và không có khái niệm thắng-thua. Lời giải tổng quát của trò chơi phải có khả năng xác định trước kết cục trận đấu (số điểm mà Trái đạt được) khi 2 người chơi đều đi những nước tối ưu, và cho biết những nước đi tối ưu ấy là gì. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi Trái luôn cố tăng tối đa điểm của mình còn Phải luôn cố giảm tối thiểu điểm của Trái, có thể áp dụng cấu trúc giá trị của một trò chơi kết hợp vào "Phong tỏa" (tại ***<ins>Bài giảng số 20</ins>*** cung cấp một cách hiểu về việc chuyển đổi từ trò chơi tính điểm sang trò chơi kết hợp), giá trị trò chơi khi kết thúc chính là số điểm của Trái. Gọi giá trị của 1 dải đất $n$ ô trống là: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnL$ nếu nó bị chặn 2 đầu bởi 2 ô xanh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnR$ nếu 1 đầu xanh và 1 đầu đỏ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$RnR$ nếu 2 đầu đều là ô đỏ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dễ thấy: $LnR$ và $RnL$ là đối xứng của nhau nên có ý nghĩa như nhau; trường hợp dải đất có (1 hoặc 2) đầu tự do (không bị chặn bởi ô màu nào cả) tương đương với việc đầu tự do bị chặn bởi 1 ô đỏ, vì ô đỏ ở đó không ảnh hưởng đến điểm số. Mỗi dải đất là 1 trò chơi con, vì thực hiện 1 nước đi ở dải đất này không phụ thuộc hoặc ảnh hưởng đến dải đất khác $\rightarrow$ giá trị của trò chơi = tổng giá trị của các dải đất cấu thành trò chơi. <br>  
#### &nbsp;&nbsp;&nbsp;&nbsp;Ví dụ: 
<div align="center">

![image](https://github.com/user-attachments/assets/2c60d693-84b0-43be-a8c2-c5274b146f11)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ta quy ước đánh dấu $L$ (Trái-xanh) và $R$ (Phải-đỏ) để phân biệt. Trong hình trên mô phỏng 5 dải đất: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	a) $L5R$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	b) $R3R$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	c) Cũng là $R3R$ , dễ thấy 2 cạnh ngoài cùng ở 2 đầu không thể tạo ra điểm số dù bạn tô màu gì vào ô vuông của chúng (chúng sẽ chỉ có màu ở 1 bên), vì vậy nên dải đất này hoàn toàn tương đương với dải đất ở b). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	d) Trái tô màu xanh vào giữa dải đất $R10R$ và làm nó bị tách thành 2 dải đất $L3R$ và $L6R$ (2 đầu tự do có thể gắn thêm 1 ô đỏ, đã giải thích ở trên). Giá trị của trò chơi này là $L3R+L6R$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	e) Dải đất gọi là $L0L$ , thật ra nó chỉ là 1 cạnh giữa 2 ô xanh, nhưng cần lưu ý rằng nó có giá trị là 1 (được tính 1 điểm theo luật chơi). Các dải $L0R$ và $R0R$ có thể bỏ qua được vì chúng đều bằng $0$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Theo luật chơi, 3 dãy $LnL$ , $LnR$ và $RnR$ được xác định bằng hồi quy như sau: Với $k$ từ $0$ đến $n-1$ , ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$L0L = 1,L0R = R0R = 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnL =\\{ LkL + L \( n-1-k \)L|LkR + L\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnR =\\{ LkL + L \( n-1-k \)R|LkR + R\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$RnR =\\{ LkR + L \( n-1-k \)R|RkR + R\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các giá trị này phần lớn ở dạng phi số và rất cồng kềnh, chỉ riêng việc tính ra chúng (dựa vào các công thức hồi quy trên) cũng đủ nặng nề chứ chưa nói đến chuyện đem cộng chúng lại với nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Vậy phải giải quyết vấn đề này như thế nào đây ? <br>

### 2. Toán tử quá nhiệt <br>
&nbsp;&nbsp;&nbsp;&nbsp;Lời giải cho các nan đề trong toán học thường dựa trên việc mở rộng khái niệm. ***<ins>"Phong tỏa"</ins>*** cũng không ngoại lệ, giải thuật tổng quát của nó cần dùng đến một loại ***<ins>phép toán mới - quá nhiệt</ins>***, có cách hoạt động gần tương tự "làm mát và làm ấm" trong tàn cục cờ vây. Trước khi giới thiệu về quá nhiệt, ta sẽ điểm lại một số định lý trong các bài cũ để thuận tiện cho việc trích dẫn và tra cứu. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-①: Mục 1.5a ở bài Nhiệt đồ (bài giảng số 20) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-②: Hệ quả của (3.3) ở bài Số siêu thực, mục 6 (bài giảng số 17) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-③: Mục (1.5c) ở bài Nhiệt đồ mục 1 (bài giảng số 20) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-④: Hệ quả của định lý tránh số nguyên ở bài Số siêu thực, mục 7 (bài giảng số 17) <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.1a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Định nghĩa phép toán "quá nhiệt từ $s$ tới $t$ " đối với $G$ ( $G,s,t$ là các trò chơi tùy ý, $s>0$ ) bằng đệ quy như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\int_s^t G  = G \bullet s$ nếu $G \in \mathbb{Z}$ 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\int_s^t G  = \\{ {\int_s^t {GL + t} |\int_s^t {GR - t} } \\}$ nếu $G \notin \mathbb{Z}$ <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.1b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; Định nghĩa: $\oint G = \int_1^{* + 1} G$  là phép toán giới hạn trên $G \in \\{ {n,n + *{\rm{ }}:n \in \mathbb{R}} \\}$ <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Ta quy ước kí hiệu $\approx$ như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $a = n \pm \delta$ (với $n$ là số, $\delta  \to {0^+}$ thì ta nói $a \approx n$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $a \approx c$ và  $b \approx c$ thì theo tính chất bắc cầu ta suy ra  $a \approx b$ <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 1.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Ta luôn có: $l\left( {G + \ast} \right) \approx l\left( G \right),{\rm{ }}r\left( {G + \ast} \right) \approx r\left( G \right)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.3:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với trò chơi $G$ tùy ý, xét số $x$ bất kỳ thỏa $l\left( G \right) \ne x - \delta ,l\left( G \right) < x \to \exists x':l\left( G \right) < x' < x \to G \le x'$  (theo ①) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $G + \ast \le x' + \ast < x \to l\left( {G + \ast} \right) < x$ (theo ①). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi vậy, $l \( G + \ast \) \lessapprox l(G)$ , nhưng nếu coi $G' = G + \ast$ thì $l\( {G' + \ast} \) \lessapprox l \( {G'} \) \Leftrightarrow l\( G \) \lessapprox l \( {G + \ast} \)$ . Từ đây suy ra $l \( {G + \ast} \) \approx l \( G \),{\rm{ }}\forall G$ . Khi đó ta chỉ ra $r \( {G + \ast} \) \approx r \( G \)$ theo cách tương tự. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.3*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 1.4:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G \in \\{ {n,{\rm{ }}n + \ast {\rm{ }}:n \in \mathbb{R}} \\} \backslash \mathbb{Z}$ thì $\oint G$ là phi số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 1.4:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $G = n + \ast {\rm{ }} \( {n \in \mathbb{Z}} \),G = \\{ {n + 1 + \ast|n - 1 + \ast} \\} = n \pm 1 + \ast$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $G \in \\{ {n,{\rm{ }}n + \ast:n \in \mathbb{R} \backslash \mathbb{Z} } \\},\exists k \in \mathbb{Z} :k < G < k + 1$ $\rightarrow$ Theo ②, có: $k \le G' \le k + 1$ với $G'$ là tùy chọn (dạng $x$ hoặc $x + \ast$ , với $x$ là số) phát sinh từ $G$ (#). Ta quy nạp theo giả thiết ***(1.4)*** đúng với mọi $G'$ , và cho thấy nó cũng đúng với $G$ . Giả sử $\oint G$ là số, ta có: <br> 
&nbsp;&nbsp;&nbsp;&nbsp; $r \( {\oint GL + 1 + \ast} \) < \oint G < l \( {\oint GR - 1 + \ast } \)$ (theo ①). Bởi ③, ***(1.3)*** , giả thiết quy nạp, định nghĩa của $r,l$ , ta có:<br>

&nbsp;&nbsp;&nbsp;&nbsp; $r \( {\oint GL + 1 + \ast} \) \approx r \( {\oint GL} \) + 1 = l \( {\oint GLR - 1 + \ast} \) + 1 \approx l \( {\oint GLR} \) \approx r \( {\oint GLRL} \) + 1 \approx l \( {\oint GLRLR} \) \approx ... \approx k + 1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;(theo #, với $G' \in \mathbb{Z}$ , nếu $G'=G...L$ thì $G'=k$ , nếu $G'=G...R$ thì $G'=k+1$ ); tương tự, ta cũng có được: <br>  
&nbsp;&nbsp;&nbsp;&nbsp; $l \( {\oint GR - 1 + \ast} \) \approx l \( {\oint GR} \) - 1 \approx r \( {\oint GRL} \) \approx l \( {\oint GRLR} \) - 1 \approx r \( {\oint GRLRL} \) \approx ... \approx k$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ đây ta có $k + 1 \lessapprox \oint G \lessapprox k \to k + 1 \lessapprox k$ , điều này là vô lý! $\Rightarrow$ $\oint G$ không thể là số (đpcm). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 1.4*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 1.5:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $\oint \( {G + H} \) = \oint G + \oint H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.5:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ ***(1.1b), (1.4)***, và ④, ta chỉ ra ***(1.5)*** đúng $\forall G,H \in \\{ {n,{\rm{ }}n + \ast {\rm{ }}:n \in \mathbb{R} } \\}$ bằng quy nạp. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.5*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 1.6:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $\oint G \ge \oint H \to \;G \ge H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.6:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $M=G-H$ , có $\oint M = \oint G - \oint H$ (theo ***1.5***). Cần chỉ ra: $\oint M \ge 0 \to M \ge 0$ ***(1.6o)***. Thật vậy, nếu $M \in \mathbb{Z}$ thì ***(1.6o)*** là hiển nhiên, với $M \notin ,\oint M \ge 0{\rm{ }} \Leftrightarrow$ Phải luôn thua khi đi trước trong $\oint M{\rm{ }} \Leftrightarrow \forall MR$ , Trái có nước đi chiến thắng trong $\oint MR - 1 + \ast {\rm{ }} \Leftrightarrow \forall MR,\oint MR - 1 = \oint \( {MR - 1} \) \ge 0$ hoặc $\exists MRL:\oint MRL \ge 0$ ; nếu ***(1.6o)*** đúng khi thay $M$ bằng $MR - 1,MRL$ thì $\forall MR,\exists MRL \ge 0{\rm{ }} \Leftrightarrow$ Phải luôn thua khi đi trước trong $M$ $\Leftrightarrow \ge 0$ , ***(1.6o)*** cũng đúng với $M$ (quy nạp). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.6*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $\oint G = \oint H \Leftrightarrow G = H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\oint G = \oint H \Leftrightarrow \oint G \ge \oint H$ và $\oint G \le \oint H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $G \ge H$ mà theo ***1.6*** ta có: $G \le H$ nên suy ra $G = H$ . 
&nbsp;&nbsp;&nbsp;&nbsp;Ngược lại, nếu $G = H$ , thì $\to \oint G - \oint H = \oint \( {G - H} \) = \oint 0 = 0$ (theo ***1.5***) có nghĩa là khi tính $\oint G$ , $G$ không bắt buộc phải ở dạng hợp quy. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***hệ quả*** <br>

### 3. Giải thuật tổng quát <br>





