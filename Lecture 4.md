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
Ta tìm cách cân với tìm cách cân với $\left\lceil {{{\log }_3}\left( {2n} \right)} \right\rceil$ lần cân (trong trường hợp xấu nhất). Giá trị ${\log _3}n$ gợi cho chúng ta việc liên tục chia đống xu đã cho thành 3 phần bằng nhau nhất có thể. Phương pháp cân của chúng ta sẽ thực hiện tương tự như trong ***Ví dụ 1.2***. Chúng ta sẽ thử giải thích heuristic này bằng khái niệm ***entropy thông tin*** . <br>
#### *<ins>Định nghĩa 2.1:</ins>*
Cho $X$ là biến ngẫu nhiên rời rạc với $n$ giá trị ${x_1},{x_2},...{x_n}$ và phân bố xác suất tương ứng đó là ${p_1},{p_2},...{p_n}$ . Ta thiết lập định nghĩa entrophy của nó bởi hệ thức được biểu diễn như sau: 
```math
{H\left( X \right): = \sum\limits_{i = 1}^n { - {p_i}\log \left( {{p_i}} \right)}  = \sum\limits_{i = 1}^n {{p_i}\log \left( {\frac{1}{{{p_i}}}} \right)} }
```
















