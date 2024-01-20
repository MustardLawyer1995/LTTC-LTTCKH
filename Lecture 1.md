# Sheep Game
- <ins>Không gian giới hạn của trò chơi:</ins> Cánh đồng có kích thước $n \times 1$ gồm $n$ các ô vuông thành phần có kích thước $1 \times 1$
- <ins>Mô phỏng luật chơi</ins>: Sau mỗi lượt con cừu ở vị trí (0) sẻ nhảy qua con cừu 2, con cừu 2 nhảy qua con cừu 3 và kế đến con cừu 3 nhảy về con cừu 1 (tất cả con cừu phải nhảy qua điểm đối xứng, chẳng hạn như con cừu 1 nhảy qua con cừu 2 và rơi xuống điểm đối xứng). Hỏi phải đặt 3 con cừu như thế nào để chúng nhảy không vượt qua cánh đồng đó.
## Lời giải
<ins>Phân tích:</ins> Để biểu diễn tương quan mô hình chuyển động của 3 con cừu trên, ta cần lập ra phương trình chuyển động như sau:
Gọi ${a_i},{b_i},{c_i}|\forall i = \overline {0,1,2,...}$ lần lượt là các vị trí sau mỗi lần $i$ di chuyển của con cừu 1,2 và 3. Khi ấy ta có hệ phương trình sau:
```math
\left\{ \begin{array}{l}
{a_1} = 2{b_0} - {a_0}\\
{b_1} = 2{c_0} - {b_0}\\
{c_1} = 2{a_1} - {c_0} = 2\left( {2{b_0} - {a_0}} \right) - {c_0} =  - 2{a_0} + 4{b_0} - {c_0}
\end{array} \right.
```
Khi ấy ta có hệ phương trình tổng quát tương ứng là: 
```math
\left\{ \begin{array}{l}
{a_{n + 1}} = 2{b_n} - {a_n}\\
{b_{n + 1}} = 2{c_n} - {b_n}\\
{c_{n + 1}} =  - 2{a_n} + 4{b_n} - {c_n}
\end{array} \right.,\forall n = \overline {0,1,2,...}
```
Tiếp đến ta chuyển về hệ ma trận như sau; Với ${X_{x + 1}} = M{X_n}$ ta có hệ ma trận tương ứng là: 
```math
M = {\left[ {\begin{array}{*{20}{c}}
{ - 1}&2&0\\
0&{ - 1}&2\\
{ - 2}&4&{ - 1}
\end{array}} \right]^n},{X_n} = \left[ {\begin{array}{*{20}{c}}
{{a_n}}\\
{{b_n}}\\
{{c_n}}
\end{array}} \right]$ 
```
với ma trận $M$ có cùng hệ số là: 
```math
\left\{ \begin{array}{l}
{X_{x + 1}} = {M^n}{X_0}\\
M = {\left[ {\begin{array}{*{20}{c}}
{ - 1}&2&0\\
0&{ - 1}&2\\
{ - 2}&4&{ - 1}
\end{array}} \right]^n},{X_0} = \left[ {\begin{array}{*{20}{c}}
{{a_0}}\\
{{b_0}}\\
{{c_0}}
\end{array}} \right]
\end{array} \right.$
```
Kế tiếp ta sẽ tìm lũy thừa bậc $n$ của ma trận $M$ bằng phương pháp chéo hóa ma trận.
Trước hết ta điểm từng bước như sau:
- <ins>Bước 1:</ins> Giá trị riêng của $\lambda$ : ta có: $\left( {A - \lambda I} \right)v = 0$ khi và chỉ khi $\det \left( {A - \lambda I} \right) = 0$
- <ins>Bước 2:</ins> Nhắc lại sơ về khái niệm nghịch thế
  <p>
  Cho tập  $S = \\{ 1;2;3;...;n \\}$ với $n!$ hoán vị. <br>
  Xét các hoán vị $\{ j_{1};j_{2};...;j_{n} \}$ nghịch thế là cặp ${j_a} > {j_b}$ với $a < b$ . <br>
  Diễn đạt thay thế: phần tử đứng trước luôn “lắn” hơn phần tử đứng sau. <br>
  Ví dụ: $(3,1,2)$ có nghịch thế lần lượt là $(3;1)$ và $(3;2)$ .  <br>
  Kí hiệu nghịch thế: $N = \{ j_{1},j_{2},...,j_{n} \}$ là một số nghịch thế. <br>
  </p>
- <ins>Bước 3:</ins> Tính định thức ma trận $M$ và các giá trị riêng
  <p> Ta có định nghĩa định thức như sau: ${\det A - |A| - \sum {{{\left( { - 1} \right)}^{ \\{ {j_1};{j_2};...;{j_n} \\} }}{a_{1{j_1}}}{a_{2{j_2}.....}}{a_{n{j_n}}}} }$ <br>
  Trong đó: $\{ j_{1};j_{2};...;j_{n} \}$ là các hoán vị của $\{ 1;2;3;...;n \}$ đã nêu khái niệm ở trên. <br>
  Khi đó, ta có được: <br>
```math
\det \left( {\left( {A - \lambda I} \right)} \right) - \left[ {\begin{array}{*{20}{c}}
{ - 1 - \lambda }&2&0\\
0&{ - 1 - \lambda }&2\\
{ - 2}&4&{ - 1 - \lambda }
\end{array}} \right] = \left\{ {\begin{array}{*{20}{c}}
{\left( {{a_{11}}{a_{22}}{a_{33}} + {a_{12}}{a_{23}}{a_{31}} + {a_{13}}{a_{21}}{a_{32}}} \right) - }\\
{\left( {{a_{11}}{a_{23}}{a_{32}} + {a_{12}}{a_{21}}{a_{33}} + {a_{13}}{a_{22}}{a_{31}}} \right)}
\end{array}} \right\}
```
```math
 =  - {\lambda ^3} - 3{\lambda ^2} + 5\lambda  - 1 + \left( {\lambda  - 1\,} \right)\left( {{\lambda ^2} + 4\lambda  - 1} \right) = 0 \Leftrightarrow \left[ \begin{array}{l}
{\lambda _1} = 1;\
{\lambda _2} =  - \sqrt 5  - 2
\end{array} \right.;{\lambda _3} = \sqrt 5  - 2
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Nhận xét:* với ba giá trị riêng trên thì ma trận $3 \times 3$ này có thể giải bằng cách chéo hóa 

  </p> 

- <ins>Bước 4:</ins> Chéo hóa ma trận (dùng để tìm lũy thừa tổng quát bậc $n$)
  <p
    Trước hết ta kí hiệu chéo hóa ma trận dưới dạng đại số thuần túy là $A = PD{P^{ - 1}}$$ .<br>
    Trong đó $D$ là ma trận đường chéo nên với lũy thừa $D$ chỉ cần lũy thừa các phần tử ở <ins>đường chéo</ins>. <br>
    Khi ấy ta cần chứng minh đánh giá sau: ${A^n} = {\left( {PD{P^{ - 1}}} \right)^n} = P{D^n}{P^{ - 1}}$ <br>
    Thật vậy, giả sử tồn tại $k$ sao cho ${A^k} = {\left( {PD{P^{ - 1}}} \right)^k} = P{D^k}{P^{ - 1}}$ <br>
    Khi đó, tại $k+1$ , ta có: ${\left( {PD{P^{ - 1}}} \right)^{k + 1}} = {\left( {PD{P^{ - 1}}} \right)^k}PD{P^{ - 1}} = P{D^k}{P^{ - 1}}PD{P^{ - 1}}$ <br>
    Lại có với ma trận nghịch đảo thì ${P^{ - 1}}P = I$ nên $P{D^k}{P^{ - 1}}PD{P^{ - 1}} = P.{D^k}.I.D.{P^{ - 1}} = P.{D^k}.D.{P^{ - 1}} = P.{D^{k + 1}}.{P^{ - 1}}$ (đúng với nguyên lí quy nạp) . <br>
  </p>       
- <ins>Bước 5:</ins> Với mỗi $\lambda$ tính được, ta sẽ tìm được trị số vector riêng tương ứng (tìm $P$ và $D$)
  <p>
  <i>Trường hợp 1:</i> với $\lambda _{1} = 1$ , ta có: 
   <ol>
$$
\left[
\begin{array}{ccc|c}
  -2 & 2 & 0 & 0 \\
  0 & -2 & 2 & 0 \\
  -2 & 4 & -2 & 0 \\
\end{array}
\right]
$$       
    </ol>
   </p>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng phương pháp khử Gauss, ta suy ra:

```math
\left[
\begin{array}{ccc|c}
  -2 & 2 & 0 & 0 \\
  0 & -2 & 2 & 0 \\
  -2 & 4 & -2 & 0 \
\end{array}
\right]{\rm{  }}\begin{array}{* {20}{c}}
{/2}\\
{/2}\\
{/2 - {R_1}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  -1 & 1 & 0 & 0 \\
  0 & -1 & 1 & 0 \\
  0 & 1 & -1 & 0 \
\end{array}
\right]{\rm{     +   }}\begin{array}{*{20}{c}}
{ + {R_2}}\\
{}\\
{ - 2{R_2}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  -1 & 0 & 1 & 0 \\
  0 & -1 & 1 & 0 \\
  0 & 0 & 0 & 0 \
\end{array}
\right]
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sau khi quy về dạng ma trận bậc thang ta có hệ phương trình sau: 
```math
\left\{ \begin{array}{l}
 - {x_1} + {x_3} = 0\
 - {x_2} + {x_3} = 0
\end{array} \right. \Leftrightarrow \left\{\begin{array}{l}
{x_1} = {x_3}\
{x_2} = {x_3}
\end{array} \right.  \Rightarrow \text{ Nghiệm tổng quát } X = \left( {\begin{array}{*{20}{c}}
{{x_3}}\\
{{x_3}}\
{{x_3}}
\end{array}} \right)  \xRightarrow[\text{}]{x_{3}=1} \text{ Vector riêng } {v_1} = \left( {\begin{array}{*{20}{c}}
1\\
1\
1
\end{array}} \right)
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<i>Trường hợp 2:</i> với $\lambda _{2} =- \sqrt {5}  - 2$ , ta có: 
```math
\left[
\begin{array}{ccc|c}
  \sqrt {5}+1 & 2 & 0 & 0 \\
  0 & \sqrt {5}+1 & 2 & 0 \\
  -2 & 4 & \sqrt {5}+1 & 0 \
\end{array}
\right]   
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng phương pháp khử Gauss, ta suy ra:
```math
\left[
\begin{array}{ccc|c}
  \sqrt {5}+1 & 2 & 0 & 0 \\
  0 & \sqrt {5}+1 & 2 & 0 \\
  -2 & 4 & \sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{  }}\begin{array}{* {20}{c}}
{{\frac{{\sqrt 5  - 1}}{4}}}\\
{}\\
{{\frac{{\sqrt 5  - 1}}{4}}}
\end{array}
{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & \frac{\sqrt {5}-1}{2} & 0 & 0 \\
  0 & 1 & \frac{\sqrt {5}-1}{2} & 0 \\
  -2 & 4 & \sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{     +   }}\begin{array}{*{20}{c}}
{}\\
{2R_{1}}\\
{}
\end{array}
```
```math
{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & \frac{\sqrt {5}-1}{2} & 0 & 0 \\
  0 & 1 & \frac{\sqrt {5}-1}{2} & 0 \\
  0 & 3 + \sqrt5 & \sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{  }}\begin{array}{* {20}{c}}
{{ - \left( {\frac{{\sqrt 5  - 1}}{2}} \right){R_2}}}\\
{}\\
{{ - \left( {\sqrt 5  + 3} \right){R_2}}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & 0 & \frac{\sqrt {5}-3}{2} & 0 \\
  0 & 1 & \frac{\sqrt {5}-1}{2} & 0 \\
  0 & 0 & 0 & 0 \
\end{array}
\right]
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sau khi quy về dạng ma trận bậc thang ta có hệ phương trình sau: 
```math
\left\{ \begin{array}{l}
{x_1} + \frac{{\sqrt 5  - 3}}{2}{x_3} = 0\
 - {x_2} + \frac{{\sqrt 5  - 1}}{2}{x_3} = 0
\end{array} \right. \Leftrightarrow \left\{ \begin{array}{l}
{x_1} = \frac{{ - \sqrt 5  + 3}}{2}{x_3}\
{x_2} = \frac{{\sqrt 5  - 1}}{2}{x_3}
\end{array} \right. \Rightarrow \text{ Nghiệm tổng quát } X = \left( {\begin{array}{*{20}{c}}
{\frac{{ - \sqrt 5  + 3}}{2}{x_3}}\\
{\frac{{ - \sqrt 5  + 1}}{2}{x_3}}\
{{x_3}}
\end{array}} \right)  \xRightarrow[\text{}]{x_{3}=1} \text{ Vector riêng } {v_2} = \left( {\begin{array}{*{20}{c}}
\frac{{ - \sqrt 5  + 3}}{2}\\
\frac{{ - \sqrt 5  + 1}}{2}\
1
\end{array}} \right)
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<i>Trường hợp 3:</i> với $\lambda _{3} = \sqrt {5}  - 2$ , ta có: 
```math
\left[
\begin{array}{ccc|c}
  -\sqrt {5}+1 & 2 & 0 & 0 \
  0 & \sqrt {5}+1 & 2 & 0 \
  -2 & 4 & -\sqrt {5}+1 & 0 \
\end{array}
\right]   
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng phương pháp khử Gauss, ta suy ra:
```math
\left[
\begin{array}{ccc|c}
  -\sqrt {5}+1 & 2 & 0 & 0 \
  0 & \sqrt {5}+1 & 2 & 0 \
  -2 & 4 & -\sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{  }}\begin{array}{* {20}{c}}
{{\frac{{-\sqrt 5  - 1}}{4}}}\
{}\\
{{\frac{{-\sqrt 5  - 1}}{4}}}
\end{array}
{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & \frac{-\sqrt {5}-1}{2} & 0 & 0 \
  0 & 1 & \frac{-\sqrt {5}-1}{2} & 0 \
  -2 & 4 & -\sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{     +   }}\begin{array}{*{20}{c}}
{}\\
{2R_{1}}\\
{}
\end{array}
```
```math
{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & \frac{-\sqrt {5}-1}{2} & 0 & 0 \
  0 & 1 & \frac{-\sqrt {5}-1}{2} & 0 \
  0 & 3 + \sqrt5 & -\sqrt {5}+1 & 0 \
\end{array}
\right]{\rm{  }}\begin{array}{* {20}{c}}
{{ - \left( {\frac{{-\sqrt 5  - 1}}{2}} \right){R_2}}}\
{}\
{{ - \left( {-\sqrt 5  + 3} \right){R_2}}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[
\begin{array}{ccc|c}
  1 & 0 & \frac{-\sqrt {5}-3}{2} & 0 \
  0 & 1 & \frac{-\sqrt {5}-1}{2} & 0 \
  0 & 0 & 0 & 0 \
\end{array}
\right]
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sau khi quy về dạng ma trận bậc thang ta có hệ phương trình sau: 
```math
\left\{ \begin{array}{l}
{x_1} - \frac{{\sqrt 5  + 3}}{2}{x_3} = 0\
 - {x_2} - \frac{{\sqrt 5  + 1}}{2}{x_3} = 0
\end{array} \right. \Leftrightarrow \left\{ \begin{array}{l}
{x_1} = \frac{{\sqrt 5  + 3}}{2}{x_3}\
{x_2} = \frac{{\sqrt 5  + 1}}{2}{x_3}
\end{array} \right.{; ^{}}{ x_3} = {x_3} \Rightarrow \text{ Nghiệm tổng quát } X = \left( {\begin{array}{*{20}{c}}
{\frac{{  \sqrt 5  + 3}}{2}{x_3}}\
{\frac{{  \sqrt 5  + 1}}{2}{x_3}}\
{{x_3}}
\end{array}} \right)\xRightarrow[\text{}]{x_{3}=1} \text{ Vector riêng } {v_3} = \left( {\begin{array}{*{20}{c}}
\frac{{  \sqrt 5  + 3}}{2}\
\frac{{  \sqrt 5  + 1}}{2}\
1
\end{array}} \right)
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Từ ba vector riêng $v_{1}, v_{2}, v_{3}$ tính được ta suy ra: 
```math
D = \left[ {\begin{array}{*{20}{c}}
{{\lambda _1}}&2&0\
0&{{\lambda _2}}&0\
0&0&{{\lambda _3}}
\end{array}} \right] = \left[ {\begin{array}{*{20}{c}}
{{1^n}}&2&0\
0&{{{\left( { - \sqrt 5  - 2} \right)}^n}}&0\
0&0&{{{\left( {\sqrt 5  - 2} \right)}^n}}
\end{array}} \right] \to {D^n}\left[ {\begin{array}{*{20}{c}}
1&2&0\
0&{ - \sqrt 5  - 2}&0\
0&0&{\sqrt 5  - 2}
\end{array}} \right]
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Khi đó ma trận $P$ nhận các vector riêng làm cột, tức ta biểu diễn $P$ như sau: 
```math
P = \left[ {\begin{array}{*{20}{c}}
1&{\frac{{ - \sqrt 5  + 3}}{2}}&{\frac{{\sqrt 5  + 3}}{2}}\
1&{\frac{{ - \sqrt 5  + 1}}{2}}&{\frac{{\sqrt 5  + 1}}{2}}\
1&1&1
\end{array}} \right]
```
 - <ins>Bước 6:</ins> Tiếp đến ta sẽ tính ma trận nghịch đảo $P^-1$
   <p></p> Ta có công thức tính ma trận nghịch đảo là: <br>
```math
{A^{ - 1}} = \frac{1}{{\det A}}.{\left[ {\begin{array}{*{20}{c}}
{{A_{11}}}&{{A_{12}}}&{...}&{{A_{1n}}}\\
{{A_{21}}}&{{A_{22}}}&{...}&{{A_{2n}}}\\
 \vdots & \vdots & \ddots & \vdots \\
{{A_{m1}}}&{{A_{m2}}}& \cdots &{{A_{mn}}}
\end{array}} \right]^T}
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Trong đó $A_{ij}$ là phần bù của đại số  $- {\left( { - 1} \right)^{i + j}}\det \left( {{M_{ij}}} \right)$
   
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Trước hết áp dụng công thức đã nêu ở bước 3, ta dễ dàng tính được: 
```math
\det \left( P \right) - \left| {\begin{array}{*{20}{c}}
1&{\frac{{ - \sqrt 5  + 3}}{2}}&{\frac{{\sqrt 5  + 3}}{2}}\\
1&{\frac{{ - \sqrt 5  + 1}}{2}}&{\frac{{\sqrt 5  + 1}}{2}}\\
1&1&1
\end{array}} \right| = \sqrt 5 
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tính đến cần tính hạng tử của các ma trận sau:    
```math
\left( {{u_{11}};{u_{12}};{u_{13}}} \right) = \left( {\left| {\begin{array}{*{20}{c}}
{\frac{{ - \sqrt 5  + 1}}{2}}&{\frac{{\sqrt 5  + 1}}{2}}\\
1&1
\end{array}} \right|; - \left| {\begin{array}{*{20}{c}}
1&{\frac{{\sqrt 5  + 1}}{2}}\\
1&1
\end{array}} \right|;\left| {\begin{array}{*{20}{c}}
1&{\frac{{ - \sqrt 5  + 1}}{2}}\\
1&1
\end{array}} \right|} \right) = \left( { - \sqrt 5 ;\frac{{1 - \sqrt 5 }}{2};\frac{{1 + \sqrt 5 }}{2}} \right)
```
```math
\left( {{u_{21}};{u_{22}};{u_{23}}} \right) = \left( { - \left| {\begin{array}{*{20}{c}}
{\frac{{ - \sqrt 5  + 3}}{2}}&{\frac{{\sqrt 5  + 3}}{2}}\\
1&1
\end{array}} \right|;\left| {\begin{array}{*{20}{c}}
1&{\frac{{\sqrt 5  + 3}}{2}}\\
1&1
\end{array}} \right|; - \left| {\begin{array}{*{20}{c}}
1&{\frac{{ - \sqrt 5  + 3}}{2}}\\
1&1
\end{array}} \right|} \right) = \left( {\sqrt 5 ;\frac{{ - 1 - \sqrt 5 }}{2};\frac{{1 - \sqrt 5 }}{2}} \right)
```
```math
\left( {{u_{31}};{u_{32}};{u_{33}}} \right) = \left( {\left| {\begin{array}{*{20}{c}}
{\frac{{ - \sqrt 5  + 3}}{2}}&{\frac{{\sqrt 5  + 3}}{2}}\\
{\frac{{ - \sqrt 5  + 1}}{2}}&{\frac{{\sqrt 5  + 1}}{2}}
\end{array}} \right|; - \left| {\begin{array}{*{20}{c}}
1&{\frac{{\sqrt 5  + 3}}{2}}\\
1&{\frac{{\sqrt 5  + 1}}{2}}
\end{array}} \right|;\left| {\begin{array}{*{20}{c}}
1&{\frac{{ - \sqrt 5  + 3}}{2}}\\
1&{\frac{{ - \sqrt 5  + 1}}{2}}
\end{array}} \right|} \right) = \left( {\sqrt 5 ;1; - 1} \right)
```
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tới đây áp dụng công thức nghịch đảo ma trận vừa nêu, khi đó ta suy ra: 
   
```math
 {P^{ - 1}} = \frac{1}{{\sqrt 5 }}.{\left[ {\begin{array}{*{20}{c}}
{{u_{11}}}&{{u_{12}}}&{{u_{13}}}\\
{{u_{21}}}&{{u_{22}}}&{{u_{23}}}\\
{{u_{31}}}&{{u_{32}}}&{{u_{33}}}
\end{array}} \right]^T} = \frac{1}{{\sqrt 5 }}.{\left[ {\begin{array}{*{20}{c}}
{ - \sqrt 5 }&{\frac{{1 - \sqrt 5 }}{2}}&{\frac{{1 + \sqrt 5 }}{2}}\\
{\sqrt 5 }&{\frac{{ - 1 - \sqrt 5 }}{2}}&{\frac{{ - 1 + \sqrt 5 }}{2}}\\
{\sqrt 5 }&1&{ - 1}
\end{array}} \right]^T} = {\left[ {\begin{array}{*{20}{c}}
{ - 1}&1&1\\
{\frac{{ - 5 + \sqrt 5 }}{{10}}}&{\frac{{ - 5 - \sqrt 5 }}{{10}}}&{\frac{{\sqrt 5 }}{5}}\\
{\frac{{5 + \sqrt 5 }}{{10}}}&{\frac{{ - 5 + \sqrt 5 }}{{10}}}&{ - \frac{{\sqrt 5 }}{5}}
\end{array}} \right]^T}
```
