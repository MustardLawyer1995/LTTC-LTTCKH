# Partisan game – Nhiệt đồ và lời giải cho tàn cuộc cờ vây (phần 2)
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











