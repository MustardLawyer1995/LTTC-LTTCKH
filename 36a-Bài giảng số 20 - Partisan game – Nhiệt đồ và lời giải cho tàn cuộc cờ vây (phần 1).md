# Partisan game – Nhiệt đồ và lời giải cho tàn cuộc cờ vây (phần 1)
Các partisan game gồm 2 loại là trò chơi lạnh và nóng, định nghĩa của chúng đã được nói đến ở loạt vấn đề trong
bài giảng số 17. Người chơi sẽ thích chơi trò chơi nóng hơn lạnh. Một vài trò chơi nóng lại được ưa thích hơn (nóng
hơn/tối ưu hơn về mặt chiến thuật) những trò chơi nóng khác. Đây là động cơ ban đầu để xây dựng thang đo nhiệt độ
cho các trò chơi, nhưng nó còn dẫn ta đến điều gì nữa...
### 0. Trò chơi tổng của các $\\{ a|b \\}$ với $a,b$ là số <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi cấu thành từ các trò chơi con dạng $\\{ a|b \\}$ với $a,b$ là số chỉ chứa 2 loại giá trị ứng với 2 trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $a<b$ , $\\{ a|b \\}$ là số <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $a≥b$ , $\\{ a|b \\} = \frac{a+b}{2} ± \frac{a-b}{2}$ (với số $n≥0$ , ký hiệu: $\\{ n|-n \\} = ±n$ , không mất tính tổng quát, $*=±0$ , do định nghĩa này nên $- \( ±n \) = ±n$ hay $±n±n=0$ ), kết quả này đến từ nguyên lý chuyển dịch số (xem lại ***<ins>Số siêu thực - phần 5, VII/, Định lí 4.4a</ins>***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi tồn tại một chiến lược thắng đơn giản mà không cần qua thao tác cộng các giá trị: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tránh chơi các giá trị số nếu có thể, theo Định lý tránh số (xem lại ***<ins>Số siêu thực - phần 5, VII/, hệ quả 4.4b </ins>***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Chơi ở phi số $\\{ a|b \\}$ $\( a≥b \)$ nào có $a-b$ lớn nhất. Thật vậy: Khi viết tất cả các $\\{ a|b \\}$ 
 $\( a≥b \)$ về dạng $\frac{a+b}{2} ± \frac{ab}{2}$, chỉ cần quan tâm đến phần $±\frac{a-b}{2}$ vì $\frac{a+b}{2}$ là số. Cho $m>n$ , có: $m-n±m±n>0$ (chứng minh bằng cách chỉ ra Trái luôn thắng) $\Leftrightarrow$ $m±n>±m+n$ $\rightarrow$ Cho $a_{1}>a_{2}>a_{3}>...>0$ , có: $a_{1}±a_{2}±a_{3}±...> ±a_{1}+a_{2}±a_{3}±...> ±a_{1}±a_{2}+a_{3}±...>...$ , chứng minh tương tự cho nước đi ở bên Phải. $\Rightarrow$ Nếu phải thực hiện 1 nước đi trong $±a_{1}±a_{2}±a_{3}±...$ , chơi ở $±a_{1}$ là tốt nhất. (điều phải chứng minh) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả 0.0:</ins>***  
&nbsp;&nbsp;&nbsp;&nbsp;Cho dãy số $a_{1}>a_{2}>a_{3}>...>0$ , ta có dạng hợp quy sau: <br>
```math
±a_{1}±a_{2}±a_{3}±...= \\{ a_{1}±a_{2}±a_{3}±...|-a_{1}±a_{2}±a_{3}±... \\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Chiến lược này còn có thể hiểu theo một cách trực quan hơn như sau: Trò chơi trở thành cuộc đua giữa 2 người chơi để "cướp" lấy những giá trị $±\frac{a-b}{2}$ lớn nhất (Trái chơi $±n$ sẽ biến nó thành $n$ và Phải chơi $±n$ sẽ biến nó thành $-n$ ), bởi vì Trái mong muốn tổng giá trị cuối cùng là dương nhất có thể và Phải muốn nó là âm nhất có thể $\Rightarrow$ Một cách tự nhiên, họ sẽ chọn chơi ở giá trị có $a-b$ lớn nhất khi đến lượt mình, và đây là chiến lược tối ưu. <br>
### 1. Toán tử làm lạnh và nhiệt độ trò chơi <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Cho trò chơi $G$ và số $t≥0$ , $G\( t \)$ được định nghĩa đệ quy như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp; $G \( t \) = \\{ GL \( t \) -t|GR \( t \)+t \\}$ khi $t≤r$ với $r$ là giá trị nhỏ nhất để $G(r)$ là số; $G(t)=G(r)$ khi $t>r$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta nói $G(t)$ là trò chơi $G$ bị "làm lạnh" bởi $t$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;***Ví dụ:*** Nếu $G$ là số thì $G(t)=G \forall t≥0$; nếu $G$ là phi số vô cùng bé $\( *,↑,↓,... \)$ thì $G(t)=0 \forall t>0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;Với $G=±1, G\( 0 \)=±1, G\( \frac{1}{2} \) = \\{ 1-\frac{1}{2}|-1+\frac{1}{2} \\} = \frac{1}{2} , G(1)= \\{ 1-1|-1+1 \\} =\\{ 0|0 \\} =*, G(t)=0 \text{   } \forall t>1$ <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Luôn tồn tại $t$ để $G(t)$ là số <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Quy nạp với giả thiết rằng các tùy chọn của $G$ đều có thể được làm lạnh thành số, chọn $t$ đủ lớn để $GL(t)$ và $GR(t)$ là số $\Rightarrow$ $G(t)= \\{ a|b \\}$ với $a,b$ là số. Nếu $a<b$ thì $G(t)$ cũng là số; nếu $a≥b$ , đặt $k=\frac{a-b}{2}+1$ $\rightarrow$ $G(t+k)= \\{ \frac{a+b}{2}-1|\frac{a+b}{2}+1 \\}$ là số. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 1.2*** <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 1.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nhiệt độ của trò chơi $G$ là số không âm $t(G)$ nhỏ nhất để $G(r)$ là số $\forall r>t(G)$. <br>
&nbsp;&nbsp;&nbsp;&nbsp;***Ví dụ:*** Nếu $G$ là số hay phi số vô cùng bé thì $t(G)=0$ . Vì vậy các số được coi là "lạnh" và các phi số vô cùng bé là "âm ấm". <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G= \\{ p|q \\}$ với $p,q$ là số, $p>q$ thì $t(G)=\frac{p-q}{2}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Định nghĩa này phù hợp một cách hoàn hảo với kết quả ở ***mục O/***, khi người chơi luôn chơi ở trò chơi con có nhiệt độ cao nhất, ta nói anh ta sử dụng "chiến lược nóng". Đáng tiếc, chiến lược nóng không phải luôn là chiến lược tối ưu, ta chỉ nên áp dụng nó cho dạng trò chơi ở ***mục O/***. Tuy nhiên khái niệm nhiệt độ lại mở ra lý thuyết mới giải quyết được nhiều dạng trò chơi khó, một trong số đó là tàn cục cờ vây. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4: Các tính chất của toán tử làm lạnh (quy nạp cho 1.4a,b,c):</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4a:</ins>*** $(-G)(t)= -G(t)$ (theo ***Định nghĩa 1.1***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4b:</ins>*** $(G+x)(t)=G(t)+x$ ( $x$ là số) (theo ***Định nghĩa 1.1*** và nguyên lý chuyển dịch số) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4c:</ins>*** $G(t_{1})(t_{1})=G(t_{1}+t_{2})$ (theo ***Định nghĩa 1.1*** và ***tính chất 1.4b***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4d:</ins>*** $(G+H)(t)=G(t)+H(t)$ <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 1.4d:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gọi $u$ là số nhỏ nhất để ít nhất 1 trong 3 giá trị $G(u), H(u), (G+H)(u)$ là số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $t≤u$ ta có: $(G+H)(t)= \\{ (GL+H)(t)-t, (G+HL)(t)-t | (GR+H)(t)+t, (G+HR)(t)+t \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $= \\{ GL(t)+H(t)-t, G(t)+HL(t)-t | GR(t)+H(t)+t, G(t)+HR(t)+t \\} =G(t)+H(t)$ *(quy nạp)* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $t>u$ , bởi định nghĩa của $u$ nên: $(G(u)+H(u))(t-u)=G(u)(t-u)+H(u)(t-u)$ theo ***Tính chất 1.4a,b,c***, rồi từ đó dẫn đến kết luận của ***1.4d*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 1.4d*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4e:</ins>*** $G≥H \Rightarrow G(t)≥H(t)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 1.4e:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Đặt $G-H=M$ $\rightarrow$ $G(t)-H(t)=M(t)$ (theo ***1.4d***), ta cần chứng tỏ: $M≥0 \rightarrow M(t)≥0$ (gọi là mệnh đề ***e'***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Với $M$ là số, ***(e')*** hiển nhiên đúng; với $M$ là phi số: $M≥0$ $\Leftrightarrow$ Phải đi trước luôn thua trong trò chơi M $\Leftrightarrow$ $\forall MR$ , $\exists MRL ≥ 0$ . Theo ***Định nghĩa 1.1***: $M(t)R = MR(t_{1})+t_{1}, M(t)RL=MRL(t_{2})+t_{1}-t_{2} \( t_{2}≤t_{1}≤t \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu ***(e')*** đúng $\forall MRL$ , có $MRL≥0$ $\Rightarrow MRL(t_{2}) ≥ 0$ $\Rightarrow \forall (t)R$ , $\exists M(t)RL = MRL(t_{2})+t_{1}-t_{2} ≥ 0 \Leftrightarrow M(t)≥0$ $\Rightarrow$ ***(e')*** cũng đúng với $M$ (quy nạp). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 1.4e*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.4f:</ins>*** $t(G+H)≤max \\{ t(G),t(H) \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 1.4f:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $t(G+H)>max \\{ t(G),t(H) \\} =T$ thì $(G+H)(T)$ là phi số, mặt khác, bởi $G(T)$ , $H(T)$ là số nên $(G+H)(T)=G(T)+H(T)$ là số, điều này là mâu thuẫn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 1.4f*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5: Cần nhớ lại khái niệm về các hàm r(G), l(G) đã đề cập ở bài Số siêu thực phần 5, do dung lượng bài viết nên ta sẽ không nhắc lại, chỉ bổ sung một số kết quả quan trọng như :</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5a:</ins>*** Hệ quả của ***Định lý 4.2 (Số siêu thực phần 5- bài giảng số 17e, mục 7/)***: Cho trò chơi $G$ và số $x$ bất kỳ, có: $x≥G \Leftrightarrow x>l(G), x≤G \Leftrightarrow x<r(G), x \parallel G \Leftrightarrow r(G)<x<l(G)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 1.5a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Theo định nghĩa, giá trị $r,l$ luôn có dạng $n±δ$ với $n$ là số, $δ→0^{+}$ (với $r,l$ là tiệm cận của các số), nên giữa $x$ với $r$ hoặc $l$ không thể có quan hệ $=$ hay $\parallel$ . Từ ***định lý 4.2***: $x< \parallel G$ $\Leftrightarrow$ $x<l(G)$ và $x \parallel >G \Leftrightarrow x>r(G)$ , ta thấy ***1.5a*** chỉ đơn giản là trường hợp các dấu so sánh đảo ngược lại. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 1.5a*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5b:</ins>*** $G$ là số $\Leftrightarrow$ $l(G)<r(G)$ (rút ra từ ***1.5a***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5c:</ins>*** $r(G+x)=r(G)+x, l(G+x)=l(G)+x$ (với $x$ là số) (nếu $G$ là số, ***1.5c*** là hiển nhiên; nếu $G$ là phi số, hãy quy nạp từ ***<ins>nguyên lý chuyển dịch số</ins>***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5d:</ins>*** Nếu $G(u)$ là phi số thì: $r(G(u))= min l(GR(u))+u$ và  $l(G(u))= max r(GL(u))-u$ (suy ra trực tiếp từ ***1.1*** và ***1.5c***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 1.5e:</ins>*** Cho trò chơi $G$ và số $u>0$ , luôn có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $r(G)≤r(G(u))$ , nếu dấu = xảy ra thì $r(G)=n+δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $l(G)≥l(G(u))$ , nếu dấu = xảy ra thì $l(G)=n-δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 1.5e:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Quy nạp theo giả thiết ***1.5e*** đúng với mọi tùy chọn phát sinh từ $G$ , và chỉ ra là nó cũng đúng với $G$ . Thật vậy, $r(GRL)≤r(GRL(u))$ $\rightarrow$ $l(GR)≤l(GR(u))+u$ (theo ***1.5d***; với $GR(u)$ là số, thay $u$ bằng $t$ nhỏ nhất để $GR(t)$ là số) $\rightarrow r(G)≤r(G(u)$ ) (theo ***1.5d***; với $G(u)$ là số, thay $u$ bằng $t$ nhỏ nhất để $G(t)$ là số) (đpcm). Chứng minh $l(G)≥l(G(u))$ theo cách tương tự. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 1.5e*** <br>

### 2. Áp dụng lý thuyết trò chơi kết hợp vào cờ vây <br>
#### 1. Cờ vây và cờ vây toán học 
&nbsp;&nbsp;&nbsp;&nbsp;Luật chơi cơ bản của cờ vây đã được nói đến trong ***<ins>bài giảng số 35 Phụ lục: Tản mạn về cờ vây</ins>*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta sẽ thay đổi/bổ sung một số luật để cờ vây trở thành ***"cờ vây toán học"***: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) Gửi trả lại 1 tù binh bị bắt cho bên đối thủ cũng được coi là 1 nước đi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) Không được phép bỏ lượt. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•3) Người chơi nào không thể thực hiện 1 nước đi hợp lệ khi đến lượt của mình bị coi là thua. Luật mới này làm kết quả trận đấu giống như khi chơi theo luật thông thường trừ trường hợp số điểm 2 bên bằng nhau: luật thông thường cho ta 1 trận hòa, còn luật mới cho biết người đi sau sẽ thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•4) Không có các trạng thái dẫn đến vòng lặp. Về cơ bản điều này nghĩa là không có "Ko" trong cờ vây toán học. Ta cũng giả định rằng không có "Seki", tình trạng 2 nhóm quân trái màu cùng sống sót. "Ko" và "Seki" rất quan trọng trong cờ vây thường nhưng lý thuyết trò chơi kết hợp (LTTCKH) chỉ xét những game kết thúc sau hữu hạn lượt đi, nên yêu cầu này là bắt buộc. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•5) Một quân trên bàn cờ được coi là sống sót cho đến khi bị bắt. Không cần bận tâm về tình trạng sống/chết. Trong cờ vây thường, điều này cũng luôn xảy ra khi có đủ số nước đi. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Vậy là ta đã tìm ra cách chuyển đổi hệ thống tính điểm của cờ vây về luật "đi nước cuối" của LTTCKH. Bằng cách coi hành động trả lại 1 tù binh là 1 nước đi, cờ vây trở thành một game mà ai hết nước đi trước là người thua, và vì vậy, có cấu trúc tương tự một trò chơi kết hợp. Từ đoạn này về sau, cụm từ "cờ vây" sẽ được ngầm hiểu là ***<ins>cờ vây toán học</ins>*** <br>
#### 2. Công thức hóa các thế cờ cơ bản
&nbsp;&nbsp;&nbsp;&nbsp;Độ phức tạp tính toán của cờ vây là rất lớn, nên LTTCKH chỉ phô diễn được tối đa sức mạnh ở tàn cục, khi bàn cờ đã phân chia ra các vùng không liên quan đến nhau. Mỗi vùng này là một chiến trường riêng biệt-một trò chơi con, và cờ vây tàn cục chính là tổng của các trò chơi con này (xem ví dụ tương tự, cờ vua bị phân rã thành nhiều trò chơi con ở tàn cục (xem lại ***<ins>bài giảng số 18</ins>***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta thống nhất quy ước phe Đen là người chơi Trái và phe Trắng là người chơi Phải. Theo định nghĩa, những trạng thái mà 2 người chơi đều không còn nước đi hợp lệ ứng với giá trị 0. Đó là khi không còn ô trống trên bàn cờ, và không còn tù binh ở cả 2 bên. Giá trị của các thế cờ (trò chơi) con quan trọng khác được trình bày ở các hình sau: <br>
<div align="center">

 Hình 1            | Hình 2            | Hình 3            |
:-------------------------:|:-------------------------:|:-------------------------:|
![image](https://github.com/user-attachments/assets/ef5c97a8-5226-44e4-9e4d-4125f23f815d)|![image](https://github.com/user-attachments/assets/baf5f471-04ca-42c2-9a02-5827b0930947)|![image](https://github.com/user-attachments/assets/2e898d23-4d84-4b1c-a305-c19f8fefb050)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu Đen (Trái) có 1 tù binh trắng, nước đi duy nhất của anh ta là trả lại tù binh đó cho Trắng (Phải), đưa giá trị trò chơi về 0, còn Trắng không có nước đi hợp lệ nào. Bởi vậy giá trị của thế này là $\\{ 0| \\} = 1$ . Tương tự nếu Trắng có 1 tù binh đen thì giá trị là $-1$ . Theo cách này, Đen (Trắng) có $n$ tù binh thì giá trị trò chơi là $n +(-n)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trên bàn cờ, thế cờ mà Đen có 1 nước đi còn Trắng không có chính là mắt đơn Đen. Có lẽ bạn đã biết định nghĩa của "mắt" qua bài về luật cờ vây cơ bản, nếu không, hãy coi bức hình trên như định nghĩa. "Mắt" hiểu đơn giản là vùng lãnh thổ mà người chơi tạo ra bằng cách dùng các quân cờ của mình vây bọc xung quanh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Để thuận tiện trong phạm vi bài viết, ta sẽ xác định các ô bằng tọa độ $(x;y)$ với $x$ là số thứ tự của cột (từ trái qua) và $y$ là số thứ tự của hàng (từ dưới lên). Ở thế cờ trong hình bên trái, Đen có 1 nước đi là điền vào ô $(3,3)$ , đưa trò chơi về giá trị $0$ , trong khi Trắng không có nước đi nào vì đi vào ô $(3,3)$ là nước cờ "tự tử" với anh ta. Bởi vậy thế cờ này cũng có giá trị là $1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến tại hình giữa, theo cách tương tự, cả 2 thế cờ con trong hình (thế có 2 mắt đơn Đen bên trái và thế có mắt kép Đen phải), đều nhận giá trị là 2. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ đây ta biết rằng việc người chơi sở hữu $n$ tù binh hoàn toàn tương đương với việc anh ta có một vùng lãnh thổ diện tích $n$ ô trên bàn cờ, trong đó thao tác trả lại 1 tù binh tương tự như thao tác điền vào 1 ô trên chính vùng lãnh thổ của mình. Ta cũng hiểu ngay lý do tại sao các quân cờ nằm trong lãnh thổ của địch cho đến cuối trận bị xem như tù binh và được nhấc ra khỏi bàn cờ. Về khía cạnh này, LTTCKH lại rất tương thích với cờ vây. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thế cờ con trong hình bên phải (trong thuật ngữ cờ vây gọi là "dame") có giá trị là $\\{ 0|0 \\} = \ast$ , bởi vì nước đi duy nhất của cả 2 người chơi là đi vào ô $(3,3)$ , đưa trò chơi về giá trị $0$ . <br>

------------------------------------------------------------------------------------------------------------------------------------------------------------
<div align="center">

![image](https://github.com/user-attachments/assets/080a591f-1a21-4652-9187-d0eaefd8b82a)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Một thế khác cũng rất phổ biến trong cờ vây là "hành lang" (hình trên). Cả Đen và Trắng đều có rất nhiều nước đi khả thi, tuy nhiên ta chỉ cần quan tâm đến những nước đi tối ưu. Có thể thấy rằng Đen đi ô $(7,3)$ là nước đi tối ưu, vì nó đưa thế cờ về giá trị $3$ , lớn hơn tất cả các giá trị được tạo ra khi Đen đi vào ô khác (có một mẹo để kiểm tra nhanh điều này, sẽ nói tiếp ở (\*)). Nước đi tối ưu của Trắng cũng là $(7,3)$ vì các nước đi khác đều tạo cho Đen cơ hội đi $(7,3)$ ở lượt tiếp theo, bắt luôn quân cờ mà Trắng vừa đi. Khi đi vào ô $(7,3)$ , Trắng tạo ra một hành lang nhỏ hơn, ta có thể tiếp tục tính toán giá trị của nó theo cách này, và tìm được giá trị của thế cờ trong hình là $\\{ 3| \\{  2| \\{ 1| \ast \\} \\} \\}$ . Dù nhìn có vẻ cồng kềnh nhưng giá trị này đã ở dạng hợp quy, có nghĩa là ta không thể làm nó đơn giản hơn được nữa. Thật không may, phần lớn các thế cờ trong tàn cục cờ vây đều trông gần giống như thế. Tính toán tổng của các giá trị đó là một công việc tẻ nhạt và nặng nề. Dường như hệ thống phân tích mới mà ta tạo ra cho cờ vây chỉ làm mọi chuyện phức tạp hơn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ở mục (\*), để chứng minh điều đó, cần chỉ ra $G>H$ (với $G$ là hành lang hình trên có thêm quân đen ở $(7,3)$ , $H$ là hành lang hình trên có thêm quân đen ở ô khác với $(7,3)$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bạn chỉ cần tạo ra thế cờ đối của $H$ (1 hành lang tương tự nhưng đảo ngược lại màu sắc của 2 bên, giá trị của nó sẽ là $-H$ ), đặt $G$ và $-H$ song song cạnh nhau, tạo thành trò chơi $G-H$ . Dễ thấy rằng trong trò chơi $G-H$ này, Đen luôn thắng (dù ai đi trước) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow G-H>0 \Rightarrow G>H$ $\Rightarrow$ đi vào ô $(7,3)$ là tối ưu hơn mọi nước đi khác. <br>
&nbsp;&nbsp;&nbsp;&nbsp;  Với khó khăn vừa nêu trên, đừng lo, giải pháp sẽ có trong phần tiếp theo ***<ins>(mời quay trở lại mạch chính của bài viết)</ins>***. <br>

------------------------------------------------------------------------------------------------------------------------------------------------------------












