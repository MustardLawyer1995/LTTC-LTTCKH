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

Chiều cao của một cây là ***chiều sâu của đỉnh sâu nhất của cây*** , hay nói cách khác là thế hệ muộn nhất mà cây vẫn còn đỉnh. Ở đây, chiều cao của cây quyết định chính là số lần cân trong trường hợp xấu nhất (nghĩa là số lần cân để chắc chắn xác dịnh đồng xu giả).
