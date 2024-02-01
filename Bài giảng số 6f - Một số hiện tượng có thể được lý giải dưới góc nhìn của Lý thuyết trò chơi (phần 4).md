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
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (1) **<ins>Đầy đủ (completeness):</ins>** Với mọi $x,y,z ∈ X$ , nếu $x > z$ thì $x > y$ hoặc $y > z$ . <br>

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

&nbsp;&nbsp;&nbsp;&nbsp;Xét $x,z ∈ X$ là hai lựa chọn phân biệt tùy ý và khác $y$ . Ta xét thứ tự ${R_{i}}^" ∈ O$ bất kỳ trong đó $x > y > z$ . Với các cử tri $j≠i$ , lấy thứ tự ${R_{j}}^"$ tùy ý, trừ việc giữ nguyên $y$ ở vị trí cao nhất hoặc thấp nhất sao cho giống với $R_{j}$ . Đặt ${R}^" = \( {R_{1}}^", {R_{2}}^"..., {R_{n}}^" \) ∈ O^{n}$ . Theo tính độc lập từng đôi cho $x,y,R,{R}^"$ , vì $x > y$ theo $f(R)$ nên $x > y$ theo $f\( {R}^" \)$ . Tương tự, vì $y > z$ theo $f(R')$ nên $y > z$ theo $f\( {R}^" \)$ . Theo tính truyền dẫn của thứ tự, ta có $x > z$ theo $f\( {R}^" \)$ . Vì trong các thứ tự ${R_{j}}^"$ với $j≠i$ , thứ tự của cặp $\\{ x,z \\}$ là tùy ý, nên ta luôn có $x > z$ chung cuộc mỗi khi cử tri $i$ bầu $x > y > z$ (theo tính độc lập từng đôi). Cuối cùng, ta cho cử tri $i$ bầu $x > z$ tùy ý thay vì $x > y > z$ , khi đó ta vẫn có $x > z$ chung cuộc (lại theo tính độc lập từng đôi). Vậy thứ tự chung cuộc của cặp $\\{ x,z \\}$ được hoàn toàn quyết định bởi cử tri $i$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xét $x ∈ X$ là một lựa chọn tùy ý khác $y$ . Ta cố định một cử tri thứ ba là $z$ và dùng lập luận ở trên (chỉ đổi lại ký hiệu) để tìm ra một cử tri $j$ quyết định hoàn toàn thứ tự chung cuộc của cặp mọi cặp $\\{ u,v \\}$ với $u,v≠z$ , nói riêng là với cặp $\\{ x,y \\}$ . Nhưng như ở trên ta đã thấy rằng cử tri $i$ có thể đưa $y$ từ vị trí thấp nhất chung cuộc lên vị trí cao nhất bằng lá phiếu của mình (nói riêng, $i$ có thể thay đổi thứ tự của cặp $\\{ x,y \\}$ ) ở ít nhất một tính huống nào đó, nên ta phải có $j=i$ . <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Từ đó ta hoàn tất chứng minh ***<ins>Định lí 10.6:</ins>*** cũng như ***<ins>Định lí 10.1:</ins>*** <br>

$\Longrightarrow$ Từ đó ta hoàn tất chứng minh ***<ins>Định lí Arrow:</ins>*** <br>












