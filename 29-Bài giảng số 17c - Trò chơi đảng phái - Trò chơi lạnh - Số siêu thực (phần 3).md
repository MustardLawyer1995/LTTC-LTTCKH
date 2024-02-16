# Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 3)
### 5. Các trò chơi có thành phần vô hạn
#### &nbsp;&nbsp;&nbsp;a. Vô cùng lớn và vô cùng bé
&nbsp;&nbsp;&nbsp;&nbsp;Quay lại với trò chơi Hackenbush 2 màu, xét 1 cây có số lượng đoạn kéo dài đến vô tận. Rõ ràng trạng thái này vẫn thỏa mãn yêu cầu của 1 trò chơi kết hợp - kết thúc sau hữu hạn lượt đi, vì người chơi phải chọn 1 trong số các đoạn để cắt, khiến cho cây này sau đó trở thành 1 cây có độ dài hữu hạn như trong trò chơi thông thường. Với 1 cây thẳng có vô hạn đoạn màu xanh, người chơi Xanh có thể cắt 1 đoạn tại bất cứ vị trí nào, nên cây mới được tạo ra có độ dài là một số tự nhiên tùy ý $\rightarrow$ Giá trị của cây theo định nghĩa là: $\\{ 0,1,2,3,4,... | \space\space\space \\} = \omega$ , với $\omega$ là một giá trị đặc biệt, nó lớn hơn bất cứ số tự nhiên nào. Nhưng $\omega$ không hoàn toàn giống như $\infty$ (vô cực). Với vô cực, $\infty$ hay $\infty +1$ hay $2\infty$ cũng không có gì khác biệt. Nhưng $\omega < \omega + 1$ dù cả 2 đều đại diện cho cái gì đó vô cùng lớn, lớn đến mức không đo đếm được. Thật vậy, xét 1 trò chơi gồm 3 cây thẳng: (xanh-xanh-xanh-...) (giá trị là $\omega$ ), (đỏ-đỏ-đỏ-...) (giá trị là $-\omega$ ), (xanh) (giá trị 1), giá trị của trò chơi là: $G = \omega + 1 - \omega$ . Dễ thấy người chơi Xanh luôn thắng dù ai đi trước $\rightarrow$ $G > 0$ $\rightarrow$ ta buộc phải thừa nhận $\omega + 1 > \omega$ . Một cách đơn giản hơn là tính giá trị của trò chơi gồm 2 cây thẳng (xanh-xanh-xanh-...) và (xanh) là $\omega + 1$ , mặt khác giá trị theo định nghĩa là $\\{ 0,1,2,...\omega | \space\space\space \\}$  vì Xanh có thể cắt 1 đoạn để đưa trò chơi về các giá trị $1,2,3,...$ hay một số nguyên dương tùy ý (nếu cắt cây vô hạn) hoặc $\omega$ (nếu cắt cây gồm 1 đoạn duy nhất) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ $\\{ 0,1,2,...\omega | \space\space\space \\} = \\{ \omega| \space\space\space \\} = \omega + 1$ $\rightarrow$ $\omega < \omega + 1$ theo ***tiên đề (0.2) mục 4/***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tương tự, có thể định nghĩa: <br>

```math
\left\{ {\omega  + 1|{\space\space\rm{ }}} \right\} = \omega  + 2,\left\{ {\omega  + 2|{\space\space\rm{ }}} \right\} = \omega  + 3...,\left\{ {\omega  + k|\space\space{\rm{ }}} \right\} = \omega  + k + 1{\rm{ }}(k \in \mathbb{N})
```
&nbsp;&nbsp;&nbsp;&nbsp;và vì thế $\omega  + 1 < \omega  + 2 < \omega  + 3 < \omega  + 4 < ...$ . Nếu thay đoạn xanh đơn độc trong trò chơi trên thành đỏ thì giá trị trò chơi là: $\omega  - 1 = \\{ { - 1,{\rm{ }}0,{\rm{ }}1,{\rm{ }}2,{\rm{ }}3,{\rm{ }}...|\omega } \\} \to \omega  - 1$ là giá trị nhỏ hơn $\omega$ nhưng lớn hơn mọi số tự nhiên hữu hạn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tương tự, ta cũng lần lượt có: <br>

```math
\left\{ {0,1,2,3...|\omega  - 1} \right\} = \omega  - 2,\left\{ {0,1,2,3...|\omega  - 2} \right\} = \omega  - 3,\left\{ {0,1,2,3...|\omega  - k} \right\} = \omega  - k - 1{\rm{ }}\left( {k \in \mathbb{N}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Trên thực tế, chính cách định nghĩa nêu trên đã áp đặt phép "+" lên các giá trị $\omega$ nên ***định lý (2.2)*** về sự tương đương   và ***định lý (2.3)*** về tính "đơn giản nhất" của các số siêu thực (xem lại ***mục 4/***) vẫn còn hiệu lực. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì vậy cũng có $\\{ \omega - 1|\omega + 1 \\} = \omega , \\{ \omega|\omega + 1 \\} = \omega + \frac{1}{2}$ hay $\\{ \omega|\omega + \frac{1}{2} \\} = \omega + \frac{1}{4}$ (có thể coi $\omega$ như một giá trị nguyên).<br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\\{ \omega,\omega + 1,\omega + 2,... |\space\space\space \\} = 2\omega$, vì hiển nhiên $2\omega = \omega + \omega > \omega + k$ với mọi $k \in \mathbb{N}$ , tương tự ta cũng có: <br>

```math
\;\left\{ \begin{array}{l}
\left\{ {n\omega ,n\omega  + 1,n\omega  + 2,{\rm{ }}...|\space\space\space{\rm{ }}} \right\} = \left( {n + 1} \right)\omega ,\
\left\{ {n\omega ,n\omega  + 1,n\omega  + 2,{\rm{ }}...|\left( {n + 1} \right)\omega  - k} \right\} = \left( {n + 1} \right)\omega  - k - 1,\left\{ {n\omega  + k|\space\space\space{\rm{ }}} \right\} = n\omega  + k + 1{\rm{ }}
\end{array} \right. \space\space\space\space\space \left( {n,k \in \mathbb{N}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Thế còn $\frac{\omega}{2}$ ? $\rightarrow$ Dễ thấy được rằng: <br>

```math
\frac{\omega }{2} > k{\rm{ }}\left( {\forall k \in \mathbb{N}} \right) \to \frac{\omega }{2} = \omega  - \frac{\omega }{2} < \omega  - k\left( {\forall k \in \mathbb{N}} \right) \to \frac{\omega }{2} = \left\{ {0,1,2...|\omega ,\omega  - 1,\omega  - 2...} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;, các giá trị $\frac{k \omega}{2^s}$ cũng được định nghĩa tương tự (chúng đều có vai trò như các số nguyên trong tất cả định nghĩa và định lý ở ***mục 4/***). Khi $> 1$ lựa chọn, ta chọn giá trị đơn giản nhất. Giá trị $n_{1}\omega + n_{0}$ (với $n_{0},n_{1}$ là số dyadic) đơn giản nhất được xác định bằng cách chọn lọc ra các giá trị có $n_1$ đơn giản nhất, trong số chúng chọn ra giá trị có $n_0$ đơn giản nhất. Phạm vi lớn hơn, có thể viết như sau: <br>

```math
\left\{ \begin{array}{l}
\left\{ {\omega ,2\omega ,3\omega ,...|\space\space\space\space{\rm{ }}} \right\} = \omega ,{\rm{                          }}\
\left\{ {\omega ,2\omega ,3\omega ,...|\omega } \right\} = \omega - 1,{\rm{ }}\
\left\{ {\omega ,2\omega ,3\omega ,...|\omega - 1,\omega - 2,\omega - 3,...} \right\} = {\omega}^2 - \omega ,...
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;Có thể ngoại suy được quy tắc chọn giá trị $n_{2}{\omega}^2 + n_{1}\omega + n_{0}$ (với $n_{0},n_{1},n_{2}$ là số dyadic) đơn giản nhất: ưu tiên những giá trị có $n_2$ đơn giản nhất, trong số chúng chọn ra giá trị có $n_{1}\omega + n_{0}$ đơn giản nhất; tương tự với các đa thức $N\( \omega \)$ bậc cao hơn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Phạm vi lớn hơn nữa, ta có: $\omega , {\omega}^2 , {\omega}^3 , ..... {\omega}^{\omega}$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;Xét 1 cây thẳng có vô hạn đoạn: xanh-đỏ-đỏ-..., theo ***quy tắc 3 (ở mục 3/)***, giá trị của cây là: $\\{ 0|1,\frac{1}{2},\frac{1}{4},\frac{1}{8},... \\} = \varepsilon$ , với $\varepsilon$ là một giá trị lớn hơn $0$ nhưng nhỏ hơn bất cứ số dương nào, có thể hiểu nôm na $\varepsilon$ là một giá trị "vô cùng bé", nhỏ đến mức không thể đo được. Nhưng cũng như $\omega$ , không phải các số vô cùng bé đều bằng nhau về giá trị: <br>
<div align="center">

$\\{ 0|1,\frac{1}{2},\frac{1}{4},\frac{1}{8},... \\} = 2\varepsilon$ (giá trị của 2 cây xanh-đỏ-đỏ-đỏ-... hoặc của 1 cây xanh(xanh, đỏ-đỏ-đỏ-...)), ...,
</div>

```math
\left\{ {k\varepsilon \bigg\vert 1,\frac{1}{2},\frac{1}{4},\frac{1}{8},{\rm{ }}...} \right\} = \left( {k + 1} \right)\varepsilon {\rm{ }},\space\space \left( {k \in \mathbb{N}} \right),\left\{ {0|\varepsilon } \right\} = \frac{\varepsilon }{2},\left\{ {0 \bigg\vert \frac{\varepsilon }{2}} \right\} = \frac{\varepsilon }{4},...,\left\{ {\frac{{\left( {k - 1} \right)\varepsilon }}{{{2^s}}} \bigg\vert \frac{{\left( {k + 1} \right)\varepsilon }}{{{2^s}}}} \right\} = \frac{{k\varepsilon }}{{{2^s}}} \space\space , ( k \text{ lẻ } )
```
&nbsp;&nbsp;&nbsp;&nbsp;Các định nghĩa này cũng ngụ ý $\varepsilon$ có vai trò như một phân số dyadic, và vì thế áp dụng tốt ***(2.1), (2.2), (2.3)*** của ***mục 4/***. Có thể tìm được những giá trị nhỏ hơn nữa như sau: <br>

```math
\left\{ {0 \bigg\vert \varepsilon ,\frac{\varepsilon }{2},\frac{\varepsilon }{4},\frac{\varepsilon }{8}...} \right\} = \varepsilon ,\left\{ {k\varepsilon \bigg\vert \varepsilon ,\frac{\varepsilon }{2},\frac{\varepsilon }{4},\frac{\varepsilon }{8}...} \right\} = \left( {k + 1} \right)\varepsilon , \left\{ {\frac{{\left( {k - 1} \right){\varepsilon ^2}}}{{{2^s}}} \bigg\vert \frac{{\left( {k + 1} \right){\varepsilon ^2}}}{{{2^s}}}} \right\} = \frac{{k{\varepsilon ^2}}}{{{2^s}}},\left\{ {k{\varepsilon ^2}:k \in \mathbb{N} |\varepsilon  - n{\varepsilon ^2}} \right\} = \frac{\varepsilon }{2} \space\space , \left( {n \in \mathbb{N}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, giá trị $n_{2}{\varepsilon}^2 + n_{1}\varepsilon + n_{0}$ đơn giản nhất được xác định bằng cách lần lượt lựa chọn ra $n_{0},n_{1},n_{2}$ là những số dyadic đơn giản nhất có thể; tương tự với các đa thức $N \( \varepsilon \)$ bậc cao hơn... <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo quy tắc chọn số đơn giản nhất, ta có: <br>

```math
\left\{ {\left\{ {k\varepsilon :k \in \mathbb{N}} \right\} \bigg\vert \left\{ {\frac{\omega }{{{2^s}}}:s \in \mathbb{N}} \right\}} \right\} = \varepsilon \omega 
```
&nbsp;&nbsp;&nbsp;&nbsp;vì đây là giá trị đơn giản nhất thỏa mãn: $\varepsilon  < 2\varepsilon  < 3\varepsilon  < 4\varepsilon  < ... < \varepsilon \omega {\rm{  < }}... < \frac{\omega }{8} < \frac{\omega }{4} < \frac{\omega }{2} < \omega$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, vì $k\varepsilon  - 1 < 0$ và $\varepsilon \omega ,\frac{\omega }{{{2^s}}} - 1 > 0{\rm{   }}\left( {\forall k,s \in \mathbb{N}} \right)$ ta dễ dàng nhận thấy: <br>

```math
\left\{ {\left\{ {k\varepsilon :k \in \mathbb{N}} \right\} \bigg\vert \left\{ {\frac{\omega }{{{2^s}}}:s \in \mathbb{N}} \right\}} \right\} - 1 = \left\{ {\left\{ {k\varepsilon :k \in \mathbb{N}} \right\} \bigg\vert \left\{ {\frac{\omega }{{{2^s}}}:s \in \mathbb{N}} \right\}} \right\} + \left\{ \space\space {{\rm{ }}|0} \right\} = \left\{ {\left\{ {k\varepsilon  - 1:k \in \mathbb{N}} \right\} \bigg\vert \left\{ {\frac{\omega }{{{2^s}}} - 1:s \in \mathbb{N}} \right\},\varepsilon \omega } \right\} = 0
```
&nbsp;&nbsp;&nbsp;&nbsp;Nên ta suy ra: $\varepsilon \omega - 1 = 0$ tương đương với $\varepsilon \omega = 1$ <br>
#### &nbsp;&nbsp;&nbsp;b. Tập số siêu thực và tập số thực
&nbsp;&nbsp;&nbsp;&nbsp;Không phải mọi giá trị trong trò chơi có thành phần vô hạn đều là các giá trị ở trên trời như $\omega$ và $\varepsilon$ . Một số cây vô hạn trong hackenbush 2 màu có các giá trị hữu hạn như cây: xanh-đỏ-đỏ-xanh-đỏ-xanh-đỏ-xanh-đỏ-..., giá trị của nó là: <br>

```math
1 - \frac{1}{2} - \frac{1}{4} + \frac{1}{8} - \frac{1}{{16}} + \frac{1}{{32}} - \frac{1}{{64}} + ... + \frac{1}{{{2^{2k - 1}}}} - \frac{1}{{{2^{2k}}}} + ... = \frac{1}{4} + \frac{1}{{16}} + \frac{1}{{64}} + ... + \frac{1}{{{4^k}}} + ... = \frac{1}{4}.\frac{1}{{1 - {\raise0.5ex\hbox{$\scriptstyle 1$}
\kern-0.1em/\kern-0.15em
\lower0.25ex\hbox{$\scriptstyle 4$}}}} = \frac{1}{3}
```
&nbsp;&nbsp;&nbsp;&nbsp;Nhưng $\frac{1}{3}$ không phải là một số dyadic? Phát hiện này gợi ý rằng số siêu thực có thể là một số thực bất kỳ. Giá trị $\frac{1}{3}$ có thể được biểu diễn ở dạng tiêu chuẩn là: <br>

```math
\left\{ {\frac{1}{4},\frac{5}{{16}},\frac{{21}}{{64}},...,\frac{{{4^k} - 1}}{{{{3.4}^k}}},... \bigg\vert \frac{1}{2},\frac{3}{8},\frac{{11}}{{32}},...,\frac{{{{2.4}^k} + 1}}{{{{6.4}^k}}},...} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Mà mặt khác ta lại có: $\left( {{4^k} - 1} \right) \vdots 3$ và $\left( {{{2.4}^k} + 1} \right) \vdots 3$  nên hệ quả là ta sẽ có 2 bộ số ở 2 bên dấu | chỉ gồm các số hữu tỉ dyadic, và vì vậy các kết quả ở ***mục 4/*** vẫn áp dụng được cho những số siêu thực đặc biệt này. Tính hợp lý của dạng thức trên nằm ở việc: <br>
### 6. Các giá trị trong trò chơi nóng





















