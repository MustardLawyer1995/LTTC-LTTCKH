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
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giải thích:</ins>* vì $L-g < 0$ và $n-g+1,R-g > 0$ cùng với ***2.3b*** $\rightarrow$ $n = g$  <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ $\\{ -R|-L \\} = -g$ (theo ***tiên đề 0.1b***) <br>
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

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Ví dụ 2.4:</ins>*** Trò chơi cuộc đua ếch
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* có 5 ô vuông hàng ngang, xếp vào đó 2 con ếch xanh (B) và 2 con ếch đỏ (R) tùy ý. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ví dụ như sau (số 0 là ô trống): BR0BR <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mỗi con ếch trong 1 lượt có thể tiến (1 ô), hoặc nhảy (2 ô, có thể nhảy qua đầu 1 con ếch khác)-theo chiều từ trái sang phải. 2 người chơi Xanh và Đỏ luân phiên mỗi lượt điều khiển 1 con ếch có màu tương ứng với mình. Ai khi đến lượt mà không còn nước để đi coi như thua. Để tăng độ khó, có thể xếp nhiều hàng 5 ô song song nhau, các hàng độc lập với nhau, mỗi lượt người chơi chỉ tác động vào 1 hàng (trò chơi dạng tổng của nhiều trò chơi con). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ tính giá trị cho các trạng thái của 1 hàng (người chơi Xanh sẽ ở vai trò Trái, còn Đỏ là Phải) tức được biểu diễn như sau:0XXXX (X là B hay R tùy ý), đây là điểm kết thúc trò chơi, khi không còn nước để đi với cả 2 người chơi $\rightarrow$ $G = \\{ \text{ }|\text{ } \\} = 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: B0XXX, phe Xanh có 1 nước đi dẫn trò chơi về 0, Đỏ không còn nước đi $\rightarrow$ $G = \\{ 0|\text{ } \\} = 1$ . Nếu thay B thành R thì $G = \\{ \text{ }|0 \\} = -1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có tiếp: BB0RR, phe Xanh có 2 nước đi dẫn trò chơi về 0 hoặc 1, Đỏ không có nước đi $\rightarrow$ $G = \\{ 0,1|\text{ } \\} = 2$ . Nếu đảo chỗ B và R thì $G = \\{ \text{ }|-1,0 \\} = -2$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến lại có: BR0XX, phe Xanh có 1 nước dẫn về 0, Đỏ có nước dẫn về 1  $\rightarrow$ $G = \\{ 0|1 \\} = \frac{1}{2}$ . Nếu đổi vai trò B và R thì $G = - \frac{1}{2}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với BBR0R, thì $G = \\{ 1|2 \\} = \frac{3}{2}$ . Tương tự, đổi vai trò B và R, ta suy ra: $G = - \frac{3}{2}$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp;Với BRB0R, thì $G = \\{ \frac{1}{2} | 1 \\} = \frac{3}{4}$ .     
&nbsp;&nbsp;&nbsp;&nbsp;Với BRR0B, thì $G = \\{ \frac{1}{2} | 1 \\} = 0$ . 
&nbsp;&nbsp;&nbsp;&nbsp;Với BBRR0, thì $G = \\{ \frac{3}{2} | 2 \\} = 0$ . 
&nbsp;&nbsp;&nbsp;&nbsp;Với BRBR0, thì $G = \\{ \frac{1}{2} | \frac{3}{4} \\} = \frac{5}{8}$ . 
&nbsp;&nbsp;&nbsp;&nbsp;Với BRRB0, thì $G = \\{ 0 | \frac{1}{2} \\} = \frac{1}{4}$ . [...] <br>

&nbsp;&nbsp;&nbsp;&nbsp;Với trò chơi ở dạng có nhiều hàng 5 ô, ta chỉ việc tính giá trị của từng hàng rồi đem cộng tất cả để thu được giá trị $G$ của toàn bộ trò chơi. Nếu $G > 0$ , Xanh thắng, $G < 0$ , Đỏ thắng, $G = 0$ , người đi sau thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thử 1 ví dụ: R0RBB, BR0RB, BBR0R, RBRB0 với $G = -1 + \frac{1}{2} + \frac{3}{2} - \frac{5}{8} = \frac{3}{8} > 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Xanh sẽ thắng nếu biết chọn những nước đi tối ưu, Xanh phải đi những nước để trò chơi nhận giá trị   ở lượt đối phương nếu muốn giành chiến thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu ở trò chơi trên Xanh đi trước, Xanh đưa RBRB0 ( $-\frac{5}{8}$ ) về RBR0B ( $-\frac{3}{4}$ ), tức là đưa trò chơi về $G = \frac{3}{8} + \( - \frac{3}{4} \) - \( - \frac{5}{8} \) = \frac{1}{4} > 0$ $\rightarrow$ Đây là nước đi chiến thắng. Việc này là phi lý khi xét theo lối suy nghĩ thông thường, vì rõ ràng chuyển BR0RB $\rightarrow$ 0RBRB hay chuyển BBR0R $\rightarrow$ B0RBR lợi hơn cơ mà? Xanh vẫn chỉ tốn 1 nước đi nhưng lại có thể chặn được 1 nước đi (cản đường con ếch Đỏ) của đối thủ ? $\rightarrow$ Vâng, nếu làm thế thì bạn thua chắc chắn (nếu đối thủ đi nước tối ưu, bạn đọc tự giải như trên). Thế nên, ta mới nhận ra được, việc phân tích 1 trò chơi bằng lý thuyết giúp tránh được những sai lầm khi phán đoán theo trực giác.

### *<ins>Phụ lục:</ins> Xác định nhanh giá trị của 1 số mẫu hình đặc biệt trong hackenbush 2 màu*
<div align="center">

Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/8555bc00-58fa-4b5d-ae2f-5d7de8b427cf) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/978549d2-14b9-408c-b1c6-1061a9d5cad2)
</div>

#### 1. Nguyên lí đại tràng:
&nbsp;&nbsp;&nbsp;&nbsp;Một phát hiện bất ngờ là ***<ins>nguyên lý đại tràng (colon principle)</ins>*** của hackenbush phiên bản *impartial game* vẫn có hiệu lực khi áp dụng cho hackenbush 2 màu. Đối với 1 tập hợp các nhánh được phát sinh từ cùng 1 điểm, ta có thể quy đổi chúng về 1 nhánh thẳng duy nhất có giá trị bằng với giá trị của tập hợp các nhánh bị thay thế. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br> 
&nbsp;&nbsp;&nbsp;&nbsp;Có 2 mẫu hình là $G(H)$ và $G(I)$ như trên hình 1,2 (phần không gian trong $G,H,I$ được thiết lập tùy ý), có thể chứng tỏ rằng nếu $H$ và $I$ có giá trị bằng nhau thì $G(H)$ và $G(I)$ cũng có giá trị bằng nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thiết lập mẫu hình $\( -G \)\( -I \)$ là đối xứng của $G(I)$ (các cạnh xanh và đỏ hoán đổi vai trò cho nhau), nên nếu giá trị của $G(I)$ là $q$ thì giá trị của $\( -G \)\( -I \)$ là $-q$ , xét 1 trò chơi gồm $G(H)$ và $\( -G \)\( -I \)$ , dễ thấy người đi sau luôn thắng: nếu người đi trước cắt 1 cạnh ở $G$ thì người đi sau cắt cạnh tương ứng ở $-G$ (và ngược lại) để làm cho $G$ và $-G$ tiếp tục ở dạng đối xứng khi đến lượt người đi trước, nếu người đi trước cắt ở $-H$ thì người đi sau sẽ cắt ở $-I$ sao cho diễn biến giống như trong 1 trò chơi gồm $H$ và $-I$ , mà trong trò chơi này thì người chơi sau sẽ thắng (tổng $H$ và $-I$ ,  là 0, theo giả thiết giá trị $H$ và $-I$ bằng nhau) $\rightarrow$ Người đi sau sẽ là người đi nước cuối cùng xóa hết toàn bộ $H$ và $-I$ , sau đó trò chơi sẽ chỉ còn 2 mẫu hình đối xứng ( $G$ và $-G$ ) và đến lượt người đi trước $\rightarrow$ Người đi trước thua $\rightarrow$ Trò chơi $G(H) + \( -G \)\( -I \)$ có giá trị là 0 $\rightarrow$ $G(H)$ và $G(I)$ có giá trị bằng nhau. (đpcm) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Và vì $I$ có thể là bất cứ mẫu hình nào có giá trị bằng $H$ nên ta thường lựa chọn $I$ là 1 cây thẳng (không phân nhánh) để có thể tận dụng ***quy tắc 3***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thử với mẫu hình trên: ký hiệu là xanh(đỏ, xanh(đỏ, đỏ-xanh)), giá trị của đỏ-xanh theo quy tắc 3 là $-1 + \frac{1}{2} = -\frac{1}{2}$ , khi đó giá trị của (đỏ, đỏ-xanh) là  $-1 - \frac{1}{2} = -\frac{3}{2} = -2 + \frac{1}{2}$ = giá trị của đỏ-đỏ-xanh $\rightarrow$ Ta quy đổi trò chơi về xanh(đỏ, xanh-đỏ-đỏ-xanh), giá trị của (đỏ, xanh-đỏ-đỏ-xanh) là $-1 + \(  1 - \frac{1}{2} - \frac{1}{4} + \frac{1}{8} \) = -\frac{5}{8} = -1 + \frac{1}{2} - \frac{1}{4} + \frac{1}{8}$ = giá trị của đỏ-xanh-đỏ-xanh $\rightarrow$ Trò chơi tiếp tục quy đổi về xanh-đỏ-xanh-đỏ-xanh, và giá trị của cây này là $1 - \frac{1}{2} + \frac{1}{4} - \frac{1}{8} + \frac{1}{16} = 1 + \( - \frac{5}{8} \) \times \frac{1}{2} = \frac{11}{16}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Kết luận: giá trị của trò chơi ban đầu là $\frac{11}{16}$ . <br>

#### 2. Giá trị của 1 vòng đơn gắn trực tiếp với mặt đất:
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/66fc1527-a7de-47c2-a7ca-df20a81679a6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Tính giá trị của 1 vòng bằng cách tìm 2 điểm nơi các đoạn bắt đầu đổi màu theo chiều từ mặt đất đi lên (trong hình minh họa trên, những điểm này được đánh dấu (\*)). Tiếp theo, chia phần còn lại của vòng (khoảng giữa 2 dấu \* như hình vẽ) thành 2 đoạn bằng nhau. Nếu số lượng đoạn giữa 2 dấu \* là chẵn (như ở (B)), thì cắt tại điểm nút chính giữa. Nếu có một số lẻ đoạn, cắt đôi đoạn chính giữa thành 2 đoạn (như trong (A)). Giá trị của vòng là tổng giá trị của 2 phân khúc, nói cách khác, giá trị của (A) giống với giá trị của (A') và giá trị của (B) giống với giá trị của (B'). <br>
&nbsp;&nbsp;&nbsp;&nbsp;- 2 thân cây trong (A') có giá trị $\frac{9}{8}$ và $-\frac{3}{8}$ $\rightarrow$ Giá trị của $(A) = \frac{9}{8} - \frac{3}{8} = \frac{3}{4}$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp;- 2 thân trong (B') có các giá trị $\frac{3}{16}$ và $\frac{27}{16}$ $\rightarrow$ Giá trị của $(B) = \frac{3}{16} + \frac{27}{16} = \frac{15}{8}$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp;Nguyên lý này có thể dễ dàng chứng minh bằng cách chứng tỏ tổng giá trị của 2 phân đoạn (ký hiệu $\sigma$ ) luôn $<$ tất cả các giá trị tạo ra sau 1 nước đi của Đỏ, và $>$ tất cả các giá trị tạo ra sau 1 nước đi của Xanh (gợi ý: nước đi tạo ra giá trị nhỏ nhất ( $R$ ) của Đỏ hay lớn nhất ( $L$ ) của Xanh luôn là xóa những đoạn nằm gần nhất với vị trí chia cắt vòng), và chứng tỏ rằng $\sigma$ là số hữu tỉ dyadic đơn giản nhất thỏa mãn điều kiện trên (gợi ý: coi $\sigma = \\{ \alpha|\beta \\}$ là biểu diễn theo ***định nghĩa (2.1) phần 4/***, chứng minh $\alpha \le L$ và $R \le \beta$ )



