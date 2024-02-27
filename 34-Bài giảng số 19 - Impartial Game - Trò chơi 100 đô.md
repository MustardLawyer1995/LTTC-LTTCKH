# Impartial Game - Trò chơi 100 đô
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Giới thiệu:</ins>* Cho một đĩa với các đồng xu trong hình dưới. 2 người chơi luân phiên mỗi lượt lấy 1 đồng tùy ý, sao cho tổng số tiền mà 2 người chơi lấy ra vừa đủ \$100 , ai lấy đồng xu cuối cùng là người thắng. Trong trường hợp không thể lấy được chính xác số tiền \$100 , người nào không còn nước đi hợp lệ khi đến lượt của mình bị coi là thua (không được làm số tiền ở ngoài đĩa vượt quá \$100 ). <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/0eab223f-e60e-41ea-9d0a-f5ca1ab4411a)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lời bình:</ins>* Nhiều người phàn nàn về chuyện tôi chỉ công bố lời giải mà không kể quá trình đi tới lời giải đó (thật sự thì đây mới là phần có ích). Nên ở bài này tôi sẽ lồng vào "1 chút" những điều đó, về việc tôi đã vật lộn với những ý tưởng của mình như thế nào. Dù sao thì, nếu chỉ trình bày chứng minh cho lời giải thì rất nhanh gọn thôi, nhưng toàn bộ quá trình suy nghĩ đã bị ẩn đi, điều mà tôi cũng không thích. Việc tư duy giải quyết vấn đề không nhất thiết là phải "có hệ thống" như người ta vẫn giáo điều, nhưng có 1 điều chắc chắn: nếu bạn không suy nghĩ và thử nghiệm, ý tưởng không bao giờ đến. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mở đầu lời giải:</ins>* Bắt đầu với việc khảo sát cấu trúc của trò chơi. Đây là ***<ins>1 impartial game</ins>***, nhưng nó không thể được phân tách ra thành các trò chơi con (vì điều kiện tổng các khoản tiền mà 2 người chơi lấy ra $\le$ \$100). Mặt khác, mỗi người chơi đều có thể có rất nhiều lựa chọn, nhất là trong những nước đi khai cuộc, nên việc chia từng trường hợp và lập bảng giá trị nimber là điều không tưởng. Khi bế tắc, chúng ta nên chơi một vài ván chơi mẫu để tìm kiếm quy luật. Tôi đã để ý một chi tiết quan trọng, đó là việc người chơi có thể chiến thắng bằng cách liên tục tạo ra các nhóm giá trị "chia hết cho 3".
<div align="center">

Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/a79fdb4a-c993-4532-b0e2-e67f2a2088cf) | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/8a13a6cb-255c-463e-92d3-850cc81dc89d)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Đầu tiên, dễ nhận ra các mệnh giá $20,10,5,2,1$ đều không chia hết cho 3, mặt khác 2 mệnh giá khác nhau lại có khả năng tạo tổng chia hết cho 3: $1 + 2,1+ 5,1 + 20,2 + 10,5 + 10,10 + 20$ (sơ đồ hình 1). Ý tưởng sơ khai là như sau: người chơi 1-người đi trước, lấy 10 (hoặc 1) trong lượt đầu tiên và làm cho số tiền tối đa mà 2 người chơi được phép lấy về sau là 90 (hoặc 99), một giá trị là bội số của 3; ở những lượt tiếp khi ***người chơi 2 (Nc2)*** chọn bất cứ đồng nào, ***người chơi 1 (Nc1)*** chọn 1 đồng sao cho tổng giữa nó với đồng mà Nc2 vừa chọn là bội số của 3. Do vậy, khi 2 người chơi đã lấy ra đủ 90 (hoặc 99) thì Nc1 phải là người đi lượt sau cùng. Dựa theo điều này thì có vẻ Nc1 (người đi trước) là người thắng...Tuy nhiên thực tế phức tạp hơn nhiều. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Để đơn giản, ta sẽ xét kịch bản mà Nc1 chọn \$10 ngay trong lượt đầu tiên, khi đó số tiền tối đa mà 2 người được lấy tiếp là \$90, trò chơi trở về trạng thái như hình 2, số đồng xu loại \$10 chỉ còn 4, và người đi trước là Nc2. Giả sử Nc2 chọn \$5 hoặc \$2, Nc1 phải chọn \$10 hoặc \$1 nếu muốn áp dụng chiến lược tạo các nhóm chia hết cho 3 (theo sơ đồ hình 1). Nếu điều đó tiếp diễn thì suốt cuộc chơi, Nc1 không có cơ hội để chọn \$20, và trò chơi sẽ kết thúc khi tất cả \$80 (không bao gồm \$10 trong lượt đầu tiên) bị lấy đi, lúc này trên đĩa chỉ còn loại xu \$20, người chơi không thể lấy chúng vì sẽ làm số tiền lấy ra vượt quá \$90. Và người chiến thắng lại là...Nc2, bởi vì tổng số xu đã bị lấy ra là 19 xu (4 xu \$10, 5 xu \$5, 5 xu \$2, 5 xu \$1), một số lẻ, nên Nc2 sẽ là người đi lượt cuối cùng và thắng. Kịch bản mà Nc1 chọn \$1 ở lượt đầu tiên có thể được lập luận tương tự. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thật bất ngờ khi kế hoạch tưởng như hoàn hảo của Nc1 lại khiến anh ta thua, và để thắng thì anh ấy buộc phải lấy 1 đồng \$20 trong quá trình chơi, đồng nghĩa với việc phá bỏ chiến lược của mình. Giờ ta sẽ chỉ ra rằng nếu Nc1 làm thế thì Nc2 có thể tận dụng ngược lại chiến lược của Nc1 và trở thành người chiến thắng. Như trên ta đã thừa nhận rằng để chiến thắng thì Nc1 buộc phải lấy được ít nhất 1 đồng \$20 trong quá trình chơi, có 2 trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1</ins>* Nc1 lấy \$20 ngay lượt đầu tiên. Nc2 cũng lấy \$20 sau đó, nên số tiền tối đa được phép lấy tiếp trong giai đoạn còn lại của trò chơi là \$60 , một số chia hết cho 3. Ta phân nhóm những đồng xu còn lại trên đĩa như sau: 1 cặp $\( 20+10 \)$ , 4 cặp $\( 10+5 \)$ , 5 cặp $\( 2+1 \)$ . <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/a98a5832-d723-4e44-802f-2a76b3e0579f)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nghĩa là khi Nc1 chọn \$2 thì Nc2 chọn \$1 và ngược lại, khi Nc1 chọn \$5 thì Nc2 chọn \$10 và ngược lại, khi Nc1 chọn \$20 thì Nc2 chọn \$10 và ngược lại (hình trên) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Hệ quả là 1 cặp đồng xu $2+1=3,10+5=15$ , hoặc $20+10=30$ luôn được lấy ra khỏi đĩa cùng nhau (sau 2 lượt, lượt chơi lại quay vòng về cho Nc1), đây đều là các bội số của 3 $\to$ khi đến lượt Nc1, tổng số tiền cả 2 người chơi đã lấy khỏi đĩa ( $S$ ) (không bao gồm \$40 của 2 lượt đầu tiên) luôn là bội số của 3, ngoài ra, các cặp $10+5$ và $20+10$ đều là bội số của 15 nên $S=15m+3t$ , với $t$ là số cặp $\( 2+1 \)$ đã bị lấy $\( t \le 5 \)$ . (#) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bởi vì $3 \times \( 10+5 \) + 5 \times \( 2+1 \) = 60$ , vừa bằng đúng số tiền tối đa được phép lấy (tiến độ của trò chơi có thể được đẩy nhanh bằng việc lấy ra 2 cặp $\( 20+10 \)$ hoặc 4 cặp $\( 10+5 \)$ tùy vào việc Nc1 đưa ra lựa chọn như thế nào) $\to$ Người đi nước cuối cùng luôn luôn là Nc2 và anh ta thắng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Lưu ý:** có thể sẽ có vài giai đoạn mà Nc2 buộc phải làm khác với quy tắc ghép cặp ở trên: Nc1 chọn \$10 nhưng Nc2 không thể chọn \$5, nên buộc phải chọn \$2 ( $10+2$ vẫn chia hết cho 3), tương tự các cách ghép cặp ngoại lệ khác là  . Điều này không ảnh hưởng tới chiến thắng của Nc2, ta thử phân tích 3 trường hợp sau, tương ứng với lần đầu tiên xảy ra sự ghép cặp ngoại lệ: <br>




