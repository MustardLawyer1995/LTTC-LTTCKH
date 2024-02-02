# Một số hiện tượng có thể được lý giải dưới góc nhìn của Lý thuyết trò chơi (phần 4)
### 10. Sự khiếm khuyết của các hệ thống bầu cử nhiều hơn hai lựa chọn - định lí Arrow 
---
#### *<ins>Phát biểu định lí 10.1 (Định lí Arrow):</ins>*

&nbsp;&nbsp;&nbsp;&nbsp;Xét một hệ thống bầu cử với ít nhất 3 lựa chọn trở lên, trong đó mỗi cử tri đều sắp xếp các lựa chọn của mình theo thứ tự nhất định. Khi đó, bất kỳ quy tắc sắp xếp chung cuộc nào đều vi phạm ít nhất một trong các điều kiện sau. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) **<ins>Tính nhất trí:</ins>** Với hai lựa chọn $x$ và $y$ tùy ý, nếu mọi cử tri đều xếp $x$ cao $y$ hơn $y$ , thì $x$ được xếp cao hơn $y$ chung cuộc. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (2) **<ins>Tính xác định từng đôi:</ins>** Với hai lựa chọn $x$ và $y$ tùy ý, thứ tự chung cuộc của $x$ và $y$ chỉ phụ thuộc vào thứ tự của chúng đối với các cử tri. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (3) **<ins>Tính phi độc tài:</ins>** Không tồn tại một cử tri $i$ nào sao với hai lựa chọn $x$ và $y$ tùy ý, nếu $i$ xếp $x$ cao hơn $y$ thì $x$ được xếp cao hơn $y$ chung cuộc. <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lý Arrow</ins>*** không áp dụng cho hệ thống bầu cử mà trong đó các cử tri **chấm điểm** cho từng lựa chọn, vì trong trường hợp này thì điểm số mang lại nhiều thông tin hơn thứ tự đơn thuần. Tuy nhiên, hệ thống bầu cử này vẫn khiếm khuyết ở chỗ nó có thể bị thao túng bởi **bầu chiến thuật (tactical voting)**. Định lý sau đây giải quyết điều này - ***<ins>Định lý Gibbard</ins>*** <br>

---
#### *<ins>Phát biểu định lí 10.2 (Định lí Gibbard):</ins>*

&nbsp;&nbsp;&nbsp;&nbsp;Xét một trò chơi trong đó mỗi người chơi lựa chọn một trong một số hữu hạn chiến thuật. Khi đó ít nhất một trong các khả năng sau xảy ra. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) Ít nhất một người chơi có thể thao túng trò chơi bằng "bầu chiến thuật". <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (2) Trò chơi có không quá 2 kết cục. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (3) Tồn tại kẻ độc tài, người có thể hoàn toàn quyết định kết cục trò chơi bằng lựa chọn của mình. <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* Ta xét trò chơi bầu cử, trong đó mỗi người chơi là một cử tri, mỗi chiến lược của từng người chơi là danh sách xếp hạn các lựa chọn của người đó. Chỉ có một lựa chọn được chọn ra sau cùng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khả năng (1) ở trên có thể hiểu là có ít nhất một người chơi có thể dựa theo lựa chọn của những người chơi khác để bầu một cách không trung thực (nghĩa là bầu trái với ý muốn thực sự của người đó), để đạt được kết quả bầu cử chung cuộc tốt hơn. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trường hợp riêng ở trên của *định lý Gibbard* còn được gọi là ***<ins>định lý Gibbard-Satterthwaite</ins>***. Định lý Gibbard được chứng minh bằng cách dùng định lý Arrow. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Để phát biểu và chứng minh các định lý này, ta cần một số định nghĩa chặt chẽ. Các tập hợp trong bài viết này đều hữu hạn. <br>

---
#### *<ins>Định nghĩa 10.3:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Cho $X$ là một tập hợp. ***<ins>Một quan hệ hai ngôi (binary relation)</ins>*** trên $X$ là một tập con $P$ của tích Descartes $X \times X$. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặc dù định nghĩa trừu tượng như trên, ta có thể hiểu một quan hệ $P$ trên $X$ như một phép so sánh các cặp phần tử của $X$ : nếu $x,y ∈ X$ , ta sẽ viết $x > y$ theo quan hệ $P$ (hay đơn giản hơn là $x > y$ nếu không gây nhầm lẫn) nếu $\( x,y \) ∈ P$ . <br>

---
#### *<ins>Định nghĩa 10.4:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Một quan hệ hai ngôi $P$ trên $X$ được gọi là **một thứ tự (ordering)** nếu nó thỏa mãn hai điều kiện sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) **<ins>Bất đối xứng (non-symmetry):</ins>** Với mọi $x,y ∈ X$ , hai điều kiện $x > y$ và $y > x$ không thể cùng đúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (2) **<ins>Đầy đủ (completeness):</ins>** Với mọi $x,y,z ∈ X$ , nếu $x > z$ thì $x > y$ hoặc $y > z$ . <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;Một thứ tự luôn thỏa mãn tính **bất phản xạ (irreflexivity)**: $x > x$ luôn sai (điều kiện 1 cho $x=y$ ), cũng như tính **truyền dẫn (transitivity)**: Nếu $x > y$ và $y > z$ thì $x > z$ (thật vậy, vì $x > y$ nên theo điều kiện 2 thì $x > z$ hoặc $z > y$ , nhưng $y > z$ nên theo điều kiện 1 thì ta không thể có $z > y$ , do đó $x > z$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Khi ta có một thứ tự $P$ , các ký hiệu $<, ≥, ≤$ (theo $P$ ) sẽ được hiểu một cách hiển nhiên. Chú ý rằng ta không giả sử rằng 2 phần tử khác nhau bất kỳ luôn so sánh được: nếu $x$ và $y$ là hai phần tử sao cho $x < y$ và $x > y$ đều sai thì ta viết $x ~ y$ (theo $P$ ). <br>

---
#### *<ins>Định nghĩa 10.5:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Một **hàm phúc lợi xã hội (social welfare function)** là một ánh xạ $f: {O}^{n} \longrightarrow O$ . <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;Một hệ thống bầu cử của chúng ta sẽ bao gồm: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) Một tập hợp $X$ (gồm các lựa chọn). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (2) Ta ký hiệu $O$ là tập hợp các thứ tự trên $X$ . Mỗi phần tử của $O$ có thể được hiểu như lựa chọn của mỗi cử tri, hoặc như kết quả cuối cùng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (3) Ta giả sử có $n$ cử tri. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (4) Bao gồm cả **định nghĩa 10.5** <br> 

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, một hàm phúc lợi xã hội sẽ gán cho mỗi bộ gồm $n$ thứ tự $\( P_{1},P_{2}...,P_{n} \)$ (có thể hiểu $P_{i}$ như sắp xếp của cử tri thứ $i$ một thứ tự $f\( P_{1},P_{2}...,P_{n} \)$ (có thể hiểu như kết quả bầu cử chung cuộc). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Trong một hệ thống bầu cử công bằng, hàm phúc lợi xã hội $f$ nên thỏa mãn các điều kiện sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) **<ins>Tính nhất trí (unanimity):</ins>** Với mọi $x,y ∈ X$ và $P_{1},P_{2}...,P_{n} ∈ O$ , nếu $x > y$ theo $P_{i}$ $\forall i =1,2,...n$ thì $x > y$ theo $f\( P_{1},P_{2}...,P_{n} \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (2) **<ins>Tính xác định từng đôi (pairwise determination): </ins>** Với mọi $x,y ∈ X$ và $P_{1},P_{2}...,P_{n},Q_{1},Q_{2}...,Q_{n} ∈ O$ , nếu ta có " $x > y$ theo $P_{i} \Leftrightarrow x>y$ theo $Q_{i}$ " và " $y>x$ theo $P_{i} \Leftrightarrow y>x$ theo $Q_{i}$ " $\forall i =1,2,...n$ thì " $x > y$ theo $f\( P_{1},P_{2}...,P_{n} \)$ $\Leftrightarrow x>y$ theo $f\( Q_{1},Q_{2}...,Q_{n} \)$ ". Ở đây, ký hiệu " $A \Longleftrightarrow B$ " nghĩa là $A$ và $B$ cùng đúng hoặc cùng sai. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (3) **<ins>Tính phi độc tài (non-dictatorship):</ins>** Không tồn tại kẻ độc tài (dictator), tức là một cử tri $i$ sao cho: Với mọi $x,y ∈ X$ và $P_{1},P_{2}...,P_{n} ∈ O$ , nếu $x > y$ theo $P_{i}$ thì $x > y$ theo $f\( P_{1},P_{2}...,P_{n} \)$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Đến đây ta đã sẵn sàng phát biểu hoàn chỉnh ***<ins>Định lý Arrow</ins>*** như sau: <br>

---
#### *<ins>Phát biểu định lí 10.6 (Định lí Arrow - 1963):</ins>*

&nbsp;&nbsp;&nbsp;&nbsp;Nếu $X$ có ít nhất 3 phần tử và $f$ là một hàm phúc lợi xã hội thỏa mãn tính nhất trí và tính xác định từng đôi thì tồn tại kẻ độc tài trong hệ bầu cử. <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 10.6:</ins>* Cố định $y ∈ X$ . Ta sẽ chứng minh bổ đề sau đây:

---
#### *<ins>Bổ đề 10.7:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $P_{1},P_{2}...,P_{n} ∈ O$ là các thứ tự sao cho $\forall i =1,2,...n$ , $y$ được bầu cao nhất hoặc thấp nhất theo thứ tự $P_{i}$ . Thế thì xếp cao nhất hoặc thấp nhất theo thứ tự chung cuộc $P = f\( P_{1},P_{2}...,P_{n} \)$ . <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;Vì $X$ có ít nhất 3 phần tử, ta xét hai phần tử phân biệt (và khác $y$ ) tùy ý $x,z ∈ X$ . Ta sửa lại từng thứ tự $P_{i}$ thành thứ tự $Q_{i}$ $\forall i =1,2,...n$ trong đó $x > z$ , nhưng vẫn giữ nguyên $y$ ở vị trí cao nhất hoặc thấp nhất. Theo tính nhất trí, ta có $x > z$ theo $Q = f\( Q_{1},Q_{2}...,Q_{n} \)$ , suy ra $x > y$ hoặc $y > z$ (tính chất của thứ tự) theo $Q$ . Vì thứ tự của các cặp $\\{ x,y \\}$ và $\\{ y,z \\}$ giữ nguyên khi thay $P_{i}$ bởi $Q_{i}$ $\forall i =1,2,...n$ nên theo tính xác định từng đôi, ta có $x > y$ hoặc $y > z$ theo $P$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nói riêng, ta thấy có ít nhất một lựa chọn so sánh được với $y$ theo $P$ . Xét hai trường hợp sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* Nếu tồn tại lựa chọn $x ∈ X$ sao cho $y > x$ theo $P$ : Với mọi $z ∈ X$ $\(z ≠ x,y \)$ , ta có $x > y$ hoặc $y > z$ theo $P$ như đã lập luận ở trên. Hiển nhiên khả năng thứ nhất không xảy ra, nên $y > z$ theo $P$ . Vậy $y$ xếp cao nhất theo $P$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* Nếu tồn tại lựa chọn $z ∈ X$ sao cho $z > y$ theo $P$ : Với mọi $x ∈ X \( x ≠ y,z \)$ , ta có $x > y$ hoặc $y > z$ theo $P$ như đã lập luận ở trên. Tương tự, ta phải có $x > y$ theo $P$ . Vậy $y$ xếp thấp nhất theo $P$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Từ đó ta hoàn tất chứng minh ***<ins>Bổ đề 10.7:</ins>*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Bây giờ, ta xét các thứ tự $P_{1},P_{2}...,P_{n} ∈ O$ trong đó $y$ xếp thấp nhất. Theo tính xác định từng đôi, $y$ xếp thấp nhất theo thứ tự chung cuộc $f\( P_{1},P_{2}...,P_{n} \)$ . Ta lần lượt sửa các thứ tự $P_{1},P_{2}...,P_{n}$ thành các thứ tự $Q_{1},Q_{2}...,Q_{n}$ sao cho $y$ xếp cao nhất. Theo nhận xét trên, ở mỗi lần thay, $y$ luôn xếp cao nhất hoặc thấp nhất theo thứ tự chung cuộc. Sau khi thay tất cả $n$ thứ tự thì $y$ xếp cao nhất theo thứ tự chung cuộc $f\( Q_{1},Q_{2}...,Q_{n} \)$ (theo tính xác định từng đôi). Như vậy có một cử tri $i$ sao cho sau khi sửa thứ tự $P_{i}$ thành $Q_{i}$ thì $y$ thay đổi từ thấp nhất lên cao nhất theo thứ tự chung cuộc (nhưng $y$ luôn xếp thấp nhất trước đó). (\*) <br>

---
#### *<ins>Bổ đề 10.8:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Tồn tại cử tri $i$ và bộ $R_{1},R_{2}...,R_{n} ∈ {O}^{n}$ sao cho: $y$ xếp cao nhất hoặc thấp nhất theo mọi thứ tự $R_{j}$ , $\forall j =1,2,...n$ ; $y$ xếp thấp nhất theo $R_{i}$ và $f(R)$ ; và bằng cách thay đổi $R_{i}$ thành một thứ tự $R_{i}'$ trong đó $y$ xếp cao nhất, ta có $y$ xếp cao nhất theo thứ tự chung cuộc $f\( R' \)$ (với $R' ∈ O^{n}$ là bộ thu được khi thay tọa độ thứ $i$ của $R$ từ $R_{i}$ thành $R_{i}'$ ). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Nhờ (*) mà ta hoàn tất chứng minh ***<ins>Bổ đề 10.8:</ins>*** <br>

&nbsp;&nbsp;&nbsp;&nbsp;Tiếp đến ta sẽ chỉ ra rằng cử tri $i$ ở trên là một kẻ độc tài. <br>

&nbsp;&nbsp;&nbsp;&nbsp;1) Xét $x,z ∈ X$ là hai lựa chọn phân biệt tùy ý và khác $y$ . Ta xét thứ tự ${R_{i}}^" ∈ O$ bất kỳ trong đó $x > y > z$ . Với các cử tri $j≠i$ , lấy thứ tự ${R_{j}}^"$ tùy ý, trừ việc giữ nguyên $y$ ở vị trí cao nhất hoặc thấp nhất sao cho giống với $R_{j}$ . Đặt ${R}^" = \( {R_{1}}^", {R_{2}}^"..., {R_{n}}^" \) ∈ O^{n}$ . Theo tính độc lập từng đôi cho $x,y,R,{R}^"$ , vì $x > y$ theo $f(R)$ nên $x > y$ theo $f\( {R}^" \)$ . Tương tự, vì $y > z$ theo $f(R')$ nên $y > z$ theo $f\( {R}^" \)$ . Theo tính truyền dẫn của thứ tự, ta có $x > z$ theo $f\( {R}^" \)$ . Vì trong các thứ tự ${R_{j}}^"$ với $j≠i$ , thứ tự của cặp $\\{ x,z \\}$ là tùy ý, nên ta luôn có $x > z$ chung cuộc mỗi khi cử tri $i$ bầu $x > y > z$ (theo tính độc lập từng đôi). Cuối cùng, ta cho cử tri $i$ bầu $x > z$ tùy ý thay vì $x > y > z$ , khi đó ta vẫn có $x > z$ chung cuộc (lại theo tính độc lập từng đôi). Vậy thứ tự chung cuộc của cặp $\\{ x,z \\}$ được hoàn toàn quyết định bởi cử tri $i$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;2) Xét $x ∈ X$ là một lựa chọn tùy ý khác $y$ . Ta cố định một cử tri thứ ba là $z$ và dùng lập luận ở trên (chỉ đổi lại ký hiệu) để tìm ra một cử tri $j$ quyết định hoàn toàn thứ tự chung cuộc của cặp mọi cặp $\\{ u,v \\}$ với $u,v≠z$ , nói riêng là với cặp $\\{ x,y \\}$ . Nhưng như ở trên ta đã thấy rằng cử tri $i$ có thể đưa $y$ từ vị trí thấp nhất chung cuộc lên vị trí cao nhất bằng lá phiếu của mình (nói riêng, $i$ có thể thay đổi thứ tự của cặp $\\{ x,y \\}$ ) ở ít nhất một tính huống nào đó, nên ta phải có $j=i$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Từ đó ta hoàn tất chứng minh ***<ins>Định lí 10.6:</ins>*** cũng như ***<ins>Định lí 10.1:</ins>*** <br>

$\Longrightarrow$ Từ đó ta hoàn tất chứng minh ***<ins>Định lí Arrow:</ins>*** <br>

### 11. Sự khiếm khuyết của các hệ thống bầu cử nhiều hơn hai lựa chọn - định lí Gibbard 
&nbsp;&nbsp;&nbsp;&nbsp;Tiếp nối từ phát biểu ***<ins>định lí 10.2</ins>***, ở mục này ta sẽ phân tích sâu hơn về ***<ins>định lí Gibbard</ins>*** như sau:<br>
#### a. Phát biểu định lí và hệ quả 
&nbsp;&nbsp;&nbsp;&nbsp;Trong bài này, một **trò chơi** gồm: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Một tập hợp $X$ gồm các kết cục. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $n$ người chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Với mỗi $i=1,...,n$ , một tập hợp $S_{i}$ gồm các chiến lược mà người chơi $i$ có thể chọn. Ta đặt $S = S_{1} \times S_{2} \times ... \times S_{n}$ là tập hợp tất cả những khả năng mà trò chơi diễn ra. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Một hàm $g: S \longrightarrow X$ , xác định kết cục của mỗi khả năng diễn ra của trò chơi. Để đưa bài toán về dạng lí tưởng, ta giả sử rằng $g$ là toàn ánh (hay mọi kết cục đều có thể xảy ra). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Với $s = \( s_{1},s_{2},...,s_{2} \) ∈ S$ , $\forall i ∈ \\{ 1,...,n \\\}$ và $t ∈ S_{i}$ , ta sẽ viết $s\( i,t \)$ để chỉ bộ thu được khi thay tọa độ thứ $i$ của $s$ từ $s_{i}$ thành $t$ (người chơi $i$ đổi chiến thuật sang $t$ , các người chơi khác giữ nguyên chiến thuật). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Với $P$ là một thứ tự trên $X$ và $i ∈ \\{ 1,2,...,n \\}$ , ta nói một chiến thuật $t ∈ S_{i}$ là $P$ - áp đảo ( $P$ - dominant) cho $i$ nếu với mọi $s ∈ S$ , ta có $g(s(i,t)) > g(s)$ hoặc $g\( s\( i,t \) \) \sim g(s)$ theo $P$ , nghĩa là nếu $i$ chọn chiến thuật $t$ thì $i$ không thể thu được kết cục tệ hơn (theo thứ tự $P$ ) khi chọn chiến thuật khác, bất kể chiến thuật mà những người chơi khác chọn. Một trò chơi được gọi là **thẳng thắn (straightforward)** nếu với mỗi thứ tự $P$ trên tập hợp $X$ các kết cục, mỗi người chơi $i=1,2...,n$ đều sở hữu một chiến thuật $P$ - áp đảo. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Một người chơi $i$ được gọi là **kẻ độc tài (dictator)** nếu với mọi kết cục $x ∈ X$ , tồn tại một chiến thuật $s(x) ∈ S_{i}$ sao cho với mọi $s = \( s_{1},s_{2},...,s_{2} \) ∈ S$ mà $s_{i}=s(x)$ , ta đều có $g(s) = x$ , nghĩa là $i$ luôn quyết định được kết cục của trò chơi, bất kể chiến thuật của những người khác. <br>

&nbsp;&nbsp; $\Longrightarrow$ Từ đây ta đã sẵn sàng phát biểu hoàn chỉnh ***<ins>định lí Gibbard</ins>*** <br>

---
#### *<ins>Phát biểu định lí 11.1 (Định lí Gibbard - 1973):</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Mọi trò chơi thẳng thắn với 3 kết cục trở lên đều có kẻ độc tài. <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;*Định lý Gibbard* có thể áp dụng vào mô hình bầu cử **chỉ lấy một kết quả sau cùng**: Cho $Z$ là một tập hợp các kết quả, sao cho $X ⊆ Z$ . Giả sử rằng với mọi $i=1,...,n$ , tập hợp $S_{i}$ chính là tập hợp $O$ các thứ tự trên $Z$ . Khi đó trò chơi của chúng ta là một hệ thống bầu cử; trong đó mỗi người chơi là một cử tri và bầu ra một danh sách ưu tiên (xếp thứ tự các lựa chọn) cho bản thân; và kết cục của trò chơi là một trong các lựa chọn. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Ta nói một hệ thống bầu cử như trên **có thể bị thao túng (manipulable)** nếu tồn tại một cử tri $i$ , một bộ $P = \( P_{1},P_{2}...,P_{n} \) ∈ O^{n}$ và một thứ tự $P^{\*} ∈ O$ sao cho $g(P) > g\( P(i,P^{\*}) \)$ theo $P^{\*}$ . Điều này có nghĩa như sau: Giả sử mỗi cử tri $j≠i$ đều đã định sẵn một thứ tự ưu tiên $P_{j}$ cho bản thân mình. Cử tri $i$ định sẵn cho mình thứ tự $P^{\*}$ mà theo đó lựa chọn $x=g(P)$ được xếp cao hơn $y=g\( P(i,P^{\*}) \)$ . Sự thao túng ở đây nghĩa là người chơi $i$ có thể cố tình bầu một theo một thứ tự $P_{i}$ (không trung thực) khác ý định ban đầu (là $P^{\*}$ ), để kết cục sau cùng là $x$ được chọn thay vì $y$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;***<ins>Định lý 11.2 (Gibbard-Satterthwaite):</ins>*** Mọi hệ thống bầu cử g như trên với $|X|≥3$ đều hoặc có kẻ độc tài, hoặc có thể bị thao túng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh định lí 11.2:</ins>* (bằng định lí Gibbard) Giả sử $g$ là một hệ thống bầu cử như trên, trong đó không có kẻ độc tài. Theo định lý Gibbard, $g$ không thẳng thắn, nghĩa là tồn tại một cử tri (người chơi) $i$ , một thứ tự $P$ trên $X$ sao cho không có chiến thuật nào khác là $P$ - áp đảo cho $i$ . Ta mở rộng $P$ thành một thứ tự $P^{\*} ∈ O$ trên $Z$ , nghĩa là: với mọi $x,y ∈ X$ , ta có $x > y$ theo $P^{\*}$ $⇔ x > y$ theo $P$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;(chẳng hạn, ta có thể lấy $P^{\*}$ sao cho nếu $x$ hoặc $y ∉ X$ thì $x$ và $y$ không so sánh được). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo giả thiết, chiến thuật $P^{\*}$ không phải là $P$ - áp đảo cho $i$ , nghĩa là tồn tại $R = \( R_{1},R_{2}...,R_{n} \) ∈ O^{n}$ sao cho $g(R) > g\( R(i,P^{\*}) \)$ theo $P$ . Chú ý rằng $g(R) ∈ X$ và $g\( R(i,P^{\*}) \) ∈ X$ nên theo định nghĩa của $P^{\*}$ , ta có $g(R) > g\( R(i,P^{\*}) \)$ theo $P^{\*}$ . Điều này nghĩa là $g$ có thể bị $i$ thao túng. <br>

#### b. Chứng minh định lí Gibbard
&nbsp;&nbsp;&nbsp;&nbsp;Trong mục này, ta cố định một trò chơi thẳng thắn $g: S → X$ với ít nhất $|X|≥3$ kết cục. Để chứng minh *định lý Gibbard* , ta cần chứng minh rằng tồn tại kẻ độc tài trong trò chơi $g$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ký hiệu $O$ là tập hợp các thứ tự trên $X$ . Theo định nghĩa, với mỗi người chơi $i$ và thứ tự $P_{i} ∈ O$ , ta có thể chọn một chiến thuật $P_{i}$ - áp đảo cho $i$ , ký hiệu bởi $\sigma_{i} \( P_{i} \) ∈ S_{i}$. Với $P = \( P_{1},P_{2}...,P_{n} \) ∈ O^{n}$ , ta ký hiệu $σ(P) = \( σ_{1}(P_{1}),...,σ_{n}(P_{n}) \) ∈ S$ và $v(P) = g\( σ(P) \) ∈ X$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mục tiêu của chúng ta là dùng ánh xạ $v: O^{n} → X$ vừa xây dựng để xây dựng một hàm phúc lợi xã hội $f: O^{n} → O$ thỏa mãn các điều kiện của *định lý Arrow*, từ đó tồn tại kẻ độc tài đối với $f$ . Cuối cùng, ta chỉ ra rằng đó cũng là kẻ độc tài đối với trò chơi $g$ . <br>

---
#### *<ins>Định nghĩa 11.3:</ins>* 
&nbsp;&nbsp;&nbsp;&nbsp;Một thứ tự $Q ∈ O$ được gọi là **tuyến tính (linear)** hay **toàn phần (total)** nếu hai phần tử khác nhau bất kỳ đều so sánh được theo $Q$ . <br>

---
&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, một thứ tự tuyến tính thỏa mãn tính **tam phân (trichotomy)**: với mọi $x,y ∈ X$ , đúng một trong ba khả năng $x > y$ , $x = y$ hoặc $x < y$ xảy ra. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ cố định một thứ tự tuyến tính $Q ∈ O$ cho đến hết chứng minh. Xét $P = \( P_{1},P_{2}...,P_{n} \) ∈ O^{n}$ . Với mỗi tập con $Z ⊆ X$ và người chơi $i$ , ta xây dựng thứ tự tuyến tính $P_{i}^{\*}Z ∈ O$ bằng cách đưa tất cả phần tử của $Z$ lên cao nhất, bảo toàn thứ tự (theo $P_{i}$ ) của chúng và dùng $Q$ để tie-break nếu cần. Cuối cùng, các phần tử ngoài $Z$ được sắp xếp theo $Q$ . Một cách chính xác, thứ tự $P_{i}^{\*}Z$ được định nghĩa như sau: với mọi $x,y ∈ X$ , ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $x,y ∈ Z$ thì $x > y$ theo $P_{i}^{\*}Z$ khi và chỉ khi $x > y$ theo $P_{i}$ hoặc ( $x \sim y$ theo $P_{i}$ và $x > y$ theo $Q$ ) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $x ∈ Z$ và $y ∉ Z$ thì $x > y$ theo $P_{i}^{\*}Z$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $x,y ∉ Z$ thì $x > y$ theo $P_{i}^{\*}Z$ khi và chỉ khi $x > y$ theo $Q$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Ta đặt $P^{\*}Z = \( P_{1}^{\*}Z,P_{2}^{\*}Z,...,P_{n}^{\*}Z \) ∈ O^{n}$ . Dễ dàng kiểm tra được các tính chất sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu $Y ⊆ Z$ là một tập con khác thì $(P^{\*}Z)\*Y = P\*Y$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Giả sử $P' = \( P_{1}',P_{2}'...,P_{n}' \) ∈ O^{n}$ thỏa mãn: với mọi $i=1,...,n$ và $x,y ∈ Z$ , ta có ( $x > y$ theo $P_{i}$ $⇔$ $x > y$ theo $P_{i}'$ ). Thế thì $P\*Z = P'\*Z$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Ta định nghĩa quan hệ hai ngôi $f(P)$ trên $X$ như sau: Với $x,y ∈ X$ , quy ước $x > y$ theo $f(P)$ nếu $x ≠ y$ và $x = v\( P^{\*}\\{ x,y \\} \) = g(σ_{1}(P_{1})^{\*}Z,g(σ_{2}(P_{2})^{\*}Z,...,σ_{n}(P_{n})^{\*}Z)$ . <br>

#### *<ins>Bổ đề 11.4:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Ta có $f(P)$ thỏa mãn tính bất phản xạ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 11.4:</ins>* Giả sử $x > y$ theo $f(P)$ , nghĩa là $x ≠ y$ và $x = v\( P^{\*} \\{ x,y \\} \)$ . Nói riêng, $y ≠ v\( P^{\*} \\{ x,y \\} \)$ , nên ta không có $y > x$ theo $f(P)$ . <br>

#### *<ins>Bổ đề 11.5:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Ta có $f$ thỏa mãn tính xác định từng đôi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 11.5:</ins>* Xét $x,y ∈ X$ . Giả sử $P = \( P_{1},P_{2}...,P_{n} \)$ , $P = \( P_{1}',P_{2}'...,P_{n}' \) ∈ O^{n}$  thỏa mãn: với mọi $i=1,...,n$ , ta có ( $x > y$ theo $P_{i}$ $⇔$ $x > y$ theo $P_{i}'$ ). Như đã nhận xét ở trên, ta thấy rằng $P^{\*} \\{ x,y \\} = P'^{\*}\\{ x,y \\}$, do đó $x = v\( P^{\*}\\{ x,y \\} \) ⇔ x = v\( P'^{\*}\\{ x,y \\} \)$ , từ đó $x > y$ theo $f(P) ⇔ x > y$ theo $f(P')$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;Bổ đề sau đây tương đối kỹ thuật và sẽ được dùng nhiều lần trong chứng minh sau. <br>

#### *<ins>Bổ đề 11.6:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $s = σ(P) = \( σ_{1}(P_{1}),σ_{2}(P_{2}),...,σ_{n}(P_{n}) \) ∈ S$ và cho $s' = \(s_{1}',s_{2}',...,s_{n}' \) ∈ S$ cũng như $x,y ∈ X$ , $x ≠ y$ . Nếu: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Với mỗi $i=1,...n$ , nếu $y > x$ theo $P_{i}$ thì $s_{i}' = σ_{i}(P_{i})$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Với mỗi $i=1,...,n$ , $x$ và $y$ so sánh được theo $P_{i}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $y > x$ hoặc $y \sim x$ theo $f(P)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;... thì khi đó $x ≠ g(s')$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 11.6:</ins>* Giả sử phản chứng rằng $x = g(s')$ . Ta có: <br>
&nbsp;&nbsp;&nbsp;&nbsp;Đặt $P^{\*} = P^{\*}\\{ x,y \\}, t = \(t_{1},t_{2},...,t_{n} \) = σ\( P^{\*} \)$ . Chú ý rằng $x ≠ g(t)$ , vì nếu $x = g(t) = v(P^{
\*} \\{ x,y \\})$ thì $x > y$ theo $f(P)$ , mâu thuẫn với giả thiết. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta xét dãy $s^{0},s^{1},...,s^{n} ∈ S$ , trong đó $s^{0}=s'$ và $s^{i} =s^{i-1} \( i,t_{i} \)$ với $i=1,2,...,n$ (lần lượt thay các tọa độ của $s'$ bởi các tọa độ tương ứng của $t$ ). Ta có $x = g(s') = g(s^{0})$ và $x ≠ g(t) = g(s^{n})$ , vì thế ta có thể lấy chỉ số $i$ nhỏ nhất sao cho $x ≠ g(s^{i})$ . Theo giả thiết, $x$ và $y$ so sánh được theo $P_{i}$ . Ta xét hai trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* Nếu $g(s^{i}) = y$ và $y > x$ theo $P_{i}$ .Theo cách xây dựng $i$ , ta có $x = g(s^{i-1})$ , suy ra $g(s^{i}) > g(s^{i-1})$ theo $P_{i}$ . Mà $s^{i-1} = s^{i} \( i,s_{i}' \)$ nên theo định nghĩa thì $s_{i}'$ không phải là một chiến thuật $P_{i}$ - áp đảo cho $i$ . Mặt khác, từ $y > x$ theo $P_{i}$ và giả thiết, ta có $s_{i}' = σ_{i}(P_{i})$ , điều này mâu thuẫn với định nghĩa của hàm $σ_{i}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* Nếu $g(s^{i}) ≠ y$ hoặc $y < x$ theo $P_{i}$ . Trong trường hợp này, ta luôn có $x > g(s^{i})$ theo $P_{i}^{\*} \\{ x,y \\}$ . Mà $x = g(s^{i-1})$ nên $g(s^{i-1}) > g(s^{i})$ theo $P_{i}^{\*} \\{ x,y \\}$ . Hơn nữa, $s^{i} =s^{i-1} \( i,t_{i} \)$ nên theo định nghĩa thì $t_{i}$ không phải là một chiến thuật $P_{i}^{\*} \\{ x,y \\}$ - áp đảo cho $i$ . Nhưng $t_{i} = σ_{i} \( P_{i}^{\*}\\{ x,y \\} \)$ , mâu thuẫn với định nghãi của hàm $σ_{i}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Các mâu thuẫn trên bác bỏ giả sử $x = g(s')$ , ta có điều phải chứng minh. <br>

#### *<ins>Hệ quả 11.7:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Ta có $f$ thỏa mãn tính nhất trí. <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả 11.7:</ins>* Giả sử $x,y ∈ X$ sao cho $x > y$ theo $P_{i}$ với $i=1,2,...,n$ . Vì $g$ là toàn ánh nên $x = g(s')$ với $s' ∈ S$ nào đó. Đặt $s = σ(P)$ , thế thì hai giả thiết ở ***Bổ đề 11.6*** đều được thỏa mãn, do đó giả thiết thứ ba không thể được thỏa mãn (vì kết luận không được thỏa mãn), nghĩa là $x > y$ theo $f(P)$ . <br>

#### *<ins>Hệ quả 11.8:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Nếu $x,y ∈ X$ so sánh được theo $P_{i}$ với $i=1,...,n$ , và $x = v(P)$ , thì $x > y$ theo $f(P)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả 11.8:</ins>* Giả sử phản chứng rằng $y > x$ hoặc $x \sim y$ theo $f(P)$ . Đặt $s' = s = σ(P)$ . Theo ***Bổ đề 11.6*** , ta có $x ≠ g(s') = g(s) = v(P)$ , mâu thuẫn. <br>

#### *<ins>Bổ đề 11.9:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp; $f(P)$ là một thứ tự trên $X$ (hay $f$ là một hàm $O^{n} → O$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh hệ quả 11.9:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Theo ***Bổ đề 11.4***, ta chỉ còn phải chứng minh rằng $f(P)$ thỏa mãn tính đầy đủ, nghĩa là với mọi $x,y,z ∈ X$ thỏa mãn $x > z$ theo $f(P)$ , ta có $x > y$ hoặc $y > z$ theo $f(P)$ . Đặt $P' = P^{\*}\\{ x,y,z \\}$ . Ta có $P'^{\*}\\{ x,z \\} = P^{\*}\\{ x,z \\}$ vì $\\{ x,z \\} ⊆ \\{ x,y,z \\}$ . Do đó $x = v(P^{\*} \\{ x,z \\}) ⇔ x = v(P'^{\*} \\{ x,z \\})$ , hay $x > z$ theo $f(P) ⇔ x > z$ theo $f(P')$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Tương tự, $x > y$ theo $f(P) ⇔ x > y$ theo $f(P')$ , và $y > z$ theo $f(P) ⇔ y > z$ theo $f(P')$ . Do đó, ta cần chứng minh rằng nếu $x > z$ theo $f(P')$ thì $x > y$ hoặc $y > z$ theo $f(P')$ . Điều này nhiển nhiên đúng nếu $x = y$ hoặc $y = z$ , nên ta giả sử rằng $y ≠ x,z$. Xét hai trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $x = v(P')$ thì theo ***Hệ quả 11.8*** , $x > y$ theo $f(P')$ (chú ý rằng $P'_{i}$ là thứ tự tuyến tính với $i=1,...,n$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $x ≠ v(P')$ . Theo ***Hệ quả 11.8*** , $v(P') > x$ theo $f(P')$ . Nói riêng, $z ≠ v(P')$ 
vì $x > z$ theo $f(P')$ . Ta khẳng định rằng $y = v(P')$ . Thật vậy, nếu $y ≠ v(P')$ thì theo định nghĩa của $P'$ , ta có $x > v(P')$ theo $P_{i}'$ với $i=1,...,n$ . Theo ***Hệ quả 11.7***, ta có $x > v(P')$ theo $f(P')$ , mâu thuẫn. Do đó $y = v(P')$ và $y > z$ theo $f(P')$ (lại theo ***Hệ quả 11.8***). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, ta đã chứng minh rằng $f$ là một hàm phúc lợi xã hội (***Bổ đề 11.9***) thỏa mãn tính nhất trí (***Hệ quả 11.7***) và xác định từng đôi (***Bổ đề 11.5***). Vì $|X|≥3$ nên theo *Định lý Arrow* đã chứng minh ở mục trước, tồn tại kẻ độc tài đối với $f$ . Ta kết thúc chứng minh của định lý Gibbard bằng bổ đề sau: <br>

#### *<ins>Bổ đề 11.10:</ins>*
&nbsp;&nbsp;&nbsp;&nbsp;Kẻ độc tài đối với hệ thống bầu cử $f$ cũng là kẻ độc tài đối với trò chơi $g$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề 11.10:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét $i$ là kẻ độc tài với hệ thống bầu cử $f$ . Cho $y ∈ X$ là một kết cục tùy ý và lấy thứ tự $P(y) ∈ O$ bất kỳ mà theo đó $y$ là cao nhất. Ta chứng minh rằng người chơi $i$ có thể đưa kết cục của trò chơi về $y$ bằng cách chơi theo chiến thuật $s(y) = σ_{i}\( P(y) \)$ , bất kể chiến thuật của những người khác là gì. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thật vậy, xét $s' = \(s_{1}',s_{2}',...,s_{n}' \) ∈ S$ với $s_{i}' = s(y)$ . Ta cần chứng minh rằng $g(s') = y$ . Đặt $x = g(s')$ và giả sử phản chứng rằng $x ≠ y$ . Ta lấy $P = \( P_{1},P_{2}...,P_{n} \) ∈ O^{n}$ sao cho $P_{i} = P(x)$ và với mọi chỉ số $j ≠ i$ , ta có $x > y$ theo $P_{j}$ . Ta kiểm tra các giả thiết của ***Bổ đề 11.6***. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Giả thiết 1 được thỏa mãn vì $y$ chỉ lớn hơn $x$ theo $P_{i}$ , và $s_{i}' = s(x) = σ_{i}\( P(x) \) = σ_{i}(P_{i})$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Giả thiết 2 đương nhiên được thỏa mãn vì $y > x$ theo $P_{i}$ và $x > y$ theo $P_{j}$ với mọi $j ≠ i$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Giả thiết 3 được thỏa mãn: ta có $y > x$ theo $f(P)$ vì $y > x$ theo $P_{i}$ và $i$ là kẻ độc tài đối với $f$ . <br>

&nbsp;&nbsp; $\longrightarrow$ Kết luận của ***Bổ đề 11.6*** nói rằng $x ≠ g(s')$ , mâu thuẫn. <br>

$\Longrightarrow$ Vậy $g(s') = y$ và điều này kết thúc chứng minh của ***định lý Gibbard***. <br>
