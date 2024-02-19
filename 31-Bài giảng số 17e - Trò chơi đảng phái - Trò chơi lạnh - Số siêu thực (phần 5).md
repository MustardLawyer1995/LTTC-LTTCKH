# Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 5)
### 7. Số chưa bao giờ là tốt
&nbsp;&nbsp;&nbsp;&nbsp;Trong chương này ta sẽ đi tới 1 kết quả quan trọng của lý thuyết về partisan games, tuyên bố rằng trong trò chơi tổng của các thành phần gồm cả số và phi số, nên tránh việc chọn nước đi ở các trò chơi con nhận giá trị là số. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 4.1:</ins>*** 
&nbsp;&nbsp;&nbsp;&nbsp;*(Định lí tránh số yếu)* Trong trò chơi $G + x$ có $G$ là phi số và $x$ là số, thực hiện nước đi trong $G$ luôn đem lại kết quả tốt hơn hoặc bằng thực hiện nước đi trong $x$ . Nói cách khác: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G + x \parallel > 0 \Leftrightarrow \exists GL: GL + x \ge 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G + x < \parallel 0 \Leftrightarrow \exists GR: GR + x \le 0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 4.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G + x \parallel > 0$ , Trái sẽ thắng nếu đi trước (nước đi chiến thắng nằm trong $G$ hoặc $x$ ) $\Leftrightarrow \exists GL: GL + x \ge 0$  hoặc $\exists xL: G + xL \ge 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử $\exists y = xL: G + y \ge 0$ . Xét dãy số $\\{ y_{1} = yL , y_{k+1} = y_{k}L \\}$ , hiển nhiên $x > y > y_{1} > y_{2} > y_{3} > ...$ . Trong dãy số này, chọn ra $y_n$ là số nhỏ nhất thỏa mãn $G + y_{n} \ge 0$ , vì $G$ không phải là số nên $G \ne -y_{n}$ $\rightarrow$ $G + y_{n} > 0$ $\rightarrow$ Trong trò chơi $G + y_{n}$ người chơi Trái có nước đi chiến thắng. Nước đi này không nằm trong $y_n$ vì không thể có $G + y_{n+1} \ge 0$ (theo giả thiết $y_n$ là số nhỏ nhất thỏa mãn $G + y_{n} \ge 0$ ) $\rightarrow$ nước đi chiến thắng của Trái phải nằm trong $G$  <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $\exists GL:GL + y_{n} \ge 0 \to GL + x > GL + y_{n} \ge 0$ (đpcm) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4.1*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Định nghĩa các hàm $l(G)$ và $r(G)$ như sau: (với $\delta \to 0^+$ , là một số dương vô cùng bé) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $l(G) = G - \delta$ , nếu $G$ là số, $l(G) = \text{ max } r \( GL \)$ , nếu $G$ không phải là số <br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $r(G) = G + \delta$ , nếu $G$ là số, $r(G) = \text{ min } l \( GR \)$ , nếu $G$ không phải là số <br>  

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 4.2:</ins>*** 
&nbsp;&nbsp;&nbsp;&nbsp;Cho $x$ là 1 số bất kì, có: $l(G) > x \Leftrightarrow G \parallel > x$ và $r(G) < x \Leftrightarrow G < \parallel x$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 4.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $G$ là số, định lý hiển nhiên đúng. Với $G$ là phi số, ta sẽ chứng minh: $l(G) > x \Leftrightarrow \exists r\( GL \) > x \Leftrightarrow \exists GL \ge x \Leftrightarrow G \parallel > x$ (#). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với: $l(G) > x \Leftrightarrow \exists r\( GL \) > x$ theo định nghĩa $l(G) , r(G)$ và: $\exists GL \ge x \Leftrightarrow G \parallel > x$ theo ***(4.1)***. Toàn bộ (#) sẽ được chứng minh bằng quy nạp: giả sử (#) đúng khi thay bằng $GL,GR,GLL,GLR,GRL,GRR,...$ thì nó cũng đúng với $G$ .Thật vậy, nếu $GL$ là số thì $r\( GL \) > x \Leftrightarrow GL \ge x$ là hiển nhiên theo định nghĩa $r(G)$ nên ta xét $GL$ là phi số: $r\( GL \) > x \Leftrightarrow \text{ min } l \( GLR \) > x$ (định nghĩa $l(G)$ ) $\Leftrightarrow \forall GLR,l\( GLR \) > x \Leftrightarrow \forall GLR, GLR \parallel > x$ (do giả thiết quy nạp) $\Leftrightarrow Gl \ge x$ (theo ***4.1***, Phải sẽ luôn thua trong trò chơi $GL - x$ nếu đi trước vì nước đi tối ưu của Phải luôn đưa trò chơi về $GLR - x \parallel > 0$ ) $\rightarrow$ Quy nạp hoàn tất. Đến đây ta chứng minh $r(G) < x \Leftrightarrow G < \parallel x$ theo cách tương tự. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4.2*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 4.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G$ là phi số thì tồn tại $GL$ để $GL - G$ lớn hơn một số âm bất kỳ. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 4.3:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chọn ra $GL$ để $r\( GL \) = l(G)$ , xét số dương $\xi$ tùy ý, viết nó dưới dạng tổng của 2 số dương khác nhau: $\xi = \xi_{1} + \xi_{2}$ (luôn thực hiện được nhờ chọn ra số dương $\xi_{1} < \xi$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi ***(4.2)*** có: $GL + \xi_{1} > GL \Leftrightarrow GL + \xi_{1} > r\( GL \)$ và $G > G - \xi_{2} \Leftrightarrow l(G) > G - \xi_{2}$ 
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $GL + \xi_{1} > r\( GL \) = l(G) > G - \xi_{2} \Rightarrow GL - G > -\xi$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 4.3*** <br>
&nbsp;&nbsp;&nbsp;&nbspTất cả những ý trên là tiền đề dẫn tới kết luận sau, là một công cụ quan trọng để tính toán các giá trị phi số <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 4.4a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nguyên lý chuyển dịch số: Nếu $G = \\{ GL|GR \\}$ là phi số và $x$ là số thì $G + x = \\{ GL + x|GR + x \\}$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 4.4a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $x = \\{ xL|xR \\}$ , có $G + x = \\{ GL + x,G + xL|GR + x,GR + xR \\}$ . Vì $x$ là số nên $xL < x < xR \rightarrow xL - x$ là một số âm. Bởi ***(4.3)***, tồn tại $GL$ để $GL - G > xL - x \Leftrightarrow GL + x > G + xL$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với lập luận tương tự, có thể chứng minh $GR + x < G + xR \to G + x = \\{ GL + x|GR + x \\}$ theo ***(3.4a)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4.4a*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Ví dụ: Với $n \in \mathbb{R}$ , khi ấy ta có: <br>

```math
\left\{ {n|n + *} \right\} = n + \left\{ {0|*} \right\} = n +  \uparrow ,\left\{ {n|n} \right\} = n + \left\{ {0|0} \right\} = n + *,\left\{ {n,n + *|n} \right\} = n + \left\{ {0,*|0} \right\} = n +  \uparrow  + *
```
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy, ta rút ra được một hệ quả khác nhưng là phiên bản mạnh hơn, hoàn chỉnh hơn của ***(4.1)***, như sau: <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hệ quả 4.4b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;*(Định lí tránh số)* Trong trò chơi $G + x + H$ có $G$ là phi số và $x$ là số, chọn nước đi ở $G$ luôn tốt hơn hoặc bằng chọn nước đi ở $x$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả 4.4b:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu bạn là Trái, hiển nhiên bạn muốn giá trị của trò chơi càng dương (lớn hơn) càng tốt. Theo ***(4.3)***, tồn tại $GL$ để $GL + x > G + xL$ $\rightarrow$ Bạn sẽ thích chơi ở $G$ hơn là ở $x$ . Lập luận tương tự nếu bạn là Phải. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, trong 1 trò chơi gồm cả thành phần số và phi số, nên tránh chơi ở thành phần số, bởi nếu ở đó có nước đi chiến thắng thì cũng tồn tại nước đi chiến thắng ở thành phần phi số. Hiểu biết này giúp người chơi giảm bớt gánh nặng tính toán chiến lược khi anh ta không cần để tâm đến các giá trị số. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***hệ quả 4.4b*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Một kết quả phụ khác cũng khá thú vị là trong trò chơi có cả số nguyên và giá trị không phải số nguyên, nên ưu tiên lựa chọn các giá trị không phải số nguyên. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 4.5:</ins>*** 
&nbsp;&nbsp;&nbsp;&nbsp;*(Định lí tránh số nguyên)* Trong trò chơi $G + x + M$ với $G$ không phải là số nguyên và $x$ là số nguyên, chơi trong $G$ luôn đem lại kết quả tốt hơn hoặc bằng chơi trong $x$ . <br> 

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 4.5:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Điều này là hiển nhiên vì người chơi Phải/Trái luôn muốn độ tăng/giảm giá trị trò chơi là thấp nhất có thể. Nếu $G$ là phân số thì $|GL - G| < 1,|GR - G| < 1$ ; với $x \in \mathbb{Z} , |xL - x| \ge 1,|xR - x| \ge 1$ $\rightarrow$ Chơi trong $G$ luôn tốt hơn chơi trong $x$ . Nếu $G$ là phi số thì định lý tự động được thỏa mãn bởi ***(4.4b)***. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4.5*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;***Hệ quả:*** Nếu $G \notin \mathbb{Z}, x \in \mathbb{Z}$ thì $G + x = \\{ GL + x|GR + x \\}$ (theo ***4.4b và định nghĩa 2.1***). <br>

### 8. Liên kết partisan game và impartial game 
&nbsp;&nbsp;&nbsp;&nbsp;Ta phát hiện ra rằng lý thuyết về partisan game là tổng quát hơn lý thuyết về impartial game, bởi vì 1 impartial game hoàn toàn có thể được coi như 1 trường hợp đặc biệt của partisan game. Hãy nghĩ về trò chơi hackenbush 3 màu ở phần 2, nếu ta cho số lượng đoạn xanh lam và đỏ về 0 thì trò chơi chỉ còn các đoạn xanh lục, tương đương với 1 ván hackenbush cổ điển (impartial game), nhưng ta vẫn có thể áp dụng mô hình phân tích của hackenbush 3 màu cho nó. Theo định nghĩa, 1 impartial game $G = \\{ GL|GR \\}$ phải có $GL = GR$ , dựa vào lý thuyết về nimber trong bài về impartial game ***(bài giảng số 7)***, có thể xác định được dạng hợp quy của các trạng thái trò chơi như sau: <br>

```math
\left\{ {{\rm{ }}\space\space|{\rm{ }}} \right\} = 0,\left\{ {0|0} \right\} = *,\left\{ {0,*|0,*} \right\} = *2,\left\{ {0,*,*2|0,*,*2} \right\} = *3,\left\{ {0,*,*2,*3|0,*,*2,*3} \right\} = *4,{\rm{ }}...
```
&nbsp;&nbsp;&nbsp;&nbsp;Bởi ***<ins>định lí Sprague-Grundy</ins>*** ta có: $\ast n + \ast m = \ast \( n \text { xor } m \)$ . Giá trị $\ast n$ có 1 số tính chất như sau:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\ast n$ là phi số $\forall b \ne 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\ast n = - \ast n$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Với $n \ne m$ thì $\ast n \parallel \ast m$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\downarrow < \ast n < \uparrow$ , $\forall n \ne 1$ <br>
























