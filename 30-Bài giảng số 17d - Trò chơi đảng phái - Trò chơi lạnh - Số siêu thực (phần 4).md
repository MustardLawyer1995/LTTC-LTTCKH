# Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 4)
### 6.	Các giá trị trong trò chơi nóng 
&nbsp;&nbsp;&nbsp;&nbsp;Vì tính tổng quát, ta sẽ xét những trò chơi chứa cả các thành phần nóng và lạnh. Điều này nghĩa là trong trò chơi vẫn có sự hiện diện của số siêu thực. Ta chấp nhận toàn bộ ***tiên đề (0.1) ở mục 4/***, nhưng bổ sung thêm 1 trạng thái đặc biệt: $G \parallel 0$ , người chơi đi trước sẽ thắng, vì $G$ không $< 0, > 0$ hay $=0$ , ta nói rằng $G$ không thể so sánh với 0 ( $G$ còn được gọi là giá trị "mờ"). $G \parallel H$ ( $G$ không thể so sánh với $H$ ) $\Leftrightarrow G - H \parallel 0$ , mệnh đề này là hiển nhiên vì nếu giữa $G,H$ có 1 trong 3 mối quan hệ $<,>,=$ thì giữa $G - H$ và 0 cũng có mối quan hệ tương tự và ngược lại. Giờ đây, giữa 2 giá trị bất kỳ, có 4 mối quan hệ có thể xảy ra: $<,>,=, \parallel$ . Với $a \parallel b$ và $b \parallel c$ , không nhất thiết phải có $a \parallel c$ ( $\parallel$ không có tính chất bắc cầu). Nhưng với $a \le b$ và $b < \parallel c$ (tức $b < c$ hoặc $b \parallel c$ ), có thể kết luận $a < \parallel c$ , chứng minh: nếu $a \ge c$ thì $b \ge a \ge c$ $\rightarrow$ (mâu thuẫn với $b < \parallel c$ ) $\rightarrow$ $a < \parallel c$ . Tương tự, $a \ge b$ và $b \parallel > c$ $\rightarrow$ $a \parallel > c$ . Điều này dự báo sự xuất hiện của những giá trị không phải là số trong trò chơi, bởi nếu tất cả đều là số thì sao lại có mối quan hệ $\parallel$ (không thể so sánh) được? <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ký hiệu $\\{ L|R \\}$ vẫn được sử dụng theo cách cũ, nhưng trò chơi tổng quát chứa cả những giá trị $\\{ L|R \\}$ với $L \ge R$ , nên không thể được biểu diễn bằng một số. Những giá trị không thể biểu diễn bằng số trong trò chơi được gọi chung là phi số. Ở ***tiên đề (0.2) ở 4/*** cần điều chỉnh lại một chút để áp dụng được cho cả số và phi số. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy ước 3.1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Gọi $GL$ là 1 nước đi khả dụng của Trái trong trò chơi $G$ (và $GR$ là của Phải), xét trò chơi $G + \( -G \) = 0$ , bởi ***tiên đề (0.1)*** nên ai đi trước sẽ thua, nếu Trái đưa $G$ về $GL$ thì trạng thái tiếp theo là $GL + \( -G \) < \parallel 0$ (Phải đi trước và thắng) $\Leftrightarrow GL < \parallel 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tương tự: $GR > \parallel G$ $\Rightarrow$ $GL < \parallel G < \parallel GR$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một vài giá trị phi số sẽ có quy ước riêng, nhưng phần lớn chúng được viết ở dạng $G = \\{ GL|GR \\} ; H = \\{ HL|HR \\} ; ...$ vì ta không thể đặt ký hiệu cho tất cả. Các giá trị phi số không có trật tự rõ ràng và đẹp như các giá trị số. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy ước 3.2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Kí hiệu $\\{ 0|0 \\} = \ast$ (star),  $\\{ 0|\ast \\} =\space\uparrow$ (up), $\\{ \ast|0 \\} =\space\downarrow$ (down). Từ đó ta thu được một số nhận xét sau từ ***(0.1),(0.1b)*** và từ định nghĩa của chúng, như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\* + \* = 0 \Leftrightarrow \* = - \*$ , $\uparrow + \downarrow = 0 \Leftrightarrow \uparrow = - \downarrow$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Vì $\uparrow - \ast = \uparrow + \ast \parallel 0$ nên $\ast \parallel 0$ và $\uparrow \parallel \ast$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\forall n \in \mathbb{R}^{+} , -n < \ast < n$ và $-n < \downarrow < 0 < \uparrow < n$ điều thú vị là $\ast$ nhỏ hơn mọi số thực dương và lớn hơn mọi số thực âm, nhưng $\ast \ne 0$ , $\ast$ và 0 là 2 giá trị không thể so sánh như đã nói; $\uparrow$ nằm giữa 0 và mọi số thực dương nhưng lại không phải là số, $\ast$ và $\uparrow$ thậm chí không phải là các số vô cùng bé vì chúng nhỏ hơn cả các số vô cùng bé: $\varepsilon + \ast > 0$ , $\varepsilon + \downarrow > 0$ vì người chơi Trái luôn thắng (kiểm tra xem). $\Leftrightarrow \varepsilon > \ast$ và $\varepsilon > \uparrow$ , ngay cả khi thay $\varepsilon \rightarrow \frac{\varepsilon}{2}$ hay $\varepsilon \rightarrow 2\varepsilon$ thì kết quả vẫn như vậy (các số vô cùng bé vẫn được coi là "số"). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\ast < \uparrow + \uparrow = 2 \uparrow$ $\rightarrow$ $0 < 2 \uparrow + \ast < n$ (với $n \in \mathbb{R}$ ) <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 3.3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Cho $G = \\{ GL|GR \\} ; g = \\{ a|b \\}$ , nếu $a \le GL < \parallel g < \parallel GR \le b$ thì $G = g$ (chứng minh tương tự với ***2.3 mục 4/***) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Hệ quả:</ins>* Có thể tính giá trị $G$ bất kỳ bằng cách chọn ra $g$ là số đơn giản nhất thỏa mãn $GL < \parallel g < \parallel GR$ . Theo đó ***Định lý (2.3)*** đã được mở rộng để áp dụng cho cả các giá trị phi số. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* 

```math
\left\{ { \downarrow | \uparrow } \right\} = \left\{ { \downarrow |*} \right\} = \left\{ {*| \uparrow } \right\} = \left\{ {*|*} \right\} = \left\{ {*|\space\space{\rm{ }}} \right\} = \left\{ \space\space{{\rm{ }}|*} \right\} = \left\{ \space\space{{\rm{ }}| \uparrow } \right\} = \left\{ { \downarrow |\space\space{\rm{ }}} \right\} = 0,\left\{ { \uparrow |\space\space{\rm{ }}} \right\} = \left\{ {* + \frac{1}{2} \bigg\vert \space\space{\rm{ }}} \right\} = \left\{ {\left\{ {0| \uparrow } \right\}|1 + *} \right\} = 1
```
```math
\left\{ { \uparrow |1} \right\} = \left\{ {* + \frac{1}{2} \bigg\vert 1} \right\} = 1/2,{\rm{ }}\left\{ {2 \uparrow  \bigg\vert \frac{1}{2} +  \downarrow } \right\} = \left\{ {2 \uparrow  + * \bigg\vert \frac{1}{4} +  \uparrow } \right\} = \frac{1}{4},{\rm{ }}...
```
&nbsp;&nbsp;&nbsp;&nbsp;Ngược lại, khi không có số $g$ nào thỏa mãn $GL < \parallel g < \parallel GR$ thì có thể kết luận $\\{ GL|GR \\}$ không phải là số (thật ra điều này là hiển nhiên bởi ***(quy ước 3.1)***). <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Mệnh đề 3.4a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $A \le B$ thì $\\{ A,B,C... | R \\} = \\{ B,C... | R \\}$ và $\\{ L | A,B,C... \\} = \\{ L | A,C... \\}$

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh mệnh đề 3.4a:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét trò chơi $\\{ A,B,C... | R \\} - \\{ B,C... | R \\} = \\{ A,B,C... | R \\} = \\{ -R | -B,-C... \\}$ . Nếu Trái đi trước chọn $A$ , Phải chỉ cần chọn $B$ và trò chơi trở thành $A - B \le 0$ , Trái thua. Nếu người đi trước chọn bất kỳ nước nào ngoài $A$ , người còn lại chỉ cần chọn nước đi trái dấu và đưa trò chơi về 0, người đi trước thua.<br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $\\{ A,B,C... | R \\} - \\{ B,C... | R \\} =0$ $\Leftrightarrow$ $\\{ A,B,C... | R \\} = \\{ B,C... | R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Thực hiện chứng minh tương tự với ý còn lại <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***mệnh đề 3.4a*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Mệnh đề 3.4b:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Cho $G = \\{ A,B,C...|GR \\}$ , nếu $\exists AL \le G,AR = \\{ ARL|... \\}$ thì $G = \\{ ARL,B,C...|GR \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cho $H = \\{ GL|A,B,C... \\}$ , nếu $\exists AL \ge G,AR = \\{ ...|ARL \\}$ thì $H = \\{ GL|ALR,B,C... \\}$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh mệnh đề 3.4b:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét trò chơi $G - \\{ ARL,B,C...|GR \\} = \\{ A,B,C...|GR \\} + \\{ -GR|-ARL,-B,-C... \\}$ . Nếu Phải đi trước chọn $-ARL$ , trò chơi trở thành $G - ARL \parallel > 0$ ( $ARL < \parallel AR \le G \rightarrow ARL < \parallel G$ ) $\rightarrow$ Trái thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu Trái đi trước chọn $A$ , Phải đưa $A$ về $AR$ , trò chơi trở thành $AR + \\{ -GR|-ARL,-B,-C... \\}$ , Trái không thể chọn $-GR$ vì $AR - GR < \parallel 0$ ( $AR \le G < \parallel GR$ ) , nếu Trái chuyển $AR$ về $ARL$ thì Phải chọn $-ARL$ , trò chơi về 0, Trái Thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu nước đi bắt đầu $\ne A,-ARL$ , người đi sau chọn nước đi trái dấu và thắng <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $G - \\{ ARL,B,C...|GR \\} = 0$ $\Leftrightarrow$ $G = \\{ ARL,B,C...|GR \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Thực hiện chứng minh tương tự với ý còn lại <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***mệnh đề 3.4b*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Ví dụ 3.4c:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Theo ***3.4b***, ta có: <br>

```math
 - 3 < \left\{ {\left\{ {5| - 3} \right\}|0} \right\}{\rm{ }}\left( {3 + \left\{ {\left\{ {5| - 3} \right\}|0} \right\} > 0} \right), - 3 = \left\{ {{\rm{ }}| - 2} \right\} \to \left\{ {\left\{ {5| - 3} \right\}|0} \right\} = \left\{ {{\rm{ }}|0} \right\} =  - 1
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Theo ***0.1b***, ta có:

```math
\left\{ { \uparrow | \downarrow } \right\} = *{\rm{ }}\left( {\left\{ { \uparrow | \downarrow } \right\} + * = 0} \right)
```















