# Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 6)
### 9. Tích Norton
&nbsp;&nbsp;&nbsp;&nbsp;Cho $U > 0$ , tích $G \bullet U$ được định nghĩa như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G \bullet U = U + U + ... + U$ ( $G$ lần) nếu $G \in \mathbb{N}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G \bullet U = - U - U - ... - U$ ( $-G$ lần) nếu $G \in \mathbb{Z}^{-}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $G \bullet U = \\{ GL \bullet U + U +I|GR \bullet U - U - I \\}$ nếu $G$ không phải là số nguyên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong đó $I \in \Delta U = \\{ u - U:u \in UL \\} \cup \\{ U - u:u \in UR \\} , U = \\{ UL|UR \\}$ là dạng hợp quy. Đơn giản hơn có thể chọn $I = \text{ max } \Delta U$ (theo ***3.4a***). Lưu ý rằng, tích Norton $G \bullet U$ khác với tích thông thường giữa 2 số ( $G \times U$ ). <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Tính chất 5.1:</ins>*** 
&nbsp;&nbsp;&nbsp;&nbsp;Tích Norton có các tính chất sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;*(5.1a)*: $\( -G \) \bullet U = -G \bullet U$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 5.1a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $G \in \mathbb{Z}$ , mệnh đề là hiển nhiên theo định nghĩa tích Norton nên ta giả thiết $G$ không phải số nguyên. Giả sử ***5.1a*** đúng nếu thay $G$ bằng $GL,GR$ , chứng minh bằng quy nạp: <br>

```math
\left( { - G} \right) \bullet U = \left\{ {\left( { - GR} \right) \bullet U + U + I|\left( { - GL} \right) \bullet U - U - I} \right\} = \left\{ { - GR \bullet U + U + I| - GL \bullet U - U - I} \right\} =  - G \bullet U
```
&nbsp;&nbsp;&nbsp;&nbsp;*(5.1b)*: $A \ge B \Leftrightarrow A \bullet U \ge B \bullet U$ (tính đơn điệu) <br>
&nbsp;&nbsp;&nbsp;&nbsp;*Hệ quả*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $A = B \Leftrightarrow A \bullet U = B \bullet U$ (bởi $A = B$ ngụ ý $A \ge B$ và $A \le B$ $\Leftrightarrow$ $A \bullet U \ge B \bullet U$ và $A \bullet U \le B \bullet U$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $A > B \Leftrightarrow A \bullet U > B \bullet U$ ( $A > B$ $\to$ $A \bullet U \ge B \bullet U$ , nếu $A \bullet U = B \bullet U$ $\to$ mâu thuẫn) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $A \parallel B \Leftrightarrow A \bullet U \parallel B \bullet U$ (giả định $A >=< B$ dẫn tới mâu thuẫn) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*(5.1c)*: $A \bullet U + B \bullet U = \( A + B \) \bullet U$ (tính chất phân phối với phép cộng) <br>
&nbsp;&nbsp;&nbsp;&nbsp;*(5.1d)*: Với $B,C > 0$ và $B \notin \mathbb{Z}$ , ta có: $\( A \bullet B \) \bullet C = A \bullet \( B \bullet C \)$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét</ins>* Chứng minh cho ***5.1b,c,d*** tương đối phức tạp, ta cần trang bị 1 số công cụ khác trước khi giải quyết vấn đề. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 5.2a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Cho $H > 0$ có: $G_{1} + G_{2} + G_{3} \ge 0 \to G_{1} \bullet H + G_{2} \bullet H + G_{3} \bullet H \ge 0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 5.2a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu tất cả $G_{i} \in \mathbb{Z}$ thì ***5.2a*** hiển nhiên đúng. Với những trường hợp còn lại, ta sử dụng quy nạp với giả thiết rằng ***(5.2a)*** đúng khi thay $G_i$ bất kỳ bằng $G_{i}L,G_{i}R,G_{i}LL,G_{i}LR,G_{i}RL,G_{i}RR,...$ Cần chỉ ra rằng, Phải luôn thua nếu đi trước trong trò chơi $G_{1} \bullet H + G_{2} \bullet H + G_{3} \bullet H$ . Không mất tính tổng quát, giả định rằng Phải đi nước đầu tiên ở $G_{i} \bullet H$ . Có những trường hợp nhỏ sau đây: <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* $G_{1} = n \in \mathbb{Z} , G_{2} \notin \mathbb{Z}$ , khi đó $\( n + 1 \) + G_{2} + G_{3} \ge 1 > 0$ , bởi ***(4.5)***, có thể giả định nước đi chiến thắng của Trái nằm ở $G_{2} \to \( n + 1 \) + G_{2}L + G_{3} \ge 0 \to \( n + 1 \)H + G_{2}L \bullet H + G_{3} \bullet H \ge 0$ (do giả thiết quy nạp). Ta đến với 3 trường hợp nhỏ hơn phụ thuộc dấu của $n$ như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 1a:</ins>* $n = 0$ , Phải sẽ không còn nước đi trong $G_{1} \bullet H = 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 1b:</ins>* $n > 0$ , mọi nước đi của Phải trong $G_{1} \bullet H = nH$ sẽ đưa nó về $\( n-1 \)H + HR$ . Trái đáp trả bằng cách đưa $G_{2} \bullet H$ về $G_{2}L \bullet H + 2H - HR$ , và trò chơi khi ấy trở thành: <br>

```math
\left( {n - 1} \right)H + HR + {G_2}L \bullet H + 2H - HR + {G_3} \bullet H = \left( {n + 1} \right)H + {G_2}L \bullet H + {G_3} \bullet H \ge 0
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 1c:</ins>* $n < 0$ , như TH1b, đưa $G_{1} \bullet H = nH$ về $\( n+1 \)H - HL$ , Trái đưa $G_{2} \bullet H$ về dạng $G_{2} \bullet H$ về $G_{2}L \bullet H + HL$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* $G_{1} \notin \mathbb{Z}$ , nên mọi nước đi của Phải trong $G_{1} \bullet H$ sẽ đưa về $G_{1}R \bullet H - HL$ hay $G_{1}R \bullet H - 2H + HR$ . Bởi $G_{1} + G_{2} + G_{3} \ge 0$ , nên $G_{1}R + G_{2} + G_{3} \parallel > 0$ . Ta đến với 2 trường hợp nhỏ hơn như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 2a:</ins>* $G_{1}R,G_{2},G_{3} \in \mathbb{Z}$ . Bởi $G_{1}R + G_{2} + G_{3} \parallel > 0$ nên $G_{1}R + G_{2} + G_{3} = m \ge 1$ . Nước đi đầu tiên của Phải đưa trò chơi trở về: $G_{1}R \bullet H - 2H + HR + G_{2} \bullet H + G_{3} \bullet H = \( m-2 \)H + HR$ hoặc $G_{1}R \bullet H - HL + G_{2} \bullet H + G_{3} \bullet H = mH - HL$ . Bởi $m \ge 1 \to mH - HL \ge H - HL \ge 0$ và $\( m-2 \)H + HR \ge HR - H \parallel > 0$ nên khi ấy ở lượt tiếp, Trái có nước đi chiến thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *<ins>Trường hợp 2b:</ins>* không phải tất cả  $G_{1}R,G_{2},G_{3}$ đều $\in \mathbb{Z}$ . Nước đi đầu của Phải đưa trò chơi về:  $G_{1}R \bullet H - 2H + HR + G_{2} \bullet H + G_{3} \bullet H$ hoặc $G_{1}R \bullet H - HL + G_{2} \bullet H + G_{3} \bullet H$ . Bởi $G_{1}R + G_{2} + G_{3} \parallel > 0$ , nên không mất tính tổng quát, giả định $G_{1}R \notin \mathbb{Z}$ và $G_{1}RL + G_{2} + G_{3} \ge 0$ (theo ***4.5***) khi ấy suy ra $G_{1}RL \bullet H + G_{2} \bullet H + G_{3} \bullet H \ge 0$ (theo giả thiết quy nạp). Sau nước đi đầu tiên của Phải, Trái có thể đưa $G_{1}R \bullet H$ về $G_{1}RL \bullet H + HL$ hay $G_{1}RL \bullet H + 2H - HR$ và trò chơi trở thành $G_{1}RL \bullet H + G_{2} \bullet H + G_{3} \bullet H \ge 0$ , Phải đi lượt tiếp và thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Từ tất các trường hợp trên thấy rằng, dù Phải đi bất cứ nước nào trong trò chơi $G_{1} \bullet H + G_{2} \bullet H + G_{3} \bullet H$ cũng thua nên suy ra $G_{1} \bullet H + G_{2} \bullet H + G_{3} \bullet H \ge 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 5.2a*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 5.1b và 5.1c:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với $U > 0 , A \ge B \to A + \( -B \) + 0 \ge 0$ , bởi ***(5.2a) và (5.1a)*** nên $A \bullet U + \( -B \) \bullet U + 0 \bullet U = A \bullet U - B \bullet U \ge 0 \Leftrightarrow  A \bullet U \ge B \bullet U$ nên ta kết luận $A \ge B \to A \bullet U \ge B \bullet U$ (##) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Lại có: $-\( A+B \) + A + B \ge 0,\( A+B \) + \( -A \) + \( -B \) \ge 0$, bởi ***(5.2a),(5.1a)*** nên $-\( A+B \) \bullet U + A \bullet U + B \bullet U \ge 0$ và $\( A+B \) \bullet U - A \bullet U - B \bullet U \ge 0$ $\Leftrightarrow A \bullet U + B \bullet U = \( A+B \) \bullet U$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 5.1c*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $K \parallel > 0 \to KL \ge 0 \to KL \bullet U \ge 0$ (theo ***5.2a***) $\to KL \bullet U + UL \ge 0$ (vì $U > 0 \to UL \ge 0$ ). Xét trò chơi $K \bullet U$ , Trái đi trước có nước thắng: đưa trò chơi về $KL \bullet U + UL \ge 0 \to K \bullet U \parallel > 0$ . Suy ra: $K \parallel > 0 \to K \bullet U \parallel > 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ điều này ta suy ra: $A \parallel > B \Leftrightarrow A - B \parallel > 0 \to \( A-B \) \bullet U = A \bullet U - B \bullet U \parallel > 0$ (theo ***5.1c***) $\Leftrightarrow A \bullet U \parallel > B \bullet U$ . Bởi vậy nên: $A \bullet U \ge B \bullet U \to A \ge B$ (giả định $A < \parallel B$ dẫn đến $A \bullet U < \parallel B \bullet U$ , mâu thuẫn), kết hợp với (##) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 5.1b*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Bổ đề 5.2b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Với $G \notin \mathbb{Z},U > 0$ thì $G \bullet U = \\{ GL \bullet U + U + I|GR \bullet U - U - I \\}$ là dạng hợp quy $\Leftrightarrow G = \\{ GL|GR \\}$ cũng chính là dạng hợp quy. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 5.2b:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi $I = \text{ max } \( UL - U,U - UR \)$ nên $GL \bullet U + U + I = \text{ max } \( GL \bullet U + UL,GL \bullet U + 2U - UR \)$ , ta cần chỉ ra với mọi phần tử trong tập sau: <br>
<div align="center">

$\( GL \bullet U + U + I\)R = \\{ GLR \bullet U,GL \bullet U + ULR,GL \bullet U + U,GL \bullet U + 2U -  ULR \\}$ đều $\parallel > G \bullet U$ 
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Thật vậy, ta có: $GLR \parallel > G$ (do giả thiết $G = \\{ GL|GR \\}$ là dạng hợp quy) $\Leftrightarrow GLR \bullet U \parallel > G \bullet U$ (từ ***hệ quả 5.1b***); có $ULR \parallel > U$ và $ULR < \parallel U$ (do $U = \\{ UL|UR \\}$ là dạng hợp quy) $GL \bullet U + ULR \parallel > GL \bullet U + U$ và $GL \bullet U + 2U - URL \parallel > GL \bullet U + U$ , mặt khác bởi $G \notin \mathbb{Z}$ nên $1 > G - GL$ (theo ***2.1 và 4.3***) $\Leftrightarrow U > \( G - GL \) \bullet U$ và $\( GR \bullet U - U - I \)L$ đều $< \parallel G \bullet U$ , dẫn đến kết luận bổ đề. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***bổ đề 5.2b*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh tính chất 5.1d:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi $A \in \mathbb{Z}$ thì đẳng thức tự động thỏa mãn bởi ***5.1c***, nên ta xét trường hợp $A \notin \mathbb{Z}$ .<br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $Ib = \text{ max } \( BL - B,B - BR \) , Ic = \text{ max } \( CL - C,C - CR \)$ . Khi ấy ta có: <br>

```math
\begin{array}{l}
\left( {A \bullet B} \right) \bullet C = \left\{ {AL \bullet B + B + Ib|AR \bullet B - B - Ib} \right\} \bullet C\\
{\rm{                          }} = \left\{ {\left( {AL \bullet B} \right) \bullet C + \left( {B + Ib} \right) \bullet C + C + Ic|\left( {AR \bullet B} \right) \bullet C - \left( {B + Ib} \right) \bullet C - C - Ic} \right\}.
\end{array}
```
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, $B \bullet C = \\{ BL \bullet C + C + Ic|BR \bullet C - C - Ic \\}$ là dạng hợp quy ***theo 5.2b***, lại có: <br>

```math
\left\{ \begin{array}{l}
\left( {B \bullet C} \right)L - B \bullet C = \left( {BL - B} \right) \bullet C + C + Ic\
B \bullet C - \left( {B \bullet C} \right)R = \left( {B - BR} \right) \bullet C + C + Ic
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;Nên khi ấy: $\text{ max } = \( \( B \bullet C \)L - B \bullet C , B \bullet C - \( B \bullet C \)R \) = Ib \bullet C + C + Ic$ . Từ đó ta suy ra: <br>

```math
\begin{array}{l}
A \bullet \left( {B \bullet C} \right) = A \bullet \left\{ {BL \bullet C + C + Ic|BR \bullet C - C - Ic} \right\}\\
{\rm{                 }} = \left\{ {AL \bullet \left( {B \bullet C} \right) + \left( {B + Ib} \right) \bullet C + C + Ic|AR \bullet \left( {B \bullet C} \right) - \left( {B + Ib} \right) \bullet C - C - Ic} \right\}
\end{array}
```
&nbsp;&nbsp;&nbsp;&nbsp;Do vậy $\( A \bullet B \) \bullet C = A \bullet \( B \bullet C \)$ được thỏa mãn bởi quy nạp (giả định đẳng thức đúng khi thay $A \to AL,AR$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***tính chất 5.2d*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* Ta có ví dụ minh họa về tích Norton như sau, với: <br>

```math
G \notin \mathbb{Z} \bigg\vert \frac{{Gp}}{{{2^s}}} = \left\{ {\frac{{Gp}}{{{2^s}}} + \frac{{p - 1}}{{{2^s}}} \bigg\vert \frac{{GRp}}{{{2^s}}} - \frac{{p - 1}}{{{2^s}}}} \right\}
```
```math
\Rightarrow * \bullet \frac{1}{2} = *,* \bullet \frac{3}{2} = \left\{ {1| - 1} \right\},\left( {\frac{1}{2}} \right) \bullet \frac{3}{2} = \left\{ {1 \bigg\vert \frac{1}{2}} \right\}, \uparrow  \bullet \frac{1}{2} = \left\{ {0 \bigg\vert * \bullet \frac{1}{2}} \right\} = \left\{ {0|*} \right\} =  \uparrow ,{\rm{ }}...
```
```math
\Rightarrow G \bullet n = \left\{ {GL \bullet n + n - 1|GR \bullet n - n + 1} \right\}\; \to * \bullet n = \left\{ {n - 1| - n + 1} \right\},{\rm{ }}\left( {\frac{1}{2}} \right) \bullet n = \left\{ {n - 1|1} \right\},{\rm{ }}...
```
```math
\left\{ \begin{array}{l}
G \bullet  \uparrow  = \left\{ {GL \bullet  \uparrow  + 2 \uparrow  + *|GR \bullet  \uparrow  + 2 \downarrow  + *} \right\}\; \to \;\left( {\frac{1}{2}} \right) \bullet  \uparrow  = \left\{ {2 \uparrow  + *| \downarrow  + *} \right\},* \bullet  \uparrow \\
{\rm{                                                               }} = \left\{ {2 \uparrow  + *|2 \downarrow  + *} \right\},\left\{ {1| - 1} \right\} \bullet  \uparrow  = \left\{ {3 \uparrow  + *|3 \downarrow  + *} \right\}...
\end{array} \right.
```

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Nguyên lí 5.3a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nguyên lý chuyển dịch sao: $\forall G \notin \mathbb{Z}$ , ta có: <br>

```math
G \bullet  \uparrow  + *n = \left\{ {GL \bullet  \uparrow  + 2 \uparrow  + * + *n|GR \bullet  \uparrow  + 2 \downarrow  + * + *n} \right\}
```

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh nguyên lí 5.3a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét trò chơi $\\{ GL \bullet \uparrow + 2\uparrow + \ast + \ast n | GR \bullet \uparrow + 2\downarrow + \ast + \ast n \\} - G \bullet \uparrow + \ast n$ , nước đi duy nhất mà người chơi có thể nghĩ đến là chơi ở $\ast n$ , bởi những nước đi còn lại đều dễ dàng bị đối thủ khắc chế bằng cách đưa toàn bộ trò chơi về 0. Không mất tính tổng quát, giả định Phải đưa $\ast n$ về $\ast n'$ (với $n' < n$ ), Trái có thể đưa trò chơi về: <br>

```math
GL \bullet  \uparrow  + 2 \uparrow  + * + *n - G \bullet  \uparrow  + *n'{\rm{ }} = \left( {GL - G + 2} \right) \bullet  \uparrow  + * + *n + *n'
```
&nbsp;&nbsp;&nbsp;&nbsp;bởi $G \notin \mathbb{Z}$ nên $GL - G > -1$ (theo ***2.1 và 4.3***) $\to \( GL - G + 2 \) \bullet \uparrow + \ast + \ast n + \ast n' > \uparrow + \ast + \ast n + \ast n' > 0$ $\to$ Phải thua. Do vậy, trong trò chơi ban đầu, người đi trước luôn thua nên giá trị của trò chơi $= 0$ , dẫn tới kết luận hiển nhiên của ***(5.3a)***. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***nguyên lí 5.3a*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Nguyên lí 5.3b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Với $n \in \mathbb{N}, m \in \mathbb{Z}^{+}$ hoặc $n \in \mathbb{Z}^{+}, m \in \mathbb{N}$ , có: $\\{ 0|n\uparrow + \ast m \\} = \( n+1 \)\uparrow + \ast + \ast m$ và đây cũng là dạng hợp quy. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh nguyên lí 5.3b:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh bằng cách chỉ ra trò chơi $\\{ 0|n\uparrow + \ast m \\} + \( n+1 \)\downarrow + \ast + \ast m = 0$ , tức là người đi trước luôn thua, cũng như chỉ ra $\\{ 0|n\uparrow + \ast m \\}$ không thể rút gọn bởi ***3.4a,b***) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***nguyên lí 5.3b*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Nguyên lí 5.3c:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: 







