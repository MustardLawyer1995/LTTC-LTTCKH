# Trò chơi Luật Thiểu Số 
<ins>Mô phỏng luật chơi:</ins> Mỗi người chơi đều bỏ phiếu (Yes/No) tùy ý theo vòng, ai thuộc bên có số phiếu nhiều hơn bị loại (đúng như tên gọi của trò này), nếu bằng nhau thì bỏ phiếu lại lần nữa. Những người thắng đi vào vòng bỏ phiếu tiếp, loại dần cho tới khi chỉ còn 1 hoặc 2 người ở lại. <br>

<ins>Chiến thuật trong truyện (nguyên tác): </ins> <br>
Có 22 người, lập ra nhóm 8 người rồi chia đôi ra nửa đội bỏ Yes nửa đội bỏ No, nên sẽ luôn có 1 nửa đội ở lại sau mỗi vòng. Tác giả trò chơi này tức Ngô Thanh Liêm đã sáng tạo hơn khi nghĩ ra cách là lập team 2 người lúc bắt đầu và chỉ kết nạp thêm 1 người vào đội sau mỗi vòng, như vậy hạn chế được số người trong team và số Tiền thưởng chia ra được nhiều hơn. Nhưng trong bài này ta sẽ không làm vậy, hơn nữa lập team kiểu đó cũng có rất nhiều rủi ro so với việc lập 1 team hoàn chỉnh ngay khi mới bắt đầu. <br>

Khi cho tổng quát với $n$ người, việc chọn lựa sẽ khó khăn hơn, nhất là phải xét đến trường hợp mà team bị lẻ người ở 1 vòng nào đó, vì không phải lúc nào cũng chọn được số người có dạng $2^{k}$ (số chính phương).

## Lời giải 
### 1. Thu hẹp phạm vi tìm kiếm 
- Số người của nhóm mình và số người ở nhóm tự do (bỏ phiếu ngẫu nhiên) sẽ thay đổi sau mỗi vòng như thế nào ? <br>
- Gọi số người nhóm mình là $a$ , nhóm tự do là $b$ . Ta quy ước dấu “ $\rightarrow$ ” dùng để biểu diễn sự thay đổi số người mỗi bên sau 1 vòng bỏ phiếu.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 1:* $a$ chẵn thì khi đó $a \rightarrow \frac{a}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b-2}{2} = \frac{b}{2} - 1$ <br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 2:* $a$ lẻ thì khi đó $a \rightarrow \frac{a-1}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b}{2}$  **(*)** <br><br>
$\Longrightarrow$ Tới đây ta đặt ra tình huống xấu nhất như sau: sau mỗi vòng số người tự do còn lại nhiều nhất, số người nhóm mình còn lại ít nhất; dựa trên nhận xét: nếu thế $(a,b)$ đảm bảo chiến thắng thì $(a,b-1)$ và $(a+1,b-1)$ cũng vậy (theo nguyên lí quy nạp). <br>

- Gọi $V$ là số người cần lấy ra từ $N$ người để tạo ra nhóm, khi đó ta thu hẹp giới hạn để tìm $V$ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>*Giới hạn dưới*</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $(a;b)=(a_{0};b_{0})$ ở vòng cuối cùng, có thể thực hiện 1 thuật toán để truy ngược lại các giá trị $V,N-V$ ban đầu bằng cách làm quay lùi thời gian qua các vòng bỏ phiếu cùng với đó là số người của 2 bên tăng dần tới $V$ và $N-V$ (xem lại **(*)** ): Nếu $(a,b)$ là kết quả sau 1 vòng bỏ phiếu thì lùi về trước khi bỏ phiếu là $(2a;2b+2)$ , vì ta kỳ vọng $V$ là nhỏ nhất và $N-V$ là lớn nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giả sử có $n$ vòng bỏ phiếu, khi đó ta có dãy số như sau: 
```math
\left\{ \begin{array}{l}
{a_{k + 1}} = 2{a_k}\\
{b_{k + 1}} = 2\left( {{b_k} + 1} \right)
\end{array} \right.;\left\{ \begin{array}{l}
V = {a_n}\\
N - V = {b_n}
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giải dãy số trên, ta thu được: 
```math
\left\{ \begin{array}{l}
{a_n} = {2^n}{a_0}\\
{b_n} = {2^{n + 1}}{b_0} - 2
\end{array} \right. \Rightarrow N = {a_n} + {b_n} = \left( {{a_0} + 2{b_0}} \right){2^n} - 2 = \left( {1 + 2\frac{{{b_0}}}{{{a_0}}}} \right)V - 2 \Leftrightarrow V = \left( {N + 2} \right)\left( {1 + 2\frac{{{b_0}}}{{{a_0}}}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Đến đây ta nhận xét tỉ số $\frac{{{b_0}}}{{{a_0}}}$ lớn nhất chỉ có thể bằng 1 vì $a = 1,b > 1$ thì không đảm bảo chiến thắng <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Suy ra: $(a,b)=(2,2)$ vì $(1,1)$ là thế hòa (các $(a,b)$ lớn hơn đều có thể giảm số người xuống bằng cách tổ chức thêm 1 vòng bỏ phiếu nữa). <br>

$\Longrightarrow$ <ins>Lý tưởng:</ins>  ${a_0} = {b_0} = 2 \Rightarrow V = \frac{{N + 2}}{3}$ <br>
$\Longrightarrow$ Đây cũng chính là *giới hạn dưới* của số người cần lập nhóm <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>*Giới hạn trên*</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tôi đã mất kha khá thời gian để vật lộn với ý tưởng này. Đầu tiên là thử lại mẹo vặt khi tìm giới hạn dưới, nhưng không có kết quả, cứ mỗi khi tìm được 1 giá trị đẹp thỏa mãn với các $N$ lớn thì lại gặp phản ví dụ với các giá trị $N$ nhỏ, tầm 20 đổ lại. Ban đầu tôi đã nghĩ giới hạn trên là cái gì đó như $\approx \frac{N + 1}{2}$ , vì niềm tin giản đơn rằng số người của đội mình qua mỗi vòng luôn $≥$ phe tự do nên trò chơi có thể kết thúc với $(2,1)$ hay $(2,2)$ . Nhưng không, số người có thể kết thúc với $(1,1)$ , hòa! Thậm chí 1 tỉ lệ như $(3,2)$ vẫn có thể hòa vì nó dẫn đến $(1,1)$ , điểm trái khoáy ở đây là $(2,2)$ đảm bảo chiến thắng trong khi  $(3,2)$ có vẻ tốt hơn (vì nhóm ta có nhiều người hơn) lại không. Những điểm phi lý này làm cho câu đố khó hơn nhiều so với vẻ ngoài. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nên ta thử mạo hiểm với ý tưởng: hãy đảm bảo tỉ lệ $a:b$ ở vòng cuối là $2:1$ , vì $\left( {2;1} \right),\left( {4;2} \right),\left( {6;3} \right),....$ đều dẫn đến chiến thắng. Ước lượng $V:\left( {N - V} \right) \approx 2:1$ hay $V \approx \frac{2}{3}N$ . Ta sẽ chứng minh nhận xét sau bằng quy nạp: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu trò chơi bắt đầu với $a:b \ge 2:1$ , thì ở mọi thời điểm trong trò chơi $a:b$ vẫn giữ tỉ lệ lớn hơn $2:1$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh </ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Với $a$ chẵn tức $\left( {a,b} \right) = \left( {2m + 2k,m} \right)$ sau 1 vòng bỏ phiếu $a = m + k,{\rm{ }}b \le \frac{{m - 1}}{2} \Rightarrow a:b \ge 2:1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Với $a$ lẻ tức $\left( {a,b} \right) = \left( {2m + 1 + 2k,m} \right)$ sau 1 vòng bỏ phiếu $a = m + k,{\rm{ }}b \le \frac{m}{2} \Rightarrow a:b \ge 2:1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Như vậy trước khi bỏ phiếu $a:b \ge 2:1$ thì thì sau 1 vòng bỏ phiếu điều đó vẫn giữ nguyên, và vòng bỏ phiếu tiếp cũng thế,...,cứ thế cho tới tận vòng cuối. Như vậy tôi chỉ cần chọn $V:\left( {N - V} \right)$ ở thời điểm bắt đầu giữ tỉ lệ $\ge 2:1$ là đảm bảo một thắng lợi cho đội mình. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Có ba trường hợp $N$ rơi vào: $N = \\{ 3m,3m + 1,3m + 2 \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ $V \le \frac{2}{3}\left( {N + 1} \right)$ là *giới hạn trên* của $V$ trong mọi trường hơp. <br> <br>
$\Longrightarrow$ Tóm lại giới hạn của $V$ là: 
```math
{\frac{1}{3}\left( {N + 2} \right) \le V \le \frac{2}{3}\left( {N + 1} \right)}$
```
### 2. Công thức chính xác cho $V$





















