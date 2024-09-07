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
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $M=G-H$ , có $\oint M = \oint G - \oint H$ (theo ***1.5***). Cần chỉ ra: $\oint M \ge 0 \to M \ge 0$ ***(1.6o)***. Thật vậy, nếu $M \in \mathbb{Z}$ thì ***(1.6o)*** là hiển nhiên, với $M \notin ,\oint M \ge 0{\rm{ }} \Leftrightarrow$ Phải luôn thua khi đi trước trong $\oint M{\rm{ }} \Leftrightarrow \forall MR$ , Trái có nước đi chiến thắng trong $\oint MR - 1 + \ast {\rm{ }} \Leftrightarrow \forall MR,\oint MR - 1 = \oint \( {MR - 1} \) \ge 0$ hoặc $\exists MRL:\oint MRL \ge 0$ ; nếu ***(1.6o)*** đúng khi thay $M$ bằng $MR - 1,MRL$ thì $\forall MR,\exists MRL \ge 0{\rm{ }} \Leftrightarrow$ Phải luôn thua khi đi trước trong $M$ $\Leftrightarrow M \ge 0$ , ***(1.6o)*** cũng đúng với $M$ (quy nạp). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.6*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $\oint G = \oint H \Leftrightarrow G = H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\oint G = \oint H \Leftrightarrow \oint G \ge \oint H$ và $\oint G \le \oint H$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $G \ge H$ mà theo ***1.6*** ta có: $G \le H$ nên suy ra $G = H$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ngược lại, nếu $G = H$ , thì $\to \oint G - \oint H = \oint \( {G - H} \) = \oint 0 = 0$ (theo ***1.5***) có nghĩa là khi tính $\oint G$ , $G$ không bắt buộc phải ở dạng hợp quy. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***hệ quả*** <br>

### 3. Giải thuật tổng quát <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G$ là giá trị của trò chơi Phong tỏa và $G \notin \mathbb{Z}$ thì $G + \ast = \\{ {GL + \ast|GR + \ast} \\}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dễ thấy $R1R = \ast$ $\to$ Trò chơi $G+\ast$ tương đương với $G+R1R$ . Việc đi vào $R1R$ là vô dụng với cả 2 người chơi (nó không mang lại điểm số cho Trái). Mặt khác, đi trước trong trò chơi $G$ luôn có lợi hơn. Thật vậy, giả sử Trái thu được mức điểm lớn hơn khi đi sau, Trái sẽ có một chiến lược $S$ tối ưu để đối phó với mọi nước đi của Phải. Sử dụng lập luận đánh cắp chiến lược (xem lại ***<ins>bài giảng số 15</ins>***) xét trường hợp Trái đi trước, ta cho Trái sử dụng lại $S$ , diễn biến sẽ tương tự như trường hợp Trái đi sau, chỉ khác là có thêm 1 ô xanh "bổ sung" trên chiến trường. Hệ quả là khi trò chơi kết thúc, nếu Phải đi nước cuối cùng, bố cục các ô màu sẽ y hệt như TH Trái đi sau; nếu Trái đi cuối cùng, bố cục các ô màu giống như trường hợp Trái đi sau trừ 1 ô đỏ bị đổi thành xanh $\to$ Số điểm của Trái khi đi trước luôn bằng hoặc lớn hơn khi đi sau $\to$ Đi trước có lợi cho Trái hơn. Lập luận tương tự để chỉ ra đi trước cũng có lợi hơn cho Phải $\to$ Từ những điều trên, người đi trước trong $G+\ast$ luôn tránh chơi ở $\ast$ vì đó là nước đi vô dụng, lại còn làm cho đối thủ được chơi trước ở $G$ trong lượt tiếp theo $\to$ $G + \ast = \\{ {GL + \ast|GR + \ast} \\}$ (đpcm). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 2.1*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.2a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $L_{n}L=n \bullet \ast + \oint x_{n}$ , $L_{n}R=n \bullet \ast + \oint y_{n}$ , $R_{n}R=n \bullet \ast + \oint z_{n}$ sao cho thỏa mãn hai điều kiện như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ***(2.2a1)***: $x_{n},y_{n},z_{n} \in \\{ m,m+\:m \in \mathbb{R} \\}$ (mục đích là để các phép toán về hàm $\oint$ sử dụng được). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ***(2.2a2)***: $\\{ x_{k} + x_{n-1-k} -1|y_{k} + y_{n-1-k} +1 \\} = m \in \mathbb{Z}$ thì <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1): $\\{ {\oint \( {{x_k} + {x_{n - 1 - k}}} \) + \ast|\oint \( {{y_k} + {y_{n - 1 - k}}} \) + \ast} \\} = m$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2): $\\{ {{x_k} + {y_{n - 1 - k}} - 1|{y_k} + {z_{n - 1 - k}} + 1} \\} = m \in \mathbb{Z}$ thì $\\{ {\oint \( {{x_k} + {y_{n - 1 - k}}} \) + \ast|\oint \( {{y_k} + {z_{n - 1 - k}}} \) + \ast} \\} = m$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(3): $\\{ {{y_k} + {y_{n - 1 - k}} - 1|{z_k} + {z_{n - 1 - k}} + 1} \\} = m \in \mathbb{Z}$ thì $\\{ {\oint \( {{y_k} + {y_{n - 1 - k}}} \) + \ast|\oint \( {{z_k} + {z_{n - 1 - k}}} \) + \ast} \\} = m$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;Từ công thức hồi quy của $L_{n}L,L{n}R,R_{n}R$ ở mục I/, ta suy ra: <br>
```math
n \bullet * + \oint {x_n} = \left\{ {\oint {x_k} + \oint {x_{n - 1 - k}} + \left( {n - 1} \right) \bullet *|\oint {y_k} + \oint {y_{n - 1 - k}} + \left( {n - 1} \right) \bullet *} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $\oint {x_n} = \\{ {\oint \( {{x_k} + {x_{n - 1 - k}} - 1} \) + 1 + \ast|\oint \( {{y_k} + {y_{n - 1 - k}} + 1} \) - 1 + \ast} \\}$ theo ***1.5 và 2.1***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: ${x_n} = \\{ {{x_k} + {x_{n - 1 - k}} - 1|{y_k} + {y_{n - 1 - k}} + 1} \\}$ theo ***1.1b, hệ quả của 1.6, 2.2a2*** và tương tự với ${y_n}$ và ${z_n}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Khi ấy ta có công thức hồi quy của ba dãy ${x_n}$ , ${y_n}$ , ${z_n}$ như sau: <br>
```math
\left\{ {{x_n}} \right\}:{x_0} = 1;{x_n} = \left\{ {\max \left( {{x_k} + {x_{n - 1 - k}}} \right) - 1|\min \left( {{y_k} + {y_{n - 1 - k}}} \right) + 1} \right\}
```
```math
\left\{ {{y_n}} \right\}:{y_0} = 0;{y_n} = \left\{ {\max \left( {{x_k} + {y_{n - 1 - k}}} \right) - 1|\min \left( {{y_k} + {z_{n - 1 - k}}} \right) + 1} \right\}
```
```math
\left\{ {{z_n}} \right\}:{z_0} = 0;{z_n} = \left\{ {\max \left( {{y_k} + {y_{n - 1 - k}}} \right) - 1|\min \left( {{z_k} + {z_{n - 1 - k}}} \right) + 1} \right\}
```

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 2.2b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; Các dãy ${x_n}$ , ${y_n}$ , ${z_n}$ có tính chu kì như sau: <br>
<div align="center">

| n | $x_{n}$ | $y_{n}$ | $z_{n}$ |
|:----------:|:----------:|:----------:|:----------:|
| $0$ | $1$ | $0$ | $0$ |
| $1$ | $1+\ast$ | $\frac{1}{2}$ | $0$ |
| $2$ | $1$ | $\frac{3}{4}$ | $0$ |
| $3$ | $1+\frac{1}{2}$ | $\frac{7}{8}$ | $\frac{1}{2}$ |
| $4$ | $1+\frac{3}{4}$ | $1$ | $\frac{1}{2}$ |
| $5$ | $1+\frac{7}{8}$ | $1+\frac{1}{4}$ | $\frac{3}{4}$ |
| $6$ | $2$ | $1+\frac{1}{2}$ | $1$ |
| $7$ | $2+\frac{1}{4}$ | $1+\frac{3}{4}$ | $1$ |
| $...$ | $...$ | $...$ | $...$ |
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Tổng quát được: ${x_{j + 5}} = {x_j} + 1{\rm{ }}\left( {j \ge 3} \right)$ &nbsp;&nbsp;&nbsp;&nbsp; ${y_{j + 5}} = {y_j} + 1{\rm{ }}\left( {j \ge 1} \right)$ &nbsp;&nbsp;&nbsp;&nbsp; ${z_{j + 5}} = {z_j} + 1{\rm{ }}\left( {j \ge 1} \right)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 2.2b:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng phương pháp quy nạp, với gợi ý như sau: <br>
```math
\left( {n \ge 1} \right):\left\{ \begin{array}{l}
\max \left( {{x_k} + {x_{n - 1 - k}}} \right) = {x_0} + {x_{n - 1}},{\rm{ min}}\left( {{y_k} + {y_{n - 1 - k}}} \right) = {y_0} + {y_{n - 1}},{\rm{ }}\\
\max \left( {{x_k} + {y_{n - 1 - k}}} \right){\rm{ }} = {x_0} + {y_{n - 1}},{\rm{ min}}\left( {{y_k} + {z_{n - 1 - k}}} \right) = {y_0} + {z_{n - 1}};
\end{array} \right.
```
```math
\left( {n \ge 4} \right):\max \left( {{y_k} + {y_{n - 1 - k}}} \right) = {y_2} + {y_{n - 3}},{\rm{ min}}\left( {{z_k} + {z_{n - 1 - k}}} \right) = {z_2} + {z_{n - 3}} \left( \text{2.3c} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Điều này có thể được kiểm tra dễ dàng nhưng rườm rà, do đó không diễn giải cụ thể ở đây. Từ ***(2.2b)***, có thể thấy ${x_n}$ , ${y_n}$ , ${z_n}$ đã thỏa mãn ***(2.2a1,a2)*** $\to$ các thiết lập ở (2.2a) là hợp lệ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tới đây, lời giải cho trò chơi Phong tỏa đã rõ ràng: Để tổng quát nhất, ta xem xét trò chơi $G$ gồm nhiều dải đất tách biệt $G_{1},G_{2},G_{3}...$ thay vì chỉ 1 dải đất (hơn nữa, 1 dải đất cũng có thể bị phân rã thành nhiều dải đất nhỏ hơn trong quá trình chơi). Để tính $G$ , ta tính giá trị của từng dải đất: $G_{1},G_{2},G_{3}...$ , quy đổi ${G_i} = {h_i} \bullet \ast + \oint {g_i}$ (sử dụng ***2.2a,b***), theo ***(1.5)*** ta có: <br>
```math
{G_1} + {G_2} + {G_3} + ... = \left( {{h_1} + {h_2} + {h_3} + ...} \right) \bullet * + \oint \left( {{g_1} + {g_2} + {g_3} + ...} \right) = h \bullet * + \oint g
```
&nbsp;&nbsp;&nbsp;&nbsp;Cuối cùng, 






