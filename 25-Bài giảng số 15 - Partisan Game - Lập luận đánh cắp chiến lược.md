# Partisan Game - Lập luận đánh cắp chiến lược
&nbsp;&nbsp;&nbsp;&nbsp;Trong lý thuyết trò chơi kết hợp, lập luận đánh cắp chiến lược là một kiểu lập luận cho thấy, đối với nhiều trò chơi 2 người chơi, người chơi thứ 2 (người đi lượt sau) không thể có chiến lược để thắng. Lập luận đánh cắp chiến lược chỉ áp dụng cho các trò chơi đối xứng (trong đó 2 người chơi có cùng một bộ di chuyển và có cùng giá trị phần thưởng, để người chơi thứ nhất có thể "sử dụng" chiến lược của người chơi thứ 2). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Lập luận hoạt động bằng cách tạo ra một mâu thuẫn. Chiến lược chiến thắng của người chơi thứ 2 được giả định là có tồn tại. Nhưng sau khi người chơi thứ 2 thực hiện nước đi đầu tiên của họ, người chơi đầu tiên cũng có thể chơi theo chiến lược chiến thắng này. Kết quả là cả 2 người chơi đều được đảm bảo để giành chiến thắng - điều này là vô lý, do đó mâu thuẫn với giả định rằng một chiến lược như vậy tồn tại. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta đi đến các ví dụ sau: <br>

#### Ví dụ 1: $m,n,k$ Game 
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/358b432d-a1c4-4015-b76a-03aa890f62c6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Một $m,n,k$ - game là một boardgame khái quát hóa của cờ Caro, trong đó 2 người chơi lần lượt đặt một quân cờ (khác màu hoặc X/O) của họ lên một bảng $m \times n$ , người chiến thắng là người chơi đầu tiên tạo được một hàng liên tục k quân (ngang/dọc/chéo) có màu của riêng mình. Vậy tic-tac-toe là 3,3,3 - game và cờ Caro là 15,15,5 - game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Lập luận đánh cắp chiến lược cho thấy rằng không có $m,n,k$ - game nào có thể có một chiến lược đảm bảo rằng người chơi thứ 2 sẽ thắng. Giả định rằng người chơi thứ 2 có chiến lược để thắng và sử dụng nó. Người chơi đầu tiên thực hiện một nước đi tùy ý để bắt đầu. Sau khi người chơi thứ 2 đi nước tiếp theo, người chơi đầu tiên áp dụng chiến lược chiến thắng của người chơi thứ 2 đối với những nước cờ người chơi thứ 2 vừa đánh. Anh ta có thể làm điều này miễn là chiến lược không yêu cầu đặt 1 quân cờ vào ô 'tùy ý' đã bị sử dụng trong nước đi đầu tiên của chính anh ta. Tuy nhiên, nếu điều này xảy ra, anh ta lại có thể đi một nước cờ tùy ý ở vị trí khác và tiếp tục làm như trước. Vì 1 quân cờ của 1 trong 2 người chơi được thêm vào bất kỳ vị trí nào chỉ có thể làm tăng thêm cơ hội thắng cho người chơi đó, quân cờ tùy ý bổ sung không thể gây hại cho người chơi đầu tiên $\rightarrow$ Đây là một chiến lược chiến thắng cho người chơi đầu tiên $\rightarrow$ Cả 2 người chơi đều thắng. Mâu thuẫn này ngụ ý rằng giả định ban đầu là sai, không thể tồn tại một chiến lược chiến thắng cho người chơi thứ 2. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì vậy một $m,n,k$ - game  khi 2 người chơi đều đi những nước tối ưu thì chỉ có thể có kết quả là chiến thắng cho người đi trước, hoặc hòa. <br>

#### Ví dụ 2: Hex Game
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/fe1224b0-e0a2-40b1-b578-354af8801581)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Là một boardgame chiến lược cho 2 người chơi được chơi trên mạng lưới hình lục giác, về mặt lý thuyết có kích thước bất kỳ và hình dạng tùy ý, nhưng theo truyền thống là hình thoi $11 \times 11$ . Mỗi người chơi có một màu đại diện, theo quy ước là Đỏ/Xanh hoặc Trắng/Đen. Người chơi thay phiên nhau đặt quân cờ/đánh dấu màu của họ lên các ô trống trong bảng. Sau khi được đặt, quân cờ không được di chuyển hoặc xóa khỏi bảng. Mục tiêu của mỗi người chơi là hình thành một đường nối các quân cờ của mình liên kết 2 mặt đối diện của bảng có cùng màu sắc với anh ta, trước khi đối thủ làm điều tương tự. Người chơi đầu tiên hoàn thành kết nối của mình sẽ thắng trò chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hex không thể kết thúc bằng một trận hòa-nghĩa là 2 người chơi đều không còn khả năng tạo đường kết nối. Kết luận này không hề hiển nhiên mà phải được chứng minh chặt chẽ (xem chứng minh ở phần ***<ins>phụ lục 2</ins>***). <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có thể dùng lập luận đánh cắp chiến lược tương tự như ở ví dụ $m,n,k$ - game để chứng minh rằng với lối chơi hoàn hảo, người đi trước luôn thắng: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.	Không có kết quả hòa, do đó phải có chiến lược chiến thắng cho người chơi thứ nhất hoặc thứ 2. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.	Hãy giả định rằng người chơi thứ 2 có một chiến lược chiến thắng.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.	Người chơi đầu tiên thực hiện một động thái tùy ý, sau đó sử dụng chiến lược của người chơi thứ 2 được giả định ở trên. Nếu chiến lược này bắt buộc anh ta phải đánh vào ô nơi thực hiện động thái tùy ý ban đầu, anh ta chỉ cần thực hiện một động thái tùy ý khác. Theo cách này, anh ta đã chơi theo chiến lược chiến thắng và có thêm 1 quân cờ bổ sung trên bảng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.	Quân cờ bổ sung này không thể can thiệp vào việc bắt chước chiến lược chiến thắng của người chơi đầu tiên, vì nó được tính như là tài sản của anh ta. Do đó, người chơi đầu tiên có thể giành chiến thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.	Bởi vì hiện tại đã mâu thuẫn với giả định ban đầu rằng có một chiến lược chiến thắng cho người chơi thứ 2, chúng ta buộc phải bỏ giả định này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.	Do đó, phải có một chiến lược chiến thắng cho người chơi đầu tiên. <br>

#### Ví dụ 3: Chomp Game
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/6e4b7093-ae63-4d2a-ab28-53a839963882)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi chiến lược 2 người chơi được chơi trên một bảng hình chữ nhật tạo thành từ các ô vuông nhỏ hơn, có thể coi là các khối của một thanh chocolate. Người chơi lần lượt chọn một ô và "ăn nó" (xóa khỏi bảng) cùng với các ô nằm bên dưới và bên phải nó. Khối trên cùng bên trái bị "nhiễm độc" và người chơi ăn thứ này sẽ thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với bất kỳ trạng thái bắt đầu bằng hình chữ nhật nào ngoài $1 \times 1$ , người chơi đầu tiên có thể giành chiến thắng. Sử dụng lập luận đánh cắp chiến lược: giả sử người chơi thứ 2 có chiến lược chiến thắng trước bất kỳ nước đi khởi động nào của người chơi thứ nhất. Người chơi đầu tiên chỉ ăn ô vuông góc dưới cùng bên phải. Theo giả định ban đầu, người chơi thứ 2 có nước đi đáp lại dẫn đến chiến thắng cho anh ta. Nhưng nếu một nước đi như vậy tồn tại, người chơi đầu tiên có thể dùng nó như là nước đi đầu tiên của họ và do đó là người chiến thắng (mâu thuẫn) $\rightarrow$ Người chơi thứ 2 không thể có chiến lược chiến thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chomp có thể được mô tả bằng dạng số. Một số tự nhiên ban đầu có dạng $p^{a}q^{b}$ (với $p,q$ là các số nguyên tố) được đưa ra và người chơi thay phiên nhau chọn các ước số dương của số ban đầu, nhưng không được chọn 1 hoặc bội số của một ước số đã bị chọn trước đó. Trò chơi này tương đương với chomp bắt đầu bằng thanh chocolate có kích thước $\( a+1 \) \times \( b+1 \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Số tự nhiên ban đầu có thể là tích của nhiều hơn 2 số nguyên tố. Trò chơi này là mô hình $n$ chiều của chomp, số tự nhiên ban đầu có $n$ thừa số nguyên tố và kích thước của thanh chocolate quyết định bởi số mũ của các số nguyên tố, lập luận đánh cắp chiến lược vẫn còn giá trị. <br>

#### Ví dụ 4: Hệ thống tiền tệ Sylver
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi toán học dành cho 2 người chơi, được phát minh bởi John H. Conway. 2 người chơi lần lượt gọi tên các số nguyên dương $> 1$ không phải là tổng của bội số không âm của các số nguyên được gọi tên trước đó. Người chơi không thể gọi tên như vậy sẽ thua. Chẳng hạn, nếu người chơi A mở đầu bằng 2, B có thể thắng bằng cách gọi 3. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi được đặt theo tên của *Sylvester* - người đã chứng minh rằng nếu $a,b$ là các số nguyên dương nguyên tố cùng nhau, thì $\( a-1\) \( b-1 \) - 1$ là số lớn nhất không phải là tổng của bội số không âm của $a,b$ . Do đó, nếu $a,b$ là 2 nước đi đầu tiên trong trò chơi thì công thức này cho biết số lớn nhất có thể chơi được sau đó. Con số này phải giảm ở những nước đi tiếp theo. Do đó, trò chơi cuối cùng sẽ phải kết thúc. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Không giống như nhiều trò chơi toán học tương tự, Tiền tệ Sylver chưa được giải quyết hoàn toàn, chủ yếu là do nhiều trạng thái có vô số động thái có thể. Định lý Hutchings tuyên bố rằng chọn bất kỳ số nguyên tố nào $≥ 5$ làm nước đi đầu tiên đều dẫn đến chiến thắng, nhưng rất ít thông tin về chiến lược cho các nước đi tiếp theo, đây là những cách mở đầu chiến thắng duy nhất được biết đến. Để hiểu được định lý Hutchings, ta cần biết rõ về định lý Sylvester đã nêu trên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hệ quả của định lý là số lớn nhất không phải là tổng các bội số không âm của $a,b$ (với $a,b$ nguyên tố cùng nhau) là $S=ab-a-b$ , vì bất cứ số $n > S$ nào cũng có $S-n < 0$ với $S-n$ không thể là tổng các bội số không âm của $a,b$ $\rightarrow$ $n$ phải là tổng các bội số không âm của $a,b$ .  <br>

&nbsp;&nbsp;&nbsp;&nbsp;Khi ước số chung lớn nhất của các nước đi được thực hiện cho đến nay là 1, tập hợp các số còn lại có thể chơi sẽ là một tập hợp hữu hạn. Một vài số trong đó cho phép một nước đi đặc biệt gọi là "ender". Một ender là một số chỉ có thể được chơi ngay lập tức, vì chơi bất kỳ số nào khác sẽ loại bỏ ender ra khỏi danh sách những số có thể gọi ở lượt sau. Chẳng hạn, sau khi gọi $\( 4;5 \)$ , số lớn nhất có thể chơi là 11. Chơi 11 không thể loại trừ bất kỳ số nào nhỏ hơn, nhưng chơi bất kỳ số nào nhỏ hơn có sẵn $\\{ 1,2,3,6,7 \\}$ sẽ loại trừ việc chơi 11, vì vậy 11 là một ender. Khi một ender tồn tại, người đi trước có thể giành chiến thắng theo lập luận đánh cắp chiến lược: giả định người đi sau có một chiến lược thắng, nếu người đi trước chọn 11 (ender), người đi sau sẽ có 1 nước đi đối phó lại bằng cách chọn một số trong $\\{ 1,2,3,6,7 \\}$ mà sẽ dẫn tới chiến thắng cho anh ta, nhưng nếu 1 nước đi như thế tồn tại thì người đi trước có thể chọn nó ngay lượt đầu (nước đi này đồng thời cũng loại luôn 11 - ender ra khỏi tập hợp) và giành chiến thắng (mâu thuẫn) $\rightarrow$ giả định ban đầu không thể xảy ra, người đi trước có chiến lược thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta thấy rằng, khi $a,b$ là 2 số đã gọi ( $a,b$ nguyên tố cùng nhau), $S=ab-a-b$ chính là một ender, vì gọi $S$ không thể loại đi bất cứ số nào còn lại trong tập hợp những số có thể gọi ( $S$ là giá trị lớn nhất trong đó), nhưng gọi một số $p < S$ sẽ loại bỏ $S$ ở lượt sau ( $S = p+q$ , với $p$ không phải là tổng bội số không âm của $a,b$ nên $q$ sẽ là dạng đó, $q=xa+yb$ với mọi $x,y \in \mathbb{N}$ $\rightarrow$ $S=p + xa + yb$ $\rightarrow$ $S$ là tổng các bội số không âm của $p,a,b$ ). <br>
Nếu người chơi đầu tiên gọi số nguyên tố $n \ge 5$ , thì người chơi thứ 2 buộc phải gọi $m$ không phải là bội số của $n$ $\rightarrow$ $m,n$ nguyên tố cùng nhau $\rightarrow$ người chơi đầu tiên thắng. <br>

&nbsp;&nbsp;&nbsp;&nbsp;***Trở lại mạch chính của bài viết....*** <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong nhiều tình huống, lập luận đánh cắp chiến lược giúp ta xác định được kết cục của một trò chơi với lối chơi hoàn hảo (2 người chơi đều đi những nước tối ưu nhất cho bản thân), nhưng không cho biết một chiến lược cụ thể dẫn đến kết cục ấy và vì vậy bị coi là "không mang tính xây dựng". Tuy nhiên, lập luận đánh cắp chiến lược có ý nghĩa về mặt lý thuyết, khi người ta quan tâm đến kết quả trò chơi nhiều hơn là quá trình chơi, nhất là ở các trò chơi có số lượng trạng thái lớn hoặc vô hạn, nơi mà việc tìm thấy một chiến lược chiến thắng bằng cách tìm kiếm toàn diện là không thực tế. <br>

#### Phụ lục 1: Người chiến thắng trong misere Hex game
&nbsp;&nbsp;&nbsp;&nbsp;Ở ***ví dụ 2*** ta đã xem qua trò chơi Hex, sự kích thích còn tăng thêm bội phần khi xét phiên bản misere của nó: người chơi hoàn thành đường kết nối giữa 2 biên của mình sẽ thua. Sự đảo ngược luật chơi này làm cho các phân tích trở nên khó khăn hơn để xác định ai trong 2 người chơi thắng. Misere Hex là một trò chơi "chậm" - chỉ kết thúc khi phần lớn các ô trong bảng đã bị chiếm, misere Hex không thể kết thúc bằng trận hòa với lý do tương tự ở normal Hex. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một chứng minh tao nhã sử dụng lập luận đánh cắp chiến lược cho thấy rằng: misere Hex game bắt đầu bằng bảng lục giác $N \times N$ với lối chơi hoàn hảo có chiến thắng thuộc về người chơi đầu tiên với $N$ chẵn và người chơi thứ 2 với $N$ lẻ (\*).  <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Bổ đề:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Người chơi ở thế thua cuộc trong misere Hex game luôn có cách để kéo dài cuộc chơi sao cho tất cả các ô đều bị chiếm trước khi trò chơi kết thúc (trò chơi dừng lại ngay khi đường kết nối được hoàn thành). <nr>
&nbsp;&nbsp;&nbsp;&nbsp;Điều này ngụ ý người điền vào ô cuối cùng lấp đầy bảng là người thua. Dễ thấy chỉ cần chứng minh được bổ đề trên là đồng thời chứng minh được (*), vì tính chẵn lẻ của $N$ quyết định tính chẵn lẻ của số lượng ô trong bảng $N \times N$ , qua đó quyết định ai sẽ là người đi nước cuối cùng. Khi $N$ chẵn, số ô là $N^2$ chẵn $\rightarrow$ Bảng được lấp đầy sau một số chẵn nước đi $\rightarrow$ người chơi thứ 2 thua vì anh ta đi nước cuối cùng; tương tự khi $N$ lẻ thì $N$ lẻ, người chơi đầu tiên thua vì là người đi nước cuối cùng.  <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Gọi $P$ là người chơi có chiến lược để thắng - ký hiệu $L$ , người ở thế thua cuộc là $Q$ , đặt $m(L)$ là giá trị tối thiểu của số ô còn trống sau khi trò chơi kết thúc (xét tất cả những kịch bản mà $P$ sử dụng $L$ , chọn kịch bản mà số ô trống còn lại là ít nhất và lấy giá trị này làm $m(L)$ ). Ta phải chứng minh rằng $m(L) = 0$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh bằng cách giả định $m(L) \ge 1$ , từ đó làm phát sinh một mâu thuẫn. Chứng minh sử dụng tính chất sau: ở trạng thái cuối cùng của game nếu $Q$ là người thắng cuộc, sẽ có một đường kết nối của $P$ đã hoàn thành, khi đó, dù biến đổi trạng thái của bảng bằng cách lấp đầy các ô trống còn lại bởi các quân của $Q$ , hay thay thế một số quân của $Q$ trong bảng thành quân của $P$ thì $Q$ vẫn thắng vì những thay đổi này không hề ảnh hưởng đến đường kết nối của $P$ (#). Giả sử $P$ sử dụng chiến lược $L$ và $m(L) \ge 1$ , xét 2 trường hợp như sau: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* $Q$ là người đi trước, lúc này người đi sau $(P)$ có chiến lược thắng $(L)$ . $Q$ đi nước đầu tiên tùy ý, rồi sử dụng $L$ (đánh cắp chiến lược của $P$ ) để đối phó với những nước cờ của $P$ . Điều này tương đương với việc $Q$ đang chơi ván game $G$ với vai trò của một người đi sau, chỉ khác là có thêm 1 quân cờ bổ sung (là nước cờ tùy ý đầu tiên), nếu trong quá trình chơi $L$ yêu cầu $Q$ phải đánh ở ô này, $Q$ chỉ cần đánh vào 1 ô trống tùy ý khác và vị trí mới này trở thành quân cờ bổ sung. Xét ván game $G'$ chơi song song với $G$ và diễn biến y hệt $G$ , chỉ khác là không có quân cờ bổ sung này, hiển nhiên $Q$ thắng $G'$ do $Q$ là người đi sau và sử dụng $L$ , mặt khác trạng thái bàn cờ của $G$ và $G'$ chỉ khác ở việc ô cờ bổ sung chứa quân của $Q$ trong $G$ lại là ô trống ở $G'$ , nên nếu $Q$ thắng trong $G'$ thì cũng thắng trong $G$ bởi nhận xét (#). Điều kiện $m(L) \ge 1$ làm cho bàn cờ $G$ luôn có ít nhất 1 ô trống khi đến lượt $P$ nên bàn cờ $G'$ luôn có ít nhất 2 ô trống (1 ô trong đó là ô chứa quân cờ bổ sung ở $G$ ) khi đến lượt $P$ , điều này giúp $P$ luôn có nước để đi ở $G'$ mà không cần phải đánh vào ô bổ sung đã bị $Q$ chiếm ở $G$ (nếu $P$ bắt buộc phải đánh vào ô bổ sung này sẽ làm cục diện của $G$ và $G'$ khác nhau hoàn toàn). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* $Q$ là người đi sau, lúc này người đi trước $(P)$ có chiến lược thắng $(L)$ . $P$ đi nước cờ đầu tiên, $Q$ sau đó đánh 1 nước tùy ý và coi đây là nước cờ "bổ sung". Ta đặt ra ván game $G'$ chơi song song với $G$ chỉ khác $G$ ở 2 điểm: ô chứa quân cờ đầu tiên của $P$ ở $G$ lại chứa quân của $Q$ ở $G'$ , ô cờ bổ sung của $Q$ ở $G$ là ô trống ở $G'$ . $P$ đi những nước tiếp theo ở $G$ và làm y hệt ở $G'$ , $Q$ bây giờ chỉ việc sử dụng $L$ ở $G'$ vì anh ta là người đi trước, và $Q$ thực hiện lại những nước đi này ở $G$ , khi $L$ yêu cầu $Q$ phải đánh vào ô bổ sung (đã bị chiếm ở G bởi chính $Q$ ), $Q$ đánh vào ô này ở $G'$ (vẫn còn trống) song song với đánh vào 1 ô trống tùy ý khác ở $G$ và coi đây là quân cờ bổ sung mới. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, mạch trò chơi ở $G$ và $G'$ chỉ có 2 điểm khác nhau duy nhất đã nêu lúc đầu. Hiển nhiên $Q$ thắng $G'$ $\rightarrow$ $Q$ cũng thắng ở $G$ do sự tương ứng giữa trạng thái của $G$ và $G'$ cùng với nhận xét (#). Mặt khác, điều kiện $m(L) \ge 1$ duy trì sự đối ứng giữa $G$ và $G'$ tương tự như ở trường hợp 1. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trong cả 2 trường hợp nêu trên, hệ quả rút ra là $Q$ thắng trong $G$ hoàn toàn mâu thuẫn với giả định ban đầu $P$ là người chiến thắng $\rightarrow$ điều kiện $m(L) \ge 1$ không thể xảy ra do nó làm phát sinh mâu thuẫn $\rightarrow$ $m(L) = 0$ $\Rightarrow$ Chứng minh hoàn tất. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Điểm đặc biệt là lập luận đánh cắp chiến lược được sử dụng ở đây không phải để xác định người chiến thắng, nó thiên về việc cho thấy khi giả định $m(L) \ge 1$ , không có ai thắng cả (vì người này thắng thì người kia cũng thắng), từ đó cho thấy giả định $m(L) \ge 1$ không thể xảy ra vì nó dẫn đến hệ quả phi lý như vậy. <br>

#### Phụ lục 2: : Chứng minh Hex game không thể có kết quả hòa

<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/a54a315c-71d2-4871-8989-da40cb772a5a)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Giản hóa các ô lục giác thành các điểm, 2 ô kề nhau sẽ được mô tả bằng một cạnh nối giữa 2 điểm. Trò chơi trở thành như hình trái, các đường biên được tô màu đỏ (R) và xanh (B). Ta sẽ chỉ ra rằng khi tất cả các điểm đều bị đánh dấu xanh hoặc đỏ, sẽ có [1 đường xanh kết nối 2 biên xanh] hoặc [1 đường đỏ kết nối 2 biên đỏ] được hình thành. Ta sẽ chứng minh điều này đúng với mạng lưới Hex có hình dạng bất kỳ, không nhất thiết là hình thoi như Hex game nguyên bản (hình phải). <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/45138610-7424-44bb-aeaf-512b230da3ea)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Cho một bảng Hex với hình dạng tùy ý (Hình a). Ta sẽ chứng minh kết luận trên đúng với bảng Hex này, theo giả thiết quy nạp rằng nó đúng với tất cả các bảng Hex con được hình thành từ việc cắt bỏ một/nhiều phần của bảng Hex ban đầu (Hình b,c)
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ee074365-2a17-4177-9ee7-66b45d1a31ac)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Gọi lần lượt 2 biên đỏ và 2 biên xanh là $R_{1};R_{2};B_{1};B_{2}$ . Ta lược bỏ 2 lớp điểm nằm sát 2 biên $R_{1};R_{2}$ để tạo 2 biên mới là $R_{1}';R_{2}'$ . Theo giả thiết quy nạp, phải có đường đỏ $r_1$ nối $R_{1} - R_{2}'$ và đường đỏ $r_2$ nối $R_{1}' - R_{2}$ (nếu không thì sẽ có 1 đường xanh nối $B_{1}-B_{2}$ , và ta có luôn đpcm). Gọi $B$ là điểm nằm trên $R_2$ và kề với $B'$ , $C$ là điểm nằm trên $R_1$ và kề với $C'$ $\rightarrow$ hình thành bảng Hex $ACDB$ , theo giả thiết quy nạp, phải có: 1 đường đỏ nối $r_{1}-r_{2}$ (khi ấy sẽ thành đường nối $R_{1}-R_{2}$ tức ta có luôn đpcm) hoặc 1 đường nét đứt $b$ nối $R_{1}-R_{2}$ , đường $b$ chia bảng Hex ban đầu thành 2 bảng con và như vậy phải có các đường xanh nối $B_{1} - b$ và $b - B_{2}$ (nếu không sẽ có 1 đường đỏ nối $R_{1}-R_{2}$ , có luôn đpcm) $\rightarrow$ hình thành đường xanh nối $B_{1} - B_{2}$ , tức ta có đpcm.  <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Vậy ta hoàn tất chứng minh mệnh đề trên. <br>
