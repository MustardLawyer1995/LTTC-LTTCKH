# Partisan game – Nhiệt đồ và lời giải cho tàn cuộc cờ vây
Các partisan game gồm 2 loại là trò chơi lạnh và nóng, định nghĩa của chúng đã được nói đến ở loạt vấn đề trong
bài giảng số 17. Người chơi sẽ thích chơi trò chơi nóng hơn lạnh. Một vài trò chơi nóng lại được ưa thích hơn (nóng
hơn/tối ưu hơn về mặt chiến thuật) những trò chơi nóng khác. Đây là động cơ ban đầu để xây dựng thang đo nhiệt độ
cho các trò chơi, nhưng nó còn dẫn ta đến điều gì nữa...
### 0. Trò chơi tổng của các $\\{ a|b \\}$ với $a,b$ là số <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một trò chơi cấu thành từ các trò chơi con dạng $\\{ a|b \\}$ với $a,b$ là số chỉ chứa 2 loại giá trị ứng với 2 trường hợp như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $a<b$ , $\\{ a|b \\}$ là số <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $a≥b$ , $\\{ a|b \\} = \frac{a+b}{2} ± \frac{a-b}{2}$ (với số $n≥0$ , ký hiệu: $\\{ n|-n \\} = ±n$ , không mất tính tổng quát, $*=±0$ , do định nghĩa này nên $- \( ±n \) = ±n$ hay $±n±n=0$ ), kết quả này đến từ nguyên lý chuyển dịch số (xem lại ***<ins>Số siêu thực - phần 5, VII/, Định lí 4.4a</ins>***) <br>
&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi tồn tại một chiến lược thắng đơn giản mà không cần qua thao tác cộng các giá trị: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tránh chơi các giá trị số nếu có thể, theo Định lý tránh số (xem lại ***<ins>Số siêu thực - phần 5, VII/, hệ quả 4.4b </ins>***). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Chơi ở phi số $\\{ a|b \\}$ $\( a≥b \)$ nào có $a-b$ lớn nhất. Thật vậy: Khi viết tất cả các $\\{ a|b \\}$ 
 $\( a≥b \)$ về dạng $\frac{a+b}{2} ± \frac{ab}{2}$, chỉ cần quan tâm đến phần $±\frac{a-b}{2}$ vì $\frac{a+b}{2}$ là số. Cho $m>n$ , có: $m-n±m±n>0$ (chứng minh bằng cách chỉ ra Trái luôn thắng) $\Leftrightarrow$ $m±n>±m+n$ $\rightarrow$ Cho $a_{1}>a_{2}>a_{3}>...>0$ , có: $a_{1}±a_{2}±a_{3}±...> ±a_{1}+a_{2}±a_{3}±...> ±a_{1}±a_{2}+a_{3}±...>...$ , chứng minh tương tự cho nước đi ở bên Phải. $\Rightarrow$ Nếu phải thực hiện 1 nước đi trong $±a_{1}±a_{2}±a_{3}±...$ , chơi ở $±a_{1}$ là tốt nhất. (điều phải chứng minh) <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Ta hoàn tất chứng minh ***định lí 4.4a*** <br>


