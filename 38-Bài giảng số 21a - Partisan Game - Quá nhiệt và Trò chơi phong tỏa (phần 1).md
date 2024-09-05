# Partisan Game - Quá nhiệt và Trò chơi phong tỏa (phần 1)
### 1. Tổng quan về trò chơi <br>
&nbsp;&nbsp;&nbsp;&nbsp; ***<ins>"Phong tỏa"</ins>*** là một partisan game với 2 người chơi là Xanh và Đỏ (Xanh thường được quy ước là Trái, và Đỏ là Phải). Chiến trường là một dải ô vuông $n \times 1$ (dải đất), mỗi người chơi khi đến lượt sẽ "xác nhận quyền sở hữu" bằng cách tô màu vào 1 ô (lô đất) trống mà mình chọn. Trò chơi kết thúc khi tất cả các ô đã bị tô màu, số điểm của Trái (Xanh) sẽ là số lượng "cạnh" hình vuông mà được tô màu xanh ở cả 2 phía. Mục đích của Trái là cố gắng tối đa hóa số lượng này, còn Phải cố gắng giảm nó xuống thấp nhất có thể. Như vậy, chỉ có các cặp ô vuông liền kề Trái-Trái (xanh-xanh) mới được tính điểm, các cặp Trái-Phải (xanh-đỏ) và Phải-Phải (đỏ-đỏ) đều không ảnh hưởng đến kết quả, không có điểm số cho người chơi Phải. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi là một phép ẩn dụ về hành vi "phong tỏa" trong kinh doanh bất động sản ngoài đời thực: 2 người chơi là 2 đại lý bất động sản đối địch nhau đang thu mua hết các lô đất trên một con phố, Trái theo chủ nghĩa phân biệt chủng tộc, cố gắng sắp đặt để các khách hàng tương lai của mình là hàng xóm của nhau, còn Phải là người theo chủ nghĩa hợp chủng, cố gắng chia tách họ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đây là một loại trò chơi đặc biệt, 2 người chơi có vai trò khác nhau và không có khái niệm thắng-thua. Lời giải tổng quát của trò chơi phải có khả năng xác định trước kết cục trận đấu (số điểm mà Trái đạt được) khi 2 người chơi đều đi những nước tối ưu, và cho biết những nước đi tối ưu ấy là gì. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi Trái luôn cố tăng tối đa điểm của mình còn Phải luôn cố giảm tối thiểu điểm của Trái, có thể áp dụng cấu trúc giá trị của một trò chơi kết hợp vào "Phong tỏa" (tại ***<ins>Bài giảng số 20</ins>*** cung cấp một cách hiểu về việc chuyển đổi từ trò chơi tính điểm sang trò chơi kết hợp), giá trị trò chơi khi kết thúc chính là số điểm của Trái. Gọi giá trị của 1 dải đất $n$ ô trống là: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnL$ nếu nó bị chặn 2 đầu bởi 2 ô xanh. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnR$ nếu 1 đầu xanh và 1 đầu đỏ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$RnR$ nếu 2 đầu đều là ô đỏ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dễ thấy: $LnR$ và $RnL$ là đối xứng của nhau nên có ý nghĩa như nhau; trường hợp dải đất có (1 hoặc 2) đầu tự do (không bị chặn bởi ô màu nào cả) tương đương với việc đầu tự do bị chặn bởi 1 ô đỏ, vì ô đỏ ở đó không ảnh hưởng đến điểm số. Mỗi dải đất là 1 trò chơi con, vì thực hiện 1 nước đi ở dải đất này không phụ thuộc hoặc ảnh hưởng đến dải đất khác $\rightarrow$ giá trị của trò chơi = tổng giá trị của các dải đất cấu thành trò chơi. <br>  
#### &nbsp;&nbsp;&nbsp;&nbsp;Ví dụ: 
<div align="center">

![image](https://github.com/user-attachments/assets/2c60d693-84b0-43be-a8c2-c5274b146f11)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ta quy ước đánh dấu $L$ (Trái-xanh) và $R$ (Phải-đỏ) để phân biệt. Trong hình trên mô phỏng 5 dải đất: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	a) $L5R$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	b) $R3R$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	c) Cũng là $R3R$ , dễ thấy 2 cạnh ngoài cùng ở 2 đầu không thể tạo ra điểm số dù bạn tô màu gì vào ô vuông của chúng (chúng sẽ chỉ có màu ở 1 bên), vì vậy nên dải đất này hoàn toàn tương đương với dải đất ở b). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	d) Trái tô màu xanh vào giữa dải đất $R10R$ và làm nó bị tách thành 2 dải đất $L3R$ và $L6R$ (2 đầu tự do có thể gắn thêm 1 ô đỏ, đã giải thích ở trên). Giá trị của trò chơi này là $L3R+L6R$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	e) Dải đất gọi là $L0L$ , thật ra nó chỉ là 1 cạnh giữa 2 ô xanh, nhưng cần lưu ý rằng nó có giá trị là 1 (được tính 1 điểm theo luật chơi). Các dải $L0R$ và $R0R$ có thể bỏ qua được vì chúng đều bằng $0$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Theo luật chơi, 3 dãy $LnL$ , $LnR$ và $RnR$ được xác định bằng hồi quy như sau: Với $k$ từ $0$ đến $n-1$ , ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$L0L = 1,L0R = R0R = 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnL =\\{ LkL + L \( n-1-k \)L|LkR + L\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$LnR =\\{ LkL + L \( n-1-k \)R|LkR + R\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	$RnR =\\{ LkR + L \( n-1-k \)R|RkR + R\( n-1-k \)R \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các giá trị này phần lớn ở dạng phi số và rất cồng kềnh, chỉ riêng việc tính ra chúng (dựa vào các công thức hồi quy trên) cũng đủ nặng nề chứ chưa nói đến chuyện đem cộng chúng lại với nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Vậy phải giải quyết vấn đề này như thế nào đây ? <br>

### 2. Toán tử quá nhiệt <br>


