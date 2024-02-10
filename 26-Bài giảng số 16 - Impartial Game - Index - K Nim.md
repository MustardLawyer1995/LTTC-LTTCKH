# Impartial Game - Index - K Nim
### Giới thiệu
&nbsp;&nbsp;&nbsp;&nbsp;Đây là 1 biến thể khác của nim game, luật chơi như nim game thông thường chỉ khác ở điểm: ở mỗi lượt, người chơi được phép lấy quân từ ít nhất 1 và nhiều nhất là $k$ đống (khi $k = 1$ thì trò chơi trở về nim game thông thường). <br>
### Lời giải cho index $k$ - nim 
&nbsp;&nbsp;&nbsp;&nbsp;Chiến lược tất thắng của trò chơi dựa vào 1 khái niệm phát triển từ tổng xor là tổng xor theo modulo $p$ , được định nghĩa như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tổng $\text{xor}$ theo modulo $p$ (viết gọn là $\text{xor} (p)$ ) giữa các số $M_{1};M_{2};...;M_{n}$ được tính bằng cách: <br>
<div align="center">
  
$M_{1}\text{ xor } (p)M_{2}\text{ xor } (p)M_{3}\text{ xor } (p)...M_{n-1}\text{ xor }(p) M_{n} = M$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Viết $M_i$ (với $1 \le i \le n$ ) về dạng nhị phân với $m_{i}(j)$ là chữ số thứ $j$ của nó. Khi đó ta có: <br>
<div align="center">
  
$m(j) \equiv m_{1}(j) + m_{2}(j) + m_{3}(j) + ... + m_{n}(j) \( \text{ mod p} \)$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Khi kết quả $M$ đã được tính xong bạn có thể tùy ý quy đổi nó về dạng thập phân thông dụng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Định nghĩa này cho thấy phép cộng $\text{ xor }(2)$ chính là phép cộng xor thông thường mà ta đã làm quen ở bài về định lý Sprague Grundy, phần giới thiệu về trò chơi nim (xem lại ***bài giảng số 7a***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chiến lược tất thắng của index- $k$ nim khi chơi theo luật normal là tính tổng $\text{ xor } \( k+1 \)$ của tất cả các số lượng quân của mỗi đống nim, rồi dùng giá trị này như một số Grundy "giả" (nó không hoàn toàn tương đương với số Grundy/Nimber thực sự của trò chơi theo định nghĩa), tức là liên tục đưa đối phương về trạng thái tổng $\text{ xor } \( k+1 \) = 0$ . Chiến lược dựa trên sự thật: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1) Khi tổng $\text{ xor } \( k+1 \) = 0$ , mọi nước đi đều dẫn đến trạng thái có tổng $\text{ xor } \( k+1 \) = 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2) Khi tổng $\text{ xor } \( k+1 \) = 0$ , luôn tồn tại ít nhất 1 nước đi có thể đưa trò chơi về trạng thái có tổng $\text{ xor } \( k+1 \) = 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;<ins>Giải thích</ins>:Ta nhận thấy 2 điều này là hiển nhiên bởi vì mỗi nước đi chỉ được phép tác động vào nhiều nhất $k$  đống) $\rightarrow$ các trạng thái tất bại có tổng $\text{ xor } \( k+1 \) = 0$ , các trạng thái tất thắng có tổng $\text{ xor } \( k+1 \) \ne 0$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu trò chơi ở trạng thái tổng $\text{ xor } \( k+1 \) = 0$ ở lượt của đối thủ, bạn có thể liên tục dồn hắn vào trạng thái này theo vòng lặp 1) 2) cho đến khi trò chơi kết thúc - tất cả các đống đều có 0 quân, đây là 1 trạng thái có tổng $\text{ xor } \( k+1 \) = 0$ nên đương nhiên là lượt của đối thủ, và hắn không còn nước nào để đi cả, bạn thắng. Điều ngược lại cũng đúng, nếu bạn rơi vào trạng thái có tổng $\text{ xor } \( k+1 \) = 0$ thì bạn chắc chắn sẽ thua, trừ khi đối phương không biết về chiến lược tất thắng này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ở phiên bản misere, chiến lược cũng tương tự và chỉ khác ở những nước đi về cuối game. Liên tục dồn đối thủ về các trạng thái có tổng $\text{ xor } \( k+1 \) = 0$ nếu bạn có thể, cho đến khi số lượng đống có $> 1$ quân là $\le k$ (đây là trạng thái có tổng $\text{ xor } \( k+1 \) \ne 0$ nên chắc chắn là lượt của bạn). Hãy chọn nước đi sao cho ở lượt đối thủ chỉ còn các đống có 1 quân và số lượng của chúng $\equiv 1 \text{ mod } \( k+1 \)$ . Nếu đối thủ lấy đi $s$ đống thì bạn chỉ cần lấy $k+1-s$ đống, duy trì như vậy cho đến khi chỉ còn 1 quân ở lượt đối thủ, bạn thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Index- $k$ nim cũng là một tame game. Dễ nhận thấy khi chỉ còn các đống 1 quân (gọi trạng thái này là $y$ ), trò chơi tương đương với trò chơi Loại Trừ gồm 1 đống - ở mỗi lượt số lượng quân lấy ra $\le k$ $\Rightarrow$ khi đó $\( G^{+};G^{-} \)$ phụ thuộc vào số lượng đống 1 quân $(L)$ : <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1) $L \equiv 0 \text{ mod } \( k+1 \)$ $\rightarrow$ $y = \( 0,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2) $L \equiv 1 \text{ mod } \( k+1 \)$ $\rightarrow$ $y = \( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3) $L \equiv a \text{ mod } \( k+1 \)$ với $2 \le a \le k$ $\rightarrow$ $y = \( a,a \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với một trạng thái $x \ne y$ từ $x$ có nước dẫn đến $y = \( 0,1 \)$ $\Leftrightarrow$ Từ $x$ có nước dẫn đến $y = \( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Nếu $x \ne y$ thì $x = \( a,a \)$ với $a \in \mathbb{N}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Trò chơi chính là một ***tame game*** theo định nghĩa. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Tuy 2 khái niệm không đồng nhất nhưng giữa tổng  và nimber/số Grundy của index - $k$ nim có một vài mối liên hệ. Nếu tổng $\text{ xor } \( k+1 \)$ của một trạng thái $x$ bất kỳ là $M(x)$ , và normal nimber của $x$ là $G(x)$ thì: <br>
<div align="center">
  
$G(x) = m$ $\Leftrightarrow$ $M(x) = m$ với $m \in \( 0;1 \)$ 
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo chiến lược tất thắng của trò chơi, $x$ là trạng thái tất bại, điều này tương đương với $M(x) =0$ . Mặt khác theo định nghĩa của nimber: $x$ là trạng thái tất bại $\Leftrightarrow$ $G(x) = 0$ . Suy ra ta có mệnh đề sau: $G(x) = 0$ $\Leftrightarrow$ $M(x) = 0$ . (\*) <br>

&nbsp;&nbsp;&nbsp;&nbsp;Đặt tập hợp tất cả các trạng thái $x$ có $M(x) = 1$ là $W(1)$ và tập hợp các trạng thái $x$ có $M(x) = 1$ là $W(0)$ . Trong phần chứng minh index - $k$ nim là tame game ta đã xác định được:<br>
<div align="center">
  
$V\( 0;1 \) = \\{ y|L(y)  \equiv 0 \text{ mod } \( k+1 \) \\}$ <br>
$V\( 1;0 \) = \\{ y|L(y)  \equiv 1 \text{ mod } \( k+1 \) \\}$ <br>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Với $y = \( 0,1 \)$ và $M(y) = 0$ $\rightarrow$ $V\( 0,1 \) = W(0)$ và với $y = \( 1,0 \)$ và $M(y) = 1$ $\rightarrow$ $V\( 1,0 \) = W(1)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ (\*) ta đã biết được: $V\( 0,0 \) = W(0) \backslash V\( 0,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $V'\( 1,1 \) = W(1) \backslash V\( 1,0 \)$ , khi đó điều cần phải chứng minh hiện tại là $V'\( 1,1 \) = V\( 1,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có bốn tập trạng thái $V\( 0,1 \);V\( 1,0 \);V\( 0,0 \);V\( 1,1 \)$ thỏa mãn tất cả các mệnh đề từ (i) đến (vii) của ***định lý 1.2*** trong bài về ***<ins>Lí thuyết Chi</ins>*** trong ***bài giảng số 10a*** nên theo định lí này ta suy ra $V'\( 1,1 \) = V\( 1,1 \)$ tức ta có điều phải chứng minh. <br>












