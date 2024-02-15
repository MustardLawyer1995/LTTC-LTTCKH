# Trò chơi đảng phái - Trò chơi lạnh - Số siêu thực (phần 1)
### 1. Trò chơi đảng phái
&nbsp;&nbsp;&nbsp;&nbsp;Là một nửa còn lại của Lý thuyết trò chơi kết hợp bên cạnh nhánh ***<ins>trò chơi không thiên vị (impartial game)</ins>***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi là trò chơi đảng phái (partisan game) nếu nó không phải là impartial game. Nghĩa là, có một số nước đi mà chỉ 1 trong 2 người chơi được quyền thực hiện. Hầu hết các trò chơi trong thực tế là partisan game. Ví dụ, trong cờ vua, chỉ 1 trong 2 người chơi có thể di chuyển các quân cờ trắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Sức mạnh của Lý thuyết trò chơi kết hợp dựa trên thao tác "chia nhỏ" một trò chơi ra thành nhiều phần (các trò chơi con) độc lập với nhau, cùng với việc tính toán các giá trị đặc trưng của chúng. Điều này vẫn đúng với partisan game, cần nhớ rằng ***định lý Sprague Grundy*** không áp dụng được ở đây, nên ta cần phát triển một loại công cụ khác để phân tích những trò chơi này. Với impartial game, giá trị của một trò chơi là nimber, vậy với các partisan game, hệ thống giá trị sẽ là gì? Một trong số đó là ***<ins>Số siêu thực.</ins>*** <br>
### 2. Trò chơi nóng và lạnh 
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi nóng là 1 trò chơi trong đó mỗi người chơi có thể làm tăng cơ hội thắng của mình khi thực hiện 1 nước đi. Ngược lại, trong trò chơi lạnh, mỗi người chơi sẽ càng làm tình trạng của mình bất lợi hơn nếu thực hiện 1 nước đi bất kỳ. Ví dụ: hãy xem xét 1 trò chơi trong đó 2 người chơi luân phiên loại bỏ các tấm thẻ có màu của riêng họ khỏi bảng, người chơi Xanh chỉ xóa thẻ xanh và người chơi Đỏ chỉ xóa thẻ đỏ, người chiến thắng là người thực hiện nước đi cuối cùng. Rõ ràng, chiến thắng sẽ thuộc về người chơi có nhiều thẻ hơn hoặc người chơi sau nếu số lượng thẻ đỏ và xanh bằng nhau. Việc xóa thẻ màu của chính mình sẽ khiến tình trạng của người chơi tệ hơn, vì người chơi đó sẽ có ít thẻ hơn trên bàn. Do đó, mỗi thẻ đại diện cho một thành phần "lạnh" của trò chơi. Bây giờ hãy thêm vào 1 thẻ màu tím đặc biệt có số "100", có thể bị xóa bởi cả 2 người chơi, người xóa sau đó được thưởng 100 thẻ màu của riêng họ. Thẻ tím là 1 thành phần "nóng", bởi vì người chơi xóa thẻ tím sẽ có lợi. Nếu có bất kỳ thẻ màu tím nào trên bàn, người chơi sẽ thích xóa chúng trước và để các thẻ màu đỏ hoặc xanh đến cuối cùng. Nói chung, người chơi luôn thích thực hiện nước đi trong 1 trò chơi nóng hơn là 1 trò chơi lạnh, bởi vì mỗi động thái trong trò chơi nóng sẽ cải thiện lợi thế của họ, trong khi mỗi động thái trong trò chơi lạnh chỉ gây tổn hại cho họ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trên thực tế, các trò chơi thường không thuần nóng hay lạnh mà là hỗn hợp của 2 thành phần như ví dụ trên, nhưng nếu ta bỏ luật thẻ tím, nó sẽ chỉ còn là 1 trò chơi lạnh. Các trò chơi lạnh rất có ý nghĩa nền tảng, bởi vì chúng mở đường cho khái niệm về số siêu thực. Một trò chơi lạnh luôn nhận các giá trị là số (siêu thực), 1 trò chơi nóng nhận các giá trị không phải là số (các ký hiệu), và 1 trò chơi hỗn hợp nóng lạnh sử dụng cả 2 loại giá trị này.  <br>
### 3. Hackenbush 2 màu 
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Hackenbush 2 màu</ins>*** là phiên bản partisan của game Hackenbush cổ điển-vốn là 1 impartial game. Luật chơi của Hackenbush 2 màu về cơ bản giống Hackenbush cổ điển (sẽ được nêu ở 1 bài giảng riêng), chỉ có 1 điểm khác biệt: mỗi đoạn thẳng đều thuộc 1 trong 2 màu (Xanh/Đỏ), người chơi chỉ được phép xóa các đoạn thẳng cùng màu với mình. Đây là 1 trò chơi lạnh, bất cứ khi nào người chơi xóa 1 cạnh, tình huống luôn trở nên tồi tệ hơn với anh ta vì giờ anh ta có ít lựa chọn hơn cho những nước đi tiếp theo. Để hiểu được lời giải của trò chơi, ta sẽ đi từ những suy diễn thô sơ nhất khi xem xét 1 số trường hợp đặc biệt như sau: <br>
<div align="center">

Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/5a2f129b-fe6c-4810-b1c5-9cb5ba6c50b3) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/e712de9d-6151-4cca-828b-3090b1c96ed3)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu trò chơi cấu thành từ 2 phần riêng biệt, một bên chỉ gồm những cạnh xanh, một bên chỉ gồm những cạnh đỏ, khi đó việc xóa 1 cạnh xanh sẽ không ảnh hưởng gì tới các cạnh đỏ và ngược lại. Như những gì đã nói về trò chơi lạnh, người chơi chắc chắn sẽ ưu tiên xóa những cạnh trên cùng của mô hình sao cho mỗi nước đi chỉ làm mất 1 cạnh, bởi vì mất càng nhiều cạnh đồng nghĩa với càng nhiều bất lợi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy nên phân tích tình huống này rất đơn giản:<br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy tắc 1:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Coi số lượng cạnh xanh là một số dương, số lượng cạnh đỏ là một số âm, cộng 2 số này vào để có giá trị $G$ , là giá trị đại diện của trò chơi, khi đó: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $G > 0$ thì người chơi Xanh luôn thắng <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $G < 0$ thì người chơi Đỏ luôn thắng <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $G = 0$ thì người chơi trước thua, không quan trọng màu gì (xem hình 1) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét</ins>*: Quy tắc (#1) vẫn đúng khi trò chơi có nhiều cây hơn, có thể coi mỗi cây như 1 trò chơi con vì chúng độc lập hoàn toàn với những cây khác và mỗi nước đi chỉ có thể gây ảnh hưởng tới 1 cây. Điều này rất tương đồng với khái niệm "một trò chơi là tổng của nhiều trò chơi con" trong lý thuyết về impartial game nên thật hợp lý nếu giá trị của toàn bộ trò chơi = tổng các giá trị của từng trò chơi con. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giá trị của trò chơi ở hình: $G = 3 + 1 + 3 - 2 - 3 = 2 > 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Người chơi Xanh thắng (xem hình 2) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở rộng</ins>*:Giờ sẽ ra sao nếu "áp đặt" 3 quy tắc thành phần ở (#1) cho bất kỳ trạng thái nào của trò chơi? Nó dẫn đến nhiều hệ quả thú vị sau đây... <br>
<div align="center">

Hình 3            | Hình 4
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/0b57b909-0f3b-4b66-bcd0-b1acce397640) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/97dc478e-1f60-4f3f-b540-a13fbe877df6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp; (Hình 3) Nếu 1 cây gồm cả 2 màu, giá trị của nó không thể tính theo cách vừa rồi vì rõ ràng giữa các cạnh xanh và cạnh đỏ có mối liên hệ ràng buộc. Xóa 1 cạnh xanh có thể làm mất luôn 1 cạnh đỏ đồng thời và ngược lại. Ví dụ như cây thẳng gồm 2 đoạn từ dưới lên là xanh - đỏ (hình trên), giá trị của nó sẽ là gì? Tạm gọi giá trị của nó là $x$ . Trò chơi trên hình gồm 3 cây trong đó có 2 cây với giá trị $x$ và 1 cây giá trị $-1$ $\rightarrow$ Trò chơi này có $G = x + x - 1$ . Khi 2 người chơi đều sử dụng những nước tối ưu, người đi trước luôn thua dù anh ta là Xanh hay Đỏ $\rightarrow$ theo (#1) ta suy ra: $G = x + x - 1 = 0 \Leftrightarrow x = \frac{1}{2}$ $\rightarrow$ Thật bất ngờ khi 1 trạng thái lại có thể nhận giá trị là phân số. <br>
&nbsp;&nbsp;&nbsp;&nbsp; (Hình 4) Nếu trò chơi gồm 2 mô hình có hình dạng giống nhau nhưng vị trí các màu đảo ngược lại hoàn toàn, những cạnh ở hình bên này màu xanh thì ở bên kia màu đỏ và ngược lại, thì người đi sau luôn thắng bằng chiến lược đối xứng. Bất kể người đi trước xóa 1 cạnh ở hình nào, người đi sau chỉ cần xóa cạnh tương ứng ở hình còn lại, hệ quả là 2 mô hình sẽ luôn giống nhau khi đến lượt người đi trước và người đi sau sẽ luôn là người đi nước cuối cùng kết thúc trò chơi. Theo quy tắc (#1), trò chơi phải nhận giá trị $G = 0$ , cho nên nếu 1 trong 2 mô hình có giá trị $g$ , thì mô hình còn lại phải là $-g$ . (Xem #1.a) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy tắc 2:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Quy tắc sau đây có thể cho biết giá trị chính xác của 1 mẫu hình. Cho mẫu hình $v$ có giá trị $G(v)$ , giả sử từ $v$ phe Xanh có nước đi tới các trạng thái khác nhận giá trị lần lượt là $L_{1};L_{2};...;L_{n}$ , còn phe Đỏ có nước đi tới $R_{1};R_{2};...;R_{m}$ , khi ấy ta ký hiệu: $G(v) = \\{ L_{1};L_{2};...;L_{n} | R_{1};R_{2};...;R_{m} \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nhớ lại rằng đây là 1 trò chơi lạnh, do đó sau nước đi của phe Xanh, giá trị của trò chơi giảm vì giá trị càng lớn (dương) càng có lợi cho phe Xanh, tương tự sau nước đi của phe Đỏ thì giá trị phải tăng (giá trị càng âm càng có lợi cho phe Đỏ), suy ra $L < G(v) < R$ trong đó $L = \text{ max } \( L_{1};L_{2};...;L_{n} \)$ và $R = \text{ min } \( R_{1};R_{2};...;R_{m} \)$ <br>
<div align="center">

Hình 5            | Hình 6
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/d52ae5ff-d597-4346-8a4f-094563739996) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/769c8be9-8447-4bc2-8e55-df6b8e728061)
</div>

#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy tắc 2#.a:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Điều này chưa đủ, vì có thể có rất nhiều giá trị nằm giữa $L$ và $R$ , hãy chọn $G(v)$ là số hữu tỉ mẫu số $2^{s}$ sao cho $s$ là nhỏ nhất có thể, nếu có nhiều hơn 1 giá trị thỏa mãn thì chọn số gần với 0 nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thử với mẫu hình có giá trị $x$ trong hình 5,6. Từ mẫu hình này phe Xanh có nước đi tới 1 trong 2 trạng thái có giá trị $0$ và $\frac{1}{2}$ , phe Đỏ có nước đi tới 1 trạng thái với giá trị $2$  $\rightarrow$ $x = \\{ 0,\frac{1}{2} | 2 \\} = 1$ . Theo phán đoán này, trò chơi ở nửa dưới ảnh sẽ có giá trị là $x - 1 = 0$ , và qua việc chơi thử xác nhận điều này hoàn toàn đúng, người đi trước luôn thua. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp;***<ins>Quy tắc 3:</ins>***
&nbsp;&nbsp;&nbsp;&nbsp;Để tính nhanh $G$ của 1 cây không phân nhánh (hình dưới): xem số lượng tối đa những đoạn dưới cùng liền nhau cùng màu, nếu là xanh thì tính mỗi đoạn là $+1$ , đỏ thì tính mỗi đoạn là $-1$ , sau đó xem tới những đoạn tiếp theo lần lượt từ dưới lên, giá trị tuyệt đối của mỗi đoạn = nửa đoạn trước nó, nếu xanh thì coi là số dương, đỏ là số âm, đem cộng tất cả các đoạn lại, kết quả là $G$ của toàn bộ cây (có thể chứng minh điều này bằng quy nạp sử dụng quy tắc (#2)). Hãy cùng thử áp dụng để dự đoán người chiến thắng trong trò chơi dưới đây. <br> 
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/888bd881-2085-4fae-9918-7ab74fff40f6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Cây thẳng *đỏ-đỏ-xanh-đỏ-đỏ-xanh* có giá trị là $x$ , có thể tính được  $x = -2 + \frac{1}{2} - \frac{1}{4} - \frac{1}{8} + \frac{1}{16} = -\frac{29}{16}$ trò chơi trong hình có giá trị $G = 8x + 13 = -\frac{3}{2} < 0$ $\rightarrow$ người chơi Đỏ sẽ luôn thắng (bạn đọc tự kiểm tra).<br>
&nbsp;&nbsp;&nbsp;&nbsp;Không chỉ vậy, ta còn biết được phải tăng độ dài cây 13 thêm ít nhất 2 cạnh để Xanh có thể dành chiến thắng: $G = 8x + 15 = \frac{1}{2} > 0$ . Và ta còn biết phải thực hiện những nước đi chính xác nào để thắng, giả sử trong trò chơi mới (13 đã tăng lên 15) Xanh đi trước, Xanh phải chọn nước đi sao cho giá trị trò chơi sau khi đi vẫn $\ge 0$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mỗi nước đi của Xanh đều làm $G$ giảm, lượng giá trị giảm không được quá $\frac{1}{2}$ $\rightarrow$ Không thể cắt cây 15 vì sẽ làm $G$ giảm ít nhất 1 $\rightarrow$ Phải cắt 1 trong 8 cây còn lại, cắt đoạn xanh trên cùng (giảm $\frac{1}{16}$ ), hoặc cắt đoạn xanh bên dưới (giảm $\frac{3}{16}$ ) đều được (thật ra nên cắt đoạn dưới vì $G$ vẫn $\ge 0$ nên Đỏ vẫn sẽ thua mà trận đấu lại kết thúc nhanh hơn). <br>
