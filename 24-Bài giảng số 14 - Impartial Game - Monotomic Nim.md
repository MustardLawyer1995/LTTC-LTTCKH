# Impartial Game - Monotomic Nim
&nbsp;&nbsp;&nbsp;&nbsp;Là một biến thể khác của nim game (xem lại ***bài giảng số 7a***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* Có nhiều đống vật thể (đồng xu/thẻ bài/bút chì/...) trên bàn, mỗi người khi đến lượt của mình phải lấy ít nhất 1 quân và chỉ được phép lấy từ 1 đống, các đống được sắp xếp theo thứ tự có số lượng quân tăng dần: $a_{1} \le a_{2} \le ... \le a_{n}$ ( $a_{i}$ là số lượng quân trong đống thứ $i$ ), chọn 1 đống để lấy, lấy bao nhiêu cũng được nhưng phải làm cho số lượng quân trong các đống vẫn xếp theo thứ tự như trước: $a_{1} \le a_{2} \le ... \le a_{n}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật normal:</ins>* ai không còn nước để đi thì thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật misere:</ins>* ai bị ép phải đi nước cuối cùng thì thua. <br>

&nbsp;&nbsp;&nbsp;&nbsp;1) Sự ràng buộc số lượng quân của các đống có thể nghiêm ngặt hơn $a_{1} < a_{2} < ... < a_{n}$ . Nhưng điều này có thể được giải quyết bằng cách đặt các đống mới có số lượng quân tương ứng: <br>

```math
b_{1}=a_{1};b_{2}=a_{2}-1;b_{3}=a_{3}-2;...;b_{i}=a_{i}-i+1;...;b_{n}=a_{n}-n+1
```
&nbsp;&nbsp;&nbsp;&nbsp;Khi đó: $b_{1} \le b_{2} \le ... \le b_{n}$ , và ta có thể áp dụng chiến lược của monotonic nim bản gốc. <br>
&nbsp;&nbsp;&nbsp;&nbsp;2) Cho một dãy ô vuông được đánh số từ 0 đến $m$ , có $n$ đồng xu (với $n < m$ ), mỗi xu được đặt vào 1 ô riêng biệt. Mỗi người chơi khi đến lượt phải di chuyển 1 đồng xu theo chiều hướng về ô 0, các đồng xu không được phép vượt qua nhau hoặc nằm cùng 1 ô. Người chơi không còn nước để đi thua (normal), hoặc người chơi đi nước cuối cùng thua (misere). Dễ nhận ra đây chính là biến thể 1/ được phát biểu dưới dạng khác, với mỗi đồng xu đại diện cho 1 đống và vị trí của đồng xu tượng trưng cho số lượng quân trong đống. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lời giải cho monotomic nim:</ins>* Chiến lược tất thắng của trò chơi là một phép biến đổi tương đương để quy về nim game thông thường. Khi ấy ta có bổ đề sau:<br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Bổ đề:</ins>* Monotonic nim game gồm $2k$ đống: $a_{1};a_{2};a_{3};...a_{2k-1};a_{2k}$ tương đương với nim game gồm $k$ đống: $b_{1};b_{2};...;b_{k}$ trong đó số lượng quân trong đống là: $b_{i}=a_{2i}-a_{2i-1}$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Với một monotonic nim game đang ở trạng thái trên, dễ thấy một động thái làm giảm đống $a_{2i}$ của người chơi tương tự như động thái làm giảm đống bi trong nim game tương đương (với số lượng quân bị lấy ra là tương đương), điều này cũng phù hợp với yêu cầu $a_{2i-1} \le a_{2i}$ của luật monotonic nim và vì thế đảm bảo số lượng $b_{i} \ge 0$ . Mặt khác, nếu bạn làm giảm đống $a_{2i-1}$ , đống bi sẽ tăng lên một lượng tương đương, nhưng ở lượt tiếp theo đối phương có thể làm giảm một lượng tương đương ở đống $a_{2i}$ khiến đống bi giảm trở lại mức ban đầu, hành động vừa rồi của đối thủ chính là một nước đi "undo" lại bước bạn vừa thực hiện. Nếu nhìn nhận theo cách này, monotonic nim game chính là một nim game thông thường nhưng có thêm những "động thái khả đảo" - những nước đi làm giảm các đống $a_{2i-1}$ (hay chính là làm tăng đống bi tương ứng) , như những gì đã nói tới ở các bài trước, chúng là 2 trò chơi tương đương và có giá trị nimber tương ứng là như nhau. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Hoàn tất chứng minh. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nếu trò chơi bắt đầu với một số lẻ đống thì sao? Không có vấn đề gì vì ta chỉ cần thêm vào một đống có 0 quân vào trước đống nhỏ nhất là xong. Đáng chú ý là sự quy đổi từ monotonic nim game về nim game có giá trị trong cả phiên bản normal và misere.











