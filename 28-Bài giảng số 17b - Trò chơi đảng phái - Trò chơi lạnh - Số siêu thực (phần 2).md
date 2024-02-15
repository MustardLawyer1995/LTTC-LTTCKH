#  Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 2)
&nbsp;&nbsp;&nbsp;&nbsp;Để chứng minh lời giải của ***<ins>Hackenbush 2 màu</ins>*** ở ***mục 3/***, ta phải phát triển 1 hệ đếm để đo lường giá trị của 1 trò chơi lạnh, giống cái cách mà ta đã phát triển hệ thống số Nimber trong các impartial game. Để mang tính tổng quát, 2 người chơi sẽ được gọi là Trái và Phải thay cho Xanh và Đỏ. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tiên đề 0.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Mỗi trạng thái của trò chơi sẽ được gán cho 1 giá trị $G$ thỏa mãn các điều kiện sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G > 0$ khi Trái luôn thắng dù ai đi trước <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G < 0$ khi Phải luôn thắng dù ai đi trước <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G = 0$ khi người đi trước luôn thua bất kể Trái hay Phải <br>

&nbsp;&nbsp;&nbsp;&nbsp;Giá trị của trạng thái mà từ đó Trái có nước dẫn tới các trạng thái khác nhận giá trị lần lượt là $L_{1};L_{2};...;L_{n}$ , còn Phải có nước dẫn tới các trạng thái khác nhận giá trị lần lượt là $R_{1};R_{2};...;R_{m}$ , sẽ được kí hiệu là $\\{ L_{1};L_{2};...;L_{n} | R_{1};R_{2};...;R_{m} \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>(0.1a)</ins>*: Đặt $L = \text{ max } \( L_{1};L_{2};...;L_{n} \)$ và $R = \text{ min } \( R_{1};R_{2};...;R_{m} \)$ , với lối chơi tối ưu, Trái sẽ chọn nước đi tạo ra giá trị lớn nhất $(L)$ và Phải sẽ chọn nước đi tạo ra giá trị nhỏ nhất $(R)$ , vì vậy: <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\\{ L_{1};L_{2};...;L_{n} | R_{1};R_{2};...;R_{m} \\} = \\{ L|R \\}$ (2 trạng thái hoàn toàn tương đương). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>(0.1b)</ins>*: Do tính đối xứng của trò chơi nên: $G = \\{ L|R \\} \Leftrightarrow -G = \\{ -R|-L \\}$ (khi 2 người chơi đảo ngược vai trò thì các giá trị cũng đảo ngược dấu $±$ )<br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tiên đề 0.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Với $\\{ L|R \\} = G$ , theo định nghĩa của trò chơi lạnh, mọi nước đi của Trái đều làm giảm giá trị trò chơi và mọi nước đi của Phải đều làm tăng giá trị trò chơi, nên: $L < G < R$ , điều này cũng ràng buộc $L < R$ để $\\{ L|R \\}$ có thể xác định được. Với $\\{ \text{ }|\text{ } \\}$ là trạng thái mà tại đó không còn nước đi nào tiếp theo với cả 2 người chơi, nên ai đi trước sẽ thua $\rightarrow$  $\\{ \text{ }|\text{ } \\} = 0$ (theo ***tiên đề (0.1)***) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Các trạng thái sau được định nghĩa đệ quy: $\\{ 0|\text{ } \\} = 1;\\{ 1|\text{ } \\} = 2;\\{ 2|\text{ } \\} = 3;...;\\{ k-1|\text{ } \\} = k$ với $k \in \mathbb{Z}^{+}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Và bởi tính đối xứng (***tiên đề 0.1b***) nên: $\\{ \text{ }|0 \\} = -1;\\{ \text{ }|-1 \\} = -2;\\{ \text{ }|-2 \\} = -3;...;\\{ \text{ }|-k+1 \\} = -k$ với $k \in \mathbb{Z}^{+}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hệ thống các số như vậy được gọi là số siêu thực. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi gồm 2 trò chơi con có giá trị là $\\{ L_{1}|R_{1} \\} = g_{1}$ và $\\{ L_{2}|R_{2} \\} = g_{2}$ thì giá trị của toàn bộ trò chơi là: $\\{ L_{1}|R_{1} \\} \oplus \\{ L_{2}|R_{2} \\} = g_{1} \oplus g_{2} = \\{ L_{1} \oplus g_{2},L_{2} \oplus g_{1} | R_{1} \oplus g_{2},R_{2} \oplus g_{1} \\}$ , công thức này suy ra từ định nghĩa của các kí hiệu.<br>
&nbsp;&nbsp;&nbsp;&nbsp;Cũng bởi tính chất của trò chơi dạng tổng (của nhiều trò chơi con) nên phép cộng số siêu thực "⊕" có các tính chất như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1)Giao hoán $\( a \oplus b = b \oplus a \)$ và kết hợp $\( \( a \oplus b \) \oplus c = a \oplus \( b \oplus c \) \)$ như phép cộng số học "+" thông thường. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2) $n \oplus 0 = n \oplus \\{ \text{ }|\text{ } \\} = n$ (vì theo định nghĩa $0 = \\{ \text{ }|\text{ } \\}$ là 1 trò chơi rỗng.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(3) $n \oplus \( -n \) = 0$ (nếu $n = \\{ L|R \\}$ và $-n = \\{ -L|-R \\}$ ), đây là 2 trò chơi đối xứng, với mỗi nước đi của người đi trước ở $n$ , người đi sau chỉ việc đi nước tương ứng ở $-n$ và ngược lại, cứ tiếp diễn như vậy cho đến khi trò chơi kết thúc nên người đi sau sẽ luôn là người đi nước cuối cùng và thắng) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 1.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $n \oplus m = n + m$ với $m,n \in \mathbb{Z}$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta xét $n,m \ne 0$ vì khi 1 trong 2 giá trị $=0$ thì mệnh đề trên hiển nhiên đúng. Giả sử tồn tại các cặp số $m,n \in \mathbb{Z}^{+}$ , thỏa mãn $n \oplus m \ne n + m$ , chọn ra cặp số có tổng $n + m$ nhỏ nhất, khi đó ta có: <br>
<div align="center">

$n \oplus m \\{ n-1|\text{ } \\} \oplus \\{ m-1|\text{ } \\} = \\{ n \oplus \( m-1 \),m \oplus \( n-1 \) |\text{ } \\}$ 
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác phải có $n \oplus \( m-1 \) = n + m - 1 = m \oplus \( n-1 \)$ (nếu $m = 1$ hoặc $n = 1$ thì điều này hiển nhiên đúng), vì nếu không sẽ hình thành 1 cặp số $m' , n' \in \mathbb{Z}^{+}$ khác thỏa mãn $n' \oplus m' \ne n' + m'$ có tổng $n' + m' < n + m$ , vi phạm giả định ban đầu rằng $n + m$ là nhỏ nhất $\rightarrow$ $n \oplus m = \\{ n+m-1|\text{ } \\} = n +m$ , mâu thuẫn với giả định ban đầu $\rightarrow$ Không tồn tại các cặp $m,n \in \mathbb{Z}^{+}$ thỏa mãn $n \oplus m \ne n + m$ $\Rightarrow$ $n \oplus m = n + m$ , $\forall m,n \in \mathbb{Z}^{+}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì tính đối xứng (***tiên đề 0.1b***) nên đẳng thức cũng đúng cho trường hợp $\forall m,n \in \mathbb{Z}^{-}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $n \in \mathbb{Z}^{+}$ , $m \in \mathbb{Z}^{-}$ , giả sử $n + m > 0$ thì: $n = n + m + \( -m \) = \( n+m \) \oplus \( -m \)$ (vì $n+m,-m \in \mathbb{Z}^{+}$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $\( n+m \) \oplus \( -m \) \oplus m = \( n+m \) \oplus 0 = n+m$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh tương tự với $n + m < 0$ và với $n + m = 0$ thì $n \oplus m = n \oplus \( -n \) = 0 = n+m$ (hiển nhiên). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ các ý trên kết luận $n \oplus m = n + m$ với $m,n \in \mathbb{Z}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.2*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* Với trạng thái $\\{ k|k+1 \\} = n$ với $k \in \mathbb{Z}$ , rõ ràng $n$ không thể là số nguyên vì $k < n < k+1$ . Do ta mới chỉ sử dụng các số siêu thực là số nguyên nên $n$ hoàn toàn có thể được định giá tùy ý, ta sẽ đặt $n = k + \frac{1}{2}$ . Tương tự, vì ta mới chỉ sử dụng các phân số mẫu 2 nên $\\{ \frac{k}{2}|\frac{k+1}{2} \\} = n$ có thể được đặt tùy ý sao cho $\frac{k}{2} < n <\frac{k+1}{2}$ , chọn $n = \frac{2k+1}{4}$ .<br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 2.1:</ins>***

```math
\frac{k}{{{2^s}}}|\frac{{k + 1}}{{{2^s}}} = \frac{{2k + 1}}{{{2^{s + 1}}}}\left( {k \in \mathbb{Z} ,s \in \mathbb{N} } \right) \text{ hoặc } \frac{k}{{{2^s}}} = \frac{{k - 1}}{{{2^s}}}|\frac{{k + 1}}{{{2^s}}}\left( {k \equiv 1\left( {\bmod 2} \right),s \in \mathbb{Z}^{+}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Có vẻ hợp lý khi ta luôn chọn các số "chính giữa", sau cùng hãy nhớ rằng đây là những lựa chọn mang tính quy ước mà thôi. Nói cách khác ta đã "đặt tên" cho trạng thái $\\{ 0|1 \\}$ (một trạng thái có thực trong trò chơi nhưng lại không thể biểu diễn bằng giá trị nguyên) là $\frac{1}{2}$ . Các số siêu thực định nghĩa ở ***(2.1)*** được gọi là số hữu tỉ dyadic-số hữu tỉ mà mẫu số là lũy thừa của 2. Một số dyadic được coi là đơn giản hơn các số dyadic khác khi lũy thừa 2 của nó có số mũ nhỏ hơn, nếu số mũ bằng nhau, số dyadic nào gần 0 hơn được coi là đơn giản hơn. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $n \oplus m = n + m$ với $m,n$ là các số hữu tỉ dyadic.<br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại các cặp số $\( n;m \) = \( \frac{a}{2^s};\frac{b}{2^r} \)$ với $a,b$ lẻ và $s \ge r \ge 1$ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\\{ L|R \\} = n$ (với $L,R$ là các số hữu tỉ dyadic) được xác định bằng cách chọn $n$ là số hữu tỉ dyadic đơn giản nhất thỏa mãn $L < n < R$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.3:</ins>* <br>


















