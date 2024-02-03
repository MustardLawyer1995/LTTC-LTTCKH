# Misere Partial game và Lí thuyết chi - Chiến lược đối xứng (phần 2)
### 3. Chiến thuật của Misere Nim Game <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Định nghĩa*
&nbsp;&nbsp;&nbsp;&nbsp;Đây là 1 trò chơi mở rộng từ những trò chơi như nim game và trò chơi loại trừ, chúng có dạng sau: Cho trước nhiều đống vật thể, mỗi lượt người chơi chọn 1 đống rồi lấy ra khỏi đó 1 số lượng vật thể, số lượng này không tùy ý mà phải nằm trong 1 tập hợp các giá trị được phép chọn-tập $S$ . Trò chơi kết thúc khi không còn quân nào trên bàn, thắng thua dựa theo 2 phiên bản: normal - người đi nước cuối cùng thắng, misere-người đi nước cuối cùng thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Như vậy nim là ***<ins>trò chơi gia giảm</ins>*** với $S \in \mathbb{Z}^{+}$ và trò chơi loại trừ là trò chơi gia giảm với $S= \\{ 1,2,3...,k \\}$ . <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Pet game-một trường hợp riêng của tame game*
&nbsp;&nbsp;&nbsp;&nbsp;Ta đưa ra định nghĩa của 1 loại trò chơi mới là ***<ins>trò chơi thú cưng (Pet Game)</ins>***, là trường hợp đặc biệt của trò chơi thuần hóa (tame): Pet game là impartial game chỉ gồm các trạng thái giá trị nimber là $\( 0;1 \);\( 1;0 \);\( k;k \)$ với $k \ge 2$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giải thích:</ins>Bởi pet game là tame game nên nó mặc nhiên thỏa mãn các ***định lý 1.1 và 1.2***, khi ta coi $V\( 0,0 \) = V\( 1,1 \) = V'\( 0,0 \) = V'\( 1,1 \) = \emptyset$ <br>

#### *<ins>Định lí 2.3</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Cho một impartial game $A$ , những mệnh đề sau đây hoàn toàn tương đương với nhau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(i) $A$ là pet game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(ii) $A$ không chứa các điểm $\( 0;0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(iii) Với mọi $x \in A$ , nếu $G^{+}(x)=0$ và $x$ không phải tận điểm thì tồn tại nước đi từ $x \longrightarrow x'$ , $G^{+}\( x' \)=1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(iv) Với mọi $x \in A$ , nếu $G^{-}(x)=0$ thì tồn tại nước đi từ $x \longrightarrow x'$ , $G^{-}\( x' \)=1$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 2.3:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều thuận)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh (i) $\longrightarrow$ (ii), (i) $\longrightarrow$ (iii) và (i) $\longrightarrow$ (iv) thì hoàn toàn hiển nhiên theo định nghĩa ***pet game*** $\Rightarrow$ Ta có điều phải chứng minh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều nghịch)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh (i) $\longleftarrow$ (ii): Trong 1 game $A$ thỏa mãn (ii), mọi $x$ có $d(x)=0$ đều là $\( 0;1 \)$ nên mặc định thỏa mãn (i), quy nạp rằng nếu mọi $x$ với $d(x) \le D$ đều thỏa mãn (i) thì bất cứ $x$ nào có $d(x)=D+1$ cũng thỏa mãn (i). Thật vậy, xét $x$ có $d(x)=D+1$ , có 4 trường hợp sau xảy ra: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) Từ $x$ có nước tới $\( 0;1 \)$ và $\( 1;0 \)$ $\rightarrow$ $x= \( k;k \)$ với $k \ge 2$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) Từ $x$ có nước tới $\( 0;1 \)$ , không có nước tới $\( 1;0 \)$ $\rightarrow$ $x= \( 1;0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•3) Từ $x$ có nước tới $\( 1;0 \)$ , không có nước tới $\( 0;1 \)$ $\rightarrow$ $x= \( 0;1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•4) Từ $x$ không có nước tới cả $\( 1;0 \)$ và $\( 0;1 \)$ $\rightarrow$ $x= \( 0;0 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Rõ ràng •4) không thể xảy ra theo<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Theo quy nạp, ta có điều phải chứng minh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh (i) $\longleftarrow$ (iii): Tương tự, quy nạp rằng trong 1 game $A$ thỏa mãn (iii), nếu mọi $x$ với $d(x) \le D$ đều thỏa mãn (i) thì bất cứ $x$ nào có $d(x)=D+1$ cũng thỏa mãn (i). Xét $x$ có $d(x)=D+1$ , ta cũng có các trường hợp sau xảy ra: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) Nếu $x=\( 0;j \)$ , $x$ có thể đi tới $\( 1;0 \)$ và không thể đi tới $\( 0;1 \)$ $\rightarrow$ $j=\text{Mex} \\{ 0 \\} = 1$ (tương tự với $x=\( 1;0 \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) Nếu $x=\( i;j \)$ (với $i,j \ne 0$ ), $x$ có thể đi tới cả $\( 1;0 \)$ và $\( 0;1 \)$ , ngoài các hoán điểm, $x$ chỉ có thể tới $\( k;k \)$ với $k \ge 2$ $\rightarrow$ $j \ge 2$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Theo quy nạp, ta có điều phải chứng minh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh (i) $\longleftarrow$ (iv): theo các tương tự như chứng minh (i) $\longleftarrow$ (ii) và (i) $\longleftarrow$ (iii). <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Vậy bằng chứng cho ***định lí 2.3*** hoàn thành tức hoàn tất chứng minh ***định lí 2.3***. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Trò chơi gia giảm là tame game*
#### *<ins>Định lí 3.1</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi gia giảm gồm 1 đống là pet game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ chứng minh rằng mọi trò chơi gia giảm chỉ có 1 đống đều thỏa mãn ***mệnh đề (iii)*** của ***định lý 2.3*** và do đó chúng cũng thỏa mãn (i), tức chúng là pet game. <br>

#### *<ins>Bổ đề 3.2</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi gia giảm có tập giá trị gia giảm là $S$ và chỉ có 1 đống duy nhất. Đặt $k=\text{ min } \( S \)$ , $G^{+}$ là normal nimber của đống có kích thước $N$ , thì: $G^{+}(N)=0 \Leftrightarrow G^{+}\( N+k \) = 1$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 3.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều thuận)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại $n$ là số nhỏ nhất có $G^{+}(n)=0$ và $G^{+}\( n+k \) > 1$ . Bởi định nghĩa của $G^{+}$ nên $\exists s \in S:G^{+}\( n+k-s \) = 1$ , vì $k$ là giá trị nhỏ nhất trong tập $S$ nên $k-s \le 0$ . Hơn nữa do $G^{+}(N)=0$ $\forall N < k$ $\rightarrow$ $n+k-s \ge k$ nên điều này tương đương với $n-s \ge 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Lại có $G^{+}(n)=0$ $\rightarrow$ $G^{+}\( n-s \) \ne 0$ nên suy ra $\exists {s'} \in S:G^{+}\( n-s-s' \) = 0$ . Đặt $m=n-s-s'$ , vì $m < n$ và $G^{+}(m)=0$ nên $G^{+}\( m+k \)=1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giải thích thêm: do ta đã chọn $n$ là giá trị nhỏ nhất có $G^{+}(n)=0$ và $G^{+}\( n+k \) > 1$ nên lập luận trên là hợp lí. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ $G^{+}\( m+k+s' \) \ne 1$ $\rightarrow$ Mâu thuẫn với kết quả $G^{+}\( n+k-s \) = 1$ đã xác lập bên trên $\rightarrow$ $n$ không tồn tại $\rightarrow$ Mọi giá trị $N$ đều thỏa  $G^{+}(N)=0 \Rightarrow G^{+}\( N+k \) = 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *(Chiều nghịch)*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu tồn tại $n$ thỏa mãn $G^{+}\( n+k \) = 1$ nhưng $G^{+}(n) \ne 0$ thì $\exists s \in S:G^{+}\( n-s \) = 0$ . Theo *(chiều thuận)* đã chứng minh, $G^{+}\( n-s \) = 0 \rightarrow G^{+}\( n-s+k \) = 1$ , điều này mâu thuẫn với $G^{+}\( N+k \) = 1$ như giả định ban đầu $\rightarrow$ $n$ không tồn tại $\rightarrow$ Mọi giá trị $N$ đều thỏa  $G^{+}(N+k)=1 \Rightarrow G^{+}(N) = 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 3.2***. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định đề 3.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Xét một giá trị $n$ không phải là tận điểm của trò chơi tức $n \ge k | k = \text{   min   } (S)$ có $G^{+}(n)=0$ , theo định nghĩa $G^+$ , $G^{+}\( n-k \) \ne 0$ . Khi ấy ta suy ra $\exists s \in S:G^{+}\( n-k-s \) = 0$ , theo ***bổ đề 3.2*** thì $G^{+}\( n-s \) = 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Tồn tại nước đi (lấy bớt $s$ quân ra khỏi đống) để đưa từ trạng thái bất kỳ có $G^{+}=0$ (miễn là không phải tận điểm) tới trạng thái có  $G^{+}=1$ $\rightarrow$ Mọi trò chơi gia giảm gồm 1 đống duy nhất đều thỏa mãn ***mệnh đề (iii)*** của ***định lí 2.3***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định đề 3.1***. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Kết quả ấn tượng của ***định đề 3.1*** nói lên rằng 1 *trò chơi gia giảm* khi chỉ có 1 đống sẽ là *pet game* (và vì vậy cũng là tame game luôn) nên phiên bản gồm nhiều đống của chúng là tổng của nhiều trò chơi con (1 đống) mà mỗi trò chơi con đều là tame game <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Trò chơi gia giảm với số lượng đống bất kỳ là tame game bởi ***định lý 2.1*** và ***hệ quả 2.2***. <br>


















