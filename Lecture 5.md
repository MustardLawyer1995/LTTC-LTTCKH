# Lý Thuyết Trò Chơi (phần 1) 
### 0. Giới thiệu tổng quan <br>
&nbsp;&nbsp;&nbsp;&nbsp;*Lý thuyết trò chơi* ***(LTTC)*** là một nhánh của Toán học ứng dụng, nghiên cứu các tình huống chiến thuật trong đó các đối thủ lựa chọn các hành động khác nhau để cố gắng tối đa hóa kết quả nhận được. Ban đầu được phát triển như một công cụ nghiên cứu hành vi kinh tế học, ngày nay LTTC được sử dụng trong nhiều ngành khoa học, từ Sinh học tới Triết học. LTTC đã có sự phát triển lớn từ trước và trong Chiến tranh Lạnh, chủ yếu do áp dụng của nó trong chiến lược quân sự, nổi tiếng nhất là khái niệm "song phương tận diệt" (mutual assured destruction). Từ những năm 1970, LTTC bắt đầu được áp dụng cho nghiên cứu hành vi động vật, bao gồm sự phát triển của các loài qua chọn lọc tự nhiên. Do các trò chơi hay như Song đề tù nhân (prisoner’s dilemma), trong đó lợi ích cá nhân gây hại cho tất cả mọi người, LTTC bắt đầu được dùng trong Chính trị học, Đạo đức học và Triết học. LTTC còn thu hút sự chú ý của các nhà Khoa học máy tính do ứng dụng của nó trong Trí tuệ nhân tạo và Điều khiển học. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Dù có tính chất hàn lâm, LTTC đã nhận được sự chú ý trong văn hóa đại chúng. <br>
-   John Nash, một nhà LTTC đã nhận được giải thưởng Nobel, là chủ đề trong cuốn hồi ký năm 1998 của tác giả Sylvia Nasar và trong bộ phim Trí tuệ đẹp (A Beautiful Mind-2001). 
-   Một số game show đã sử dụng các tình huống của LTTC, như Friend or Foe? và Survivor.
-   Liar Game, một bộ truyện tranh Nhật Bản (2005) và phim truyền hình (2007), các vấn đề trong mỗi tập thường được rút ra từ LTTC, thể hiện bằng chiến lược mà các nhân vật áp dụng.
-   Tiểu thuyết The Dark Forest (2008) của Liu Cixin khám phá mối quan hệ giữa sự sống ngoài Trái đất, loài người và LTTC. <br>
Tuy hơi giống Lý thuyết quyết định, nhưng LTTC nghiên cứu các quyết định đưa ra trong một môi trường có sự tương tác giữa các đối thủ. Nói cách khác, LTTC nghiên cứu cách lựa chọn hành vi tối ưu khi chi phí và lợi ích của mỗi lựa chọn là không cố định mà phụ thuộc vào lựa chọn của các cá nhân khác. Vẫn mơ hồ quá nhỉ ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mời xem qua ví dụ sau đây: Bạn muốn đi qua 1 con sông có 3 chiếc cầu (giả sử đây là cách di chuyển khả thi duy nhất): cầu 1 an toàn và không có trở ngại gì; cầu 2 nằm dưới chân một mỏm đá có những tảng đá lớn thỉnh thoảng vẫn rơi xuống; cầu 3 là nơi ở của những con rắn hổ mang rất độc. Nếu phân hạng 3 chiếc cầu theo mức độ ưa thích của bạn, cầu 1 rõ ràng là tốt nhất. Để xếp hạng 2 chiếc cầu còn lại bạn cần có thông tin về các cấp độ liên quan đến mức nguy hiểm của nó. Khi nghiên cứu tần suất đá rơi và hoạt động của các con rắn hổ mang, bạn tính được tỉ lệ bị đá rơi trúng là ⅓ và bị rắn tấn công là ½. Đây là sự suy lý bằng thông số chặt chẽ, những tảng đá và những con rắn không cố lừa bạn (chẳng hạn như che giấu các hành vi của chúng) hay biết bạn đang nghiên cứu chúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giờ hãy phức tạp hóa tình huống lên một chút: cầu 2 ở ngay trước mặt, trong khi cầu 1 cách xa một ngày đi bộ. Bạn phải xét xem liệu chi phí cho cuộc đi bộ ấy có đáng để đổi lấy ⅓ cơ hội bị đá rơi vào người không. Nhưng khả năng vượt sông thành công vẫn phụ thuộc toàn bộ vào quyết định của bạn, môi trường không hề quan tâm gì đến kế hoạch của bạn cả. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tuy nhiên tình huống trở nên rắc rối hơn nhiều nếu ta đưa vào một nhân tố có khả năng duy lý - một người chơi khác. Giả sử 1 người săn đuổi có súng muốn giết bạn đang đợi bên kia bờ sông. Hắn sẽ đuổi kịp và bắn bạn khi hắn đợi ở đúng chiếc cầu bạn đi qua, nếu không thì bạn thoát. Bạn suy xét việc lựa chọn cây cầu, chọn cây cầu an toàn để đi sẽ là một sai lầm, vì hắn sẽ chờ ở đó. Vậy có lẽ mạo hiểm với những tảng đá hoặc rắn hổ mang thì ổn hơn. Chờ đã... liệu thợ săn có đoán được suy nghĩ này của bạn không? Hay là nên quay lại với cây cầu an toàn? Bạn nhận ra một vấn đề nan giải: bạn phải làm điều mà thợ săn ít ngờ đến nhất, nhưng bất cứ kế hoạch gì bạn có thể nghĩ ra thì hắn-một người duy lý và có đủ thông tin về 3 cây cầu, cũng có thể nghĩ tới. Điều an ủi bạn là ở bờ sông bên kia, thợ săn cũng bị rơi vào tình thế khó xử đó, không thể quyết định được nên đợi ở cây cầu nào, vì ngay khi hắn tìm ra một lý do hợp lý để chọn một cây cầu, thì bạn lại có thể đoán trước được cái lý do đó để tránh hắn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tóm lại, LTTC nghiên cứu về những tình huống/trò chơi như trên, cung cấp một giải pháp-một lựa chọn duy lý nhất cho tất cả người chơi, để thoát khỏi những vòng tròn suy luận luẩn quẩn đó. <br>
### 1. Các định đề của lý thuyết trò chơi
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Tiện ích* 
&nbsp;&nbsp;&nbsp;&nbsp;Những phúc lợi mà người chơi thu được trong trò chơi được mô tả bằng khái niệm "tiện ích" - một chỉ số biểu thị tình trạng hạnh phúc tương đối theo một khung cơ sở nào đó. Với mỗi kết quả trong trò chơi, người chơi sẽ nhận được một mức điểm thưởng (đo bằng hàm tiện ích), đại diện cho mức độ ưa thích của người chơi đối với kết quả đó. Nếu kết quả A mang lại nhiều điểm cho người chơi hơn kết quả B, thì đơn giản là vì anh ta thích kết quả A hơn B. 
&nbsp;&nbsp;&nbsp;&nbsp;Chẳng hạn trong trò chơi ở I/, nếu người chạy trốn qua sông an toàn thì anh ta nhận được 1 điểm và thợ săn được 0, nếu bị bắn/gặp nạn thì anh ta được 0 và thợ săn được 1. Khi ấy ta có phân tích như sau: <br>
-	Khi qua cầu 2, nếu không có thợ săn chặn bắt ở đó thì người chạy trốn nhận được $\frac{2}{3}$  
-	Mức thưởng trung bình khi tính đến tỉ lệ đá rơi trúng là: $\frac{1}{3} \( 1 \times \( 1 - \frac{1}{3} \) + 0 \times \frac{1}{3} \) = \frac{2}{3}$ , khi đó thợ săn tương ứng nhận được $\frac{2}{3}$ điểm cho trường hợp này. 
-	Tương tự, khi qua cầu 3 mà không gặp thợ săn thì mỗi người chơi đều được $\frac{1}{2}$ , do khả năng bị rắn cắn là $\frac{1}{2}$ .
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Tính duy lý* 
&nbsp;&nbsp;&nbsp;&nbsp;LTTC giả định rằng các tay chơi đều ***"duy lý"***. Nghĩa là một tay chơi có thể: 
- Đánh giá các kết quả (hàm tiện ích). <br>
- Tính toán các con đường dẫn đến các kết quả, bao gồm cả hành động của các tay chơi khác. <br>
- Lựa chọn các hành động để đạt được kết quả ưa thích nhất (tối đa hóa tiện ích). <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Thông tin và dạng biểu diễn*
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi có thông tin hoàn hảo nếu mỗi tay chơi biết mọi hành động mà các tay chơi khác đã thực hiện (ngụ ý rằng các tay chơi phải thực hiện nước đi lần lượt). Chúng thường được biểu diễn bằng dạng mở rộng như sau.
<div align="center">
  
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/8c1c7797-2764-4592-b21b-54922df32ef1)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Dạng mở rộng mô tả các trò chơi có hành động thực hiện theo thứ tự. Chúng được biểu diễn bằng một sơ đồ hình cây như hình vẽ trên. Mỗi nút biểu thị một trạng thái của trò chơi mà ở đó 1 người chơi sẽ đưa ra lựa chọn-biểu thị bằng các đoạn thẳng đi ra từ nút đó. Tiện ích của các tay chơi được ghi rõ tại mỗi nút kết quả ở đáy cây.
Trò chơi trong ảnh có 2 người chơi (I và II) thực hiện nước đi lần lượt, mỗi lượt đều có 2 lựa chọn là L hoặc R. Tại các nút kết quả trò chơi, thường thì tiện ích của người chơi trước-Player I, được viết trước, sau đó là tiện ích của Player II (8, 9, 10 chỉ là số thứ tự để gọi các nút, không có ý nghĩa gì khác). Trò chơi thuộc loại thông tin hoàn hảo có thể được giải dễ dàng bằng thuật toán quy nạp ngược *(thuật toán Zermelo)* , dựa vào 2 điểm: <br>
- Mỗi tay chơi có thể quan sát được toàn bộ hành động mà những tay chơi khác đã thực hiện. <br>
- Tất cả các tay chơi đều duy lý. <br>

$\longrightarrow$ Mỗi tay chơi có thể tự đặt mình vào vị trí của các tay chơi khác và dự đoán được lựa chọn của họ ở mỗi nút, quá trình suy diễn đi ngược từ đáy cây về nút bắt đầu nên được gọi là "quy nạp ngược". Ở trò chơi trong ảnh, tại nút 10, Player I chắc chắn sẽ chọn L vì nó mang lại 3 điểm thay vì 2 điểm khi chọn R $\longrightarrow$ có thể cắt bỏ nhánh 10R khỏi sơ đồ $\longrightarrow$ tại nút 9, nếu Player II chọn R sẽ dẫn thẳng tới kết quả $(3,1)$ , nên chọn L sẽ mang lại tiện ích lớn hơn cho anh ta $(2>1)$ $\longrightarrow$ nhánh 9R bị cắt bỏ $\longrightarrow$ ở nút 8, Player I chọn L với lý do tương tự $\longrightarrow$ $(1,10)$ là kết quả tất yếu của trò chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ngược lại, trò chơi qua cầu ở I/ có thông tin không hoàn hảo, vì người chạy trốn và thợ săn phải đưa ra quyết định trong khi không biết hành động của người còn lại. Nó được biểu diễn bằng dạng chuẩn tắc thông qua ví dụ sau: <br>

<div align="center">
<table style="border-collapse: collapse;">
  <tr>
    <td style="border: 1px solid black; position: relative; width: 60px; height: 60px;">
      <div style="position: absolute; width: 100%; height: 100%; background: linear-gradient(to bottom right, transparent calc(50% - 1px), black calc(50% - 1px), black 50%, transparent 50%);"></div>
      <div style="position: relative; z-index: 2; padding: 5px;">
        Cell 1
      </div>
    </td>
    <!-- More cells with similar inline styling -->
    <td style="/* ... */">Cell 2</td>
    <td style="/* ... */">Cell 3</td>
    <td style="/* ... */">Cell 4</td>
  </tr>
  <!-- More rows with inline styling -->
  <tr>
    <!-- ... -->
  </tr>
  <!-- ... -->
</table>

</div>

















