# Bài toán đồng xu giả 
### 1. Cây quyết định 
Chúng ta cùng nhau khám phá và phân tích bài toán mở đầu như sau: “Cho $n$ đồng xu, trong đó có $n-1$ đồng xu thật và 1 đồng xu giả nhẹ hơn các đồng khác. Hãy sử dụng cân dĩa ***(cân Rô-béc-van)*** để xác định đồng xu giả đó. 
#### *<ins>Định lí 1.1:</ins>* Mọi phương pháp cân đều cần ít nhất $\left\lceil {{{\log }_3}n} \right\rceil$ lần cân để xác định đồng xu giả. 
Ta chứng minh định lí này bằng cách sử dụng *cây quyết định*. Với mỗi phương pháp cân, ta sẽ xây dựng 1 cây như sau: Các đỉnh sẽ là trạng thái thông tin đã biết sau mỗi lần cân. Bắt đầu từ gốc cây là trạng thái ban đầu khi chưa có thông tin gì. Từ mỗi trạng thái thông tin, ta có thể làm một trong hai điều sau đây: 
-	Cân xu theo một cách duy nhất dựa vào trạng thái thông tin hiện tại. Có khộng quá 3 khả năng xảy ra (bên trái nặng hơn, bên phải nặng hơn hoặc cân thăng bằng) vì có thể có tối đa ba cách để thực hiện tiếp lần cân tiếp theo. Với mỗi khả năng, ta thu được một trạng thái thông tin mới. Ta thêm các trạng thái mới ở dạng đỉnh con của trạng thái trước. 
-	Kết luận đã tìm được đồng xu giả dựa trên trạng thái thông tin hiện tại. Đỉnh tương ứng là lá của cây, và số lần cân để đi tới trạng thái thông tin này là chiều sâu của đỉnh đó. <br>
Như vậy cây quyết định là một *cây tam phân (ternary tree)*, tức là mỗi đỉnh có không quá 3 đỉnh con. Ở mỗi lá cây, ta kết luận được đã tìm được đồng xu giả, nên cây quyết định cần ít nhất $n$ lá.
#### *<ins>Ví dụ 1.2:</ins>* Đây là cây quyết định với trường hợp 5 đồng xu (tức $n=5$ ).

<div align="center">
  
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/7a46f667-f34e-4c4d-a35d-f8f6748c0c71)
</div>

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
H(X) := \sum_{i = 1}^n p_i \log \left( \frac{1}{p_i} \right) \leq \log \left( \sum_{i = 1}^n \left( p_i \frac{1}{p_i} \right) \right) = \log \left( \sum_{i = 1}^n 1 \right) = \log \left( \underbrace{1 + 1 + \ldots + 1}_{\text{n times}} \right) = \log n
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
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $n = 3k + r,r \in  \\{ 1,2 \\}$ , thì ở lần cân tiếp theo, ta cần $k$ hoặc $k+1$ đồng xu. Khi ấy theo nguyên lí quy nạp, cần không quá:
```math
{1 + \left\lceil {{{\log }_3}\left( {k + 1} \right)} \right\rceil  = \left\lceil {1 + {{\log }_3}\left( {k + 1} \right)} \right\rceil  = \left\lceil {{{\log }_3}\left( {3k + 3} \right)} \right\rceil } \text{    (lần cân)}
```
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $h = \left\lceil {{{\log }_3}n} \right\rceil$ thì $h \ge 1$ và ${3^{h - 1}} < n \le {3^h}$ . Do ${3^h}$ là bội của 3 nên ${3^{h - 1}} < n < 3k + 3 \le {3^h}$ . <br>
$\Longrightarrow$ $\left\lceil {{{\log }_3}\left( {3k + 3} \right)} \right\rceil  = h = \left\lceil {{{\log }_3}n} \right\rceil$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tóm lại ta kết luận cần không quá $\left\lceil {{{\log }_3}n} \right\rceil$ lần cân. 
### 3. Mã Huffman <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trước khi đến với vấn đề tìm cách cân với số lần cân trung bình nhỏ nhất, chúng ta giới thiệu bài toán có vẻ không liên quan sau đây về mã hóa và nén dữ liệu. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bây giờ giả sử chúng ta cần mã hóa 1 văn bản sang hệ nhị phân (chẳng hạn, văn bản chỉ gồm $26$ kí tự in thường trong bảng chữ cái tiếng Anh). Tất nhiên chúng ta muốn rằng từ bản mã hóa phải dịch lại nguyên vẹn được văn bản ban đầu. Cách làm ngây thơ nhất là lấy $2^{5}=32$ chuỗi nhị phân với độ dài 5 để mã hóa: 
```math
{a \to 00000,{\rm{      }}b \to 00001,{\rm{      }}c \to 00010,......}
```
&nbsp;&nbsp;&nbsp;&nbsp;Từ bản mã hóa, ta dịch được từng chuỗi 5 kí tự nhị phân để thu được văn bản ban đầu. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta muốn làm tốt hơn thế, nhưng tất nhiên nếu chỉ dùng $2^{4}=16$ chuỗi nhị phân thì không đủ cho $26$ chữ cái. Ta muốn bản mã hóa có độ dài ngắn nhất có thể. Khi đó, với ý tưởng của mã hóa Huffman, ta sẽ dùng một bản mã với độ dài của từng ký tự có thể khác nhau. Lúc ấy ta phát sinh các vấn đề như sau: <br>
#### *<ins>Ví dụ 3.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử ta mã hóa $a \to 0,b \to 1,c \to 01$ , khi đó từ bản mã hóa $01$ ta có thể thu được hai văn bản ban đầu đó là $ab$ hoặc $c$ (không duy nhất). Đây chính là điều ta muốn tránh <br>
#### *<ins>Định nghĩa 3.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một mã được gọi là ***phi tiền tố (prefix-free)*** nếu không có hai ký tự khác nhau được mã hóa thành hai chuỗi nhị phân $,t$ với $s$ là tiền tố của $t$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chú ý:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đối với mã phi tiền tố, không ký tự nào được phép mã hóa thành chuỗi rỗng (vì chuỗi rỗng là tiền tố của mọi chuỗi khác $\rightarrow$ điều này là mâu thuẫn). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử ta mã hóa bằng một mã phi tiền tố. Để giải mã, ta cần đọc bản mã hóa từ trái sang phải. Khi gặp một chuỗi nhị phân trùng với mã hóa của một chữ cái thì ta dịch nó ra ký tự đó. <br>
#### *<ins>Bổ đề 3.3:</ins>* <br>
Mã phi tiền tố đảm bảo việc dịch về văn bản ban đầu là duy nhất (nếu việc dịch là thực hiện được) <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Gọi $s$ là bản mã hóa. Ta sử dụng nguyên lí quy nạp theo độ dài của bản mã hóa. Nếu $s$ là mã rỗng thì tất nhiên đây là văn bản rỗng. Giả sử $s$ không là chuỗi rỗng và $s$ được dịch đồng thời theo hai cách tức ta có: 
<p align="center">${s = {s_1}{s_2}....{s_n} = {t_1}{t_2}....{t_m}}$ với $s_{j},t_{j}, \forall j=1,2,...n$ là chữ cái của mã hóa nào đó</p> 

&nbsp;&nbsp;&nbsp;&nbsp;Rõ ràng $s_1$ là tiền tố của $t_1$ và ngược lại, do là mã phi tiền tố nên $s_{1}=t_{1}$ . Ngoài ra $s_1$ và $t_1$ đều không phải là chuỗi rỗng tức ta có: ${{s_2}....{s_n} = {t_2}....{t_m}}$ . Hai vế lúc này đều là một chuỗi nhỏ hơn $s$ , nên theo nguyên lí quy nạp ta suy ra $m=n$ tức ${s_i} = {t_i},\forall i = \overline {2,3,....n}$ .
#### *<ins>Ví dụ 3.4:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chẳng hạn ta có 4 chữ cái $a,b,c,d$ , khi đó ta có mã phi tiền tố như sau: 
```math
{a \to 0,{\rm{      }}b \to 10,{\rm{      }}c \to 110,{\rm{      }}d \to 111}
```
&nbsp;&nbsp;&nbsp;&nbsp;Bản mã hóa $1100010111$ được dịch lại thành văn bản $caabd$ (dễ dàng kiểm tra được rằng không có dấu hiệu thiếu nhất quán khi dịch từ trái sang phải). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mã Huffman là một mã phi tiền tố. Ý tưởng của mã là chữ cái nào xuất hiện càng nhiều thì độ dài của nó càng ngắn
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử ta có bảng chữ cái ${a_1},{a_2}....{a_n}$ với tần suất xuất hiện của các chữ cái là ${p_1},{p_2}....{p_n}$ . Ứng với mỗi phương pháp mã hóa, gọi ${\ell _i}$ là độ dài của xâu mã ký tự ${a_i},\forall i = \overline {1,2,...n}$ . Độ dài trung bình của mỗi ký tự của phương pháp mã hóa này là: 
```math
{E = {p_1}{\ell _1} + {p_2}{\ell _2} + ... + {p_n}{\ell _n}}
```
&nbsp;&nbsp;&nbsp;&nbsp;Đến đây, ta có mục tiêu là cần tìm phương pháp mã hóa sao cho $E$ nhỏ nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mã Huffman được xây dựng qua cây Huffman $T$ như sau: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Ban đầu, $T$ gồm $n$ đỉnh ứng với $n$ ký tự ban đầu và gán cho chúng tần suất tương ứng. Hàng chờ của chúng ***(queue)*** cũng gồm $n$ ký tự ban đầu. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Chọn hai đỉnh với tần suất nhỏ nhất, chẳng hạn là $a_i$ và $a_j$ . Xóa chúng khỏi queue, sau đó thêm một đỉnh mới vào cha của hai đỉnh nảy vào $T$ , gán cho nó tần suất là tổng $p_{i}+p_{j}$ . Tiếp đến ta thêm một ký tự giả $(a_{i};a_{j})$ vào queue. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Lặp lại bước 2 cho đến khi queue chỉ còn một ký tự. Khi ấy ký tự đó chính là ***gốc cây*** (tần suất bằng 1) . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Khi đó cây Huffman thu được là một ***cây nhị phân đầy đủ*** (mỗi đỉnh không phải là lá và có đúng 2 đỉnh con). Gán các mã cho đỉnh từ gốc cây như sau: Gốc cây là chuỗi trống. Nếu một đỉnh có mã là $s$ thì hai đỉnh con của nó có mã là $s_0$ và $s_1$ . Các kí tự của bảng chữ cái ban đầu đều là lá cây, vì thế dễ thấy mã thu được là phi tiền tố. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi giải mã, chúng ta bắt đầu từ gốc cây. Đọc dần các kí tự của bản mã hóa, Mỗi khi đọc ký tự 0  hoặc 1 thì ta đi xuống 1 trong 2 đỉnh con của đỉnh hiện tại (tùy theo ký tự đọc vào là 0 hay 1). Khi đi đến lá cây, ta lấy kí tự ở lá đó để thêm vào văn bản dịch, rồi sau đó quay lại gốc cây. <br>
#### *<ins>Ví dụ 3.5:</ins>* <br>
Sau đây là ví dụ về xây dựng mã Huffman <br>

<div align="center">
  
| Bảng chữ cái | $a$ | $b$ | $c$ | $d$ | $e$ |
|:------------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| Tần suất     | $0.25$   | $0.15$   | $0.20$   | $0.10$   | $0.30$   |
</div>
Thứ tự từng bước là: 

```math
a,b,c,d,e \to \left( {d,b} \right),c,a,e \to \left( {d,b,c} \right),a,e \to \left( {d,b,c} \right),\left( {a,e} \right) \to \left( {d,b,c,a,e} \right)
```
Khi đó ta có hình vẽ xây dựng cây như sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/b6639a9e-f3cb-43d5-8ffa-318585fb0e3b)
</div>
Độ dài trung bình khi mã hóa một kí tự của mã vừa xây dựng là:

```math
{0,25.2 + 0,15.3 + 0,2.3 + 0,1.3 + 0,3.2 = 2,45}
```
#### *<ins>Bổ đề 3.6:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử $n \ge 3$ và ${a_1},{a_2}....{a_n}$ là một bảng chữ cái có tần suất tương ứng ${p_1} \ge {p_2} \ge ... \ge {p_n}$ . Trong đó ta kí hiệu $\\{ 0,1 \\}^{*}$ là tập tất cả các chuỗi nhị phân có độ dài hữu hạn. Tồn tại một hàm mã hóa có dạng là: $c: \\{ {a_1},{a_2}....{a_n} \\}$ $\to \\{ 0,1 \\}^{\*}$ , tối ưu so với các mã tiền tố khác, ta có: ${p_1}\left| {c\left( 1 \right)} \right| + {p_2}\left| {c\left( 2 \right)} \right| + ... + {p_n}\left| {c\left( n \right)} \right|$ nhỏ nhất với kí hiệu $\left| s \right|$ là độ dài chuỗi nhị phân $s$ , thỏa mãn các yếu tố sau đây: 

-	Tồn tại một chuỗi nhị phân $w$ với $c\left( {n - 1} \right) = w0$ và $c\left( n \right) = w1$ .
-	Xét bảng chữ cái ${b_1},{b_2}...{b_{n - 1}}$ với tần suất ${q_1},{q_2}...{q_{n - 1}}$ 
 cho bởi: ${q_1} = {p_1}....{q_{n - 2}} = {p_{n - 2}},{q_{n - 1}} = {p_{n - 1}} + {p_n}$  và hàm mã hóa $c': \\{ {b_1},{b_2}....{b_n} \\}$ $\to \\{ 0,1 \\}^{\*}$ là cho bởi $c'\left( {{b_1}} \right) = c\left( {{a_1}} \right),....,c'\left( {{b_{n - 2}}} \right) = c\left( {{a_{n - 2}}} \right),c'\left( {{b_{n - 1}}} \right) = w$ <br>
  Khi đó ta nhận thấy $c'$ tối ưu trên bảng chữ cái $\\{ {b_1},{b_2}....b_{n - 1} \\}$ <br>

Khi ấy, từ bổ đề trên, ta suy ra mã Huffman là mã tối ưu. <br>
### 4. Mã Huffman $D-$ phân và ứng dụng <br>
&nbsp;&nbsp;&nbsp;&nbsp;Giả sử bây giờ bảng chữ cái dùng để mã hóa có $D$ kí tự thay vì chỉ hai ký tự $0,1$ . Ta vẫn sẽ xây dựng mã Huffman dưới dạng cây $D-$ phân đầy đủ. Ở mỗi bước xây dựng cây, ta chọn $D$ đỉnh với tần suất nhỏ nhất rồi gộp lại thành đỉnh mới. Khi ấy ta có một chút vấn đề như sau: <br>
#### *<ins>Bổ đề 4.1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một cây $D-$ phân đầy đủ thì có số lá  $\equiv {1^{}}^{}\left( {\bmod D - 1} \right)$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một cây $D-$ phân đầy đủ được xây dựng bằng cách trồng thêm $D-$ lá vào lá cũ ở mỗi bước, nghĩa là số lá tăng thêm $D-1$ (lá cũ trở thành đỉnh trong). Bắt đầu từ cây chỉ có gốc có số lá bằng 1, ta có điều phải chứng minh. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, số kí tự của bảng chữ cái ban đầu phải $\equiv {1^{}}^{}\left( {\bmod D - 1} \right)$ để ta có thể xây dựng cây Huffman $D-$ phân. Tuy nhiên ta có thể khắc phục rất đơn giản: thêm (không quá $D-2$ ) kí tự giả vào bảng chữ cái với tần suất bằng 0, rồi xây dựng cây Huffman như bình thường. (Với $D=2$ ,  ta không cần thêm gì cả, với  , ta chỉ cần thêm một kí tự giả nếu số kí tự ban đầu là số chẵn). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta bắt đầu xây dựng cây Huffman tam phân bằng cách bắt đầu gán tất cả các đỉnh trọng 1 (thay vì tần suất $\frac{1}{n}$ , nhằm đơn giản hóa việc tính toán). Từ đó ta lại tìm cách cân tối ưu (số lần cân trung bình ít nhất). <br>

#### *<ins>Ví dụ 4.2:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đây là ví dụ về cây Huffman với 11 đồng xu. <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/1a55eb36-13f9-4534-9e14-5833b9dcba03)
</div>
&nbsp;&nbsp;&nbsp;&nbsp;Trước hết ta chia lấy 6 đồng xu chia thành 2 đống đều nhau rồi đem cân. Nếu cân lệch thì đồng xu giả nằm trong đống nhẹ hơn. Nếu cân thăng bằng thì đồng xu giả nằm trong 5 đồng xu còn lại. Ta tiếp tục cân và đi xuống dưới theo cây Huffman đã xây dựng. Số lần cân trung bình bằng: 

```math
\frac{8}{{11}}.2 + \frac{3}{{11}}.3 = \frac{{25}}{{11}}
```
&nbsp;&nbsp;&nbsp;&nbsp;Nếu cân theo cách tối đa hóa entrophy thông tin như nêu mục trước thì ta có sơ đồ cây như sau: 
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/9e76f09b-3e1a-4971-9a3a-2fb21ec2c720)
</div>
&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy số lần cân trung bình là:

```math
\frac{7}{{11}}.2 + \frac{4}{{11}}.3 = \frac{{26}}{{11}}
```
&nbsp;&nbsp;&nbsp;&nbsp;Phương pháp cân này là một cách của *thuật toán tham lam*, nghĩa là làm tốt nhất có thể qua từng bước. Tuy nhiên, điều đó không có nghĩa rằng cách làm sau cùng chính là cách làm tối ưu *(tối ưu địa phương không thể suy ra được tối ưu toàn cục)* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Không phải lúc này ta cũng xây dựng được một cách cân từ cây Huffman. Chẳng hạn với $n=6$ , ta phải thêm 1 đỉnh giả có trọng 0. Khi ấy cây Huffman lúc này được biểu diễn như sau: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/7a50fac9-9b08-4a15-be37-d61fe52752a0)
</div>
&nbsp;&nbsp;&nbsp;&nbsp;Ta gọi 1 đỉnh với ba đỉnh con có trọng đôi một khác nhau là một đỉnh xấu. Rõ ràng, nếu gốc cây là một đỉnh xấu thì không thể cân theo cây Huffman được. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu cây Huffman có đỉnh xấu, nhưng gốc cây không phải đỉnh xấu, ta vẫn có thể ứng biến như sau. Chẳng hạn xét trường hợp $n=12$ ta có: <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/885bedd0-10c1-467b-ada0-b6c78a2bf2c8)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Để cân theo cây này, ta chia thành ba đống với số xu lần lượt là $6,3,3$ . Cân 2 đống với 3 đồng xu. Nếu xảy ra trường hợp cân thăng bằng thì đồng xu giả này nằm trong 6 đồng còn lại và quy về trường hợp $n=6$ như hình trước. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tuy nhiên, ta lại dùng được cây Huffman theo cách như sau: ta chia 6 đồng xu này thành ba đống với số lượng lần lượt là $2,1,3$ . Ta có thể xác định đồng xu giả nằm ở đống nào bằng cách mượn 1 đồng xu thật (nhờ cân lần đầu, ta đã biết chắc 6 đồng xu là thật), thêm vào 1 đống có 1 đồng, rồi cân nó cùng với đống có 2 đồng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tổng quát, ta luôn cân được theo cây Huffman nếu có thêm $\left\lfloor {\frac{n}{2}} \right\rfloor$ đồng xu thật làm mẫu. Thật vậy, ta đang ở 1 đỉnh có trọng là $m$ (nghĩa là ta biết đồng xu giả nằm trong $m$ đồng xu nào đó), $m \le n$ . Dựa vào các đỉnh con của đỉnh này trong cây Huffman để chia $m$ đồng xu thành 3 đống, với trọng ${m_1} \le {m_2} \le {m_3}$ . Ít nhất 1 trong hai số lần lượt là ${m_3} - {m_2}$ và ${m_2} - {m_1}$ không vượt quá $\frac{m}{2} \le \frac{n}{2}$ . Vì thế ta có thể lấy $k \le \left\lfloor {\frac{n}{2}} \right\rfloor$ đồng xu thật làm mẫu sao cho để cân được ${m_2} + k$ với ${m_3}$ hoặc ${m_1} + k$ với ${m_2}$  



