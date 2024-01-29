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



























