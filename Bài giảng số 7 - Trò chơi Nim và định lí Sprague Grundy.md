# Trò chơi Nim và định lí Sprague Grundy 
### 1. Trò chơi Nim<br>
&nbsp;&nbsp;&nbsp;&nbsp;Nim là một trò chơi có 2 người chơi, thực hiện nước đi theo lượt. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* Có một số lượng các vật thể (hòn đá/que diêm/đồng xu/...)-tạm gọi là "quân", được xếp thành nhiều đống khác nhau. Ở mỗi lượt, người chơi phải lấy ít nhất 1 quân và có thể lấy bất kỳ số lượng nào miễn là tất cả các quân bị lấy đều trong cùng một đống. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nim thường được chơi theo luật *misère*, trong đó người chơi lấy quân cuối cùng sẽ thua. Nim cũng có thể được chơi theo luật "normal", trong đó người chơi lấy quân cuối cùng sẽ thắng. Đây được gọi là cách chơi "normal" bởi vì nước đi cuối là nước thắng trong hầu hết các trò chơi, mặc dù đó không phải là cách mà Nim thường được chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các biến thể của Nim đã được chơi từ thời cổ đại. Trò chơi này được cho là bắt nguồn từ Trung Quốc, rất giống với trò chơi 捡石子 (kiểm thạch tử/nhặt đá) của Trung Quốc. các tài liệu tham khảo sớm nhất ở châu Âu về Nim là từ đầu thế kỷ 16. Tên hiện tại của nó được đặt ra bởi Charles L. Bouton của Đại học Harvard , người cũng đã phát triển lý thuyết hoàn chỉnh của trò chơi vào năm 1901, nhưng nguồn gốc của cái tên không bao giờ được giải thích đầy đủ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Phiên bản mặc định của Nim game (người nào lấy được quân cuối cùng thì thắng) tồn tại một chiến lược tất thắng, đó là phép cộng chuỗi nhị phân theo xor, được định nghĩa như sau: để tính $a \text{   xor   } b$ , chuyển $a$ và $b$ về dạng nhị phân, sau đó viết chúng theo 2 hàng và tính tổng xor mỗi hàng theo quy tắc: $0 \text{  } xor \text{  } 1 =1; 0 \text{  } xor \text{  } 0 = 1 \text{  } xor \text{  } 1 =0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* Cho $a = 26 = 11010,{\rm{ }}b = 9 = 1001$ , khi đó ta có: <br> 
<div align="center">

![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/221f44d2-1bd7-462f-9413-6ba9e62c5fea)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Với phép cộng xor nhiều hơn 2 số, ta có thể làm theo quy tắc tương tự, ở mỗi hàng dọc, nếu số lượng số 1 là một số lẻ thì kết quả hàng đó bằng 1, nếu là một số chẵn thì kết quả hàng đó bằng 0. Điều này đến từ việc phép cộng xor cũng có tính chất giao hoán và kết hợp như cộng thường:  $a \text{   xor   } b = b \text{   xor   } a; \( a \text{   xor   } b \) \text{   xor   } c = a \text{   xor   } \( b \text{   xor   } c \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi trò chơi ở một trạng thái gồm các đống có số lượng quân lần lượt là ${a_1},{a_2},{a_3},...$  và cần tính tổng $a_{1} \text{   xor   } a_{2} \text{   xor   } a_{3} ...$ . Nếu kết quả bằng 0, người đang đi trước ở thế thua, nếu khác 0, người đang đi trước ở thế thắng (thế thắng/thua được hiểu là kết quả trò chơi khi 2 người chơi đều đi những nước tối ưu nhất). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ở trường hợp tổng xor khác 0, người đi trước chỉ cần đi một nước nào đó sao cho tổng xor về 0. Dễ thấy đây chính là chiến lược chắc chắn dẫn đến chiến thắng cho anh ta: Nếu tổng xor đang bằng 0, một nước đi bất kỳ luôn làm nó khác 0 ở lượt tiếp theo (vì người chơi chỉ được phép tác động vào 1 đống); nếu tổng xor đang khác 0, luôn tồn tại ít nhất 1 nước đi để nó bằng 0 ở lượt kế. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Điều này nghĩa là người đi trước với tổng xor khác 0 sẽ luôn rơi vào các trạng thái có tổng khác 0, và đối thủ của anh ta luôn bị đưa vào các trạng thái có tổng bằng 0 $\rightarrow$ Anh ta không thể thua (một người chơi chỉ thua khi không còn quân để đi ở lượt của mình, tức là khi tổng xor bằng 0), mặt khác trò chơi luôn kết thúc với 1 người thắng và 1 người thua $\rightarrow$ đối thủ của anh ta không thể thoát khỏi thất bại dù chơi theo bất kì cách nào. <br>

### 2. Lý thuyết trò chơi ứng dụng - Trò chơi Nim <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dù luật chơi đơn giản nhưng Nim đã trở thành nguồn cảm hứng để các nhà toán học xây dựng nên ***<ins>Lý thuyết trò chơi kết hợp</ins>*** - một nhánh của Toán học ứng dụng (tránh nhầm với ***<ins>"Lý thuyết trò chơi"</ins>***), chuyên nghiên cứu về các trò chơi đối kháng giữa 2 người chơi, đi luân phiên theo từng lượt, kết thúc sau hữu hạn lượt đi (khi 1 trong 2 người không còn nước để đi), có thông tin hoàn hảo và đầy đủ (2 người chơi đều quan sát được toàn bộ nước đi của đối phương và biết rõ các thông tin chung của cuộc chơi), không có yếu tố may rủi - gọi chung là *"trò chơi kết hợp"* , đại diện của loại trò chơi này là: cờ vua, cờ vây, cờ caro, nim, domino,... <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong đó những trò chơi như Nim thuộc về một lớp trò chơi kết hợp gọi là ***<ins>impartial game</ins>*** (trò chơi không thiên vị), với đặc điểm: Tất cả những nước đi được phép thực hiện ở mỗi lượt là như nhau với cả 2 người chơi. Nói cách khác, sự khác biệt duy nhất giữa 2 người chơi chỉ là ai đi trước. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi không phải là *impartial* được gọi ***<ins>partisan game</ins>*** (trò chơi đảng phái), trò chơi dạng này tồn tại những nước đi mà chỉ 1 trong 2 người chơi được thực hiện. Ví dụ như các loại cờ, nơi mà mỗi người chơi chỉ được phép di chuyển những quân cờ của bên mình. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có 2 khái niệm quan trọng trong Lý thuyết trò chơi kết hợp là "trò chơi tương đương" và "tổng của các trò chơi": <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Xét trò chơi $A'$ được tạo ra từ việc thêm vào trò chơi $A$ những "động thái khả đảo" - là những nước đi mà sau khi thực hiện có thể bị đối phương "undo" (ctrl+Z) bằng 1 nước đi đảo ngược, dễ thấy những động thái khả đảo này không hề làm thay đổi mạch của trò chơi. Vì vậy $A’$ được coi là tương đương với $A$ . Cũng không cần lo về chuyện 2 người chơi sẽ lặp đi lặp lại thao tác đó khiến trò chơi không thể kết thúc, vì nếu điều đó xảy ra, nó đã vi phạm định nghĩa của trò chơi kết hợp rồi. Ta ngầm hiểu rằng có một giới hạn nhất định cho số lần "undo" ở mỗi trạng thái. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Cho $H_1$ và $H_2$ là các trò chơi kết hợp, ta có trò chơi $H_{1}+H_{2}$ được hình thành theo quy tắc sau: $H_1$ và $H_2$ được chơi cùng lúc giữa 2 người nhưng ở mỗi lượt, người chơi thực hiện duy nhất 1 nước đi trong $H_1$ hoặc $H_2$ , trò chơi kết thúc khi một người chơi không còn nước đi trong cả $H_1$ và $H_2$ ở lượt của mình $\rightarrow$ cũng là một trò chơi kết hợp, nó được gọi là tổng của 2 trò chơi  $H_1$ và $H_2$ , hay "trò chơi tổng", còn $H_1$ và $H_2$ là các "trò chơi con" bên trong $H_{1}+H_{2}$ . Ví dụ dễ thấy nhất: trò chơi Nim nhiều đống là tổng của các trò chơi Nim 1 đống, mỗi đống nim là 1 trò chơi con. (đọc đến đây chắc các bạn đọc đã hiểu nguồn gốc của cái tên ***"trò chơi kết hợp"*** rồi) <br>

### 3. Định lí Sprague Grundy <br>
&nbsp;&nbsp;&nbsp;&nbsp;Quy tắc đơn giản của trò chơi Nim ở ***mục 1/*** là nền tảng cho ***<ins>định lý Sprague Grundy</ins>***: Mỗi impartial game chơi theo luật normal luôn tương đương với một nim game. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta đặt ra một loại giá trị đại diện cho mỗi trạng thái của trò chơi gọi là nimber (còn có tên khác là số Grundy). Nimber của trạng thái $h$ , ký hiệu là $G(h)$ , được định nghĩa bằng đệ quy: $G\(h\)=0$  nếu người chơi trước tại $h$ thua ngay lập tức *(không có nước đi tiếp theo tại* $h$ *)* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $G\( h\) = \text{ Mex } \\{ g\( h_{1} \) ; g\( h_{2} \) ; g\( h_{3} \) ; ... g\( h_{n} \) \\}$ với $h_{1},h_{2},...h_{n}$ là tất cả các trạng thái trò chơi có thể xảy ra sau nước đi tiếp theo (Mex của một tập hợp là số tự nhiên nhỏ nhất ngoài tập hợp đó: $\text{Mex} \( A \) = \text{Min} \( \mathbb{N} \backslash A \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dễ thấy nếu $G(N)$ là nimber tương ứng của nim game gồm 1 đống $N$ quân thì $G(N)=N$ . Mặt khác, theo định nghĩa nimber, $\forall n < G\( h \) \ne 0 , \( {n \in \mathbb{N} } \)$ , luôn có nước đi để đưa trò chơi từ trạng thái $h$ về trạng thái $h'$ sao cho $G\(h'\)=n$ $\rightarrow$ Nếu bạn đưa trò chơi từ trạng thái $H$ về $H'$ sao cho $G\(H'\) > G\(H\)$ , đối phương sẽ luôn có nước đi để nimber trở về mức $G(H)$ $\rightarrow$ Những nước đi làm tăng nimber chính là những động thái khả đảo $\rightarrow$ trò chơi $H$ tương đương với 1 đống nim có $G(H)$ quân. ***(đpcm)*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nim game gồm 2 đống nim với số lượng $a,b$ sẽ có nimber đại diện là $a \oplus b$ (tổng nimber): 

```math
a \oplus b{\rm{ }} = \text{Mex  }\left( {\left\{ {a' \oplus b|a' < a\}  \cup \{ a \oplus b'|b' < b} \right\}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Công thức này (được suy ra trực tiếp từ định nghĩa của nimber) ngụ ý rằng nước đi tiếp theo chỉ có thể tác động vào 1 trong 2 đống nim. Ta có định lý sau: Đối với mọi impartial game chơi theo luật normal, ta có tính chất sau: $a \oplus b = a \text{   xor   }b$   <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta đặt $c = a \oplus b$ , theo định lí Sprague Grundy, 2 đống nim có số lượng $a,b$ tương đương với 1 đống nim số lượng $c$ $\rightarrow$ nim game gồm 3 đống có số lượng $a,b,c$ tương đương với nim game gồm 2 đống đều có số lượng <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Nim game này đang ở thế thua cho người đi trước, theo chiến lược tất thắng ở ***mục 1/***, phải có: <br>
```math
a \text{   xor   } b \text{   xor   } c = 0  \Leftrightarrow a \text{   xor   }b = c
```
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Từ đó ta có điều phải chứng minh. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Cách chứng minh khác:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét giá trị $k < a \text{   xor   } b$ ta thấy: $a \text{   xor   } \( a \text{   xor   } k \) = k$ và $b \text{   xor   } \( b \text{   xor   } k \) = k$ (*) , có thể chứng minh rằng ít nhất 1 trong 2 trường hợp sau đây xảy ra: $a \text{   xor   } k < b \vee b \text{   xor   } k < a$ (**) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thật vậy, ta giả sử $a \text{   xor   } k \ge b$ và $b \text{   xor   } k \ge a$ . Ở dạng nhị phân, số chữ số của $k$ phải $\le$ của $a$ hoặc $b$ (do ta xét $k < a \text{   xor   } b$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1- Riêng trường hợp số chữ số của $a$ $>$ của $b$ thì số chữ số của $k$ bằng của $a$ (do $b \text{   xor   } k \ge a$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Từ đó ta rút ra được dạng các số $a,k,b$ như sau: <br>
<div align="center">

$a = 1\left( 0 \right)x\left( {...} \right)......{\rm{      }}$ <br>
$k = 1\left( 0 \right)y\left( {...} \right)......{\rm{      }}$ <br>
$b = 0\left( 0 \right)0\left( 0 \right)1......{\rm{      }}$    <br>
(hãy chú ý các chữ số được dóng thẳng hàng dọc, những chỗ $(0)$ là 1 đoạn các số 0) <br>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $a \text{   xor   } k >b$ thì $\( x,y \) = \( 1,0 \)$ hoặc $\( 0,1 \)$ , nhưng nếu $\( 1,0 \)$ thì vi phạm $b \text{   xor   } k \ge a$ và nếu $\( 0,1 \)$ thì vi phạm $k < a \text{   xor   } b$ $\rightarrow$ Mâu thuẫn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $a \text{   xor   } k =b$ thì $a \text{   xor   } b =k$ $\rightarrow$ điều này vi phạm $k < a \text{   xor   } b$ $\rightarrow$ Mâu thuẫn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2- Trường hợp $a,k,b$ có số chữ số bằng nhau, thì khi ấy ta rút ra được dạng các số $a,k,b$ như sau: <br>
<div align="center">

$a = 1\left( 0 \right)x\left( {...} \right)......{\rm{      }}$ <br>
$k = 0\left( 0 \right)0\left( 0 \right)1......{\rm{      }}$    <br>
$b = 1\left( 0 \right)y\left( {...} \right)......{\rm{     }}$  <br>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Suy ra $\( x,y \) = \( 1,0 \)$ hoặc $\( 0,1 \)$ thỏa mãn $k < a \text{   xor   } b$ . Dễ thấy nếu  $\( 1,0 \)$ thì vi phạm $b \text{   xor   } k \ge a$ và nếu $\( 0,1 \)$ thì vi phạm $a \text{   xor   } k \ge b$ $\rightarrow$ Mâu thuẫn<br>

&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Từ 2 trường hợp trên ta nhận thấy rằng hai điều kiện $a \text{   xor   } k \ge b$ và $b \text{   xor   } k \ge a$ không thể đồng thời thỏa mãn được thỏa mãn $\longrightarrow$ Kết luận (**) là chính xác <br> 

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Quy nạp:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta giả sử $A \oplus B = A \text{   xor   }B$ đúng với $A < a,B \le b$ và $A \le a,B < b$ . Theo định nghĩa của $a \oplus b$ , ta có: <br>

```math
a \oplus b{\rm{ }} = \text{Mex} \left( {\left\{ {a' \oplus b|a' < a\}  \cup \{ a \oplus b'|b' < b} \right\}} \right){\rm{ }} \Rightarrow {\rm{ }}a \oplus b{\rm{ }} = \text{Mex} \left( {\left\{ {a' {\rm{ }} \text{   xor   } {\rm{ }}b|a'  < a} \right\} \cup \left\{ {a{\rm{ }} \text{   xor   } {\rm{ }}b' |b'  < b} \right\}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;, với mỗi giá trị $k < a \text{   xor   } b$ , theo (*) và (**) ta luôn thấy: <br>
```math
k \subset \left( {\left\{ {a' {\rm{ }} \text{   xor   }{\rm{ }}b|a'  < a} \right\} \cup \left\{ {a{\rm{ }} \text{   xor   } {\rm{ }}b' |b'  < b} \right\}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;, mặt khác, $a \text{   xor   }b$ không thể nằm trong tập hợp này (trừ khi $a'=a$ và $b'=b$ - điều này là vô lí) $\rightarrow$ khi ấy suy ra Mex của tập hợp này bằng $a \oplus b$ (theo định nghĩa về Mex) <br>
```math
\longrightarrow a \oplus b{\rm{ }} = \text{Mex} \left( {\left\{ {a' {\rm{ }} \text{   xor   }{\rm{ }}b|a'  < a} \right\} \cup \left\{ {a{\rm{ }} \text{   xor   } {\rm{ }}b' |b'  < b} \right\}} \right) = a{\rm{ }} \text{   xor   } {\rm{ }}b
```
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ $A \oplus B = A \text{   xor   }B$ vẫn đúng khi $A=a, B=b$ <br>
&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Định lý đã được chứng minh bằng quy nạp*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Điều này có nghĩa là tổng nimber có thể được tính toán thông qua tổng xor - một thao tác đơn giản hơn nhiều. Ý nghĩa của định lý Sprague Grundy bây giờ đã rõ ràng. Với một normal impartial game: $H = {H_1} + {H_2} + {H_3} + ... + {H_n}$ , nếu mỗi trò chơi con $H_i$ tương đương với 1 đống nim có $G\( H_{i} \)$ quân thì hiển nhiên $H$ tương đương với một nim game gồm các đống nim có số lượng lần lượt là $G\( H_{1} \),G\( H_{2} \),G\( H_{3} \),...G\( H_{n} \)$ . Vì vậy, quy luật chiến thắng của $H$ , cũng giống như quy luật chiến thắng của nim game, đó là: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) Tính các giá trị $G\( H_{i} \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) Tính $G(H) = G\( H_{1} \) \oplus G\( H_{2} \) \oplus G\( H_{3} \) \oplus ... \oplus G\( H_{n} \) = G\( H_{1} \) \text{   xor   } G\( H_{2} \) \text{   xor   } G\( H_{3} \) \text{   xor   }...\text{   xor   } G\( H_{n} \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•3) Nếu $G(H)=0$ , người đi trước ở thế thua. Nếu $G(H) \ne 0$ , anh ta đang ở thế thắng, lúc này chỉ cần chọn nước đi để đưa $H$ về $H'$ , sao cho $G\( H' \)=0$ , và cứ lặp lại các thao tác này cho đến khi đối thủ không còn nước để đi (thua). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Hãy cùng xem qua các ví dụ về việc vận dụng định lý này cho các impartial game chơi theo luật normal. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.1:</ins>* Trò chơi Nim thông thường<br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/d2adf3bc-83cf-4266-842e-8339242b9b8f)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.2:</ins>* Hình ảnh mô phỏng trò chơi loại trừ <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/e6a9d3ef-7fc1-494e-b7b9-12a273261e87)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mô phỏng:</ins>* Có 1 đống vật thể, mỗi người chơi khi đến lượt sẽ phải lấy ít nhất 1 quân từ đó, và được lấy nhiều nhất $k$ quân, ai lấy quân cuối cùng thì thua. Đây là dạng trò chơi mà các bạn có lẽ đã gặp rồi, nhưng thường ở dạng đếm số (bắt đầu từ 1 số lớn và đếm lùi dần, ai bị ép phải đếm "0" thì thua). Game này hay chơi theo luật misére, nhưng để có thể sử dụng định lý Sprague Grundy, ta buộc phải xét theo luật chơi normal (người lấy được quân cuối cùng thắng), còn trường hợp của các trò chơi theo phiên bản misére sẽ được xét sau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giả sử $k=3$ . Ta tính nimber $G(N)$ tương ứng với 1 đống $N$ quân: $G(0)=0$ (người đi trước thua vì không còn quân để lấy thêm), khi đó ta lần lượt có: <br>
<div align="center">

$G\( 1 \) = \text{Mex} \\{ G\( 0 \) \\} = 1$ <br>
$G\( 2 \) = \text{Mex} \\{  G\( 1 \), G\( 0 \) \\} = 2$ <br>
$G\( 3 \) = \text{Mex} \\{ G\( 2 \), G\( 1 \) , G\( 0 \) \\} = 3$ <br>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nhưng có 1 ngoại lệ khi $N=4$ , do chỉ được phép lấy tối đa $3$ quân nên: $G\( 4 \) = \text{Mex} \\{ G\( 3 \), G\( 2 \) , G\( 1 \) \\} = 0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chu kỳ tiếp diễn: $G \( 5 \) = \text{Mex} \\{ G \( 4 \), G \( 3 \) , G \( 2 \) \\} = 1 ; G \( 6 \) = 2 ; G \( 7 \) = 3 ; ...$ khi đó ta tổng quát được $G\( x \) = x \text{   mod   } 4$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dễ chứng minh rằng với giá trị $k$ bất kỳ, thì: $G\( x \) = x \text{   mod   } \( k + 1 \)$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* Thật vậy, nếu trò chơi bắt đầu với 1 đống có $N = \( k+1 \)m$  quân (với $G(N)=0$ ), thì người đi trước không thể tránh khỏi thất bại, khi anh ta lấy $s$ quân, người đi sau chỉ cần lấy $k+1-s$ quân để đưa số quân còn lại về bội số của $k+1$ , cứ tiếp diễn như vậy và anh ta sẽ lấy được quân cuối cùng <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở rộng:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vậy khi có nhiều hơn 1 đống thì sao? Trò chơi lúc này sẽ giống một nim game nhưng số quân tối đa được phép lấy từ 1 đống chỉ là $k$, chứ không phải bất kỳ số nào như Nim thường. Lúc này chỉ cần tính nimber của từng đống rồi tính tổng xor của chúng, lấy tổng này làm nimber chung của cả trò chơi, rồi cứ làm theo quy tắc đã biết: Nếu bạn đang đi trước, và nimber $= 0$ , bạn ở thế thua, hãy đi bừa 1 nước và cầu cho người kia không biết chiến lược tất thắng này; nếu nimber khác 0, đánh 1 nước sao cho nimber $= 0$ ở lượt tiếp theo, cứ như vậy cho đến khi bạn lấy được quân cuối cùng và thắng. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.3:</ins>* Hình ảnh mô phỏng Grundy Games<br>


































