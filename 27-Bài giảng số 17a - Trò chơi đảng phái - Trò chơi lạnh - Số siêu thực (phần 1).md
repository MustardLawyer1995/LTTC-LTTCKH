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




