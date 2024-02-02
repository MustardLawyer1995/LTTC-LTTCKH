# Misere Partial game và Lí thuyết chi – Chiến thuật đối xứng
### 1. Chiến thuật của Misere Nim Game <br>
&nbsp;&nbsp;&nbsp;&nbsp;Người ta nhận ra 1 điểm kỳ lạ: khi một nim game được chơi theo phiên bản misere, các tính toán trên máy tính cho thấy các nước đi (tối ưu) vẫn giống như trong phiên bản normal, chỉ khác ở những nước đi cuối cùng. Cụ thể, gần về cuối game, nếu 1 tình huống mà ở normal game người thắng phải tạo ra một số lượng chẵn các đống chỉ gồm 1 quân, thì ở misere game, phải tạo số lẻ. Có thể tổng quát chiến lược tất thắng cho misere nim game như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Nimber của mỗi đống được tính theo cách như của normal nim game, tính tổng xor giữa chúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Liên tục đưa tổng xor về 0, giống như trong normal nim game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Ở giai đoạn khi chỉ còn duy nhất 1 đống có kích thước > 1, các đống khác đều chỉ còn 1 quân (đây là giai đoạn quyết định số lượng đống 1 là chẵn hay lẻ), ta phải chọn sao cho tạo ra 1 số lẻ đống 1. Việc này có thể được quyết định dễ dàng bằng việc lấy hết các quân trong đống > 1 kia, hoặc để chừa lại 1 quân. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh đây là chiến thuật tất thắng: tất nhiên, khi bạn đã tạo ra số lẻ các đống 1, thì đối phương thua là chắc chắn rồi, bây giờ ta sẽ chỉ ra rằng việc làm cho đối phương rơi vào các thế có tổng xor = 0 liên tục sẽ khiến quyền quyết định số lượng đống 1 rơi vào tay bạn. Đầu tiên, vì trò chơi kết thúc sau hữu hạn lượt đi <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Sẽ có 1 thời điểm chỉ còn duy nhất 1 đống có > 1 quân, các đống khác đều có 1 quân (thời điểm quyết định số lượng đống 1 là chẵn hay lẻ), vấn đề là vào thời điểm này, đang là lượt của người chơi nào? (ai có quyền quyết định số lượng đống 1 là chẵn hay lẻ?) Không thể là đối phương, vì hắn ta bị bạn đưa về các trạng thái tổng xor = 0 liên tục, tức là đến lượt của hắn, tổng xor phải = 0, nhưng việc tồn tại 1 đống có > 1 quân trên bàn làm cho tổng xor không thể = 0 <br>
&nbsp;&nbsp; $\Longrightarrow$ Đó phải là lượt của bạn! Bạn thắng rồi. ***(chứng minh hoàn tất)*** <br>

### 2. Lý thuyết chi <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Tổng quan* 
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Lý thuyết chi (genus theory)</ins>*** đẩy vấn đề lên mức độ bao quát hơn, nhằm tìm lời giải cho tất cả các *impartial game* được chơi theo phiên bản misere. Cần nói thêm rằng, lý thuyết chi chưa phải 1 lý thuyết hoàn chỉnh như định lý *Sprague Grundy*. Lý thuyết chi hoạt động theo cách gán bừa giá trị nimber là 1 cho misere game ở trạng thái không còn nước đi tiếp theo (người đi trước mặc định thắng), và giá trị nimber cho các trạng thái khác cứ áp nguyên định nghĩa cũ của nimber mà tính. Chúng được gọi là misere nimber, ký hiệu $G^-$ , phân biệt với $G^+$ là nimber được tính theo luật chơi normal (normal nimber), lý thuyết chi sử dụng cả 2 loại thông số này. Một game sẽ được mô hình hóa thành dạng mạng đồ thị, mỗi điểm nút trong đó là 1 trạng thái của game, gồm 2 thông số tương ứng là $\( G^{+};G^{-} \)$ , mỗi cạnh nối giữa 2 nút là 1 nước đi. Để thuận tiện cho việc trình bày tôi sẽ dùng các ký hiệu quy ước sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $V\( G^{+};G^{-} \)$ là tập hợp tất cả các điểm có 2 giá trị normal/misere nimber là $G^+$ và $G^-$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $V(T)$ là tập hợp tất cả các "tận điểm" - điểm kết thúc của trò chơi, tại trạng thái này không còn nước đi tiếp theo nào để thực hiện nữa, như vậy $V(T) \in V\( 0,1 \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Một trạng thái $\( 0,1 \)$ hay $\( 1,0 \)$ sẽ được gọi là các "hoán điểm" <br>

&nbsp;&nbsp;&nbsp;&nbsp;Hiện chỉ có 1 lớp trò chơi misere là đã có lời giải tổng quát, chúng được gọi là ***<ins>trò chơi thuần hóa (tame game)</ins>***, thỏa mãn định nghĩa: *tame game* là trò chơi chỉ gồm các trạng thái $\( 0,1 \),\( 1,0 \),\( k,k \) , \text{   } \( k \in \mathbb{N} \)$ <br>
#### *<ins>Định lí 1.1</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Một game là tame game $\Leftrightarrow$ mọi trạng thái $x$ của nó thỏa mãn ít nhất 1 trong 3 mệnh đề sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (a) $x \in V\( 0,1 \) \cup V\( 1,0 \) \cup V\( 0,0 \) \cup V\( 1,1 \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (b) Từ $x$ có nước dẫn đến $\( 0,1 \)$ và $\( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (c) Từ $x$ có nước dẫn đến $\( 0,0 \)$ và $\( 1,1 \)$ . <br> 

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều thuận)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh tame game thoả mãn những điều trên: Theo định nghĩa của tame game, các điểm không phải là $\( 0,1 \), \( 1,0 \), \( 0,0 \), \( 1,1 \)$ đều là $\( k,k \)$ với mọi $k \ge 2$ , và vì thế từ chúng phải có các nước dẫn đến $\( 0, \textunderscore \) , \( 1, \textunderscore \), \( \textunderscore,0 \), \( \textunderscore,1 \)$ (kí hiệu <ins>gạch dưới</ins> biểu diễn rằng: 1 hoặc 0 đều được) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Chúng thỏa mãn ít nhất 1 trong 2 mệnh đề (b), (c) tức ta có điều phải chứng minh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều nghịch)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gọi $d(x)$ là khoảng cách - số nước đi tối đa để đi từ $x$ tới tận điểm. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ta chứng minh 1 game thỏa mãn những điều trên là tame game: Ta sẽ sử dụng quy nạp, chỉ ra rằng nếu các điểm $x$ với $d(x) \le D$ đều thỏa mãn định nghĩa của tame game thì các điểm $x$ với $d(x)=D+1$ cũng thỏa mãn định nghĩa tame game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Thật vậy, xét các điểm $x$ với $d(x)=D+1$ , ta có 3 trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1) Nếu $x=\( 0, \textunderscore \)$ , không thể có nước dẫn tới $\( 0,1 \)$ hay $\( 0,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2) Nếu $x=\( 1, j \)$ với $j \ne 0$ , từ $x$ không có nước dẫn đến $\( 1,0 \)$ hay $\( 1,1 \)$ $\rightarrow$ $x$ phải thỏa mãn (a) $\rightarrow$ $x=\( 1,1 \)$ (chứng minh tương tự với $x=\( i, 1 \)$ với $i \ne 0$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(3) Nếu $x=\( i, j \)$ với $i,j \ge 2$ , theo quy nạp, mọi điểm mà từ $x$ dẫn tới đều $\in V\( 0,1 \) \cup V\( 1,0 \) \cup V\( k,k \)$ $\rightarrow$ Từ $x$ có các nước dẫn tới $\( 0, \textunderscore \) , \( 1, \textunderscore \), \( \textunderscore,0 \), \( \textunderscore,1 \)$ và $\( k,k \)$ với $2 \le k \le i-1$ , không có nước dẫn tới $\( i,i \)$ $\rightarrow$ $j= \text{Mex} \\{ k \le i-1 \\} = i$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Mệnh đề quy nạp đã được chứng minh. Mặt khác, các điểm có $d(x)=0$ mặc nhiên thỏa mãn định nghĩa tame game (chúng chính là các tận điểm, và vì thế $=\( 0,1 \)$ ), quy nạp hoàn tất $\rightarrow$ Ta có điều phải chứng minh. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Chứng minh ***<ins>định lí 1.1</ins>*** hoàn tất <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở rộng:</ins>* Làm sao để xác nhận 1 game có phải là tame game hay không ?<br>

#### *<ins>Định lí 1.2</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Một game là tame game $\Leftrightarrow$ Nó phải chứa 4 tập phân biệt $V'\( 0,1 \), V'\( 1,0 \), V'\( 0,0 \), V'\( 1,1 \)$ thỏa mãn tất cả mệnh đề bên dưới đây: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (i) Các tập là phi liên kết - không có nước đi nào giữa 2 điểm trong cùng tập hợp. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (ii) $V\( T \) \in V'\( 0,1 \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (iii) Từ $V'\( 0,1 \) \backslash V(T)$ có nước đi sang $V'\( 1,0 \)$ nhưng không có nước đi sang $V'\( 0,0 \) \cup V'\( 1,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (iv) Từ $V'\( 1,0 \)$ có nước đi sang $V'\( 0,1 \)$ nhưng không có nước đi sang $V'\( 0,0 \) \cup V'\( 1,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (v) Từ $V'\( 1,1 \)$ có nước đi sang $V'\( 0,0 \)$ nhưng không có nước đi sang $V'\( 0,1 \) \cup V'\( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (vi) Từ $V'\( 0,0 \)$ không có nước đi sang $V'\( 0,1 \) \cup V'\( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- (vii) Mọi điểm $x$ trong game thỏa mãn ít nhất 1 trong 3 điều kiện dưới: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(a') $V'\( 0,1 \) \cup V'\( 1,0 \) \cup V'\( 0,0 \) \cup V'\( 1,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(b') Có nước đi từ $x$ sang $V'\( 0,1 \) \cup V'\( 1,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(c') Có nước đi từ $x$ sang $V'\( 0,0 \) \cup V'\( 1,1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Và hệ quả phụ khi tất cả các mệnh đề từ (i) đến (vii) được thỏa mãn là: $V'\( 0,1 \) = V\( 0,1 \)$ ; $V'\( 1,0 \) = V\( 1,0 \)$ ; $V'\( 0,0 \) = V\( 0,0 \)$ ; $V'\( 1,1 \) = V\( 1,1 \)$ ; <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều thuận)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh tame game thoả mãn những điều trên. Hiển nhiên rồi, đặt $V'\( 0,1 \) = V\( 0,1 \) ; V'\( 1,0 \) = V\( 1,0 \) ; V'\( 0,0 \) = V\( 0,0 \) ; V'\( 1,1 \) = V\( 1,1 \)$ thu được kết luận trên theo ***định lý 1.1*** $\rightarrow$ Ta có điều phải chứng minh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều nghịch)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh 1 game thỏa mãn những điều trên là tame game. Sử dụng quy nạp, chỉ ra rằng trong 1 game thỏa mãn các mệnh đề từ (i) đến (vii), nếu $V'\( 0,1 \) = V\( 0,1 \) ; V'\( 1,0 \) = V\( 1,0 \) ; V'\( 0,0 \) = V\( 0,0 \) ; V'\( 1,1 \) = V\( 1,1 \)$ với mọi $x$ có $d(x) \le D$ (bởi theo ***định lí 1.1***, điều này cũng có nghĩa là các điểm trong phạm vi $d(x) \le D$ đều tuân theo định nghĩa tame game) thì các điểm $x$ có $d(x)=D+1$ cũng vậy: xét $d(x)=D+1$ ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1) Nếu $x=\( 0,0 \)$ , từ $x$ không có nước đi tới hoán điểm (đồng nghĩa không có nước đi tới $V'\( 0,1 \) \cup V'\( 1,0 \)$ ) và không có nước đi tới $\( 0,0 \)$ (đồng nghĩa không có nước đi tới $V'\( 0,0 \)$ ) $\rightarrow$ $x$ phải thỏa mãn (a'), mặt khác không thể có $x \in V'\( 0,1 \) \cup V'\( 1,0 \) \cup V'\( 1,1 \)$ do (iii), (iv) và (v) $\rightarrow$ $x \in V'\( 0,0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2) Nếu $x=\( 0,j \)$ với $j>0$ , từ $x$ có nước đi tới $\( 1,0 \)$ (tức $V'\( 1,0 \)$ ) và không có nước đi tới $V'\( 0,1 \) \cup V'\( 0,0 \)$ $\rightarrow$ $x$ phải thỏa mãn (a'), mà $x \notin V'\( 1,0 \) \cup V'\( 0,0 \) \cup V'\( 1,1 \)$ do (i), (iv), (v) và (vi) $\rightarrow$ $x \in V'\( 0,1 \)$ $\rightarrow$ từ $x$ không có nước tới $\( 1,1 \)$ theo (iii) $\rightarrow$ $j=1$ (tương tự với $x=\( i,0 \)$ với $i>0$ $\rightarrow$ $x \in V'\( 1,0 \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(3) Nếu $x=\( 1,j \)$ với $j>0$ , từ $x$ có nước tới $\( 0,0 \)$ (tức $V'\( 0,0 \)$ ) không có nước tới $V'\( 1,0 \) \cup V'\( 1,1 \)$ $\rightarrow$ $x$ phải thỏa mãn (a'), mặt khác  $x \notin V'\( 0,1 \) \cup V'\( 1,0 \) \cup V'\( 0,0 \)$ do (i), (iii) và (iv) $\rightarrow$ $x \in V'\( 1,1 \)$ $\rightarrow$ từ $x$ không có nước tới $\( 0,1 \)$ theo (v) $\rightarrow$ $j=1$ (tương tự với $x=\( i,1 \)$ với $i>0$ $\rightarrow$ $i=1,x \in V'\( 1,1 \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(4) Nếu $x=\( 1,j \)$ với $i,j \ge 2$ , theo quy nạp, mọi điểm từ $x$ dẫn tới đều $V\( 0,1 \) \cup V\( 1,0 \) \cup V\( k,k \)$ $\rightarrow$ từ $x$ có các nước dẫn tới $\( 0, \textunderscore \) , \( 1, \textunderscore \), \( \textunderscore,0 \), \( \textunderscore,1 \)$ và $\( k,k \)$ với $2 \le k \le i-1$ , như vậy $x$ thỏa mãn ít nhất (b') và (c'), do đó $x \notin V'\( 1,0 \) \cup V'\( 0,0 \) \cup V'\( 1,1 \)$ , không có nước dẫn tới $\( i,i \)$ $\rightarrow$ $j= \text{Mex} \\{ k \le i-1 \\} = i$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mệnh đề quy nạp đã được chứng minh. Mặt khác các điểm có $d(x)=0$ mặc nhiên thỏa mãn ***định lý 1.2*** (chúng chính là các tận điểm, và vì thế $=\( 0,1 \)$ ), quy nạp hoàn tất. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Chứng minh ***<ins>định lí 1.2</ins>*** hoàn tất <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Tổng của các tame game*
&nbsp;&nbsp;&nbsp;&nbsp;Xét 1 game được tạo thành từ tổng của nhiều tame game. Ta sẽ chứng minh nó cũng là tame game, và vì vậy game này sẽ chỉ gồm các trạng thái $\( 0,1 \), \( 1,0 \), \( k,k \)$ , $k \in \mathbb{N}$ , thuận tiện để tìm ra chiến lược tất thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cần nhắc lại về định nghĩa tổng của 2 game: $A_1$ và $A_2$ là 2 impartial game, xét 1 trò chơi $A$ gồm $A_1$ và $A_2$ được chơi đồng thời, với quy ước rằng ở mỗi lượt người chơi chỉ được phép thực hiện 1 nước đi trong $A_1$ hoặc $A_2$ , không phải là cả 2, cũng không được phép không đi nước nào (bỏ lượt), khi đó $A$ cũng là 1 impartial game và được gọi là tổng của 2 trò chơi con $A_1$ và $A_2$ ( $A=A_{1}+A_{2}$ ). Tương tự nếu $A$ là tổng của từ 3 trò chơi con trở lên. <br>

#### *<ins>Định lí 2.1</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $A_1$ và $A_2$ là 2 tame game thì game $A=A_{1}+A_{2}$ cũng là tame game. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Quy ước trạng thái $x$ của $A$ tương ứng với $x_1$ ở $A_1$ và $x_2$ ở $A_2$ , ký hiệu $x=\[ x_{1};x_{2} \]$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Game $A$ gồm 4 tập trạng thái $V'\( 0,1 \), V'\( 1,0 \), V'\( 0,0 \), V'\( 1,1 \)$ như sau: <br>

```math
\left\{ \begin{array}{l}
V'\left( {0,1} \right) = \left\{ {\left[ {\left( {0,1} \right),\left( {0,1} \right)} \right],\left[ {\left( {1,0} \right),\left( {1,0} \right)} \right]} \right\}{\rm{                 }}\
V'\left( {1,0} \right) = \left\{ {\left[ {\left( {0,1} \right),\left( {1,0} \right)} \right]} \right\}\
V'\left( {0,0} \right) = \left\{ {\left[ {\left( {0,1} \right),\left( {0,0} \right)} \right],\left[ {\left( {1,0} \right),\left( {1,1} \right)} \right],\left[ {\left( {n,n} \right),\left( {n,n} \right)} \right]} \right\},\forall n \in \mathbb{N} \
V'\left( {1,1} \right) = \left\{ {\left[ {\left( {0,1} \right),\left( {1,1} \right)} \right],\left[ {\left( {1,0} \right),\left( {0,0} \right)} \right],\left[ {\left( {2n,2n} \right),\left( {2n + 1,2n + 1} \right)} \right]} \right\},\forall n \in \mathbb{N}
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(các trường hợp đối xứng như $\[ a;b \]$ và $\[ b;a \]$ sẽ không được viết đầy đủ ra, ta cần hiểu là chúng có được tính đến). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ta thấy 4 tập hợp này hoàn toàn thỏa mãn các mệnh đề từ (i) đến (vii) của ***định lý 1.2*** nên $A$ chính là một tame game, và ***hệ quả phụ của (1.2)*** cho biết: $V\( 0,1 \) = V'\( 0,1 \) ; V\( 1,0 \) = V'\( 1,0 \) ; V\( 0,0 \) = V'\( 0,0 \) ; V\( 1,1 \) = V'\( 1,1 \)$ . <br>

#### *<ins>Hệ quả 2.2</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $A_{1};A_{2};...;A_{n}$ là tame game thì game $A=A_{1}+A_{2}+...+A_{n}$ cũng là tame game. Hơn nữa, một trạng thái $x= \[ x_{1};x_{2};...x_{n} \]$ ở $A$ là hoán điểm $\Leftrightarrow$ $x_{1};x_{2};...x_{n}$ đều là hoán điểm. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả 2.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Phép cộng các trò chơi con thành 1 trò chơi tổng hoàn toàn thỏa mãn các **tính chất giao hoán**, kết hợp y như phép cộng đại số; bởi ***định lý 2.1*** nên $A=A_{1}+A_{2}$ cũng là tame game $\rightarrow$ $\( A_{1}+A_{2} \) +A_{3} = A_{1}+A_{2}+A_{3}$ là tame game $\rightarrow$ $\( A_{1}+A_{2}+A_{3} \) +A_{4} = A_{1}+A_{2}+A_{3}+A_{4}$ là tame game $\rightarrow$ ... $\rightarrow$ $A=A_{1}+A_{2}+...+A_{n}$ cũng là tame game. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hơn nữa, các tập trạng thái từ ***định lý 2.1*** cho biết để $x= \[ \[ x_{1};x_{2};...x_{n-1} \] ; x_{n} \]$ là hoán điểm thì $\[ x_{1};x_{2};...x_{n-1} \]$ và $x_n$ đều phải là hoán điểm, để $\[ x_{1};x_{2};...x_{n-1} \]$ là hoán điểm thì $\[ x_{1};x_{2};...x_{n-2} \]$ và $x_{n-1}$ đều phải là hoán điểm,...,theo cách tương tự ta suy ra $x_{1};x_{2};...x_{n}$ đều là hoán điểm. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Có thể suy diễn theo chiều ngược lại để chứng minh rằng nếu $x_{1};x_{2};...x_{n}$ đều là hoán điểm thì $x= \[ x_{1};x_{2};...x_{n} \]$ là hoán điểm. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Chiến lược cho tame game*
&nbsp;&nbsp;&nbsp;&nbsp;Khi chơi theo luật misere, nếu tame game chỉ gồm 1 game con đơn lẻ, chỉ việc tính toán số misere nimber $(G^{-})$ của nó, rồi liên tục thực hiện các nước đi để đưa $G^-$ về 0, với điều kiện là $G^{-} \ne 0$ khi tới lượt bạn (giống như giá trị $G^+$ khi chơi theo luật normal). (\*) <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu game đang xét là tổng của nhiều tame game, theo ***định lí 2.1*** nó cũng là tame game và vì thế các trạng thái của nó sẽ có $\( G^{+};G^{-} \)$ rơi vào $\( 0,1 \),\( 1,0 \),\( k,k \)$ với $k \in \mathbb{N}$ . Nhờ vậy có thể suy ra được $G^-$ của 1 trạng thái từ $G^+$ của nó (mà  lại có thể được tính toán thuận tiện qua tổng xor). Nếu $G^{+}=k \ge 2$ thì $G^{+} = G^{-} = k$ ; nếu $G^{+} = 0$ hoặc $1$ thì $G^{-} = 0$ hoặc $1$ chưa thể xác định ngay, song khó khăn này được giải quyết bởi ***hệ quả 2.2***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi $G^{+} = 0$ , trạng thái hiện tại có thể là $\( 0,1 \)$ hoặc $\( 0,0 \)$ , nếu là $\( 0,1 \)$ (hoán điểm) thì các game con đều phải đang ở thế $\( 0,1 \)$ và $\( 1,0 \)$ , chỉ cần có ít nhất 1 game con đang không ở thế hoán điểm là đủ để kết luận game tổng cũng đang không ở thế hoán điểm (tức là nó đang ở thế $\( 0,0 \)$ , $G^{-} = 0$ ). Tương tự với trường hợp $G^{+} = 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi đã biết cách tính $G^{-}$ của game tổng thì ta có thể thực hiện chiến lược theo phương thức như ở (*). Một cách nôm na, vì mục tiêu là đưa đối thủ về các trạng thái có $G^{-} = 0$ , chỉ cần đưa đối thủ về $\( 0,0 \)$ hoặc $\( 1,0 \)$ , nếu nước đi tiếp theo của bạn làm cho các game con đều ở thế $\( 0,1 \)$ và $\( 1,0 \)$ thì hãy đưa $G^{+}$ về 1 (nói cách khác là tạo ra 1 số lẻ các game con ở thế $\( 1,0 \)$ ); nếu không, hãy đưa   về 0. (chắc các bạn đã nhận ra nó giống chiến lược của misere nim game ở ***mục 1/***). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Các bạn có biết vì sao người ta lại chọn tame game để nghiên cứu không (dù nó không có tính tổng quát) ? <br>                       &nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Vì trong thực tế các impartial game phổ biến đều có dạng tame game (như 1 sự sắp đặt "tình cờ" của tự nhiên). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Để hiểu rõ hơn, ta cùng xem qua các ví dụ dưới sau đây. <br>

















