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















