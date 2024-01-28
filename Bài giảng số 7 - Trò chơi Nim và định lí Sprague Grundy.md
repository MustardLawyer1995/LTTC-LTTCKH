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

#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bản chất tiện ích* <br>


































