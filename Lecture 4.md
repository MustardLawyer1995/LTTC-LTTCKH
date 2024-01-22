# Bài toán đồng xu giả 
### 1. Cây quyết định 
Chúng ta cùng nhau khám phá và phân tích bài toán mở đầu như sau: “Cho $n$ đồng xu, trong đó có $n-1$ đồng xu thật và 1 đồng xu giả nhẹ hơn các đồng khác. Hãy sử dụng cân dĩa ***(cân Rô-béc-van)*** để xác định đồng xu giả đó. 
#### *<ins>Định lí 1.1:</ins>* Mọi phương pháp cân đều cần ít nhất $\left\lceil {{{\log }_3}n} \right\rceil$ lần cân để xác định đồng xu giả. 
Ta chứng minh định lí này bằng cách sử dụng *cây quyết định*. Với mỗi phương pháp cân, ta sẽ xây dựng 1 cây như sau: Các đỉnh sẽ là trạng thái thông tin đã biết sau mỗi lần cân. Bắt đầu từ gốc cây là trạng thái ban đầu khi chưa có thông tin gì. Từ mỗi trạng thái thông tin, ta có thể làm một trong hai điều sau đây: 
-	Cân xu theo một cách duy nhất dựa vào trạng thái thông tin hiện tại. Có khộng quá 3 khả năng xảy ra (bên trái nặng hơn, bên phải nặng hơn hoặc cân thăng bằng) vì có thể có tối đa ba cách để thực hiện tiếp lần cân tiếp theo. Với mỗi khả năng, ta thu được một trạng thái thông tin mới. Ta thêm các trạng thái mới ở dạng đỉnh con của trạng thái trước. 
-	Kết luận đã tìm được đồng xu giả dựa trên trạng thái thông tin hiện tại. Đỉnh tương ứng là lá của cây, và số lần cân để đi tới trạng thái thông tin này là chiều sâu của đỉnh đó. <br>
Như vậy cây quyết định là một *cây tam phân (ternary tree)*, tức là mỗi đỉnh có không quá 3 đỉnh con. Ở mỗi lá cây, ta kết luận được đã tìm được đồng xu giả, nên cây quyết định cần ít nhất $n$ lá.
#### *<ins>Ví dụ 1.2:</ins>* Đây là cây quyết định với trường hợp 5 đồng xu (tức $n=5$ ).

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/7a46f667-f34e-4c4d-a35d-f8f6748c0c71)

Chiều cao của một cây là ***chiều sâu của đỉnh sâu nhất của cây*** , hay nói cách khác là thế hệ muộn nhất mà cây vẫn còn đỉnh. Ở đây, chiều cao của cây quyết định chính là số lần cân trong trường hợp xấu nhất (nghĩa là số lần cân để chắc chắn xác định được đồng xu giả).
#### *<ins>Bổ đề 1.3:</ins>* Cho $T$ là một cây $D-$ phân. Ở thế hệ thứ $k$ , cây có không quá $D^k$ đỉnh. Nói riêng, nếu chiều cao của $T$ là $h$ thì nó không có $D^h$ lá. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta quy nạp theo $k$ . Khi $k=0$ , gốc cây là đỉnh duy nhất ở thế hệ thứ $0$ . Khi $k>0$ , thế hệ thứ $k-1$ có không quá $D^{k-1}$  đỉnh (giả thiết quy nạp), mỗi đỉnh có không quá $D$ đỉnh con, do đó thế hệ thứ $k$ có không quá $D^{k-1} \times D = D^{k}$ đỉnh <br> 
$\Longrightarrow$ Hoàn tất chứng minh *bổ để 1.3* <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 1.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với mỗi phương pháp cân, ta xây dựng cây quyết định tương ứng. Số lần cân trong trường hợp xấu nhất là chiều cao $h$ của cây. Cây có không quá $3^h$ lá. Mặt khác, cây cần ít nhất $n$ lá, do đó ta có đánh giá như sau: ${3^h} \ge n$ tức $h \ge \left\lceil {{{\log }_3}n} \right\rceil , \text{ } \forall h { \in \mathbb{Z}}$ <br>
$\Longrightarrow$ Hoàn tất chứng minh *định lí 1.1* <br>

*<ins>Chú ý:</ins>* Ta có thể xét các biến thể của bài toán: Nếu chưa biết đồng xu giả là nặng hơn hay nhẹ hơn đồng thật, thì cây cần có ít nhất $2n$ lá (vì có $2n$ trường hợp có thể xảy ra, đồng xu giả là một trong $n$ đồng, và nó có thể nặng hơn hoặc nhẹ hơn đồng thật), vì thế cần ít nhất $\left\lceil {{{\log }_3}\left( {2n} \right)} \right\rceil$ lần cân. Tương tự, nếu thêm giả thiết rằng trong $n$ đồng xu có thể có đồng giả hoặc không, thì kết quả là ta cần ít nhất $\left\lceil {{{\log }_3}\left( {2n+1} \right)} \right\rceil$ lần cân... <br>
### 2. Entrophy thông tin <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta tìm cách cân với tìm cách cân với $\left\lceil {{{\log }_3}\left( {2n} \right)} \right\rceil$ lần cân (trong trường hợp xấu nhất). Giá trị ${\log _3}n$ gợi cho chúng ta việc liên tục chia đống xu đã cho thành 3 phần bằng nhau nhất có thể. Phương pháp cân của chúng ta sẽ thực hiện tương tự như trong ***Ví dụ 1.2***. Chúng ta sẽ thử giải thích heuristic này bằng khái niệm ***entropy thông tin*** . <br>
#### *<ins>Định nghĩa 2.1:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Cho $X$ là biến ngẫu nhiên rời rạc với $n$ giá trị ${x_1},{x_2},...{x_n}$ và phân bố xác suất tương ứng đó là ${p_1},{p_2},...{p_n}$ . Ta thiết lập định nghĩa entrophy của nó bởi hệ thức được biểu diễn như sau: 
```math
{H\left( X \right): = \sum\limits_{i = 1}^n { - {p_i}\log \left( {{p_i}} \right)}  = \sum\limits_{i = 1}^n {{p_i}\log \left( {\frac{1}{{{p_i}}}} \right)} }
```
&nbsp;&nbsp;&nbsp;&nbsp;Trong đó ta quy ước $0\log 0: = 0$ với logarit có thể lấy từ bất kì cơ số nào, để đơn giản cho việc tính đạo hàm thì ta lấy cơ số $e$ đó là logarit tự nhiên, khi đó nó chính là ***entrophy tự nhiên***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vì $0 \le {p_i} \le 1,\forall i = \overline {1,2,...,n}$ nên luôn có $H\left( X \right) \ge 0$ và đẳng thức xảy ra khi và chỉ khi ${p_i} = 1$ với $i$ nào đó và ${p_j} = 0$ với mọi $j \ne i$ , nói cách khác $X$ là ***một giá trị tất định***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Entrophy thông tin là đại lượng đo độ bất định của giá trị của 1 biến ngẫu nhiên. Một cách tương đương, nó đo đại lượng thông tin trung bình nhận được sau khi thực hiện phép đo giá trị của biến ngẫu nhiên đó. Nếu entrophy bằng không (giá trị tất định) thì việc đo giá trị không mang lại thêm thông tin gì. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi $n$ cố định, ta áp dụng bất đẳng thức Jensen cho hàm lõm $log$ , khi đó ta có đánh giá sau:
```math
H\left( X \right): = \sum\limits_{i = 1}^n {{p_i}\log \left( {\frac{1}{{{p_i}}}} \right)}  \le \log \sum\limits_{i = 1}^n {\left( {{p_i}\frac{1}{{{p_i}}}} \right)}  = \log \sum\limits_{i = 1}^n {\left( 1 \right)}  = \log \left( {\underbrace {1 + 1 + ... + 1}_{n{\rm{ lan}}}} \right) = \log n
```
&nbsp;&nbsp;&nbsp;&nbsp;Dấu bằng xảy ra khi và chỉ khi ${p_1} = ... = {p_n} = \frac{1}{n}$ , nghĩa là $X$ phân bố đều tức có độ bất định thông tin cao nhất. 
&nbsp;&nbsp;&nbsp;&nbsp;Bây giờ, ta chia $n$ đồng xu thành 3 đống, 1 đống có $n-2a$ đồng và hai đống còn lại mỗi đống có $a$ đồng. Ta thực hiện cân hai đống có $a$ đồng, và từ đó có thể xác định được đồng xu giả nằm ở đống nào trong 3 đống. Như vậy, “đống xu chứa đồng giả” là một biến ngẫu nhiên nhận 3 giá trị, với phân bố xác suất theo quy tắc nhân chính là $\left( {\frac{{n - 2a}}{n}} \right)\left( {\frac{a}{n}} \right)\left( {\frac{a}{n}} \right)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy entrophy của nó là: 
```math
H\left( a \right) =  - \frac{{n - 2a}}{n}\log \left( {\frac{{n - 2a}}{n}} \right) - \frac{{2a}}{n}\log \left( {\frac{{2a}}{n}} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ chọn $a$ sao cho lượng thông tin $H(a)$ thu được là lớn nhất. Như nhận xét trên, ta thấy rằng $H(a)$ sẽ đạt max khi và chỉ khi $a \approx \frac{n}{3}$ . Cụ thể hơn, ta có thể đặt $x = \frac{a}{n}$ và xét hàm biến thực sau:   
```math
h\left( x \right) =  - \left( {1 - 2x} \right)\log \left( {1 - 2x} \right) - 2x\log x
```
&nbsp;&nbsp;&nbsp;&nbsp;Ta có $h'\left( x \right) = 2\left( {\log \left( {1 - 2x} \right) - \log x} \right)$ . Nhận xét được $h\left( x \right)$ đồng biến trên $\left[ {0;\frac{1}{3}} \right]$ và nghịch biến trên $\left[ {\frac{1}{3};1} \right]$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi đó $h\left( a \right)$ đạt max khi $a$ nhận ra một trong 2 giá trị nguyên gần $\frac{n}{3}$ nhất (ta sẽ xác định sau đây). <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 1:* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $n=3k$ thì dĩ nhiên ta chọn $a=k$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 2:* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $n=3k+1$ thì cần chọn $a=k$ hoặc $a=k+1$ , khi đó ta có 
```math
H\left( k \right) =  - \frac{{k + 1}}{n}\log \frac{{k + 1}}{n} - \frac{{2k}}{n}\log \frac{{2k}}{n};H\left( {k + 1} \right) =  - \frac{{k - 1}}{n}\log \frac{{k - 1}}{n} - \frac{{2\left( {k + 1} \right)}}{n}\log \frac{{k + 1}}{n}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Theo bất đẳng thức Jensen ta lại có đánh giá sau: 
```math
\frac{{k + 1}}{n}\log \frac{{k + 1}}{n} + \frac{{k - 1}}{n}\log \frac{{k - 1}}{n} > \frac{{2k}}{n}\log \frac{k}{n} \text{   tức   } H\left( k \right) > H\left( {k + 1} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Suy ra ở trường hợp này cách chia tốt nhất chính là $k,k,k + 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 3:* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $n=3k+2$ thì cần chọn $a=k$ hoặc $a=k+1$ , khi đó ta có 
```math
H\left( k \right) =  - \frac{{k + 2}}{n}\log \frac{{k + 2}}{n} - \frac{{2k}}{n}\log \frac{{2k}}{n};H\left( {k + 1} \right) =  - \frac{k}{n}\log \frac{k}{n} - \frac{{2\left( {k + 1} \right)}}{n}\log \frac{{k + 1}}{n}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Theo bất đẳng thức Jensen ta lại có đánh giá sau: 
```math
\frac{{k + 2}}{n}\log \frac{{k + 2}}{n} + \frac{k}{n}\log \frac{k}{n} > \frac{{2\left( {k + 1} \right)}}{n}\log \frac{{k + 1}}{n} \text{   tức   } H\left( k \right) < H\left( {k + 1} \right)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Suy ra ở trường hợp này cách chia tốt nhất chính là $k,k+1,k + 1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sau lần cân đầu tiên với $n$ đồng xu, ta xác định được đồng xu giả nằm trong 1 trong 3 đống xu nhỏ. Ta áp dụng lại cách cân này với đống xu nhỏ đó. <br>

#### *<ins>Mệnh đề 2.2:</ins>* Cách cân như trên cần không quá $\left\lceil {{{\log }_3}n} \right\rceil$ lần cân trong mọi trường hợp. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Quy nạp theo số xu $n$ . Với $n \le 2$ , ta không có gì để chứng minh. Giả sử $n \ge 3$ . Nếu $n=3k$ thì ở lần cân tiếp theo, ta cần cân $k$ đồng xu. Khi ấy theo nguyên lí quy nạp, cần không quá:
```math
{1 + \left\lceil {{{\log }_3}k} \right\rceil  = \left\lceil {1 + {{\log }_3}k} \right\rceil  = \left\lceil {{{\log }_3}\left( {3k} \right)} \right\rceil  = \left\lceil {{{\log }_3}n} \right\rceil } \text{    (lần cân)}
```
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $n = 3k + r,r \in  {1,2}$ , thì ở lần cân tiếp theo, ta cần $k$ hoặc $k+1$ đồng xu. Khi ấy theo nguyên lí quy nạp, cần không quá:
```math
{1 + \left\lceil {{{\log }_3}\left( {k + 1} \right)} \right\rceil  = \left\lceil {1 + {{\log }_3}\left( {k + 1} \right)} \right\rceil  = \left\lceil {{{\log }_3}\left( {3k + 3} \right)} \right\rceil } \text{    (lần cân)}
```
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $h = \left\lceil {{{\log }_3}n} \right\rceil$ thì $h \ge 1$ và ${3^{h - 1}} < n \le {3^h}$ . Do ${3^h}$ là bội của 3 nên ${3^{h - 1}} < n < 3k + 3 \le {3^h}$ . <br>
$\Longrightarrow$ $\left\lceil {{{\log }_3}\left( {3k + 3} \right)} \right\rceil  = h = \left\lceil {{{\log }_3}n} \right\rceil$ <br>
&nbsp;&nbsp;Tóm lại ta kết luận cần không quá $\left\lceil {{{\log }_3}n} \right\rceil$ lần cân. 
### 3. Mã Huffman
