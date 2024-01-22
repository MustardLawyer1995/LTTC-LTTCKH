# Trò chơi Luật Thiểu Số 
<ins>Mô phỏng luật chơi:</ins> Mỗi người chơi đều bỏ phiếu (Yes/No) tùy ý theo vòng, ai thuộc bên có số phiếu nhiều hơn bị loại (đúng như tên gọi của trò này), nếu bằng nhau thì bỏ phiếu lại lần nữa. Những người thắng đi vào vòng bỏ phiếu tiếp, loại dần cho tới khi chỉ còn 1 hoặc 2 người ở lại. <br>

<ins>Chiến thuật trong truyện (nguyên tác): </ins> <br>
Có 22 người, lập ra nhóm 8 người rồi chia đôi ra nửa đội bỏ Yes nửa đội bỏ No, nên sẽ luôn có 1 nửa đội ở lại sau mỗi vòng. Tác giả trò chơi này tức Ngô Thanh Liêm đã sáng tạo hơn khi nghĩ ra cách là lập team 2 người lúc bắt đầu và chỉ kết nạp thêm 1 người vào đội sau mỗi vòng, như vậy hạn chế được số người trong team và số Tiền thưởng chia ra được nhiều hơn. Nhưng trong bài này ta sẽ không làm vậy, hơn nữa lập team kiểu đó cũng có rất nhiều rủi ro so với việc lập 1 team hoàn chỉnh ngay khi mới bắt đầu. <br>

Khi cho tổng quát với $n$ người, việc chọn lựa sẽ khó khăn hơn, nhất là phải xét đến trường hợp mà team bị lẻ người ở 1 vòng nào đó, vì không phải lúc nào cũng chọn được số người có dạng $2^{k}$ (số chính phương).

## Lời giải 
### 1. Thu hẹp phạm vi tìm kiếm 
- Số người của nhóm mình và số người ở nhóm tự do (bỏ phiếu ngẫu nhiên) sẽ thay đổi sau mỗi vòng như thế nào ? <br>
- Gọi số người nhóm mình là $a$ , nhóm tự do là $b$ . Ta quy ước dấu “ $\rightarrow$ ” dùng để biểu diễn sự thay đổi số người mỗi bên sau 1 vòng bỏ phiếu.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* $a$ chẵn thì khi đó $a \rightarrow \frac{a}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b-2}{2} = \frac{b}{2} - 1$ <br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* $a$ lẻ thì khi đó $a \rightarrow \frac{a-1}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b}{2}$  *(*1)* <br><br>
$\Longrightarrow$ Tới đây ta đặt ra tình huống xấu nhất như sau: sau mỗi vòng số người tự do còn lại nhiều nhất, số người nhóm mình còn lại ít nhất; dựa trên nhận xét: nếu thế $(a,b)$ đảm bảo chiến thắng thì $(a,b-1)$ và $(a+1,b-1)$ cũng vậy (theo nguyên lí quy nạp). <br>

- Gọi $V$ là số người cần lấy ra từ $N$ người để tạo ra nhóm, khi đó ta thu hẹp giới hạn để tìm $V$ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>*Giới hạn dưới*</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $(a;b)=(a_{0};b_{0})$ ở vòng cuối cùng, có thể thực hiện 1 thuật toán để truy ngược lại các giá trị $V,N-V$ ban đầu bằng cách làm quay lùi thời gian qua các vòng bỏ phiếu cùng với đó là số người của 2 bên tăng dần tới $V$ và $N-V$ (xem lại *(*1)* ): Nếu $(a,b)$ là kết quả sau 1 vòng bỏ phiếu thì lùi về trước khi bỏ phiếu là $(2a;2b+2)$ , vì ta kỳ vọng $V$ là nhỏ nhất và $N-V$ là lớn nhất. <br>
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
### 2. Công thức chính xác cho $V$ <br>
- Sau khi tìm ra giới hạn cho $V$ , vẫn có vấn đề khi khoảng giới hạn này sẽ rộng với $N$ lớn, không thể quét qua tất cả các giá trị được. Làm các ví dụ với $N \le 100$ gợi ý cho tôi rằng giá trị tối ưu $V$ luôn có dạng $2^{k}$ . Tôi bắt đầu nghi ngờ xem giữa $\frac{N+2}{3}$ và $\frac{2(N+1)}{3}$ có bao nhiêu giá trị dạng $2^{k}$ , thật bất ngờ, luôn chỉ có tối đa là $1$ . <br>
- Tức ta có:
```math
{\log _2}\left[ {\frac{1}{3}\left( {N + 2} \right)} \right] \le k \le {\log _2}\left[ {\frac{2}{3}\left( {N + 1} \right)} \right] = {\log _2}\left[ {\frac{1}{3}\left( {N + 2} \right)} \right] + d
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Với $d = 1 - {\log _2}\left( {1 + \frac{1}{{N + 1}}} \right)$ thì $d<1$ , nhận xét $d \to {1^ - }$ khi $N \to \infty$ tức chỉ có nhiều nhất 1 số tự nhiên $k$ . Nhưng cũng có thể không có giá trị $k$ nào cả, hoặc nếu có thì cũng chưa thể khẳng định được $V=2^{k}$ là giá trị tối ưu <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Bổ đề 2.1:</ins>* Nếu tồn tại giá trị $V=2^{k}$ nhỏ nhất đảm bảo chiến thắng cho trò chơi “Luật tối thiểu” thì đây cũng đồng thời là giá trị tối ưu cần tìm cho bài toán. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ý tưởng:</ins>* Để *bổ đề* trên chứng minh trở nên thuận lợi, ta chứng minh qua ý nhỏ *(*2)* sau: Nếu $V=2^{s}$ không đảm bảo chiến thắng thì $V=2^{s+1}-1$ cũng vậy. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh ý* <ins>*(*2)</ins>* </ins>: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $V=2^{s}$ và $N-V=B$ thì sau $s$ lượt bỏ phiếu $a = 1,{\rm{ }}b \le {B_0}$ ( $B_0$ là kết quả sau khi lấy giá trị khởi đầu là $B$ và lặp lại phép toán $\frac{{Ans - 1}}{2}$ qua $s$ lần), $b \ge 1$ theo giả thiết ta không thể chiến thắng tức ${B_0} \ge b \ge 1{\rm{ }}$ *(*3)* . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến ta có: $V' = {2^{s + 1}} - 1;B' = N - V'$ do $V'$ lẻ nên số người đội ta giảm sau mỗi vòng theo kiểu $\frac{a-1}{2}$ , suy ra sau $s$ lượt bỏ phiếu cũng có $a' = 1{\rm{ }} \vee b' \ge {B_0}^\prime$ ( ${B_0}^\prime$ cũng định nghĩa như $B_0$  với giá trị khởi đầu là $B'$ )  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác do dễ nhận thấy $B' = B - {2^s} + 1$ nên ta suy ra: <br>
```math
{B_0}^\prime  = {B_0} - \frac{{{2^s} - 1}}{{{2^s}}} = {B_0} - 1 + \frac{1}{{{2^s}}}  \text{        (*4)}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Phản chứng:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giả sử $V'$ đem lại chiến thắng tức $b' = 0 \to {B_0}^\prime  \le b' = 0$ , kết hợp *(*4)* suy ra ${B_0} \le 1 - \frac{1}{{{2^s}}} < 1$ , điều này mâu thuẫn với *(*3)* nên khi đó $V'$ không thể đem lại chiến thắng tức *(*2)* được chứng minh. <br> 
Giả sử tồn tại giá trị $V=2^{k}$ nhỏ nhất đảm bảo chiến thắng cho trò chơi thì $V=2^{k-1}$ không đảm bảo chiến thắng, kéo theo *(*2)* : $V=2^{k}-1$ cũng không đảm bảo chiến thắng, suy ra tất cả các giá trị $V \le 2^{k}-1$ đều không đảm bảo chiến thắng, do đó $V=2^{k}$ là giá trị tối ưu của $V$ . <br>

$\Longrightarrow$ ***Bổ đề 2.1*** đã được chứng minh. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ta mới chỉ giả sử có 1 giá trị $2^{k}$ tồn tại, nếu nó không tồn tại ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Có thể loại bỏ điều này như sau: Xét $N=2^{m}$ , tình huống trở thành tầm thường vì chọn $V=2^{m}$ đảm bảo chiến thắng. Nên ta sẽ xét $N$ không phải là lũy thừa của 2, có thể thấy giá trị $2^m$ liền trước $N$ đảm bảo chiến thắng *(*5)* . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Khi đó ta có đủ cơ sở để quy về chứng minh mệnh đề sau:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mệnh đề 2.2:</ins>* ${2^m} < N < {2^{m + 1}}$
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh mệnh đề 2.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chọn $V = {2^m}$ và $N - V = N - {2^m} < {2^m} \Rightarrow N - V \le {2^m} - 1$  .
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dễ thấy thế bắt đầu $\left( {{2^m}{{,2}^m} - 1} \right)$ luôn dẫn đến chiến thắng vì số người 2 phe sẽ giảm dần tới $(1,0)$ sau $m$ lượt bỏ phiếu, suy ra  bất kỳ thế $\left( {{2^m},N - V} \right)$ nào thỏa mãn $N - V \le {2^m} - 1$ đều dẫn tới chiến thắng tức *(*5)* được chứng minh. Suy ra luôn tồn tại giá trị $V = {2^k}$ nhỏ nhất đảm bảo chiến thắng, kết hợp với ***bổ đề 2.1*** vừa nêu, ta kết luận đây cũng chính là giá trị tối ưu của $V$ mà ta cần chọn. 













