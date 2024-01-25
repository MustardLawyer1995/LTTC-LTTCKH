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

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/9c0cbeee-174b-4081-8d2b-ab619a77860c)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ta thấy 3 lựa chọn của người chạy trốn tạo thành các hàng của ma trận, 3 lựa chọn của thợ săn tạo thành các cột của ma trận. Mỗi ô của ma trận ghi mức thưởng tương ứng của 2 người chơi đối với mỗi kết quả tạo ra từ tổ hợp hành động của họ. Đối với mỗi kết quả, mức thưởng của người chơi Hàng (ở đây là Người chạy trốn) luôn được viết trước, sau đó đến mức thưởng của người chơi Cột (ở đây là Thợ săn). Cách biểu diễn này ngụ ý rằng 2 tay chơi thực hiện nước đi đồng thời. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hạn chế của dạng chuẩn tắc là nó chỉ mô tả được trò chơi 2 người, nên ta cũng biểu diễn trò chơi có thông tin không hoàn hảo bằng dạng mở rộng, trong đó người đi lượt sau không biết hành động của người đi lượt trước, do vậy tạo nên hiệu ứng tương tự như "chơi đồng thời". <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có ví dụ tiếp theo như sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/0c6a1ea7-861c-428d-8b47-338c72aef6f8)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ở trò chơi trong ảnh, hình oval được vạch ra xung quanh các nút b và c đã chỉ ra rằng chúng nằm bên trong một tập thông tin chung (đôi khi người ta cũng thay thế hình oval bằng 1 đường đứt đoạn nối b và c). Điều này nghĩa là khi đưa ra quyết định, Player II không biết mình đang ở nút b hay c. Nói cách khác, Player II không biết được điều mà Player I đã làm ở nút a. Nó tương đương với việc Player I và Player II đưa ra lựa chọn đồng thời (do không ai biết lựa chọn của người còn lại). Vì vậy dạng mở rộng là hoàn toàn khái quát, nó còn có thể biểu diễn được các trò chơi chứa cả những nước đi đồng thời lẫn những nước đi theo trật tự (đây vẫn là trò chơi thuộc loại thông tin không hoàn hảo). <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lưu ý:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thông tin hoàn hảo thường bị nhầm lẫn với "thông tin đầy đủ". Tính chất thông tin đầy đủ đòi hỏi mỗi tay chơi biết về các lựa chọn và hàm tiện ích của các tay chơi khác, nhưng không nhất thiết biết về nước đi cụ thể của họ. Trò chơi qua cầu thuộc loại thông tin đầy đủ. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Chiến lược*
&nbsp;&nbsp;&nbsp;&nbsp;Chiến lược là cách một người chơi chơi một trò chơi, nó xác định nước đi của người đó trong bất kỳ tình huống nào họ gặp phải trong trò chơi. "Chiến lược" dễ bị nhầm là 1 hành động đơn lẻ (trò chơi qua cầu chỉ có 1 hành động cho mỗi tay chơi, nên mỗi lựa chọn của họ chính là 1 chiến lược). 
### 2. Giải trò chơi và khái niệm điểm cân bằng <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Chiến lược thống trị* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chúng ta sẽ sử dụng trò chơi nổi tiếng nhất-trò chơi PD [Song đề tù nhân] làm ví dụ minh họa cho khái niệm này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;PD game là một trò chơi "dễ" và không điển hình, khi mà có 1 hàng/cột thống trị nghiêm ngặt tất cả những hàng/cột còn lại. Các trò chơi khác nói chung thường không đạt được điều kiện này. Bởi vậy chúng ta cần một giải pháp nào đó mang tính tổng quát cho mọi trò chơi. Và đột phá lớn nhất của LTTC là phát minh ra khái niệm "điểm cân bằng". Ta đi vào ví dụ trên bằng bảng trực quan như sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/165ecbe4-eb40-4e0f-9ff0-2ad0be690200)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Cảnh sát đã bắt 2 người mà họ biết là có tham gia vào một vụ cướp có vũ khí nhưng thiếu bằng chứng đầy đủ để thành lập một ban hội thẩm xử án. Tuy nhiên lại có đủ bằng chứng để phạt những người này 1 năm tù vì tội ăn trộm xe ô tô (để chạy trốn). Giờ đây chánh thanh tra thực hiện một đề nghị như sau đối với mỗi người tù: nếu anh nhận tội ăn cướp có dính líu đến đồng phạm (người còn lại), mà hắn ta lại không nhận thì anh được tự do, còn hắn phải chịu 10 năm tù. Nếu cả 2 cùng nhận tội thì sẽ phải chịu 5 năm tù. Nếu cả 2 không nhận tội thì mỗi người chỉ phải chịu 1 năm vì tội trộm xe. Toàn bộ thông tin trò chơi được thể hiện trên một ma trận, với các hàm tiện ích của 2 phạm nhân ( $P_1$ và $P_2$ ) là giống hệt nhau. Điểm thưởng của mỗi người chơi là một giá trị âm của số năm tù họ phải nhận. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến, $P_1$ đánh giá 2 lựa chọn của mình bằng cách so sánh phần thưởng của mình ở mỗi hàng: <br>
-	Nếu $P_2$ thú tội thì $P_1$ sẽ nhận -5 nếu thú tội hoặc -10 nếu chối tội. <br> 
-	Nếu $P_2$ chối tội, $P_1$ sẽ nhận 0 nếu thú tội hoặc -1 nếu chối tội. Dễ thấy rằng đối với $P_1$ , thú tội luôn đem lại kết quả tốt hơn chối tội bất kể $P_2$ hành động như thế nào (chúng ta nói rằng hành động thú tội "thống trị nghiêm ngặt" hành động chối tội). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì ma trận ở dạng đối xứng nên $P_2$ cũng đi tới cùng một kết luận như $P_1$ . Mỗi người chơi đều biết người còn lại nghĩ gì, vì vậy càng có lý do để chọn thú tội, và cả 2 đều sẽ ngồi tù 5 năm. Những người chơi và các nhà phân tích có thể dự đoán được kết quả này bằng một thủ thuật gọi là "sự loại bỏ các chiến lược bị thống trị nghiêm ngặt". Vì chiến lược chối tội sẽ không bao giờ được sử dụng nên chúng ta có thể xóa bỏ các hàng/cột này khỏi ma trận, dẫn đến chỉ còn 1 ô tương ứng với kết quả cả 2 cùng thú tội. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có lẽ bạn đã nhận thấy điều gì đó bối rối về kết quả của PD. Nếu 2 người cùng chối tội thì họ sẽ đạt tới kết quả $(-1,-1)$ , cả 2 đều đạt được tiện ích cao hơn kết quả $(-5,-5)$ khi cùng thú tội. Đây là điểm quan trọng và có nhiều ý nghĩa nhất của PD game. Vì vậy chúng ta sẽ còn tiếp tục bàn về nó ở những phần tiếp theo. Còn bây giờ hãy quay lại với mạch chính của bài viết. 
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Chiến lược thuần túy, chiến lược hỗn hợp* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu người chơi chỉ xác định 1 hành động duy nhất mà mình sẽ làm ở mỗi giai đoạn trò chơi thì đó là chiến lược thuần túy. Nếu người chơi ngẫu nhiên hóa hành động của mình-bằng việc gán cho mỗi lựa chọn một xác suất nào đó, thì đó là chiến lược hỗn hợp. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;khi chơi oẳn tù tì, bạn quyết định sẽ ra kéo, búa, bao với tỉ lệ là $\frac{4}{7}, \frac{1}{7}, \frac{2}{7}$ , hãy hình dung việc này như là bạn rút ngẫu nhiên 1 trong 7 lá phiếu trước khi chơi và tuân theo lựa chọn ghi trên đó. Chiến lược hỗn hợp là cách một người chơi phân phối xác suất lên các chiến lược thuần túy của mình.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chiến lược thuần túy là trường hợp riêng của chiến lược hỗn hợp, khi người chơi gán xác suất 1 cho chiến lược thuần túy đó, và 0 cho các chiến lược thuần túy còn lại. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *c. Cân bằng Nash (Nash Equilibirum - NE)* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một kết quả của trò chơi là điểm ***cân bằng Nash (NE)*** nếu không người chơi nào có thể làm tăng phần thưởng của mình bằng cách thay đổi chiến lược trong khi những người chơi khác giữ nguyên các chiến lược của họ. Phát biểu dưới dạng toán học: Gọi $\( {S_1},{S_2},{S_3},...,{S_n} \)$ là kết quả của trò chơi gồm $n$ người chơi, với $S_k$  là chiến lược của người chơi thứ $k$ và $u_{k} \( {S_1},{S_2},{S_3},...,{S_n} \)$  là tiện ích của người chơi thứ $k$ ở kết quả này. <br>
<div align="center">
  
Khi đó kết quả trên là *NE* nếu: $u_{k} \( {S_1},{S_2},{S_3},...{S_{k}'}...,{S_n} \) \le u_{k} \( {S_1},{S_2},{S_3},...{S_k}...,{S_n} \) , \text{    } \forall S_{k}' \ne S_{k} , \text{    } \forall k \in \[ 1;n \]$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lưu ý:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tiện ích của người chơi $k$ không tăng lên khi anh ta thay đổi sang một chiến lược ${S_k}'$ khác.
&nbsp;&nbsp;&nbsp;&nbsp;Đây là trạng thái mà mỗi người chơi đều không có động lực để thay đổi chiến lược hiện tại của mình. NE thỏa mãn tiên đề về tính duy lý, khi hành động của mỗi người chơi là đáp trả tốt nhất đối với hành động của những người khác, ngược lại, nếu một kết quả trò chơi thỏa mãn tính duy lý thì nó phải là NE. Vì vậy NE là giải pháp hợp lý duy nhất của trò chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* <br>
<div align="center">
  
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/12bc1c6a-5caf-4a5f-9eca-8714de665493)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Xét game trong ảnh với 2 người chơi là $X$ và $Y$ . $X$ có 2 hành động để lựa chọn là $X_1$, $X_2$ ; $Y$ có 3 hành động để lựa chọn là $Y_{1} , Y_{2} , Y_{3}$ . Mỗi ô kết quả ghi $\( u_{X}, u_{Y} \)$ lần lượt là tiện ích/phần thưởng của $X$ và $Y$ . Một NE của trò chơi được gọi là *"NE với chiến lược thuần túy"* khi tất cả người chơi đều sử dụng chiến lược thuần túy tại kết quả này; khi ít nhất 1 người chơi sử dụng chiến lược hỗn hợp thì ta gọi là "NE với chiến lược hỗn hợp". <br>
&nbsp;&nbsp;&nbsp;&nbsp;Để giải trò chơi trong ảnh, trước tiên ta tìm tất cả các NE với chiến lược thuần túy. Điều này có thể thực hiện dễ dàng bằng cách kiểm tra từng hàng của ma trận: <br>
-	Khi $X$ chọn $X_1$ thì $Y$ có tiện ích cao nhất nếu chọn $Y_2$ , khi $Y$ chọn $Y_2$ thì $X$ có tiện ích cao nhất nếu chọn $X_{1}$. Suy ra $\( X_{1}, Y_{2} \)$ là NE. <br>
-	Khi $X$ chọn $X_2$ thì $Y$ có tiện ích cao nhất nếu chọn $Y_3$ , nhưng khi $Y$ chọn $Y_3$ thì $X$ đạt tiện ích cao nhất nếu chọn $X_1$ . Suy ra không có NE nào ở hàng $X_2$ cả. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy trò chơi chỉ có một NE với chiến lược thuần túy duy nhất là $\( X_{1}, Y_{2} \)$ . Điều này sẽ giúp ta tìm kiếm các NE với chiến lược hỗn hợp ở bước tiếp theo đây: Giả sử $X$ phân phối các xác suất $x_{1} , x_{2}$ lần lượt cho $\( X_{1}, X_{2} \)$ và $Y$ phân phối các xác suất $\( y_{1} ,y_{2} , y_{3} \)$ lần lượt cho $Y_{1} , Y_{2}, Y_{3} \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta có: ${x_1} + {x_2} = {y_1} + {y_2} + {y_3} = 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Suy ra các mức tiện ích trung bình của $Y$ khi sử dụng chiến lược hỗn hợp lần lượt là: ${y_1} \( {2{x_1} + {x_2}} \) + {y_2}\( {3{x_1}} \) + {y_3}\( {{x_1} + 3{x_2}} \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nhận thấy $Y$ cố gắng để tối đa hóa giá trị này thông qua 3 khả năng thành phần sau: <br>
```math
\left[ \begin{array}{l}
2{x_1} + {x_2} > \max \left\{ {3{x_1},{x_1} + 3{x_2}} \right\} \to Y:{y_1} = 1\
3{x_1} > \max \left\{ {2{x_1} + {x_2},{x_1} + 3{x_2}} \right\} \to Y:{y_2} = 1\
{x_1} + 3{x_2} > \max \left\{ {2{x_1} + {x_2},3{x_1}} \right\} \to Y:{y_3} = 1
\end{array} \right.
```
&nbsp;&nbsp;&nbsp;&nbsp;Ở cả 3 trường hợp này, kết quả đều sẽ rơi về NE với chiến lược thuần túy $\longrightarrow$ ta phải chọn 1 trong 3 khả năng sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* 
<div align="center">
  
$2{x_1} + {x_2} \le 3{x_1} = {x_1} + 3{x_2} \to \left( {{x_1};{x_2}} \right) = \left( {\frac{3}{5};\frac{2}{5}} \right) \to 2{x_1} + {x_2} < 3{x_1} = {x_1} + 3{x_2}$
</div>

&nbsp;&nbsp;&nbsp;&nbsp;tức $Y$ cho $y_{1}=0$ tức các mức tiện ích trung bình của $X$ khi chọn $X_1$ hoặc $X_2$ lần lượt là ${y_2} + 3{y_3} \text{    } \( {{y_2} + {y_3} = 1} \)$ và $0y_{2}+3y_{3}$ . Nhưng nếu vậy $X$ sẽ chọn $X_1$ $\( x_{1}=1 \)$ , mâu thuẫn với kết luận $\( {x_1};{x_2} \) = \( \frac{3}{5}; \frac{2}{5} \)$  ở trên. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* 
```math
\left\{ \begin{array}{l}
3{x_1} \le 2{x_1} + {x_2} = {x_1} + 3{x_2}\\
{x_1} + 3{x_2} \le 2{x_1} + {x_2} = 3{x_1}
\end{array} \right. \longrightarrow \text{   } \nexists \text{   } ( x_{1} ; x_{2} )
```
















