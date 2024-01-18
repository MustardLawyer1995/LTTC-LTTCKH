# Sheep Game
- <ins>Không gian giới hạn của trò chơi:</ins> Cánh đồng có kích thước $n \times 1$ gồm các ô vuông thành phần có kích thước $1 \times 1$
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
- Khi ấy ta có hệ phương trình tổng quát tương ứng là: 
```math
\left\{ \begin{array}{l}
{a_{n + 1}} = 2{b_n} - {a_n}\\
{b_{n + 1}} = 2{c_n} - {b_n}\\
{c_{n + 1}} =  - 2{a_n} + 4{b_n} - {c_n}
\end{array} \right.,\forall n = \overline {0,1,2,...}
```
- Tiếp đến ta chuyển về hệ ma trận như sau; Với ${X_{x + 1}} = M{X_n}$ ta có hệ ma trận tương ứng là: 
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
<br>Kế tiếp ta sẽ tìm lũy thừa bậc $n$ của ma trận $M$ bằng phương pháp chéo hóa ma trận.</br>
<br>Trước hết ta điểm từng bước như sau:</br>
<ul style="list-style-type: none;">
   <li><ins>Bước 1:</ins> Giá trị riêng của $\lambda$ : ta có: $\left( {A - \lambda I} \right)v = 0$ khi và chỉ khi $\det \left( {A - \lambda I} \right) = 0$ </li>
   <li><ins>Bước 2:</ins> Nhắc lại sơ về khái niệm nghịch thế</li>
   <ul style="list-style-type: none;">
     <br>Cho tập  $S = \\{ 1;2;3;...;n \\}$ với $n!$ hoán vị.</br>
     <br>Xét các hoán vị $\\{ j_{1};j_{2};...;j_{n} \\}$ nghịch thế là cặp ${j_a} > {j_b}$ với $a < b$ </br>
     <br>Diễn đạt thay thế: phần tử đứng trước luôn “lắn” hơn phần tử đứng sau.</br>
     <br>Ví dụ: $(3,1,2)$ có nghịch thế lần lượt là $(3;1)$ và $(3;2)$ </br> 
     <br>Kí hiệu nghịch thế: $N = \\{ j_{1},j_{2},...,j_{n} \\}$ là một số nghịch thế.</br>
   </ul> 
   <li><ins>Bước 3:</ins> Tính định thức ma trận $M$ và các giá trị riêng</li>
   <ul style="list-style-type: none;">
     <br>Ta có định nghĩa định thức như sau: ${\det A - |A| - \sum {{{\left( { - 1} \right)}^{ \\{ {j_1};{j_2};...;{j_n} \\} }}{a_{1{j_1}}}{a_{2{j_2}.....}}{a_{n{j_n}}}} }$</br>
     <br>Trong đó: $\\{ j_{1};j_{2};...;j_{n} \\}$ là các hoán vị của $\\{ 1;2;3;...;n \\}$ đã nêu khái niệm ở trên.</br>
     <br>Khi đó, ta có được:</br>
     <br>
     <code> 
 $\det \left( {\left( {A - \lambda I} \right)} \right) - \left[ {\begin{array}{*{20}{c}}
{ - 1 - \lambda }&2&0\\
0&{ - 1 - \lambda }&2\\
{ - 2}&4&{ - 1 - \lambda }
\end{array}} \right] = \left\{ {\begin{array}{*{20}{c}}
{\left( {{a_{11}}{a_{22}}{a_{33}} + {a_{12}}{a_{23}}{a_{31}} + {a_{13}}{a_{21}}{a_{32}}} \right) - }\\
{\left( {{a_{11}}{a_{23}}{a_{32}} + {a_{12}}{a_{21}}{a_{33}} + {a_{13}}{a_{22}}{a_{31}}} \right)}
\end{array}} \right\}$
     <code>
     </br>
     <li>
 
     </li>      
$$
 =  - {\lambda ^3} - 3{\lambda ^2} + 5\lambda  - 1 + \left( {\lambda  - 1\,} \right)\left( {{\lambda ^2} + 4\lambda  - 1} \right) = 0 \Leftrightarrow \left[ \begin{array}{l}
{\lambda _1} = 1;\\
{\lambda _2} =  - \sqrt 5  - 2
\end{array} \right.;{\lambda _3} = \sqrt 5  - 2
$$
     </li>

   - *Nhận xét:* với ba giá trị riêng trên thì ma trận $3 \times 3$ này có thể giải bằng cách chéo hóa
   </ul>
    
     - <ins>Bước 4:</ins> Chéo hóa ma trận (dùng để tìm lũy thừa tổng quát bậc $n$)
       - Trước hết ta kí hiệu chéo hóa ma trận dưới dạng đại số thuần túy là $A = PD{P^{ - 1}}$$ .
       - Trong đó $D$ là ma trận đường chéo nên với lũy thừa $D$ chỉ cần lũy thừa các phần tử ở <ins>đường chéo</ins> .
       - Khi ấy ta cần chứng minh đánh giá sau: ${A^n} = {\left( {PD{P^{ - 1}}} \right)^n} = P{D^n}{P^{ - 1}}$
       - Thật vậy, giả sử tồn tại $k$ sao cho ${A^k} = {\left( {PD{P^{ - 1}}} \right)^k} = P{D^k}{P^{ - 1}}$
       - Khi đó, tại $k+1$ , ta có: ${\left( {PD{P^{ - 1}}} \right)^{k + 1}} = {\left( {PD{P^{ - 1}}} \right)^k}PD{P^{ - 1}} = P{D^k}{P^{ - 1}}PD{P^{ - 1}}$
    - Lại có với ma trận nghịch đảo thì ${P^{ - 1}}P = I$ nên $P{D^k}{P^{ - 1}}PD{P^{ - 1}} = P.{D^k}.I.D.{P^{ - 1}} = P.{D^k}.D.{P^{ - 1}} = P.{D^{k + 1}}.{P^{ - 1}}$ (đúng với nguyên lí quy nạp) .
     - <ins>Bước 5:</ins> Với mỗi $\lambda$ tính được, ta sẽ tìm được trị số vector riêng tương ứng (tìm $P$ và $D$)
       - <ins>*Trường hợp 1:*</ins> với $\lambda _{1} = 1$ , ta có:
```math
\left[ {\begin{array}{*{20}{c}}
{ - 2}&2&0&|& {{\rm{     }}0}\\
0&{ - 2}&2&|& {{\rm{    }}0}\\
{ - 2}&4&{ - 2}&|& {{\rm{    }}0}
\end{array}} \right]  
```
*Sử dụng phương pháp khử Gauss, ta suy ra:*
```math
\left[ {\begin{array}{*{20}{c}}
{ - 2}&2&0&|& {{\rm{     }}0}\\
0&{ - 2}&2&|& {{\rm{    }}0}\\
{ - 2}&4&{ - 2}&|& {{\rm{    }}0}
\end{array}} \right]{\rm{  }}\begin{array}{*{20}{c}}
{/2}\\
{/2}\\
{/2 - {R_1}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[ {\begin{array}{*{20}{c}}
{ - 1}&1&0&|& {{\rm{    }}0}\\
0&{ - 1}&1&|& {{\rm{    }}0}\\
0&1&{ - 1}&|& {{\rm{    }}0}
\end{array}} \right]{\rm{     +   }}\begin{array}{*{20}{c}}
{ + {R_2}}\\
{}\\
{ - 2{R_2}}
\end{array}{\rm{  }} \sim {\rm{  }}\left[ {\begin{array}{*{20}{c}}
{ - 1}&0&1&|& {{\rm{    }}0}\\
0&{ - 1}&1&|& {{\rm{    }}0}\\
0&0&0&|& {{\rm{    }}0}
\end{array}} \right]     
```
*Sau khi quy về ma trận bậc thang ta có hệ sau:*
```math
\left\{ \begin{array}{l}
 - {x_1} + {x_3} = 0\\
 - {x_2} + {x_3} = 0
\end{array} \right. \Leftrightarrow \left\{ \begin{array}{l}
{x_1} = {x_3}\\
{x_2} = {x_3}
\end{array} \right.
```
</l>
   
