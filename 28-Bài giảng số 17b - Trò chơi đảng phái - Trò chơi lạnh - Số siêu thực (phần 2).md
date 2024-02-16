#  Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 2)
### 4. Số siêu thực
&nbsp;&nbsp;&nbsp;&nbsp;Để chứng minh lời giải của ***<ins>Hackenbush 2 màu</ins>*** ở ***mục 3/***, ta phải phát triển 1 hệ đếm để đo lường giá trị của 1 trò chơi lạnh, giống cái cách mà ta đã phát triển hệ thống số Nimber trong các impartial game. Để mang tính tổng quát, 2 người chơi sẽ được gọi là Trái và Phải thay cho Xanh và Đỏ. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tiên đề 0.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Mỗi trạng thái của trò chơi sẽ được gán cho 1 giá trị $G$ thỏa mãn các điều kiện sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G > 0$ khi Trái luôn thắng dù ai đi trước <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G < 0$ khi Phải luôn thắng dù ai đi trước <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G = 0$ khi người đi trước luôn thua bất kể Trái hay Phải <br>

&nbsp;&nbsp;&nbsp;&nbsp;Giá trị của trạng thái mà từ đó Trái có nước dẫn tới các trạng thái khác nhận giá trị lần lượt là $L_{1};L_{2};...;L_{n}$ , còn Phải có nước dẫn tới các trạng thái khác nhận giá trị lần lượt là $R_{1};R_{2};...;R_{m}$ , sẽ được kí hiệu là $\\{ L_{1};L_{2};...;L_{n} | R_{1};R_{2};...;R_{m} \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>(0.1a)</ins>*: Đặt $L = \text{ max } \( L_{1};L_{2};...;L_{n} \)$ và $R = \text{ min } \( R_{1};R_{2};...;R_{m} \)$ , với lối chơi tối ưu, Trái sẽ chọn nước đi tạo ra giá trị lớn nhất $(L)$ và Phải sẽ chọn nước đi tạo ra giá trị nhỏ nhất $(R)$ , vì vậy: $\\{ L_{1};L_{2};...;L_{n} | R_{1};R_{2};...;R_{m} \\} = \\{ L|R \\}$ (2 trạng thái hoàn toàn tương đương). <br>
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

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* Với trạng thái $\\{ k|k+1 \\} = n$ với $k \in \mathbb{Z}$ , rõ ràng $n$ không thể là số nguyên vì $k < n < k+1$ . Do ta mới chỉ sử dụng các số siêu thực là số nguyên nên $n$ hoàn toàn có thể được định giá tùy ý, ta sẽ đặt $n = k + \frac{1}{2}$ . Tương tự, vì ta mới chỉ sử dụng các phân số mẫu 2 nên $\\{ \frac{k}{2} \bigg\vert \frac{k+1}{2} \\} = n$ có thể được đặt tùy ý sao cho $\frac{k}{2} < n <\frac{k+1}{2}$ , chọn $n = \frac{2k+1}{4}$ .<br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 2.1:</ins>***

```math
\left\{ {\frac{k}{{{2^s}}} \bigg\vert \frac{{k + 1}}{{{2^s}}}} \right\} = \frac{{2k + 1}}{{{2^{s + 1}}}}\left( {k \in \mathbb{Z} ,s \in \mathbb{N} } \right) \text{ hoặc } \frac{k}{{{2^s}}} = \left\{ {\frac{{k - 1}}{{{2^s}}} \bigg\vert \frac{{k + 1}}{{{2^s}}}} \right\} \left( {k \equiv 1\left( {\bmod 2} \right),s \in \mathbb{Z}^{+}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Có vẻ hợp lý khi ta luôn chọn các số "chính giữa", sau cùng hãy nhớ rằng đây là những lựa chọn mang tính quy ước. Nói cách khác ta đã "đặt tên" cho trạng thái $\\{ 0|1 \\}$ (một trạng thái có thực trong trò chơi nhưng lại không thể biểu diễn bằng giá trị nguyên) là $\frac{1}{2}$ . Các số siêu thực định nghĩa ở ***(2.1)*** được gọi là số hữu tỉ dyadic-số hữu tỉ mà mẫu số là lũy thừa của 2. Một số dyadic được coi là đơn giản hơn các số dyadic khác khi lũy thừa 2 của nó có số mũ nhỏ hơn, nếu số mũ bằng nhau, số dyadic nào gần 0 hơn được coi là đơn giản hơn. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp; $n \oplus m = n + m$ với $m,n$ là các số hữu tỉ dyadic.<br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại các cặp số $\( n;m \) = \( \frac{a}{2^s};\frac{b}{2^r} \)$ với $a,b$ lẻ và $s \ge r \ge 1$ ***vi phạm 2.2***, lựa chọn cặp có $s+r$ nhỏ nhất. Theo ***2.1***, ta suy ra được: <br>

```math
n = \left\{ {\frac{{a - 1}}{{{2^s}}} \bigg\vert \frac{{a + 1}}{{{2^s}}}} \right\},m = \left\{ {\frac{{b - 1}}{{{2^r}}} \bigg\vert \frac{{b + 1}}{{{2^r}}}} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giải thích:</ins>* Nếu $m \in \mathbb{Z}$ thì $m = \\{ m-1 |\text{ } \\}$ $\( m \ge 1 \)$ hoặc $m = \\{  \text{ }|m+1 \\}$ $\( m \le -1 \)$ , cách chứng minh bên dưới vẫn áp dụng được, nếu $m = 0$ hoặc $m,n \in \mathbb{Z}$ thì ***2.2*** hiển nhiên thỏa mãn ***1.2***<br>
&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến ta có: <br>

```math
n \oplus m = \left\{ {n \oplus \frac{{b - 1}}{{{2^r}}},m \oplus \frac{{a - 1}}{{{2^s}}} \bigg\vert n \oplus \frac{{b + 1}}{{{2^r}}},m \oplus \frac{{a + 1}}{{{2^s}}}} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Nếu cả 4 biểu thức trong $\\{ \text{ } \\}$ đều thỏa mãn ***(2.2)*** thì hệ quả sẽ là:<br>

```math
n \oplus m = \left\{ {n + \frac{{b - 1}}{{{2^r}}},m + \frac{{a - 1}}{{{2^s}}} \bigg\vert n + \frac{{b + 1}}{{{2^r}}},m + \frac{{a + 1}}{{{2^s}}}} \right\} = \left\{ {n + m - \frac{1}{{{2^r}}},n + m - \frac{1}{{{2^s}}} \bigg\vert n + m + \frac{1}{{{2^r}}},n + m + \frac{1}{{{2^s}}}} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Kết hợp biến đổi trên cùng với $s \ge r \Leftrightarrow \frac{1}{2^s} \le \frac{1}{2^r}$ (bởi ***tiên đề 0.1a***) thì khi ấy ta suy ra:<br>

```math
n \oplus m = \left\{ {n + m - \frac{1}{{{2^s}}} \bigg\vert n + m + \frac{1}{{{2^s}}}} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác theo ***2.1*** ta có: <br>

```math
\left\{ {n + m - \frac{1}{{{2^s}}} \bigg\vert n + m + \frac{1}{{{2^s}}}} \right\} = m + n
```
&nbsp;&nbsp;&nbsp;&nbsp;Nên khi ấy ta suy ra: $n \oplus m = n + m$ , mâu thuẫn với giả định ban đầu là ***vi phạm (2.2)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Phải có ít nhất 1 trong 4 cặp số: $\left( {n;\frac{{b - 1}}{{{2^r}}}} \right),\left( {m;\frac{{a - 1}}{{{2^s}}}} \right),\left( {n;\frac{{b + 1}}{{{2^r}}}} \right),\left( {m;\frac{{a + 1}}{{{2^s}}}} \right)$ ***vi phạm 2.2*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;Do giả thiết $a,b$ lẻ, $\frac{a \pm 1}{2^s}$ và $\frac{b \pm 1}{2^r}$  là các phân số chưa tối giản $\rightarrow$ tồn tại 1 cặp $\( n';m' \) = \( \frac{a'}{2^{s'}};\frac{b'}{2^{r'}} \)$ khác ***vi phạm (2.2)*** mà $s' + r' < s + r$ , mâu thuẫn với giả thiết $n,m$ là cặp có $s + r$ nhỏ nhất $\rightarrow$ không tồn tại cặp $n,m$ nào ***vi phạm (2.2)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 2.2*** <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 2.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\\{ L|R \\} = n$ (với $L,R$ là các số hữu tỉ dyadic) được xác định bằng cách chọn $n$ là số hữu tỉ dyadic đơn giản nhất thỏa mãn $L < n < R$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.3:</ins>* <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•*<ins>(2.3a)</ins>*  $\\{ L|R \\} = n \rightarrow L < n < R$ (theo ***tiên đề 0.2***)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•*<ins>(2.3b)</ins>*  Nếu $L > 0,R < 0, \\{ L|R \\} = 0$ vì người đi trước luôn thua nên theo ***2.3*** thì hiển nhiên đúng <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•*<ins>(2.3c)</ins>*  Nếu $g \in \mathbb{Z}^{+},g-1 \le L < g < R$ , bởi ***2.2*** nên ta có:<br>

```math
n \oplus \left( { - g} \right) = \left\{ {L|R} \right\} \oplus \left\{ {{\rm{ }}| - g + 1} \right\} = \left\{ {L \oplus \left( { - g} \right)|n \oplus \left( { - g + 1} \right),\left( { - g} \right) \oplus R} \right\} = \left\{ {L - g|n - g + 1, - g + R} \right\} = 0
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giải thích:</ins>* vì $L-g < 0$ và $n-g+1,R-g > 0$ cùng với ***2.3b*** $\rightarrow$ $n = g$  $\rightarrow$ $\\{ -R|-L \\} = -g$ (theo ***tiên đề 0.1b***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $\forall g \in \mathbb{Z}^{-},L < g < R \le g + 1$ ta cũng có $\\{ L|R \\} = g$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•*<ins>(2.3d)</ins>* Nếu với $k$ lẻ, $s \in \mathbb{N}$ : <br>

```math
0 < \alpha  = \frac{{k - 1}}{{{2^s}}} \le L < \sigma  = \frac{k}{{{2^s}}} < R \le \beta  = \frac{{k + 1}}{{{2^s}}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Thì khi ấy ta suy ra: $\\{ \alpha | \beta \\} = \sigma$ tức theo ***2.2*** ta có: <br>

```math
\left( { - \sigma } \right) \oplus n = \left\{ { - \beta | - \alpha } \right\} \oplus \left\{ {L|R} \right\} = \left\{ {\left( { - \beta } \right) \oplus n,\left( { - \sigma } \right) \oplus L|\left( { - \alpha } \right) \oplus n,\left( { - \sigma } \right) \oplus R} \right\} = \left\{ { - \beta  + n, - \sigma  + L| - \alpha  + n, - \sigma  + R} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Do ***2.3a*** và giả thiết ***2.3d*** nên theo ***2.3b*** ta suy ra: <br>

```math
\left\{ \begin{array}{l}
 - \beta  + n, - \sigma  + L < 0\
 - \alpha  + n, - \sigma  + R > 0
\end{array} \right. \Rightarrow \left\{ { - \beta  + n, - \sigma  + L| - \alpha  + n, - \sigma  + R} \right\} = 0 \Rightarrow \left( { - \sigma } \right) \oplus n = 0 \Leftrightarrow n = \sigma 
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tương tự khi $\alpha  \le L < \sigma  < R \le \beta  < 0$ thì ta cũng có được: $\\{ L|R \\} = \sigma$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Với mọi $L,R$ nếu $\sigma = \frac{k}{2^s}$ ( $s \ge 1$ ) là số dyadic đơn giản nhất sao cho $L < \sigma < R$ và $\sigma = \\{ \alpha | \beta \\}$ (theo ***định nghĩa 2.1***) thì phải có $\alpha  \le L < \sigma  < R \le \beta$ (giả sử điều này sai thì $\alpha$ hoặc $\beta$ sẽ nằm trong khoảng $\( L;R \)$ mà $\alpha , \beta$ là các số dyadic đơn giản hơn $\sigma$ theo ***định nghĩa 2.1***), bởi ***2.3d*** ta có $\\{ L|R \\} = \sigma$ . Nếu $s = 0$ thì $\sigma \in \mathbb{Z}$ (theo ***2.3b***) và ***2.3c*** ta có $\\{ L|R \\} = \sigma$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 2.3*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br> 
&nbsp;&nbsp;&nbsp;&nbsp;Việc xây dựng lý thuyết về hệ thống số siêu thực đã chứng minh lời giải của Hackenbush 2 màu ở ***mục 3/*** là đúng cũng như chỉ ra chiến lược tất thắng cho mọi trò chơi lạnh (bởi vì quá trình lập luận chỉ sử dụng những tiên đề phổ quát đối với mọi trò chơi lạnh): Xác định giá trị $G$ của toàn bộ trò chơi, nếu $G > 0$ , người chơi Trái thắng, nếu $G < 0$ , người chơi Phải thắng, $G = 0$ thì bất cứ ai đi trước sẽ thua. Nếu bạn là Trái và đang ở thế thắng, hãy chọn nước đi để $G \ge 0$ ở lượt của đối phương; ngược lại nếu bạn là Phải, hãy giữ cho $G \le 0$ ở lượt đối phương. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Lý thuyết số siêu thực đem lại 1 kết quả quan trọng: nếu 1 trò chơi là tổng của nhiều trò chơi con thì giá trị của nó bằng tổng các giá trị của tất cả trò chơi con cấu thành nó - điều này khiến cho việc tính toán giá trị trò chơi trở nên dễ dàng hơn bao giờ hết. Cùng thử áp dụng vào 1 trò chơi lạnh khác xem sao... <br>














