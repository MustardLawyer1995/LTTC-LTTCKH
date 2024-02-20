# Sử dụng Lí thuyết Trò chơi kết hợp trong tàn cuộc cờ vua

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giới thiệu:</ins>* Các nhà toán học yêu thích các trò chơi. Chúng khiến họ có thể bận rộn một cách vui vẻ. Ngay cả những trò chơi đơn giản nhất cũng có thể yêu cầu chiến thuật và chiến lược thông minh để giành thắng lợi. Đây là những loại vấn đề hoàn hảo để giải quyết bằng toán học.<br>
&nbsp;&nbsp;&nbsp;&nbsp;Một nhánh của toán học gọi là ***<ins>Lý thuyết trò chơi kết hợp (LTTCKH)</ins>***, đã được phát triển từ khoảng 40 năm trước để phân tích các trò chơi. Nó chia một trò chơi thành nhiều phần nhỏ dễ kiểm tra hơn, sau đó sử dụng một loại đại số đặc biệt để gán các giá trị riêng lẻ cho từng phần rồi tính tổng của chúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặc dù có sức mạnh, LTTCKH chỉ có giá trị đối với các trò chơi thỏa mãn một số điều kiện nhất định. Điều quan trọng nhất là có 2 người chơi, cả 2 đều có thông tin đầy đủ về tất cả trạng thái của trò chơi, không có yếu tố cơ hội (chẳng hạn như lắc xúc xắc hoặc xáo bài) và 2 người chơi thay phiên nhau di chuyển (không bỏ lượt), người đầu tiên không còn nước đi hợp lệ là người thua. Backgammon, Poker, Battleships, Monopoly, Solitaire,..., không thể được LTTCKH xem xét vì chúng không thỏa mãn các tiêu chí này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tất cả các trò chơi kết hợp đều có cùng một bản chất: bạn giành chiến thắng bằng cách đảm bảo rằng mình luôn có khả năng thực hiện nhiều hơn đối thủ ít nhất 1 nước đi. Ví dụ kinh điển của loại trò chơi này là các impartial game và partisan game đã được nhắc tới trong các bài trước: <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong các partisan game, 2 người chơi có các nước đi riêng biệt. Cờ vua là một trò chơi như vậy. Trên thực tế, cờ vua về mặt kỹ thuật nói chung không đủ điều kiện để phân tích bằng LTTCKH. Mặc dù cả 2 người chơi đều có thông tin đầy đủ và không có yếu tố ngẫu nhiên, có những yêu cầu tinh tế hơn để áp dụng LTTCKH. Thường thì người thắng một ván cờ không phải người chơi có nhiều nước cờ nhất, mà là người chơi bắt được Vua của đối phương. LTTCKH hoạt động tốt nhất với các trò chơi mà việc di chuyển thường gây bất lợi. Tuy nhiên trong cờ vua, việc di chuyển gần như luôn có lợi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cờ vua cũng phức tạp hơn nhiều so với các trò chơi như Nim và việc có nhiều động tác dự phòng hơn đối thủ của bạn không đủ để giúp bạn chiến thắng. Hơn nữa, cờ vua có nhiều loại quân cờ (binh chủng) và có những quân cờ rất mạnh, có thể tạo ra ảnh hưởng trên một diện tích rộng lớn, ví dụ: Hậu có thể tấn công tới 18 ô. Kết quả là bàn cờ không thể được chia thành các thành phần độc lập nhau (các trò chơi con). Tuy nhiên, trong giai đoạn cuối, khi hầu hết các quân tầm xa đã bị ăn, bàn cờ có thể bị phân cắt thành nhiều trò chơi con. Bây giờ việc di chuyển có thể không đem lại lợi thế nữa và LTTCKH trở thành một công cụ phân tích hoàn hảo. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có các trạng thái nhất định trong tàn cục mà người chơi đi nước tiếp theo sẽ thua. Chúng giống hệt với các trạng thái có giá trị 0 trong LTTCKH. Trong cờ vua, những trường hợp đặc biệt này được gọi là Zugzwang lẫn nhau . "Zugzwang" là một từ tiếng Đức có nghĩa là "bắt buộc phải di chuyển". Trạng thái Trébuchet hiển thị trong hình1 là một ví dụ điển hình của Zugzwang lẫn nhau. <br>
<div align="center">

Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/4d03e6d0-a678-44ed-9506-c2fb63f69e9a) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/811aae90-5812-403c-8417-d846d67f773b)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Những con Tốt đang chặn bước tiến của nhau nên người chơi phải di chuyển Vua tiếp theo. Tuy nhiên, Trắng không thể đi sang $f4$ , cũng như Đen không thể đến $d5$ , vì Vua sẽ tự đưa mình vào tầm chiếu của kẻ thù. Do đó, người đi trước phải di chuyển Vua ra xa khỏi Tốt của mình, khiến con Tốt này không còn được bảo vệ nữa. Đối thủ sau đó có thể bắt được con Tốt này và đi Tốt của mình lên hàng cuối. Luật chơi cho phép một con Tốt như vậy được thăng cấp lên Hậu, một lợi thế quyết định, đảm bảo một chiến thắng không thể tránh khỏi cho người chơi di chuyển sau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi vậy trạng thái Trébuchet này (hình 1) có giá trị là $0$ theo LTTCKH, vì người đi trước luôn thua. Nếu thêm 1 số phần bổ sung vào, có thể chuyển trò chơi thành trạng thái mờ - người đi trước luôn thắng (hình 2). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ở đây, người đi trước có thể đẩy con Tốt của mình trên cột $a$ về phía trước 1 ô. Tốt của người chơi còn lại bị chặn, không còn lựa chọn nào khác ngoài việc di chuyển Vua. Trong trường hợp này, có 2 thành phần của trò chơi: giá trị của cột $a = \\{ 0|0 \\} = \ast$ (quy ước người chơi Trái là Trắng và người chơi Phải là Đen, về cách tính toán các giá trị này, mời xem lại chuỗi bài viết ***Số siêu thực: bài giảng số 17*** và giá trị của Trébuchet $=0$ . Giá trị của toàn bộ trò chơi do đó là: $\ast + 0 = \ast$ . Sở dĩ thao tác này có thể thực hiện được là vì 2 thành phần: các con tốt ở cột $a$ , và Trébuchet, là 2 thành phần độc lập, các nước đi ở thành phần này không "tác động" tới thành phần kia và ngược lại, nên chúng có thể được coi như 2 trò chơi con riêng biệt. <br>
<div align="center">

Hình 3            | Hình 4
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/6ce301ab-5243-4177-a37a-d7fb12e15e4e) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/0fd80499-fe37-44e6-8ba3-f31771a111a5)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Tuy nhiên, nếu con Tốt trắng được đặt ở $a2$ chứ không phải $a3$ (hình 3), giá trị của cột $a$ sẽ trở nên dương: $\\{ 0,\ast |\ast \\} = \\{ 0|\ast \\} = \uparrow > 0$ . Tốt trắng chưa di chuyển trong trò chơi, vì vậy được phép tiến 1 hoặc 2 ô cho lần di chuyển đầu tiên. Chính sự lựa chọn này mang lại cho Trắng 1 bước đi dự phòng. Nếu Đen đi trước thì Tốt trắng tiến 1 ô, nếu Trắng đi trước thì Tốt trắng tiến 2 ô. Một lần nữa Đen buộc phải phá Trébuchet và vì thế thua. Do đó, Trắng chiến thắng bất kể ai đi trước. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các thế cờ trên vẫn khá đơn giản. ***<ins>Lý thuyết trò chơi kết hợp (LTTCKH)</ins>*** thực sự trở nên hữu ích khi có nhiều con Tốt hơn trên bàn cờ và trò chơi trở nên quá phức tạp để phân tích theo cách thông thường. Ví dụ, hình 4 phát sinh trong 1 ván đấu giữa Schweda và Sika vào năm 1929. Schweda-Trắng, đã đánh giá chính xác đó là một trạng thái chiến thắng cho anh ta. Năm 1960, Euwe đã cho thấy rằng Đen cũng có thể giành chiến thắng nếu đi trước. Nhưng anh ta không thể giải thích rõ ràng tại sao người đi trước luôn giành chiến thắng, mặc dù anh ta là nhà vô địch cờ vua thế giới trong 2 năm và có bằng tiến sĩ toán học. Tuy nhiên, bây giờ ta đã có LTTCKH, việc phân tích rất dễ dàng.<br>
&nbsp;&nbsp;&nbsp;&nbsp;Bí quyết là phân tách trò chơi thành các thành phần độc lập và tính toán giá trị của từng thành phần. 2 Vua và 2 Tốt trên 2 cột $e$ và $f$ bị khóa trong một thế Trébuchet khác, như chúng ta đã biết, nhận giá trị $= 0$ , do đó, 2 trò chơi con còn lại quyết định chiến thắng cuối cùng thuộc về ai. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Giá trị của 2 con Tốt trên cột $h$ khá dễ để tính toán. Nếu đến lượt của Đen, con tốt của Đen có thể tiến lên 1 hoặc 2 ô và đưa cột   về trạng thái mới có giá trị là $0$ hoặc $\ast$ . Nếu Trắng đi trước thì chỉ có thể tiến lên 1 ô và đưa về giá trị $\downarrow$ (có thể nhận ra đây chỉ là đối xứng của hình 3 trên cột $a$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì vậy giá trị của trò chơi con ở cột $h$ là: $\\{ \downarrow|0,\ast \\} = \\{ 0|\downarrow \\} = 2\downarrow + \ast > 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các con Tốt ở $a$ và $b$ thực sự ở trong một trạng thái khá phức tạp, ta không được tách 2 cột thành 2 trò chơi con riêng biệt bởi giữa chúng có ràng buộc - trong một vài tình huống các con Tốt ở 2 cột sẽ có cơ hội ăn lẫn nhau. Các tính toán cụ thể cho biết giá trị của thành phần này $= \uparrow$ (có thể xem chi tiết cách tính ở chú thích hình 4).  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đây là một giá trị dương - Trắng có một lợi thế rất nhỏ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tại hình 4, ta quy ước ký hiệu: $\[ xyzt \]$ là giá trị của thế cờ con trên 2 cột $a,b$ với 2 tốt trắng ở $ax,bz$ và 2 tốt đen ở $ay,bt$ ; $\[ xy \]$ là giá trị của 1 cột có tốt trắng ở hàng $x$ và tốt đen ở hàng $y$ .  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong hình 4, giá trị của trò chơi con trên 2 cột $a,b$ là: <br>

```math
\left[ {2627} \right] = \left\{ {\left[ {2637} \right],\left[ {2647} \right],\left[ {3627} \right],\left[ {4627} \right]{\rm{ }}\space|\space{\rm{ }}\left[ {2527} \right],\left[ {2626} \right],\left[ {2625} \right]} \right\}
```
&nbsp;&nbsp;&nbsp;&nbsp;Có 7 trạng thái mới phái sinh từ $\[ 2627 \]$ . Tương tự, mỗi trong số chúng lại có các trạng thái phái sinh khác. Tuy nhiên, ta không cần phải xem xét tất cả chúng, chỉ cần chú ý đến một số điểm quan trọng: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Tính đối xứng của 2 cột $a,b$ : $\[ xyzt \] = \[ ztxy \]$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Các trạng thái mà 2 cột bị tách ra (không còn gây ảnh hưởng lên nhau được nữa) có thể được định giá trị nhanh bằng cách tính giá trị riêng từng cột rồi cộng vào: $\[ xyzt \] = \[ xy \] + \[ zt \]$ <br>

```math
\left[ {2337} \right] = \left[ {23} \right] + \left[ {37} \right] = 0 + \left( {2 \downarrow  + *} \right) = 2 \downarrow  + *\;;\;\;\left[ {2447} \right] = \left[ {24} \right] + \left[ {47} \right] = * +  \downarrow \;;\;\;\left[ {2446} \right] = \left[ {24} \right] + \left[ {46} \right] = * + * = 0
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Những nước đi khiến cho người thực hiện "thua ngay lập tức" sẽ không bao giờ được sử dụng, vì vậy có thể được lược bỏ khỏi công thức. Ví dụ: tiến tốt 1 ô (nước duy nhất có thể đi) ở $\[ 4536 \]$ tạo điều kiện cho đối thủ ăn con tốt này, tốt của đối thủ sau đó không còn bị cản, có thể đi đến cuối bàn cờ để phong hậu, dẫn tới chiến thắng tất yếu  <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ $\[ 3645 \] = \[ 4536 \] = \\{ \space\space|\space\space \\} = 0 \to \[ 3636 \] = \[ 4527 \] = 0$ do người đi trước luôn thua (người đi sau chỉ cần đi những nước đưa thế cờ về giá trị bằng $0$ ) $\to \[ 3627 \] = 0$ (chứng minh diễn giải tương tự). <br>

&nbsp;&nbsp;&nbsp;&nbsp;























