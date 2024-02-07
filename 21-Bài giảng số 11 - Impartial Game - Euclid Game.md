# Impartial Game - Euclid Game
### Giới thiệu
&nbsp;&nbsp;&nbsp;&nbsp;Là 1 impartial game, xếp vào nhóm tame game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Luật chơi:</ins>*** có 2 đống đá, ở mỗi lượt người chơi lấy đá từ đống lớn hơn, và chỉ được phép lấy 1 lượng bằng *bội số* của đống nhỏ hơn (nhưng không phải là 0). Nói cách khác: 2 đống đá là $\\{ a;b \\} | a \le b$ , nước đi duy nhất được phép là lấy $ka$ viên đá khỏi $b$ với $k \in \mathbb{Z}^+$ . <br>
### Chiến lược
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Luật chơi normal:</ins>*** <br>
<div align="center">
 
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/1a6b612b-f3cd-4d54-a6a2-fbb9ce9b332f)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu chỉ cần tìm lời giải cho 1 trò chơi đơn lẻ, ta chỉ cần tìm quy luật của các thế tất bại và đưa đối phương về các thế đó là được. Người ta đã tìm ra quy luật này như sau: $\\{ a;b \\} | a \le b$ là 1 thế tất bại trong Euclid game khi chúng thỏa mãn 1 trong 2 điều dưới đây: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-(1) $a=0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-(2) $0 < a \le b \le \phi b$ với $\phi$ là tỉ lệ vàng đã nhắc tới ở bài về ***Wythoff game - bài giảng số 9***) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các thế $\\{ 0;b \\}$ đều là thế tất bại vì chúng là tận điểm của trò chơi. Nếu  $0 < a \le b$ , nó sẽ là thế tất bại khi $a < b < \phi a$ , ta sẽ cho thấy điều này:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-(1) Với 1 trạng thái có $b > \phi a$ , đặt $b \equiv c \text{ }\( \text{mod a} \)$ với $a \le c \le 2a$ , ta có các trường hợp nhỏ như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(a) $a < c < \phi a$ $\rightarrow$ Lấy bớt từ đống $b$ để giảm số lượng về $c$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(b) $\phi a < c < 2a$ $\rightarrow$ Lấy bớt từ đống $b$ để giảm số lượng về $c-a$ , khi ấy trạng thái mới $\\{ c-a;a \\}$ thỏa mãn $c-a < a < \phi \( c-a \)$ <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>Giải thích thêm:</ins> vì $\phi a < c$ nên ta suy ra: <br>

```math
\left\{ \begin{array}{l}
\phi \left( {\phi  - 1} \right)a < \phi \left( {c - a} \right)\\
\phi \left( {\phi  - 1} \right) = {\phi ^2} - \phi  = 1
\end{array} \right. \Leftrightarrow a < \phi \left( {c - a} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(c) $c=a$ $\rightarrow$ $b = ka$ $\rightarrow$ Lấy bớt từ đống $b$ cho về 0. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Khi trạng thái hiện tại đang không ở thế $a < b < \phi a$ , luôn có ít nhất 1 nước đi để đưa trò chơi về trạng thái đó khi tới lượt đối thủ hoặc 1 nước đi để đối thủ thua ngay lập tức. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-(2) Ngược lại với 1 trạng thái đã sẵn ở thế $a < b < \phi a$ , không có nước đi nào có thể đưa đối thủ về 1 thế tương tự như vậy: giả sử lấy bớt $a$ từ đống $b$ , có $\\{ b-a;a \\}$ với $b-a < a$ , nhưng $b < \phi a \Leftrightarrow \phi \( b-a \) < \phi \( \phi -1 \)a = a$ ; nếu giảm $b$ xuống bé hơn $b-a$ thì mọi chuyện còn tệ hơn nữa. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, đối thủ chỉ thắng khi tới lượt anh ta mà trạng thái là $\\{ a;ka \\}$ với $k \in \mathbb{Z}^+$ , điều này là không thể vì anh ta luôn bị bạn dồn về các thế $\\{ a;b \\}$ trong đó: hoặc $a=0$ (thua luôn), hoặc $0 < a < b < \phi a$ (nên $b$ không thể là bội số của $a$ được). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Đây là chiến lược tất thắng cho ***<ins>Euclid Game</ins>***. <br>

&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Luật chơi misere:</ins>*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;Như đã nói qua trong ***bài giảng số 10a,b*** , vì Euclid game là tame game nên bản misere có cùng chiến lược y chang như vậy, chỉ khác là khi bạn ở thế $\\{ a;ka \\}$ , bạn cần đưa đối phương về $\\{ a;a \\}$ thay vì $\\{ a;0 \\}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi sẽ khó hơn khi ở dạng tổng của nhiều Euclid game đơn lẻ, khi đó bạn cần sử dụng *khái niệm nimber*. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\( G^{+};G^{-} \)$ của $\\{ a;0 \\}$ là $\( 0;1 \)$ , của $\\{ a;a \\}$ là $\( 1;0 \)$ của $\\{ a;ka \\}$ với $k \in \mathbb{Z}^+ | k \ge 2$ là $\( k;k \)$ (xem lại ***các ví dụ ở mục 2/*** - ***bài giảng số 10a***) và của $\\{ a;b \\}$ (với $0 < a < b < \phi a$ ) là $\( 0;0 \)$ (theo chiến lược tất thắng nêu ở trên). Tuy nhiên nimber của các trường hợp khác không hề dễ tính chút nào, ta cần nhiều lý thuyết hơn nữa.  <br>

&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Biến thể khác của Grossman-Game:</ins>*** <br>
<div align="center">
 
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/60c9ff8c-1803-4b39-ac40-d17d43cdda66)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Grossman game</ins>*** có cách chơi giống hệt Euclid game chỉ khác ở việc kích thước của 2 đống không được phép = 0. Điều này có nghĩa $\\{ a;a \\}$ mới là tận điểm của trò chơi và có nimber $\( 0;1 \)$ , trong khi $\\{ a;2a \\} = \( 1;0 \)$ nên khi ấy ta suy ra: <br>
<div align="center">
  
$\\{ a;ka \\} = \( k-1;k-1 \)$ với $k \ge 3$ ; $\\{ 3a;2a \\} = \( 0;1 \)$ ; $\\{ \( 2k+1 \)a;2a \\} = \( k;k \)$ với $k \ge 2$ 
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Để bắt đầu, ta sẽ quy ước $G\( a;b \)$ là nimber của trạng thái $\\{ a;b \\}$ trong Euclid game, và $G' \( a;b \)$ là của Grossman game. Cả 2 giá trị đều được tính toán dựa trên *khái niệm "liên phân số"*. Với 1 trạng thái $\\{ a;b \\} | b \ge a$ , dạng liên phân số của $\frac{b}{a}$ là $\[ a_{0};a_{1};...;a_{n} \]$ (như hình dưới) sẽ được xem như là đại diện cho trạng thái của trò chơi (chú ý rằng chỉ dùng tỉ số $\frac{b}{a}$ khi $b \ge a$ mà không sử dụng $\frac{a}{b}$ , trừ khi $a=0$ , ta buộc phải coi dạng liên phân số là $\frac{a}{b} = [0]$ , vì không thể để 0 ở mẫu số được). Trước tiên ta xét luật chơi normal. <br>

```math
\LARGE \frac{b}{a} = a_{0} + \cfrac{1}{a_{1} + \cfrac{1}{a_{2} + \cfrac{1}{\ddots a_{n-1} + \cfrac{1}{a_n}}}}
```
#### *<ins>Định lí 1</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $\[ a_{0};a_{1};...;a_{n} \]$ là dạng liên phân số $\frac{b}{a}$ và $I\( a;b \)$ là số $i$ lớn nhất thỏa $a_{0} = a_{1} = ... a_{i-1} \le a_{i}$ với $\lfloor x \rfloor$ là hàm làm tròn dưới, thì khi ấy ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1) $G\( a;b \) = \left\lfloor {\frac{b}{a}} \right\rfloor$ nếu $I\( a;b \)$ chẵn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2) $G\( a;b \) = \left\lfloor {\frac{b}{a}} \right\rfloor - 1$ nếu $I\( a;b \)$ lẻ. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Gọi $g\( a;b \)$ là hàm số tuân thủ định nghĩa như định lý trên, cần chứng minh $G\( a;b \) = g\( a;b \)$ . Lưu ý rằng $\left\lfloor {\frac{b}{a}} \right\rfloor = a_{0}$ . Từ định nghĩa dạng liên phân số và luật Euclid game, dễ thấy từ trạng thái $p = \[ a_{0};a_{1};...;a_{n} \]$ , nước đi tiếp theo luôn dẫn đến trạng thái $q = \[ a_{0}-j;a_{1};...;a_{n} \]$ ( $j$ có thể tùy chọn trong nửa khoảng $1 \le j < a_{0}$ ) hoặc $q = \[ a_{0};a_{1};...;a_{n} \]$ . Từ đó theo định nghĩa của hàm $g$ , dễ thấy: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Luôn có $g(p) \ne g(q)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Với bất kì giá trị $k < g(p)$ , luôn có cách chọn $j$ để $g(q) = k$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $g\( a;b \)$ trùng khớp với định nghĩa Mex của $G\( a;b \)$ tức ta suy ra $G\( a;b \) = g\( a;b \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1***. <br>

#### *<ins>Định lí 2</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $\[ a_{0};a_{1};...;a_{n} \]$ là khai triển liên phân số của $\frac{b}{a}$ và $\[ a_{0};a_{1};...;a_{n};a_{n+1} \]$ là khai triển của liên phân số của $\frac{b'}{a'}$ thì khi đó $G\( a;b \) = G'\( a';b' \)$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Quá trình chơi với trạng thái khởi đầu là $\\{ a;b \\}$ (khi chơi luật Euclid) và $\\{ a';b' \\} (khi chơi ***luật Grossman***) là giống nhau hoàn toàn, chúng là *song ánh* của nhau khi mỗi trạng thái của trò chơi này lại tương ứng với 1 trạng thái của trò chơi kia ( $\[ a_{i};a_{i+1};a_{i+2};...;a_{n} \]$ với $\[ a_{i};a_{i+1};a_{i+2};...;a_{n};a_{n+1} \]$ ) và mỗi nước đi bên trò chơi này lại tương ứng với 1 nước đi bên trò chơi kia ( $\[ a_{i}-j;a_{i+1};a_{i+2};...;a_{n} \]$ với $\[ a_{i}-j;a_{i+1};a_{i+2};...;a_{n};a_{n+1} \]$ ) . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tận điểm của Euclid game là $[0]$ (1 trong 2 đống $= 0$ ) và của Grossman là $[1]$ (2 đống bằng nhau), nói cách khác điểm khác nhau chỉ là khi chơi Grossman game ta chừa số 1 lại. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Giá trị nimber của hai trò chơi là như nhau tức ta suy ra $G\( a;b \) = G'\( a';b; \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 2***. <br>

#### *<ins>Định lí 3</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Ta luôn có: $G'\( a;b \) = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 3:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi ***định lý 2*** ta biết rằng để tính $G'\( a;b \)$ ta chỉ cần viết dạng liên phân số của $\left\lfloor {\frac{b}{a}} \right\rfloor = \[ a_{0};a_{1};...;a_{n} \]$ , sau đó tính $\left\lfloor {\frac{b'}{a'}} \right\rfloor = \[ a_{0};a_{1};...;a_{n-1} \]$ và tính $G\( a';b' \)$ , có $G'\( a;b \) = G\( a';b' \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác $G\( a';b' \)$ có thể tính toán dễ dàng thông qua ***định lý 1***. Đặt $i = I\( a';b' \)$ . Bởi định nghĩa của liên phân số, ta có: <br>

```math
\frac{b}{a}-\frac{a}{b} = [ a_{0};a_{1};...;a_{n} ] - [ 0;a_{0};a_{1};...;a_{n} ] = a_{0} + [ 0;a_{1};...;a_{n} ] - [ 0;a_{0};...;a_{n} ] = a_{0} + c - d
```
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy ta suy ra được: $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0}$ nếu $c \ge d$ và $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0} - 1$ nếu $c < d$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• <ins>Trường hợp 1:</ins> $a_{0} = a_{1} = ... a_{i-1} < a_{i}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $i$ chẵn thì $a_{i} > a_{i-1}$ khiến $c > d$ tức ta suy ra $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• <ins>Trường hợp 2:</ins> $a_{0} = a_{1} = ... a_{i} > a_{i+1}$ . Dễ thấy nếu $i$ chẵn và $i+1$ lẻ thì $a_{i+1} < a_{i}$ khiến $c > d$ và ngược lại với $i$ lẻ $\rightarrow$ Khi ấy điều này tương tự trường hợp 1. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• <ins>Trường hợp 3:</ins> $a_{0} = a_{1} = ... a_{n}$ tức $i=n$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $i = n$ chẵn, $a_{n} < a_{n-1} + \frac{1}{a_{n}}$ khiến $c < d$ $\rightarrow$ $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0} - 1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $i = n$ lẻ, suy ra: $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0}$  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo ***định lí 1***, ta suy ra: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $G\( a';b' \) = a_{0} - 1$ nếu $i=n$ chẵn (vì $a_{0} = a_{1} = ... a_{n-1} > a_{n} - 1$ và $n-1$ lẻ); và $G\( a';b' \) = a_{0}$ nếu $i=n$ lẻ. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 3***. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* ***Định lý 3*** đã mang lại 1 cách tính toán thuận tiện cho nimber của Grossman game, nhưng mục đích chính của ta là tìm công thức cho nimber của Euclid game cơ, tất nhiên ta có thể dùng định lý 1 song nó hơi rắc rối 1 chút.<br>

#### *<ins>Định lí 4</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $G\( a;b \) = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor + \( -1 \)^{n}$ khi $a_{0} = a_{1} = ... a_{n}$ và ở các trường hợp còn lại, ta suy ra: $G\( a;b \) = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 4:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Làm tương tự phần chứng minh ***định lý 3***, chỉ riêng trường hợp 3 có chút khác biệt. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đó là khi $a_{0} = a_{1} = ... a_{n}$ , nếu $i=n$ chẵn, $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0} - 1$ ; nếu $i=n$ lẻ, $\left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor = a_{0}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác theo ***định lý 1***, nếu $i=n$ chẵn, $G \( a;b \) = a_{0} = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor + 1$ , nếu $i=n$ lẻ, $G \( a;b \) = a_{0} - 1 = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor - 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;...Nên suy ra $G\( a;b \) = \left\lfloor {\frac{b}{a}-\frac{a}{b}} \right\rfloor + \( -1 \)^{n}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4***. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở rộng:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nhưng liệu có cách nào để xác định nhanh trường hợp $a_{0} = a_{1} = ... a_{n}$ có xảy ra không mà không cần viết dạng liên phân số của $\frac{b}{a}$ ? <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Để làm được điều này ta cần xác định công thức tổng quát cho liên phân số $x_{n} = \[ a_{0};a_{1};...;a_{n} \]$ với $a_{0} = a_{1} = ... a_{n}$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giải dãy số:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\\{ x_{i} \\} = x_{0} = a_{0} + \frac{1}{x_{i}}$ . Viết $x_{i}$ ở dạng phân số $\frac{q_{i+1}}{q_{i}}$ với $q_{i}$ cũng là 1 dãy số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy ta suy ra: <br>

```math
\left\{ {{q_i}} \right\}:\left\{ \begin{array}{l}
{q_0} = 1,{q_1} = {a_0}\
{q_{i + 2}} = {a_0}{q_{i + 1}} + {q_i}
\end{array} \right. \to {q_n} = \frac{{\lambda _1^{n + 1} - \lambda _2^{n + 1}}}{{{\lambda _1} - {\lambda _2}}}
```
<div align="center">
 
trong đó $\left( {{\lambda _1};{\lambda _2}} \right) = \left( {\frac{{{a_0} + \sqrt {a_0^2 + 4} }}{2};\frac{{{a_0} - \sqrt {a_0^2 + 4} }}{2}} \right)$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy ta dễ dàng suy ra: 

```math
{x_n} = \frac{{\lambda _1^{n + 2} - \lambda _2^{n + 2}}}{{\lambda _1^{n + 1} - \lambda _2^{n + 1}}}
```
&nbsp;&nbsp;&nbsp;&nbsp;Có 1 ngoại lệ đặc biệt khi $a_{0}=1$ , dù $\frac{b}{a} = x_{n}$ cũng không được tính, nguyên nhân là vì $a_{0} = a_{1} = ... a_{n} = 1$ , tuy nhiên không bao giờ 1 liên phân số lại được biểu diễn ở dạng $\[ 1,1,1,...,1 \]$ cả nên trường hợp này đơn giản là sai phạm về mặt lý thuyết cơ bản. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Câu trả lời đã rõ ràng, trường hợp đặc biệt xảy ra khi $a_{0} > 1$ và $\frac{b}{a} = x_{n}$ với $n \in \mathbb{N}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy khi xét theo luật misere thì sao? <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Với Euclid game, không có gì khó khăn vì nó là *tame game*. Các hoán điểm duy nhất là $\\{ a,0 \\} = \( 0;1 \)$ và $\\{ a,a \\} = \( 1;0 \)$ như đã nói. Với Grossman game, không khó để nhận ra được rằng trạng thái $\\{ kF_{n};kF_{n+1} \\}$ ( với $F_{i}$ là số <ins>Fibonacci</ins> thứ $i$ ) là các hoán điểm, khi ấy ta có $\\{ kF_{n};kF_{n+1} \\} = \( 0;1 \)$ khi $n$ lẻ và 4$= \( 1;0 \)$ khi $n$ chẵn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, nếu từ 1 vị trí có thể đi tới $\\{ kF_{n};kF_{n+1} \\} = \( 0;1 \)$ (giả sử $n$ lẻ) hoặc nó là $\\{ kF_{n};kF_{n+1} \\} = \( 1;0 \)$ hoặc nó là $\\{ kF_{n};k\( F_{n+1}+mF_{n} \) \\}$ và có thể đi tới $\\{ kF_{n-1};kF_{n} \\} = \( 1;0 \)$ thì khi đó ta suy ra nó phải là $\( p;p \)$ với $p \ge 2$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Thực hiện lập luận tương tự với trường hợp $n$ chẵn.<br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Grossman game*** cũng là tame game và $\\{ kF_{n};kF_{n+1} \\}$ với $n > 0$ là các hoán điểm duy nhất của nó, theo công thức của số fibonacci, được biểu diễn như sau: <br>

```math
\frac{b}{a} = \frac{{{F_{n + 1}}}}{{{F_n}}} = \frac{{{\phi ^{n + 1}} - {{\left( {1 - \phi } \right)}^{n + 1}}}}{{{\phi ^n} - {{\left( {1 - \phi } \right)}^n}}}
```






