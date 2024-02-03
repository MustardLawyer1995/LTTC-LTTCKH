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

### 4. Trò chơi trừ bình phương <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo định nghĩa, trò chơi ***<ins>Trừ bình phương</ins>*** chính là 1 trò chơi gia giảm với tập $S = \\{ 1,4,9,16,...,k^{2},...\\} \text{ } , \text{ } k \in \mathbb{Z}^+$ , khi đó nó là tame game. Muốn tính dãy $G^{-}(N)$ của nó thì ta phải làm sao ? Viết dãy $G^{+}(N)$ ra, tráo đổi vị trí các số 1 và 0 cho nhau, ta đã có dãy $G^{-}(N)$ (nhớ rằng 1 đống của trò chơi Trừ bình phương là pet game).  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Qua cuộc phiêu lưu này, ta không chỉ chứng minh được Trừ bình phương là tame game, ta còn thu được 1 kết quả rộng lớn hơn rất nhiều, làm nhẹ gánh cho hành trình khám phá các impartial games về sau... <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ngoài Trừ bình phương, bạn có thể tự chế ra 1 trò chơi gia giảm nào đó và tha hồ yên tâm rằng chúng vẫn là tame game. Sau đây là trò chơi Trừ nguyên tố do tôi nghĩ ra, người chơi lấy đi lượng quân là số nguyên tố từ 1 đống ở mỗi lượt. Đây là giá trị nimber cho 1 đống có $N$ quân: <br>

```math
\left\{ {\begin{array}{*{20}{c}}
{N = \;0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,...}\
{{G^ + } = 0,0,1,1,2,2,3,3,4,0,0,1,1,2,2,...}\
{{G^ - } = 1,1,0,0,2,2,3,3,4,1,1,0,0,2,2,...}
\end{array}} \right.
```
<div align="center">

<Đến đây các bạn đọc tự làm.............> <br>
</div>

### 5. Chiến lược đối xứng <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong thực tế có nhiều impartial game mà việc khám phá ra quy luật giá trị nimber của chúng rất khó. Nhưng nếu mục đích chỉ là tìm chiến lược tất thắng cho những game này thì không cần phức tạp đến vậy, chúng có chiến lược đối xứng. <br>
<div align="center">

Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/cb22d9e1-c973-45db-a05c-3440a96a7805) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/c859ce4e-6753-4090-b06e-ffabd961dc03)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;-	***<ins>Kayles:</ins>*** Là một impartial game đơn giản, được phát minh bởi Henry Dudeney vào năm 1908. Gồm một hàng
các chốt bowling tưởng tượng, người chơi thay phiên nhau để hạ 1 hoặc 2 chốt liền kề, cho đến khi hết các chốt. Ai không còn nước đi khi đến lượt sẽ thua (quy ước normal) ***(hình 1)***. Không khó để nhận ra rằng người chơi đầu tiên có một chiến thắng đảm bảo bất cứ khi nào độ dài hàng $> 0$ . Chiến thắng này có thể đạt được bằng cách sử dụng chiến lược đối xứng. Trong lần di chuyển đầu tiên của mình, người chơi đầu tiên đi 1 nước sao cho hàng được chia thành 2 phần có độ dài bằng nhau. Điều này hạn chế tất cả các nước đi trong tương lai có thể tác động tới cả 2 phần. Bây giờ, người chơi thứ nhất chỉ cần bắt chước các động thái của người chơi thứ 2 ở hàng đối diện. Điều này đảm bảo rằng người chơi thứ nhất sẽ luôn là người đi nước cuối cùng và giành chiến thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;-	***<ins>Cram:</ins>*** Trò chơi được chơi trên một bảng hình chữ nhật/hình vuông. Hai người chơi lần lượt đặt các quân domino (miếng gỗ $1 \times 2$ ) lên bảng, theo chiều ngang hoặc dọc. Người chơi đầu tiên không còn nước đi sẽ thua ***(hình 2)***. Chiến lược thắng cho Cram rất đơn giản đối với các bảng $n \times m$ , $n$ chẵn và $m$ chẵn. Trong trường hợp này, người chơi thứ 2 thắng bằng cách chơi đối xứng. Điều này có nghĩa là với bất kỳ động tác nào mà người chơi 1 thực hiện, người chơi 2 có 1 động tác đối xứng tương ứng (đối xứng tâm). Theo một nghĩa nào đó, người chơi 2 "bắt chước" các động tác được thực hiện bởi Người chơi 1. Nếu người chơi 2 tuân theo chiến lược này, anh ta sẽ luôn thực hiện nước đi cuối cùng, và do đó giành chiến thắng trong trò chơi. Trường hợp $n$ chẵn, $m$ lẻ, người chơi đầu tiên thắng bằng cách chơi đối xứng tương tự. Người chơi 1 đặt domino đầu tiên của mình vào chính giữa bảng. Người chơi 2 sau đó thực hiện nước đi của mình, nhưng người chơi 1 có thể chơi đối xứng để bắt chước người chơi 2, do đó đảm bảo chiến thắng cho người chơi 1. Chơi đối xứng là một chiến lược vô dụng trong phiên bản misère, bởi vì trong trường hợp đó, nó chỉ đảm bảo cho người chơi rằng anh ta sẽ thua. <br>












