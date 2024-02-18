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
&nbsp;&nbsp;&nbsp;&nbsp;Theo ***3.4b***, ta có: $-3 < \\{ \\{ 5|-3 \\}|0 \\} \Leftrightarrow 3 + \\{ \\{ 5|-3 \\}|0 \\} > 0$ , $\\{ \space\space|-2 \\} = -3 \rightarrow \\{ \\{ 5|-3 \\}|0 \\} = \\{ \space\space|0 \\} = -1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\\{ \uparrow|\downarrow \\} = \ast \Leftrightarrow \\{ \uparrow|\downarrow \\} + \ast = 0$ , mặt khác $\uparrow = \\{ 0|\ast \\}$ , $\\{ 0|0 \\} = \ast$ $\rightarrow$ $\\{ \uparrow|\downarrow \\} = \\{ 0|\downarrow \\}$ ***(3.4b)*** $\rightarrow$ $\\{ \uparrow|0 \\} = \ast$ ***(0.1b)*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Ta có: $\uparrow = \\{ 0|\ast \\} ; \ast = \\{ 0|0 \\} < \uparrow + \ast \rightarrow \\{ \uparrow,\ast|0 \\} = \\{ 0,\ast|0 \\}$ (theo ***3.4b***) và $0 < \uparrow$ (theo ***3.4a***) <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $\uparrow + \ast = \\{ 0|\ast \\} + \\{ 0|0 \\} = \\{ \uparrow,\ast|0,\uparrow \\} = \\{ \uparrow,\ast|0 \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Ta có: $2\uparrow > \ast$ (theo ***3.2 và 3.4a***) nên: $\uparrow + \ast = \\{ 0|\ast \\} + \\{ \uparrow|\downarrow \\} = \\{ 2\uparrow,\ast|0 \\} = \\{ 2\uparrow|0 \\}$ $\rightarrow$ $\\{ 0,\ast|0 \\} = \\{ 2\uparrow|0 \\} = \uparrow + \ast$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một giá trị $G$ được viết dưới dạng $\\{GL|GR \\}$ mà không thể rút gọn bởi các ***quy tắc 3.4a và 3.4b*** nữa thì $\\{GL|GR \\}$ được gọi là dạng hợp quy của $G$ . Ví dụ: $\uparrow + \ast = \\{ 2\uparrow|0 \\}$ không phải là dạng hợp quy vì: $2\uparrow = \\{ \uparrow|\uparrow + \ast \\},\uparrow + \ast = \\{ \ast,\uparrow|\space\space \\} = \\{ 2\uparrow|0 \\}$ $\rightarrow$ theo ***3.4b***, có thể rút gọn $\\{ 2\uparrow|0 \\} = \\{ \ast,\uparrow|0 \\}$ và $\\{ \ast,\uparrow|0 \\}$ có thể tiếp tục rút gọn về $\\{ \ast,0|0 \\}$ (theo ***3.4c***). $\\{ \ast,0|0 \\}$ là dạng hợp quy của $\uparrow + \ast$ vì nó không thể rút gọn hơn được nữa. $2 = \\{ 1|3 \\}$ không phải dạng hợp quy vì: $3 = \\{ 2|\space\space \\} = 2 = \\{ 1|\space\space \\} = \\{ 1|3 \\}$ $\rightarrow$ (theo ***3.4b***), có thể rút gọn $\\{ 1|3 \\} = \\{ 1|\space\space \\}$ với $\\{ 1|\space\space \\}$ là dạng hợp quy của 2 vì nó không thể được rút gọn thêm nữa. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lí 3.5:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Mỗi giá trị chỉ có duy nhất một dạng hợp quy tương ứng. 

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 3.5:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại 2 dạng hợp quy khác nhau là $G$ và $H$ của cùng một giá trị $\( G = H \)$ . Không mất tính tổng quát, giả thiết cho $G$ và $H$ khác nhau ở bộ giá trị $GL$ và $HL$ $\rightarrow$ $\exists GL_{1} \in GL , \exists GL_1{1} \notin HL$. Xét trò chơi $G - H = 0$ , Trái sẽ thua nếu đi trước dù đi bất cứ nước nào. Nếu Trái đưa trò chơi về $GL_{1} - H$ , Phải sẽ có 1 nước đi chiến thắng tiếp theo (tức là đưa giá trị trò chơi về $\le 0$ ), nước đi này không nằm ở $GL_{1}$ , vì $\nexists GL_{1}R: GL_{1}R - H \le 0$ ( $\nexists GL_{1}R \le G = H$ , do $G$ đã ở dạng hợp quy) $\rightarrow$ nước đi chiến thắng nằm ở $-H$ $\rightarrow$ $\exists HL_{1}:GL_{1} - HL_{1} \le 0$ $\Leftrightarrow$ $GL_{1} < L_{1}$ (dấu bằng không xảy ra vì $GL_{1} \notin HL$ ) $\rightarrow$ $HL_{1} \notin GL$ (vì $G$ là dạng hợp quy) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thực hiện lập luận theo cách tương tự cho trò chơi $H - G = 0$ với nước đi đầu của Trái là đưa $H \to HL_{1}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ $\exists GL_{2} > HL_{1} \rightarrow GL_{2} > HL_{1} > GL_{1}$ $\rightarrow$ $\exists GL_{1};GL_{2} \in GL:  GL_{1} < GL_{2}$ mâu thuẫn với giả định ban đầu rằng $G$ và $H$ đều là dạng hợp quy $\rightarrow$ không tồn tại 2 dạng hợp quy khác nhau cho cùng 1 giá trị <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 3.5*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Hệ quả:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;1 giá trị có thể được viết ở nhiều dạng khác nhau nhưng các quá trình rút gọn của ***3.4a, 3.4b*** sẽ tối giản tất cả chúng về 1 dạng thức duy nhất - dạng hợp quy, và nó đặc trưng cho mỗi giá trị. Dạng hợp quy của các số chính là các định nghĩa ở ***(1.1),(2.1), mục 4/***, dễ thấy rằng chúng không thể rút gọn được nữa. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Theo ví dụ ở ***3.3***, $\\{ \\{ 0|\uparrow \\}|1 + \ast \\} = 1$ , bởi $\uparrow = \\{ 0|\ast \\} < 1$ nên $\\{ \\{ 0|\uparrow \\}|1 + \ast \\} = \\{ 0|1 + \ast \\}$ (theo ***3.4b***), bởi $1 + \ast = \\{ 1...|... \\},1 = \\{ 0|\space\space \\} = \\{ 0|1 + \ast \\}$ nên $\\{ 0|1 + \ast \\} = \\{ 0|\space\space \\}$ (theo ***3.4b***). <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Ví dụ 4.1:</ins>***
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/c0108178-2be8-4def-9dfe-8d924944fd41)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Về trò chơi có thành phần vô hạn. Giá trị của cây hackenbush (xanh-đỏ-xanh-đỏ-xanh-đỏ-...) có thể viết thành:  

```math
1 - \frac{1}{2} + \frac{1}{{{2^2}}} - \frac{1}{{{2^3}}} + \frac{1}{{{2^4}}} - \frac{1}{{{2^5}}} + ... = \frac{1}{2} + \frac{1}{{{2^3}}} + \frac{1}{{{2^5}}} + \frac{1}{{{2^7}}} + ... = \frac{1}{{2\left( {1 - {\raise0.5ex\hbox{$\scriptstyle 1$}
\kern-0.1em/\kern-0.15em
\lower0.25ex\hbox{$\scriptstyle 4$}}} \right)}} = \frac{2}{3}
```
&nbsp;&nbsp;&nbsp;&nbsp;Như vậy giá trị của toàn bộ trò chơi là: $\frac{2}{3} \times 3 + \( -1 \) \times 2 = 0$ tức Người đi trước thua. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Ví dụ 4.2:</ins>*** Trò chơi Cóc và Ếch
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* trò chơi được chơi trên dải hình vuông $1 \times n$ . Tại 1 thời điểm, mỗi ô vuông hoặc trống hoặc bị chiếm bởi một con cóc hay ếch. Mặc dù trò chơi có thể bắt đầu ở bất kỳ thế sắp đặt nào, nhưng theo thông lệ, thường bắt đầu với những con cóc chiếm các ô vuông liên tiếp ở phía ngoài cùng trái và ếch chiếm các ô vuông liên tiếp ở phía ngoài cùng phải. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đến lượt của mình, Trái có thể di chuyển 1 con cóc sang ô vuông trống bên phải nó. Nếu 1 con ếch đã chiếm ô này và ô bên phải con ếch đó trống, Trái có thể đưa con cóc vào khoảng trống đó; 1 động thái như vậy gọi là "nhảy". Con cóc không thể nhảy qua nhiều con ếch, cũng không được phép nhảy qua con cóc khác. Các quy tắc tương tự áp dụng cho Phải: trong 1 lượt, anh ta có thể di chuyển 1 con ếch sang ô trống lân cận bên trái hoặc nhảy qua 1 con cóc vào ô trống bên trái con cóc. Người chơi không thể di chuyển trong lượt của mình bị thua. <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/6e400aaf-b8b4-450c-b835-bcaef005cf56)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Các trạng thái trò chơi thường được thể hiện bằng 1 chuỗi gồm ba ký tự: T cho 1 con cóc, F cho 1 con ếch, và   cho 1 ô trống (như hình trên). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Phân tích: Hình trên là tập hợp tất cả các trạng thái có thể xảy ra trong trò chơi đã được tính sẵn, ta chỉ cần dùng lại. Bởi vì định giá trị cho các trạng thái trò chơi là 1 việc dễ dàng nhưng tương đối nhàm chán (bạn đọc đã được làm quen ở những bài trước). Ta chỉ điểm qua rất nhanh những thao tác này để nhuần nhuyễn chúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Việc định giá trị bao giờ cũng được thực hiện từ điểm kết thúc trò chơi đi ngược lên trạng thái bắt đầu (trừ những trò chơi đã khám phá ra công thức giá trị tổng quát). Điểm kết thúc là những trạng thái mà cả 2 người chơi đều không còn nước đi, theo quy ước chúng nhận giá trị là 
















