# Trò chơi bắt cướp 

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mô phỏng trò chơi:</ins>* Giả sử vị trí của cảnh sát và tên cướp được mặc định ở dưới hình dưới trong bối cảnh: cảnh sát bắt cướp. Biết rằng mỗi lần di chuyển cả cảnh sát và tên cướp chỉ được bước 1 đoạn thẳng (đi dọc, ngang, và đi xéo) và đến lượt ai thì người đó đi trước. Cảnh sát di chuyển trước. Liệu cảnh sát có bắt được tên trộm không ? <br>
<div align="center">
  
![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/f38dbe09-5def-4b24-8837-5e99ae70f041)
</div>

## Lời giải
&nbsp;&nbsp;&nbsp;&nbsp;Cảnh sát có thể bắt được tên trộm (kể cả trường hợp chiến thuật tối ưu của cảnh sát và tên cướp) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Ta cần thiết lập 1 khái niệm gọi là ***"khoảng cách giữa 2 người"***, được định nghĩa là số đoạn thẳng (ngang/dọc, không tính đường chéo) để đi từ vị trí của 1 người đến vị trí của người kia. Một vấn đề nảy sinh, có thể có rất nhiều "tuyến đường" để đi từ vị trí này đến vị trí kia, nên khoảng cách không phải là 1 giá trị cố định. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Tuy nhiên, tất cả các tuyến đường để đi giữa 2 vị trí luôn luôn có khoảng cách cùng là số chẵn, hoặc cùng là số lẻ, lý do rất đơn giản: hãy liên tưởng mỗi vị trí như 1 ô vuông trong bàn cờ vua, các ô đen trắng xen kẽ nhau, 1 quân cờ chỉ có thể đi theo 2 hướng ngang dọc, và đi từng bước một, nếu nó khởi đầu từ ô trắng, bước đi kế tiếp làm cho nó đi sang ô đen và ngược lại, nên hành trình của quân cờ sẽ đi qua các ô có màu xen kẽ: trắng-đen-trắng-đen-..., rõ ràng nếu ô cuối của hành trình cùng màu với ô xuất phát thì quân cờ đã đi 1 số chẵn các bước, và nếu ô cuối trái màu với ô đầu thì quân cờ đã đi lẻ bước $\rightarrow$ Số bước đi là chẵn hay lẻ chỉ phụ thuộc vào ô đầu và ô cuối, mà không phụ thuộc vào con đường mà quân cờ đã đi, các tuyến đường đi giữa 2 ô có thể khác nhau nhưng sẽ có số bước đi cùng là chẵn, hoặc cùng là lẻ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Khởi đầu khoảng cách giữa cảnh sát và tên trộm là 2 bước (chẵn), và đang tới lượt cảnh sát. Ở mỗi lượt mỗi bên đi 1 bước, tức là khoảng cách sẽ $±1$ bước $\rightarrow$ Khi tới lượt cảnh sát thì khoảng cách giữa 2 người luôn là chẵn, khi tới lượt tên trộm, khoảng cách giữa 2 người luôn là lẻ $\rightarrow$ Cảnh sát không bao giờ tóm được tên trộm nếu chỉ đi theo chiều ngang và dọc, vì để tóm được tên trộm, phải có 1 thời điểm mà ở lượt của cảnh sát khoảng cách giữa 2 bên là 1 bước (số lẻ). Nên nếu muốn thay đổi tình thế, cảnh sát bắt buộc phải đi qua cạnh chéo 1 lần. Bản thân hành động đi qua cạnh chéo này đã làm cho khoảng cách giữa tên trộm và cảnh sát trở thành lẻ ở lượt của cảnh sát và chẵn ở lượt của tên trộm vì nó tương đương với việc cảnh sát đi 2 bước theo chiều ngang/dọc. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Đó là ***điều kiện cần***, nhưng kể cả khi cảnh sát làm vậy cũng chưa chắc tóm được tên trộm, ta cần chứng minh đây cũng là ***điều kiện đủ***. Xét mạng lưới ô vuông $1 \times n$ (1 dãy ô vuông thẳng hàng ngang) tên trộm sẽ luôn bị bắt khi khoảng cách giữa 2 người ở lượt của cảnh sát là một số lẻ. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Cảnh sát sẽ dồn tên trộm về góc tường gần với hắn nhất, ta thấy rằng tên trộm muốn vượt qua cảnh sát để chạy về góc tường bên đối diện thì sẽ phải có 1 thời điểm cả 2 cùng nằm trên 1 cạnh dọc (cách nhau 1 bước), và đang tới lượt cảnh sát (không thể là lượt của trộm vì tới lượt của trộm thì khoảng cách giữa 2 người phải là chẵn), nên tên trộm sẽ bị tóm ngay lập tức trong lượt đó=>muốn vượt qua cảnh sát để tránh bị dồn về góc là không thể. Mặt khác, sau mỗi lượt đi của cảnh sát, số ô vuông từ chỗ cảnh sát tới góc tường (mà tên trộm sắp bị dồn vào) luôn bị thu hẹp lại: tới lượt của cảnh sát, tên trộm sẽ không nằm cùng 1 ô vuông với cảnh sát, vì hắn không thể ở vị trí chéo với cảnh sát (cách nhau 2 bước), cũng không thể ở 2 vị trí liền kề cảnh sát, nếu không sẽ bị tóm ngay trong lượt đó $\rightarrow$ Cảnh sát hoàn toàn có thể tiến thêm 1 bước về phía góc tường mà không lo bị tên trộm vượt qua. Từ 2 điều này cho thấy cảnh sát sẽ dồn được trộm về góc tường và cuối cùng tóm được hắn khi cả 2 đang cùng đứng trên ô vuông cuối cùng. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Giờ giải pháp đã rõ ràng: Cảnh sát phải đi về hướng ngược với tên trộm và đi qua cạnh chéo 1 lần, sau đó quay trở lại và bắt tên trộm, như đã chỉ ra ở trên, tên trộm không thể thoát được. Ta cũng loại bỏ khả năng tên trộm bắt chước và cũng tìm cách đi qua cạnh chéo 1 lần (để làm cho khoảng cách giữa 2 người khi tới lượt cảnh sát trở lại thành chẵn), vì đơn giản là nếu hắn đuổi theo cảnh sát đến chỗ cạnh chéo, hắn sẽ phải tiếp cận cảnh sát và rất nhanh bị tóm khi chưa kịp đi qua cạnh chéo, nghịch lý ở chỗ hắn phải đợi cảnh sát đi qua cạnh chéo trước rồi mới làm theo, và phải làm ngay khi cảnh sát vừa làm xong, nếu không cảnh sát sẽ kịp quay trở lại và thực hiện chiến thuật "dồn về góc" mà ta đã nói ở trên, nhưng ngay khi làm xong thì đồng nghĩa cảnh sát cũng đang đứng ngay ở đó (1 đầu của cạnh chéo), nên tên trộm không thể dám tới chỗ cạnh chéo và đi qua không nó. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* Tôi thích những cách lập luận thuần túy logic như thế này vì nó cho phép ta biết 1 kết quả chắc chắn tồn tại, mà không cần tìm ra cụ thể kết quả đó. Tuy nhiên nếu các bạn muốn lời giải kiểu mì ăn liền thì đây (xem hình dưới) <br>
<div align="center">
  
![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/5a7573bd-86a9-4026-b4c7-c15ced2d03a2)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;➡➡↘⬆⬅⬅⬅ đây là các bước đi của riêng anh cảnh sát mà đi xong sure win, còn thằng trộm thì đi những nước tối ưu nhất cho nó, nó sẽ không "đi thẳng" vào anh cảnh sát, hay đi tới các vị trí cách anh cảnh sát đúng 1 bước (để bị tóm hay sao), còn lại muốn đi kiểu gì tùy nó.

-------------------------------------------------------------------------------------------------------------------------------------------------------------

## Mở rộng
&nbsp;&nbsp;&nbsp;&nbsp;Vừa rồi là 1 lời giải đẹp cho 1 bài Toán thú vị, chứng minh dựa trên ý tưởng "khoảng cách giữa 2 người là chẵn hay lẻ". Sau đây ta  ***mở rộng*** vấn đề ra 1 chút, theo đúng tôn chỉ "khai thác một ý tưởng cho đến kiệt quệ",đó là: *Sẽ ra sao khi trộm và cảnh sát ở trong dạng bàn cờ chữ nhật, không có bất kỳ vật cản nào ?* <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Không gian trò chơi:</ins>* Hình chữ nhật có kích thước $m \times n$ và vị trí ban đầu của 2 người chơi là tùy ý. <br>

## Lời giải cho bài toán mở rộng
&nbsp;&nbsp;&nbsp;&nbsp;• Nếu khoảng cách giữa 2 bên là chẵn ở lượt cảnh sát, chắc chắn không có cách nào bắt được (đã chứng minh ở bài toán trên) <br>
&nbsp;&nbsp;&nbsp;&nbsp;• Nếu khoảng cách là lẻ ở lượt cảnh sát, luôn tồn tại ít nhất 1 cách để cảnh sát bắt được tên cướp, khi đó ta chứng minh như sau:<br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Bổ đề:</ins>* Nếu cảnh sát và tên cướp đang ở 2 đỉnh chéo nhau của 1 hình vuông $n \times n, \forall n = 2,3,4...$ , và đến lượt tên cướp, thì cuối cùng tên cướp sẽ bị tóm. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Giả sử bổ đề đúng với hình vuông $m \times m$ , nếu cả 2 ở vị trí như trên trong hình vuông $\( m+1 \) \times \( m+1 \)$ , cảnh sát ở góc dưới trái, tên cướp ở góc trên phải, nếu tên trộm di chuyển: ⬆/➡, cảnh sát chỉ cần bắt chước động tác này và cả 2 vẫn tiếp tục ở tư thế chéo nhau trên hình vuông cạnh $m+1$ , nếu tên cướp đi ⬇/⬅ (\*), cảnh sát đi ➡/⬆, vậy là cả 2 ở vị trí chéo nhau trên hình vuông cạnh $m$ và tới lượt tên cướp, theo giả định bổ đề đã đúng với hình vuông $m \times m$ $\rightarrow$ Tên cướp sẽ bị tóm. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác tên cướp không thể đi ⬆/➡ mãi được do sẽ vướng phải các cạnh biên $\rightarrow$ Sớm muộn tên cướp cũng phải đi ⬇/⬅ $\rightarrow$ quay lại (*). Mà bổ đề hiển nhiên đúng với hình vuông $2 \times 2$ nên suy ra bổ đề đúng với mọi hình vuông $n \times n$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh bổ đề trên <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu cảnh sát và tên cướp không nằm ở 2 đỉnh chéo của hình vuông thì sao? Với trường hợp cảnh sát và tên cướp sẽ ở trên 2 đỉnh của 1 chữ nhật (hoặc là thẳng hàng), có 1 cạnh dài và 1 cạnh ngắn, cảnh sát chỉ cần tiến theo hướng cạnh dài để rút ngắn cạnh dài cho đến khi nó trở thành hình vuông, tên cướp có 2 cách để ngăn chặn điều này: tiến theo hướng cạnh dài để kéo dài nó ra, hoặc đi ngang theo hướng cạnh ngắn để làm ngắn nó lại (chung quy đều là muốn duy trì hình chữ nhật), nhưng hiển nhiên cả 2 đều không thể, tên cướp sẽ vướng phải đường biên bàn cờ khi đi theo cạnh dài, và độ dài cạnh ngắn hình chữ nhật chỉ có thể giảm xuống 0 là tối đa <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Sớm muộn gì hình chữ nhật cũng chuyển thành hình vuông, và ở thời điểm khi 2 người chéo nhau trên hình vuông, khoảng cách giữa 2 người là chẵn nên tên cướp sẽ là người đi trước, theo bổ đề, tên cướp sẽ bị tóm. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất giải quyết bài toán mở rộng trên <br>
















