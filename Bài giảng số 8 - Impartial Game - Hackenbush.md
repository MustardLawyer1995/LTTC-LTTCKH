# Impartial Game - Hackenbush
### 1. Chiến thuật của Misere Nim Game <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mô phỏng:</ins>*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi bắt đầu với 1 hình vẽ gồm 1 đường "mặt đất" (đường kẻ đứt đoạn)  và một số đoạn thẳng được nối với mặt đất, trực tiếp, hoặc gián tiếp thông qua 1 chuỗi các đoạn thẳng khác được kết nối với nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Đến lượt mình, một người chơi "cắt" (xóa) bất kỳ đoạn thẳng nào mình chọn. Các đoạn thẳng nào không còn được kết nối với mặt đất sẽ "rơi" (nghĩa là bị xóa). Theo quy ước chơi normal của lý thuyết trò chơi kết hợp, người chơi đầu tiên không còn nước để đi bị thua. <br>
<div align="center">

![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/58ddfe1c-a25d-4b10-96d6-23dc84e4dca9)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Các đoạn thẳng (thật ra không bắt buộc phải thẳng lắm) được nối với nhau qua các điểm, chúng có thể tổ hợp theo nhiều cách để tạo ra 1 hình dạng bất kỳ. Ở đây là hình 1 cô gái. Ta sẽ gọi 1 cụm hình như thế này là 1 cây (hình trái). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hình bên phải là một mẫu hình để chơi Hackenbush có thể bao gồm nhiều cây như vậy, chúng là các cụm hình tách biệt, không có kết nối với nhau. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Theo ***định lý Sparague Grundy***: lời giải/chiến lược tất thắng của game cũng tương tự như các normal impartial game khác. Tính giá trị nimber của từng cây riêng lẻ, rồi tính tổng nimber của chúng (theo phép XOR), nếu tổng nimber ≠ 0 ở lượt của bạn, đi 1 nước để đưa tổng nimber về 0. Nhưng tính giá trị nimber của mỗi cây bằng cách nào? <br>

### 2. Trường hợp cây không chứa mạch vòng <br>
<div align="center">

![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/ec097201-39e6-4995-98ca-9ba873075e9f)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu chỉ có 1 cây "không phân nhánh" gồm các đoạn thẳng nối liên tiếp vào nhau theo 1 chiều  thì nó tương tự 1 chồng nim, và có nimber = số đoạn thẳng. Nếu hình cây phân nhánh (hình trái), ta có thể quy đổi tất cả các nhánh xuất phát từ cùng 1 điểm về 1 nhánh duy nhất, có độ dài = chỉ số nimber tổng của tất cả các nhánh xuất phát từ cùng 1 điểm kia (hình phải). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Hình bên phải minh họa cho ***<ins>nguyên lý đại tràng (Colon Principle)</ins>***. Các nhánh chỉ cần được xuất phát từ cùng 1 điểm đều có thể được thay thế bằng 1 nhánh duy nhất, có độ dài (số đoạn) = giá trị nimber tổng của tất cả các nhánh bị thay thế. Áp dụng thao tác này, ta có thể rút gọn, cắt tỉa để hình ban đầu trở nên đơn giản nhất có thể, từ đó dễ dàng tính giá trị nimber của hình. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lưu ý:</ins>* Quá trình rút gọn này được thực hiện trong đầu, nó chuyển hình phức tạp thành 1 hình đơn giản hơn mà vẫn có giá trị nimber như hình gốc, chứ không phải là 1 thao tác/nước đi mà bạn thực hiện trực tiếp trong trò chơi. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Điều này giúp ta tính toán các chỉ số nimber một cách rất dễ dàng, và nó được gọi là *nguyên lý đại tràng*, chứng minh đơn giản dựa vào chính định nghĩa của nimber (số Grundy), nếu một tập hợp nhiều nhánh chung gốc có nimber tổng là $n$ , thì các bước đi tiếp theo tác động vào tập hợp các nhánh này có thể đưa chúng về các số nimber $0,1,2,...n-1$ , từ đó có thể thấy chúng thể hiện tính chất giống như 1 nhánh duy nhất gồm $n$ đoạn thẳng (ta cũng có thể tùy ý cắt cụt nhánh này về $0,1,2,...n-1$ đoạn thẳng ở bước tiếp theo). <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/87a2b577-0c69-4579-b235-49ffb402e304)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Một ví dụ khác về việc rút gọn mẫu hình bằng cách sử dụng nguyên lý đại tràng. Ta sẽ chứng minh nguyên lý đại tràng là đúng: nhìn vào 2 cây cuối, cây sau là rút gọn của cây trước bằng việc thay thế 3 nhánh xuất phát từ điểm d có độ dài lần lượt là 2,2,3 thành 1 nhánh duy nhất có độ dài là 3 (kết quả phép cộng nimber $223=3$ ). Giờ xét 1 mẫu hình gồm 2 cây này, ở mỗi lượt người chơi tác động vào 1 trong 2 cây, người đi trước luôn thua, khi anh ta đi bất kỳ 1 nước nào, người kia có thể đi nước tương tự ở cây còn lại để làm cho 2 cây có nimber bằng nhau (tổng nimber = 0) <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	(1) Nếu người chơi trước xóa 1 đoạn nằm ngoài các nhánh ở điểm $d$ , người chơi sau có thể tạo nước giống hệt ở cây còn lại. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	(2) Nếu người chơi trước xóa 1 đoạn trong các nhánh ở điểm d ở cây chưa rút gọn, vì tổng nimber của các nhánh này $= 3$ , anh ta có thể sẽ giảm con số này xuống $\\{ 0,1,2 \\}$ , người chơi sau có thể làm tương tự ở cây đã rút gọn, khi nhánh ở điểm $d$ trên cây này có độ dài là 3 đoạn, và anh ta cũng có thể cắt cho nó giảm xuống còn $\\{ 0,1,2\\}$ đoạn; nếu người chơi trước tác động vào các nhánh ở điểm d trên cây chưa rút gọn và làm giá trị nimber của chúng tăng lên $>3$ thì sao? Người chơi sau có thể tác động vào các nhánh đó để tổng nimber của chúng lại trở về 3, quá trình này sẽ tiếp diễn đến khi các nhánh ở điểm $d$ trên cả 2 cây đều bị xóa, lúc này 2 cây giống hệt nhau và đang đến lượt người chơi trước, quay trở lại (1). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Người chơi trước luôn thua, do anh ta luôn bị đẩy vào các trạng thái có tổng nimber = 0, chứng tỏ trạng thái đầu tiên (gồm 2 cây ban đầu) có tổng nimber = 0, hay nói cách khác 2 cây đó có nimber bằng nhau <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Khi rút gọn hình theo nguyên lý đại tràng, giá trị nimber của hình không hề thay đổi! ***(chứng minh hoàn thành)*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét:</ins>* Đặc biệt, quá trình chứng minh này cũng cho thấy nguyên lý đại tràng có thể áp dụng cho mọi trường hợp, dù cây bị rút gọn có chứa mạch vòng hay không (thậm chí mạch vòng có thể nằm ngay trong các nhánh ở điểm d), bởi vì rõ ràng là các bước chứng minh chỉ phụ thuộc vào 1 điều kiện duy nhất: các nhánh bị rút gọn phải xuất phát từ cùng 1 điểm, mà không hề đề cập đến các mạch vòng. <br>

### 3. Trường hợp cây chứa cả các mạch vòng <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ phân tích 1 số trường hợp đơn giản: <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *<ins>Trường hợp 1</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có 1 vòng đơn gắn liền với mặt đất (cây cầu), nếu vòng gồm số chẵn đoạn, nimber $= 0$ , nếu gồm số lẻ đoạn, nimber $= 1$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu vòng gồm chẵn đoạn, lấy/xóa bất cứ đoạn nào đều tạo ra 2 cây không phân nhánh, 1 cây có chẵn đoạn, 1 cây có lẻ đoạn. Trong hệ nhị phân, số chẵn tận cùng bởi 0, số lẻ tận cùng bởi 1, nên tổng XOR của chúng tận cùng bởi 1 $\rightarrow$ Tổng nimber sẽ không thể = 0 $\rightarrow$ Mex của tập hợp không chứa 0 = 0 $\rightarrow$ vòng có chẵn đoạn thì nimber tương ứng = 0. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tương tự, nếu vòng lẻ đoạn thì xóa bất cứ đoạn nào cũng tạo ra 2 cây không phân nhánh đều có chẵn/lẻ đoạn $\rightarrow$ tổng XOR của chúng tận cùng bởi 0 $\rightarrow$ tổng nimber không thể $= 1$ . Mặt khác nếu xóa đoạn chính giữa thì tạo ra 2 cây bằng nhau, tổng nimber $= 0$ $\rightarrow$ Mex của 1 tập hợp chứa 0, không chứa 1 $= 1$ $\rightarrow$ vòng có lẻ đoạn thì nimber tương ứng $= 1$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Hoàn tất chứng minh.*** <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *<ins>Trường hợp 2</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có nhiều cây thẳng mọc trên 1 vòng đơn gắn liền mặt đất (cỏ mọc trên cầu), nimber toàn phần = nimber của vòng (cây cầu) + nimber của tất cả các cây nằm trên vòng (cỏ) . <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/536f57a2-997a-4307-a851-71643b9b2086)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sử dụng quy nạp, với 1 mẫu hình mà các cây cấu thành từ $n$ đoạn mọc trên cây cầu gồm chẵn đoạn, tổng nimber của các cây là $N$ (vậy nếu kết luận trên là đúng thì tổng nimber của mẫu hình cũng là $N$ ), giả sử kết luận trên là đúng với $\le N-1$  đoạn, sau đó bất cứ thao tác nào tác động vào các cây cũng làm giảm số đoạn xuống $\le N-1$ , và như vậy nimber của mẫu hình được đưa về các giá trị trong đoạn $\[ 0;N-1 \]$ . Mặt khác, nếu cắt 1 đoạn của "cây cầu", tổng số đoạn của mẫu hình chỉ giảm đi 1, và hình mới tạo ra chỉ gồm các cây phân nhánh không chứa vòng, xét chữ số nhị phân hàng đơn vị, ta thấy rằng tính chẵn lẻ của tổng nimber luôn = tính chẵn lẻ của tổng số đoạn thẳng trong mẫu hình <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Nimber của mẫu hình vừa tạo ra không thể $=N$  (khác tính chẵn lẻ) $\rightarrow$ Nimber của mẫu hình hiện tại bằng chính Mex của 1 tập hợp chứa tất cả các giá trị từ $0$ đến $N-1$ , nhưng không chứa $N=N$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Giả thuyết đã được chứng minh bằng quy nạp*** . Tương tự với trường hợp cây cầu có lẻ đoạn. <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *<ins>Trường hợp 3</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với những hình thù phức tạp hơn, ta có ***<ins>nguyên lý hợp nhất (Fusion principle)</ins>*** : Bất cứ 2 điểm nào trong vòng cũng có khả năng hợp nhất với nhau mà không làm thay đổi giá trị nimber. <br>
<div align="center">

![Capture](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/fe444b03-2c7c-468a-9173-b35a8d79bde9)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhắc lại:</ins>* Nguyên lý hợp nhất nói rằng việc hợp nhất các điểm khác nhau trên 1 mạch vòng luôn luôn tạo ra hình mới có giá trị nimber như hình ban đầu. Tất nhiên sự hợp nhất có thể sẽ làm các đoạn trong mạch vòng bị biến dạng, nhưng không vấn đề gì, trường hợp một đoạn thẳng bị uốn cong đến mức 2 đầu của nó chạm nhau, nó sẽ có giá trị như 1 đoạn thẳng thông thường "mọc" ra từ điểm đó. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử tồn tại những mẫu hình mà sự hợp nhất các điểm trong vòng làm thay đổi giá trị nimber tổng của mẫu hình-gọi chúng là "mẫu hình sai", ta xét mẫu hình sai đơn giản nhất trong số chúng, "đơn giản nhất" được định nghĩa như sau: hình này có số đoạn ít nhất, nếu tồn tại nhiều hình có số đoạn bằng nhau, chọn hình có số điểm ít nhất. Hình này sẽ buộc phải thỏa mãn các tính chất sau: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1/ Sự hợp nhất các điểm ở bất cứ vòng nào trong mẫu hình này đều làm thay đổi nimber của hình, vì nếu không, ta sẽ thu được 1 hình sai đơn giản hơn, vi phạm giả thiết hình sai ban đầu là đơn giản nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2/ Hình này chỉ gồm 1 cây, nếu có nhiều cây tách biệt nhau trên mặt đất, chọn ra 1 cây có chứa vòng, xét mẫu hình chỉ gồm cây này, sự hợp nhất vòng trong cây không làm thay đổi nimber của cây (vì hình này đơn giản hơn hình ban đầu gồm nhiều cây, hình ban đầu là hình sai đơn giản nhất, nên mọi hình đơn giản hơn nó đều không phải hình sai) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Sự hợp nhất vòng ở cây này không làm thay đổi nimber tổng của hình ban đầu. Mặt khác bất kỳ cây đơn lẻ (chứa vòng) nào trong mẫu hình ban đầu cũng có đặc điểm này  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Hợp nhất bất cứ vòng nào trong mẫu hình ban đầu đều không thay đổi nimber tổng, vi phạm giả thiết đây là 1 mẫu hình sai. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•3/ Không có bất kỳ 2 điểm nào được nối với nhau bởi 3 "tuyến đường" khác nhau (giữa các tuyến đường không có đoạn chung)-nói cách khác là 1 cấu trúc vòng kép. Nếu tồn tại 1 hình như vậy, gọi nó là $G$ , và gọi hình $H$ là hình được tạo ra khi hợp nhất 2 điểm kể trên trong $G$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Nimber của $G$ và nimber của $H$ không bằng nhau (theo •1). Nếu vậy mẫu hình $GH$ , gồm cả $G$ và $H$ (đứng tách rời) phải có nimber $≠ 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Người chơi trước tồn tại 1 nước đi để đưa mẫu hình về nimber $= 0$ , vì mỗi nước đi chỉ tác động lên $G$ hoặc $H$ và có 1 sự tương đồng giữa các đoạn của $G$ và $H$ , hãy để cho người chơi sau đi 1 nước tương tự ở cây còn lại (nếu người đi trước cắt 1 đoạn ở $G$ , người đi sau cắt đoạn tương ứng ở $H$ và ngược lại), nước đi sau chắc chắn sẽ làm cho nimber của mẫu hình trở về $≠ 0$ . <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nước đi đầu tiên không thể xóa đi toàn bộ cấu trúc vòng kép ở 1 trong 2 cây, vì như vậy $G'$ và $H'$ (kết quả của $G$ và $H$ sau 2 nước đi) sẽ giống hệt nhau và nimber tổng lúc đó lại $= 0$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Vẫn còn lại ít nhất 1 vòng ở cấu trúc vòng kép của $G'$ , và sự hợp nhất của 2 điểm trong vòng đó tạo ra $H'$ , nhưng $G'$ và $H'$ có giá trị nimber khác nhau (vì tổng nimber của chúng $≠ 0$ ) , suy ra tồn tại hình $G'$ là mẫu hình sai đơn giản hơn $G$ , mâu thuẫn với giả thiết $G$ là hình sai đơn giản nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•4/ Các vòng trong hình này đều phải được gắn trực tiếp với mặt đất. Nếu có 1 vòng không được gắn trực tiếp với mặt đất, giả sử nó được nối với phần bên dưới qua 1 điểm, vòng này và các phần bên trên nó theo ***nguyên lý đại tràng (colon principle)*** đã nêu ở trên, có thể được tách ra và tính nimber riêng, trong đó sự hợp nhất của vòng cũng làm thay đổi giá trị nimber này (theo •1), vậy là toàn bộ cấu trúc này có thể được coi như 1 mẫu hình sai độc lập, và đơn giản hơn hình ban đầu, mâu thuẫn với giả thiết hình ban đầu là hình sai đơn giản nhất; còn nếu vòng đó được nối với phần bên dưới qua 2 điểm trở lên, nó sẽ hình thành cấu trúc vòng kép, trong đó có 2 điểm được kết nối với nhau bởi 3 tuyến đường, vi phạm •3. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•5/ Hình chỉ gồm 1 vòng duy nhất. Nếu có $\ge 2$ vòng, chúng đều nối trực tiếp với mặt đất (•4), và chúng đều thuộc cùng 1 cây (•2) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\rightarrow$ Chúng phải "dính" với nhau (có đoạn chung), nhưng như vậy lại làm hình thành cấu trúc vòng kép, vi phạm •3. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Kết luận:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Từ 5 tính chất trên, ta thấy rằng mẫu hình đang tìm kiếm phải có dạng "cỏ mọc trên cây cầu" đã xét ở trên hình minh họa trường hợp 2, nhưng như đã chứng minh, mô hình này lại tuân theo ***nguyên lý hợp nhất (fusion principle)***, nó không phải 1 mẫu hình sai <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ ***Chứng minh cho nguyên lý hợp nhất đã được hoàn thành*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Với nguyên lý đại tràng và nguyên lý hợp nhất, một cây phức tạp có thể được quy về các hình đơn giản hơn, và từ đó dễ dàng tính ra giá trị nimber của chúng, minh họa như hình dưới đây.  <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/e547a450-8ecf-4213-878b-685e7e64e84d)
</div>


















