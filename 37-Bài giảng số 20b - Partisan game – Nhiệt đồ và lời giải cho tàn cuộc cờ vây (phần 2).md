# Partisan game – Nhiệt đồ và lời giải cho tàn cuộc cờ vây (phần 2) (fixed)
### 3. Lời giải trọn vẹn cho tàn cuộc cờ vây. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 3.1:</ins>***  
&nbsp;&nbsp;&nbsp;&nbsp;Một thế cờ có giá trị là phi số vô cùng bé luôn là thế cờ lẻ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 3.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $G$ là phi số vô cùng bé $\Leftrightarrow$ $r(G),l(G)$ là các tiệm cận của 0 (theo ***1.5a***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo định nghĩa của các hàm $r, l$ thì ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $GLRLR...LR=0$ thì $l(G)=r(GL)=l(GLR)=r(GLRL)=...=l(GLRLR...LR)=-δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $GLRLR...L=0$ thì $l(G)=r(GLRLR...L)=+δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tương tự, $GRLRL...RL=0$ thì $r(G)=r(GRLRL...RL)=+δ$ và $GRLRL...R=0$ thì $r(G)=l(GRLRL...R)=-δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tuy nhiên theo ***(2.3a)***, vì $0$ là thế chẵn nên: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $GLRLR...LR=0$ $\Leftrightarrow$ $G$ là thế chẵn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $GLRLR...L=0$ $\Leftrightarrow$ $G$ là thế lẻ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $GRLRL...RL=0$ $\Leftrightarrow$ $G$ là thế chẵn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $GRLRL...R=0$ $\Leftrightarrow$ $G$ là thế lẻ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Điều này dẫn đến việc chỉ có 2 trường hợp sau xảy ra: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 1:</ins>* $G$ là thế chẵn, $GLRLR...LR=GRLRL...RL=0$ , $l(G)=-δ$ , $r(G)=+δ$ $\Leftrightarrow$ $G=0$ (theo ***1.5a*** và ***1.5b***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 2:</ins>* $G$ là thế lẻ, $GLRLR...L=GRLRL...R=0$ , $l(G)=+δ$ , $r(G)=-δ$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Do $G$ là phi số nên trường hợp 1 bị loại bỏ, ta có đpcm. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 3.1*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 3.2:</ins>***  
&nbsp;&nbsp;&nbsp;&nbsp;Phép làm lạnh một thế cờ chẵn bởi 1 là có thể đảo ngược. Nói cách khác, với $G$ và $H$ là thế chẵn, $G(1)=H(1)$ $\Leftrightarrow$ $G=H$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 3.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ chỉ ra: $G(1)=H(1)$ $\Rightarrow$ $G=H$ (vì chiều ngược lại là hiển nhiên theo ***1.4e***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại 2 thế cờ chẵn $G≠H$ , $G(1)=H(1)$ $\Rightarrow$ tồn tại thế cờ chẵn $M=G-H≠0$ , $M(1)=G(1)-H(1)=0$ $\Rightarrow$ $M$ là phi số (với $M$ là số thì $M=M(1)=0$ ). $M(1)= \\{ ML(t)-t |MR(t)+t \\} =0 (t≤1)$ $\Rightarrow$ $ML(t)-1< \parallel 0< \parallel MR(t)+1$ $\Rightarrow$ $r(ML(t))<1$ và $l(MR(t))>-1$ (theo ***1.5a***) $\Rightarrow$ $-1<l(MR(t))≤l(MR)=r(M)≤l(M)=r(ML)≤r(ML(t))<1$ (theo ***1.5b*** và ***1.5e***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các giá trị $r,l$ luôn ở dạng $n±δ$ $\forall n \in \mathbb{Z}$ do hệ quả của ***(2.4)***, nếu $r(ML)=1-δ$ hay $l(MR)=-1+δ$ thì sẽ làm $r(ML(t))≥1+δ>1$ hay $l(MR(t))≤-1-δ<1$ (theo ***1.5e***) $\Rightarrow$ $l(M)=r(ML)=±δ$ và $r(M)=l(MR)=±δ$ $\Rightarrow$ $M$ là phi số vô cùng bé $\Rightarrow$ $M$ là thế lẻ theo ***(3.1)***, mâu thuẫn với việc $M$ là thế chẵn $\Rightarrow$ $M$ không tồn tại (đpcm). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 3.2*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả:</ins>*** 
&nbsp;&nbsp;&nbsp;&nbsp;Cho 2 thế cờ $G$ và $H$ , $G(1)=H(1)$ $\Leftrightarrow$ $G=H$ hoặc $G=H+ \ast$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $(G-H)(1)=G(1)-H(1)=0=0$ (1) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Nếu $G-H$ là thế chẵn thì $G-H=0$ (theo ***3.2***) $\Leftrightarrow$ $G=H$ . Nếu $G-H$ là thế lẻ thì $G-H + \ast$ là thế chẵn (theo ***2.3b***), và $(G-H+ \ast )(1)=G(1)-H(1)+ \ast (1)=0=0 (1)$ $\Rightarrow$ $G-H+ \ast =0$ (theo ***3.2***) $\Leftrightarrow$ $G=H+ \ast$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***hệ quả*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định nghĩa 3.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Định nghĩa hồi quy dãy $\\{ w_{n} \\} : w_{1} = \\{ 1|\ast \\} , w_{k+1} = \\{ 2|w_{k} \\}-1$ . Dễ thấy tất cả các thế $w_{n}$ đều chẵn (theo ***2.3a*** và ***2.3b***). Chúng có các tính chất sau (quy nạp cho ***3.3a*** và ***3.3b***): <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 3.3a:</ins>*** $w_{n}(1)=\frac{1}{2^n}, t(w_{n})=\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+...+\frac{1}{2^n}$ (theo ***1.1, 1.3, 1.4d***) $\Rightarrow$ $w_{n}$ là phi số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 3.3b:</ins>*** $fw_{n}=\frac{1}{2^n}, f(w_{n}+x)=fw_{n}+x$ với $x \in \mathbb{Z}$ (do ***2.2*** và hệ quả của ***<ins>định lý tránh số nguyên</ins>***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 3.3c:</ins>***  Cho tập hợp các giá trị có dạng $W=x+wk_{1}+wk_{2}+wk_{3}+... (x \in \mathbb{Z})$ , có: $fW=x+ƒwk_{1}+ƒwk_{2}+ƒwk_{3}+...$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 3.3c:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Quy nạp rằng nếu ***3.3c*** đúng với: $W∈ \\{ W_{1},W_{2},W_{1}L,W_{1}R,W_{2}L,W_{2}R,W_{1}L+W_{2},W_{1}R+W_{2},W_{1}+W_{2}L,W_{1}+W_{2}R \\}$ thì nó cũng đúng với $W=W_{1}+W_{2}$ . Ta sẽ chỉ ra rằng: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(c1) Nếu ***3.3c*** đúng với $W = W' = x' + w{k_1}^\prime  + w{k_2}^\prime  + w{k_3}^\prime  + ...$ thì: $fW^{'}=n \in \mathbb{Z}$ $\Leftrightarrow$ $W^{'}=n$ hoặc $n+ \ast$ . Thật vậy, do ***(3.3a,b),(1.4d)*** nên ta có:  $fW' = x' + w{k_1}^\prime  + w{k_2}^\prime  + w{k_3}^\prime  + ... = x'\left( 1 \right) + w{k_1}^\prime \left( 1 \right) + w{k_2}^\prime \left( 1 \right) + w{k_3}^\prime \left( 1 \right) + ... = W'\left( 1 \right)$ , nếu $ƒW'=n \in \mathbb{Z}$ thì $n(1)=W'(1)$ $\Rightarrow$ $W'=n$ hoặc $n+ \ast$ (do ***hệ quả*** của ***3.2***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(c2) $ƒ(W_{1}+W_{2})=ƒW_{1}+ƒW_{2}$ . Với $W_{1},W_{2} \in \mathbb{Z}$ thì (c2) là hiển nhiên; với $W_{1},W_{2} \notin \mathbb{Z}$ thì (c2) được thỏa mãn bởi ***(2.2a)*** và giả thiết quy nạp. Với $W_{1} \notin \mathbb{Z}, W_{2} \in \mathbb{Z}$ , nếu $ƒW_{1} \notin \mathbb{Z}$ thì (c2) được suy ra từ ***hệ quả*** của ***<ins>định lý tránh số nguyên</ins>*** và giả thiết quy nạp; nếu $ƒW_{1}=n \in \mathbb{Z}$ thì $W_{1}=n+ \ast$ theo (c1) $\Rightarrow$ (c2) trở thành hiển nhiên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Từ (c2) và giả thiết quy nạp suy ra ***3.3c*** cũng đúng với $W=W_{1}+W_{2}$ , quy nạp hoàn tất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 3.3c*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 3.3d:</ins>*** Với các giá trị $W$ được định nghĩa ở ***3.3c***, ta luôn có: $ƒ(W+ \ast)=ƒW$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 3.3d:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $(w_{1}+w_{1}-1)(1)=0=0(1)$ (do ***1.4d, 3.3a***) $\Rightarrow$ $w_{1}+w_{1}-1=0$ hoặc $\ast$ (do hệ quả của ***3.2***), mà $w_{1}+w_{1}-1$ là thế lẻ (do $w_{1}$ là thế chẵn và ***2.3b***) $\Rightarrow$ $w_{1}+w_{1}-1= \ast$ . Bởi ***3.3c***, nên ta có: $ƒ(W+ \ast)=ƒ(W+w_{1}+w_{1}-1)=ƒW+ƒ(w_{1}+w_{1}-1)=ƒW+ƒ( \ast )=ƒW$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 3.3d*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 3.4:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Trong tàn cục cờ vây, làm mát tương đương với làm lạnh bởi 1: $G(1)=ƒG$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 3.4:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G(1)=a$ là số (với $t(G)<1$ ), $a$ có thể viết thành dạng: $a=x+\frac{1}{2^{k_{1}}}+\frac{1}{2^{k_{2}}}+\frac{1}{2^{k_{3}}}+...$ (với $x \in \mathbb{Z}$ và $k_{1},k_{2},k_{3}, ... \in \mathbb{Z^+}$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $W=x+wk_{1}+wk_{2}+wk_{2}+...$ , khi đó ta có: $G(1)=a=x(1)+wk_{1}(1)+wk_{2}(1)+wk_{3}(1)+...=x+ƒwk_{1}+ƒwk_{2}+ƒwk_{3}+...$ (theo ***3.3a*** và ***3.3b***) $\Leftrightarrow$ $G(1)=W(1)=fW$ (theo ***1.4d*** và ***3.3c***) $\Rightarrow$ $G=W$ hoặc $W+ \ast$ (hệ quả của ***3.2***) $\Rightarrow$ $G(1)=fW=f(W+ \ast)=fG$ (theo ***3.3d***) (đpcm) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G(1)$ không phải là số (với $t(G)≥1$ ) thì $G(1)=\\{ GL(1)-1|GR(1)+1 \\} = \\{ f(GL)-1|f(GR)+1 \\}=fG$ (theo ***1.1*** và ***2.2a***) (quy nạp) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 3.4*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 3.5:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Với $G$ là thế cờ chẵn, ta luôn có: $\int (fG) = G$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 3.5:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $G=n$ hoặc $G=n+ \ast$ (với $n∈ \mathbb{Z}$ ) thì ***(3.5)*** là hiển nhiên theo ***2.1, 2.2***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $G≠n$ và $G≠n+ \ast$ (với $n∈ \mathbb{Z}$ ), nếu $fG=G(1)=n∈ \mathbb{Z}$ thì $G=n$ hoặc $G=n+ \ast$ (theo ***3.4*** và hệ quả của ***3.2***) $\Rightarrow$ $fG\notin \mathbb{Z}$ $\Rightarrow$ $\int(fG)= \\{ \int(f(GL)-1)+1|\int(f(GR)+1)-1 \\} = \\{ \int(f(GL-1))+1|\int(f(GR+1))-1 \\} = \\{ GL|GR \\} = G$ (bởi ***3.4***, ***1.4b*** nên $\forall$ thế cờ $H$ , có $f(H+x)=fH+x, x∈ \mathbb{Z}$ ), quy nạp theo giả thiết ***(3.5)*** đã đúng với ***GL-1, GR+1*** (chúng đều là thế chẵn bởi vì $G$ là thế chẵn, theo ***2.3a,b***). <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 3.5*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 3.6:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Cho $G$ là thế cờ vây chẵn, có $\int G(1)=G$ . Nói cách khác, làm ấm là phép toán đảo ngược của làm lạnh bởi 1. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 3.6:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với 2 phần quan trọng nhất của bằng chứng cho ***(3.6)*** đã được hoàn thành: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1) $G(1)=fG$ , theo ***bổ đề (3.4)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2) $\int (fG)=G$ , theo ***bổ đề (3.5)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Ta kết hợp 1) và 2) ta có ***định lý (3.6)***. Cần nhấn mạnh rằng toàn bộ chứng minh dựa trên khái niệm về tính chẵn lẻ của các thế cờ. Vì vậy kết quả này chỉ giới hạn cho tàn cục cờ vây. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 3.6*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G$ là thế cờ vây chẵn thì $G=\int G(1)$ . Nếu $G$ là thế cờ vây lẻ thì $G= \ast + \int G(1)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi (3.6), nếu $G$ là thế chẵn thì $\int G(1)=G$ , nếu $G$ là thế lẻ thì $G+ \ast$ là thế chẵn $\Rightarrow$ $\int G(1)= \int (G+ \ast)(1) = G+ \ast$ $\Leftrightarrow$ $G= \ast + \int G(1)$ .  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi hệ quả của ***(3.6)*** cùng với tính tuyến tính của toán tử làm lạnh và làm mát (***1.4d và 3.4***), nếu có một thế cờ là tổng của nhiều thế cờ con, ta chỉ cần làm mát từng thế cờ con rồi tính tổng của chúng, sau đó làm ấm tổng này để truy ngược lại giá trị thực của thế cờ ban đầu. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Ví dụ:</ins>***
<div align="center">

![image](https://github.com/user-attachments/assets/540c3ff1-f14f-42e7-a4e6-db9f68c54e9d)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Cùng thử phân tích một thế tàn cục trên bảng $9 \times 9$ (hình). Đen đã chiếm được 8 ô lãnh thổ, còn Trắng là 7 ô. Có 6 khu vực được đặt tên từ $A$ đến $F$ là những vùng chưa thuộc lãnh thổ của người chơi nào, tại đây đang diễn ra giao tranh giữa 2 phe. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng những kiến thức của chương 2, 3 để chứng tỏ (bằng quy nạp) rằng giá trị sau khi làm mát của một hành lang như trong hình ở phần ( $\ast$ )với $n$ ô trống ( $n≥2$ ) là $n-2+\frac{1}{2^{n-1}}$ , khi trắng và đen đảo vai trò cho nhau thì giá trị là $-(n-2) - \frac{1}{2^{n-1}}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Quay lại với hình trên, $A$ và $F$ là 2 hành lang tương đương nhau, bởi công thức trên nên $fA=fF=-\frac{1}{2}$ . $E= \ast$ như đã nói trong phần hình 3 ở ***<ins>bài giảng số 36</ins>***, nên $fE=0$ . Với $B$ , có thể nhận ra nước đi tối ưu của cả 2 người chơi là đánh vào ô $(4,7)$ $\Rightarrow$ $B=\\{ 1+ \ast|-1+ \ast \\}$ $\Rightarrow$ $fB=\\{ 0|0 \\}= \ast$ . Với $C$ , nước đi tối ưu của cả 2 là ô $(7,6)$ $\Rightarrow$ $C=\\{ 3| \\{ 2|0 \\} \\}$ $\Rightarrow$ $fC=\\{ 2|2+ \ast \\} =2+ \uparrow$ . Tương tự, $fD=-2+ \downarrow$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giá trị của trò chơi là $G=8-7+A+B+C+D+E+F$ $\Rightarrow$ $fG=1+fA+fB+fC+fD+fE+fF=1-\frac{1}{2}+ \ast +2+ \uparrow -2+ \downarrow +0-\frac{1}{2}= \ast$ . Số ô trống trên bàn cờ là một số lẻ nên đây là một thế cờ lẻ, bởi hệ quả của ***(3.6)***: $G= \ast + \int (fG)= \ast +\int ( \ast )= \ast ±1= \\{ 1+ \ast|-1+ \ast \\}$ (theo ***0.0***) $\Rightarrow$ Người đi trước luôn thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nước đi tối ưu của người đi trước là chơi ở $B$ , đánh vào ô $(4,7)$ , bằng cách này Đen (Trắng) sẽ đưa trò chơi về $1+ \ast (-1+ \ast )$ , người đi lượt sau phải nhận một thất bại không thể tránh khỏi. <br>







