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
&nbsp;&nbsp;&nbsp;&nbsp; $\[ a_{0};a_{1};...;a_{n} \]$ là dạng liên phân số $\frac{b}{a}$ và $I\( a;b \)$ là số $i$ lớn nhất thỏa 





















