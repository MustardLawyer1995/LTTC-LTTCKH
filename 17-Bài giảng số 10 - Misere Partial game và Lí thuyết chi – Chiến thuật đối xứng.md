# Misere Partial game và Lí thuyết chi – Chiến thuật đối xứng
### 1. Chiến thuật của Misere Nim Game <br>
&nbsp;&nbsp;&nbsp;&nbsp;Người ta nhận ra 1 điểm kỳ lạ: khi một nim game được chơi theo phiên bản misere, các tính toán trên máy tính cho thấy các nước đi (tối ưu) vẫn giống như trong phiên bản normal, chỉ khác ở những nước đi cuối cùng. Cụ thể, gần về cuối game, nếu 1 tình huống mà ở normal game người thắng phải tạo ra một số lượng chẵn các đống chỉ gồm 1 quân, thì ở misere game, phải tạo số lẻ. Có thể tổng quát chiến lược tất thắng cho misere nim game như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Nimber của mỗi đống được tính theo cách như của normal nim game, tính tổng xor giữa chúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Liên tục đưa tổng xor về 0, giống như trong normal nim game. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Ở giai đoạn khi chỉ còn duy nhất 1 đống có kích thước > 1, các đống khác đều chỉ còn 1 quân (đây là giai đoạn quyết định số lượng đống 1 là chẵn hay lẻ), ta phải chọn sao cho tạo ra 1 số lẻ đống 1. Việc này có thể được quyết định dễ dàng bằng việc lấy hết các quân trong đống > 1 kia, hoặc để chừa lại 1 quân. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Chứng minh đây là chiến thuật tất thắng: tất nhiên, khi bạn đã tạo ra số lẻ các đống 1, thì đối phương thua là chắc chắn rồi, bây giờ ta sẽ chỉ ra rằng việc làm cho đối phương rơi vào các thế có tổng xor = 0 liên tục sẽ khiến quyền quyết định số lượng đống 1 rơi vào tay bạn. Đầu tiên, vì trò chơi kết thúc sau hữu hạn lượt đi <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Sẽ có 1 thời điểm chỉ còn duy nhất 1 đống có > 1 quân, các đống khác đều có 1 quân (thời điểm quyết định số lượng đống 1 là chẵn hay lẻ), vấn đề là vào thời điểm này, đang là lượt của người chơi nào? (ai có quyền quyết định số lượng đống 1 là chẵn hay lẻ?) Không thể là đối phương, vì hắn ta bị bạn đưa về các trạng thái tổng xor = 0 liên tục, tức là đến lượt của hắn, tổng xor phải = 0, nhưng việc tồn tại 1 đống có > 1 quân trên bàn làm cho tổng xor không thể = 0 <br>
&nbsp;&nbsp; $\Longrightarrow$ Đó phải là lượt của bạn! Bạn thắng rồi. ***(chứng minh hoàn tất)*** <br>

### 2. Lý thuyết chi <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Tổng quan* 
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Lý thuyết chi (genus theory)</ins>*** đẩy vấn đề lên mức độ bao quát hơn, nhằm tìm lời giải cho tất cả các *impartial game* được chơi theo phiên bản misere. Cần nói thêm rằng, lý thuyết chi chưa phải 1 lý thuyết hoàn chỉnh như định lý *Sprague Grundy*. Lý thuyết chi hoạt động theo cách gán bừa giá trị nimber là 1 cho misere game ở trạng thái không còn nước đi tiếp theo (người đi trước mặc định thắng), và giá trị nimber cho các trạng thái khác cứ áp nguyên định nghĩa cũ của nimber mà tính. Chúng được gọi là misere nimber, ký hiệu $G^-$ , phân biệt với $G^+$ là nimber được tính theo luật chơi normal (normal nimber), lý thuyết chi sử dụng cả 2 loại thông số này. Một game sẽ được mô hình hóa thành dạng mạng đồ thị, mỗi điểm nút trong đó là 1 trạng thái của game, gồm 2 thông số tương ứng là $\( G^{+};G^{-} \)$ , mỗi cạnh nối giữa 2 nút là 1 nước đi. Để thuận tiện cho việc trình bày tôi sẽ dùng các ký hiệu quy ước sau: <br>





