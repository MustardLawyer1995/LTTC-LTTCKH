# Impartial Game - Wythoff Game
### 1. Mở đầu trò chơi <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/4907f772-b83c-4bb5-9515-b2cb4edf11a5)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Là một impartial game thuộc Lý thuyết trò chơi kết hợp <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* Cho 2 đống đá, 2 bên đi theo lượt, lượt của mình, người chơi phải lấy ít nhất 1 viên đá, có thể lấy từ 1 trong 2 đống với số lượng tùy ý, có thể lấy từ cả 2 đống nhưng với điều kiện lượng đá lấy ra ở 2 đống bằng nhau. Ai không còn nước để đi thì thua (phiên bản normal). Wythoff game tương đương với trò chơi sau: có 1 quân hậu trên 1 bàn cờ kích thước tùy ý, 2 người chơi lần lượt di chuyển quân hậu về góc phần tư trái-dưới, ai đưa được quân hậu về góc bàn cờ là người chiến thắng. <br>

### 2. Lời giải cho trò chơi <br>
&nbsp;&nbsp;&nbsp;&nbsp;Wythoff đã khám phá ra chiến lược tất thắng cho trò chơi này, có liên quan đến tỉ lệ vàng $\phi = \frac{1+\sqrt 5}{2} \approx 1.618$ . Tỉ lệ vàng được định nghĩa là nghiệm dương của phương trình $x^2-x-1=0$ , vì vậy: ${\phi}^2=\phi + 1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cụ thể hơn, một trạng thái của trò chơi là thế tất bại (người đi trước luôn thua) khi 2 đống đá có kích thước là $\left\lfloor {k\phi } \right\rfloor$ và $\left\lfloor {k {\phi}^2 } \right\rfloor$ (với $k \in \mathbb{N}$ ) với $\left\lfloor {...} \right\rfloor$ là hàm floor (hàm làm tròn xuống) <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhắc lại:</ins>* Nếu $y \le x < y+1$ với $y \in \mathbb{Z}$ thì $\left\lfloor {x} \right\rfloor = y$ <br>  
&nbsp;&nbsp;&nbsp;&nbsp;Để hiểu tại sao lại có điều kỳ diệu này, ta cần biết một khái niệm là ***<ins>dãy số Beatty</ins>*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dãy số Beatty là các dãy số có dạng $\left\lfloor {kr} \right\rfloor$ (với $k \in \mathbb{Z^+}$ ) với $r$ là số vô tỉ lớn hơn 1. Theo định lí Rayleigh nói rằng nếu hai dãy Beatty $\left\lfloor {kr} \right\rfloor$ và $\left\lfloor {ks} \right\rfloor$<br> thỏa mãn $\frac{1}{r}+\frac{1}{s}=1$ thì 2 dãy này là phần bù của nhau trên tập số tự nhiên. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* Xét lần lượt hai dãy sau:  <br>

```math
\left\{ \begin{array}{l}
\left\{ {\left\lfloor {k\pi } \right\rfloor } \right\} = 3,6,9,12,15,18,21,25,28,31,34,37,40,43,47,50,53,...\
\left\{ {\left\lfloor {k\frac{\pi }{{\pi  - 1}}} \right\rfloor } \right\} = 1,2,4,5,7,8,10,11,13,14,16,17,19,20,22,23,24,26,...
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ta thấy rằng nếu nếu đem 2 dãy hợp vào nhau sẽ thu được toàn bộ tập số tự nhiên trừ 0, nói cách khác, một số tự nhiên ≠ 0 bất kỳ sẽ thuộc về 1 trong 2 dãy số trên, ta gọi 2 dãy số như thế này là phần bù của nhau. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) Số tự nhiên $m \ne 0$ bất kỳ không thể ở trong cả 2 dãy số cùng lúc. Giả định $m$ thuộc cả 2 dãy số cùng lúc, tồn tại 2 số tự nhiên $≠ 0$ là $i,j$ thỏa mãn: <br>

```math
m = \left\lfloor {ir} \right\rfloor  = \left\lfloor {js} \right\rfloor  \Rightarrow \left\{ \begin{array}{l}
m < ir < m + 1\
m < js < m + 1
\end{array} \right.{\rm{ }} \Rightarrow i \in \left( {\frac{m}{r};\frac{{m + 1}}{r}} \right);j \in \left( {\frac{m}{s};\frac{{m + 1}}{s}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Cộng 2 vế với nhau: $m < i + j < m + 1$ (do giả thiết $\frac{1}{r}+\frac{1}{s}=1$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Điều này là vô lý vì giữa $m$ và $m+1$ lại tồn tại 1 số tự nhiên khác <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Giả định ban đầu không thể xảy ra tức $m$ không thể thuộc cả 2 dãy số <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) $m$ luôn thuộc về 1 trong 2 dãy số. Giả sử $m$ không thuộc về dãy nào, tồn tại 2 số tự nhiên $i,j≠ 0$ thỏa mãn <br>

```math
\left\{ \begin{array}{l}
\left\lfloor {ir} \right\rfloor  < m < \left\lfloor {\left( {i + 1} \right)r} \right\rfloor \
\left\lfloor {js} \right\rfloor  < m < \left\lfloor {\left( {j + 1} \right)s} \right\rfloor 
\end{array} \right. \Rightarrow \left\{ \begin{array}{l}
i < \frac{m}{r};\frac{{m + 1}}{r} < i + 1\
j < \frac{m}{s};\frac{{m + 1}}{s} < j + 1
\end{array} \right.
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Cộng các vế tương ứng với nhau kết hợp giả thiết $\frac{1}{r}+\frac{1}{s}=1$ , khi ấy ta có: $i + j < m,{\rm{ }}m + 1 < i + j + 2 \Rightarrow i + j < m < i + j + 1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Điều này là vô lý vì giữa 2 số tự nhiên liên tiếp lại tồn tại 1 số tự nhiên khác <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Giả định ban đầu không thể xảy ra tức $m$ luôn thuộc về 1 trong 2 dãy số <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Chứng minh 2 ý nhỏ trên đã hoàn thành bằng chứng cho <ins>định lý Rayleigh</ins>*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta thấy rằng $\left\lfloor {k\phi } \right\rfloor$ và $\left\lfloor {k {\phi}^2 } \right\rfloor$ chính là 2 dãy Beatty bù nhau do $\frac{1}{{{\phi ^2}}} + 1 = \frac{1}{\phi } \Leftrightarrow {\phi ^2} = \phi  + 1$ . Từ định nghĩa ta dễ dàng suy ra: (*) <br>

```math
\left\lfloor {k{\phi ^2}} \right\rfloor  = \left\lfloor {k\phi  + k} \right\rfloor  = \left\lfloor {k\phi } \right\rfloor  + k{\rm{ }}\left( {k \in {\mathbb{N}^*}} \right) \Leftrightarrow \left\lfloor {k{\phi ^2}} \right\rfloor  - \left\lfloor {k\phi } \right\rfloor  = k{\rm{ }}\left( {k \in {\mathbb{N}^*}} \right) (*)
```

&nbsp;&nbsp;&nbsp;&nbsp;***Chứng minh rằng*** trong Wythoff game, trạng thái có 2 đống với số lượng $\left\lfloor {k\phi } \right\rfloor$ và $\left\lfloor {k {\phi}^2 } \right\rfloor$ là trạng thái tất bại cho người đi trước, và tồn tại chiến lược tất thắng bằng cách đưa đối phương rơi vào trạng thái này: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1)  Với trạng thái $\\{ \left\lfloor {k\phi } \right\rfloor ; \left\lfloor {k {\phi}^2 } \right\rfloor \\}$ , bất kỳ nước đi nào cũng không thể đưa đối phương vào 1 trạng thái có dạng tương tự. Điều này hiển nhiên, vì nếu lấy bớt đá từ 1 trong 2 đống, đống còn lại vẫn giữ nguyên số lượng, nhưng nếu vậy thì đống kia cũng phải giữ nguyên để có dạng $\\{ \left\lfloor {k\phi } \right\rfloor ; \left\lfloor {k {\phi}^2 } \right\rfloor \\}$ , nghĩa là ta phải lấy ra 0 viên đá, vô lý. Nếu lấy từ cả 2 đống, phải lấy từ mỗi đống một lượng như nhau <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Hiệu của số lượng 2 đống không thay đổi và vẫn là $\\{ \left\lfloor {n\phi } \right\rfloor ; \left\lfloor {n {\phi}^2 } \right\rfloor \\}$ (xem (\*)), nhưng nếu ta đưa trò chơi về trạng thái mới là $\\{ \left\lfloor {n\phi } \right\rfloor ; \left\lfloor {n {\phi}^2 } \right\rfloor \\}$ thì hiệu mới ở (\*) phải là $n$ , nếu $n=k$ nghĩa là 2 dãy ấy vẫn giữ nguyên sau khi ta lấy đá, điều này hoàn toàn vô lý. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) Nếu trạng thái trò chơi không phải là dạng $\\{ \left\lfloor {k\phi } \right\rfloor ; \left\lfloor {k {\phi}^2 } \right\rfloor \\}$ , luôn tồn tại ít nhất 1 nước đi để đưa đối phương về trạng thái có dạng đó. Nếu trạng thái của ta là $\\{ a;b \\}$ với $a \le b$ ,   luôn thuộc về 1 trong 2 dãy $\left\lfloor {k\phi } \right\rfloor$ hoặc $\left\lfloor {k {\phi}^2 } \right\rfloor$ (theo định lý Rayleigh). Nếu $a = \left\lfloor {n\phi } \right\rfloor$ , ta có các trường hợp sau: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 1:</ins>*** $b > \left\lfloor {n{\phi ^2}} \right\rfloor$ chỉ cần lấy đá từ đống $b$ để nó giảm xuống $\left\lfloor {n{\phi ^2}} \right\rfloor$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Trường hợp 2:</ins>*** $b < \left\lfloor {n{\phi ^2}} \right\rfloor  \Rightarrow c = b - a = \left\lfloor {n{\phi ^2}} \right\rfloor  - \left\lfloor {n\phi } \right\rfloor  = n \Rightarrow \left\lfloor {c\phi } \right\rfloor  < \left\lfloor {n\phi } \right\rfloor$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Chỉ cần lấy từ mỗi đống một lượng như nhau sao cho $a$ giảm xuống $\left\lfloor {c\phi } \right\rfloor$ thì khi đó độ chênh lệch giữa 2 đống vẫn là $c$ <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ $b$ giảm xuống thành $\left\lfloor {c\phi } \right\rfloor  + c = \left\lfloor {c{\phi ^2}} \right\rfloor$ . Nếu $a = \left\lfloor {n{\phi ^2}} \right\rfloor$ có thể thấy $\left\lfloor {n\phi } \right\rfloor  < a \le b$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ có thể lấy đá từ $b$ cho giảm xuống $\left\lfloor {n\phi } \right\rfloor$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ 2 ý nhỏ (•) trên đây đã được chứng minh, và chúng cho biết chiến lược tất thắng của Wythoff game như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1) Nếu trạng thái trò chơi không phải là $\\{ \left\lfloor {k\phi } \right\rfloor ; \left\lfloor {k {\phi}^2 } \right\rfloor \\}$ (tất bại), nó sẽ là trạng thái tất thắng, luôn tồn tại 1 nước đi để đưa trò chơi về trạng thái tất bại. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2) Ngược lại, đối phương bị rơi vào trạng thái tất bại đi bất cứ nước nào cũng đều làm trò chơi chuyển về trạng thái tất thắng $\rightarrow$ Trở lại (1) $\rightarrow$ Vòng lặp tiếp diễn đến khi đối phương bị rơi vào trạng thái $\\{ 1,2 \\}$ (là $\\{ \left\lfloor {\phi } \right\rfloor ; \left\lfloor { {\phi}^2 } \right\rfloor \\}$ ) $\rightarrow$ Điều này đồng nghĩa với việc thua.  <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở rộng:</ins>* Một câu hỏi khác cần suy nghĩ: nếu đổi sang phiên bản misere, người nào bị ép phải đi nước cuối cùng là người thua cuộc, thì chiến lược tất thắng của game sẽ là gì ? <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lời giải cho misere wythoff game:</ins>* Các vị trí $\left( {0,1} \right),\left( {1,0} \right),\left( {2,2} \right)$ trên bàn cờ tương ứng với các trạng thái tất bại. 3 vị trí này nằm trong hình vuông $3 \times 3$ ở góc dưới trái bàn cờ, chúng tạo ra độ xen phủ lên các vị trí khác giống như tổ hợp 3 vị trí $\left( {0,0} \right),\left( {1,2} \right),\left( {2,1} \right)$ (là các thế tất bại trong phiên bản normal) $\rightarrow$ Các vị trí tất bại khác trên bàn cờ ở phiên bản misere là giống hệt như phiên bản normal <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Các trạng thái tất bại trong misere wythoff game là $\( 0;1 \)$ , $\( 2;2 \)$ và $\\{ \left\lfloor {k\phi } \right\rfloor ; \left\lfloor {k {\phi}^2 } \right\rfloor \\}$ với $k \ge 2$ . Chiến lược tất thắng là hãy liên tục đưa đối phương vào những thế này tương tự như ở normal wythoff game <br>

















