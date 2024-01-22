# Trò chơi Luật Thiểu Số 
<ins>Mô phỏng luật chơi:</ins> Mỗi người chơi đều bỏ phiếu (Yes/No) tùy ý theo vòng, ai thuộc bên có số phiếu nhiều hơn bị loại (đúng như tên gọi của trò này), nếu bằng nhau thì bỏ phiếu lại lần nữa. Những người thắng đi vào vòng bỏ phiếu tiếp, loại dần cho tới khi chỉ còn 1 hoặc 2 người ở lại. <br>

<ins>Chiến thuật trong truyện (nguyên tác): </ins> <br>
Có 22 người, lập ra nhóm 8 người rồi chia đôi ra nửa đội bỏ Yes nửa đội bỏ No, nên sẽ luôn có 1 nửa đội ở lại sau mỗi vòng. Tác giả trò chơi này tức Ngô Thanh Liêm đã sáng tạo hơn khi nghĩ ra cách là lập team 2 người lúc bắt đầu và chỉ kết nạp thêm 1 người vào đội sau mỗi vòng, như vậy hạn chế được số người trong team và số Tiền thưởng chia ra được nhiều hơn. Nhưng trong bài này ta sẽ không làm vậy, hơn nữa lập team kiểu đó cũng có rất nhiều rủi ro so với việc lập 1 team hoàn chỉnh ngay khi mới bắt đầu. <br>

Khi cho tổng quát với $n$ người, việc chọn lựa sẽ khó khăn hơn, nhất là phải xét đến trường hợp mà team bị lẻ người ở 1 vòng nào đó, vì không phải lúc nào cũng chọn được số người có dạng $2^{k}$ (số chính phương).

## Lời giải 
### 1. Thu hẹp phạm vi tìm kiếm 
- Số người của nhóm mình và số người ở nhóm tự do (bỏ phiếu ngẫu nhiên) sẽ thay đổi sau mỗi vòng như thế nào ? <br>
- Gọi số người nhóm mình là $a$ , nhóm tự do là $b$ . Ta quy ước dấu “ $\rightarrow$ ” dùng để biểu diễn sự thay đổi số người mỗi bên sau 1 vòng bỏ phiếu.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 1:* $a$ chẵn thì khi đó $a \rightarrow \frac{a}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b-2}{2} = \frac{b}{2} - 1$ <br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Trường hợp 2:* $a$ lẻ thì khi đó $a \rightarrow \frac{a-1}{2}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nếu $b$ lẻ thì $b \rightarrow \frac{b-1}{2}$ và nếu $b$ chẵn thì $b \rightarrow \frac{b}{2}$ <br><br>
$\Longrightarrow$ Tới đây ta đặt ra tình huống xấu nhất như sau: sau mỗi vòng số người tự do còn lại nhiều nhất, số người nhóm mình còn lại ít nhất; dựa trên nhận xét: nếu thế $(a,b)$ đảm bảo chiến thắng thì $(a,b-1)$ và $(a+1,b-1)$ cũng vậy (theo nguyên lí quy nạp). <br>

- Gọi $V$ là số người cần lấy ra từ $N$ người để tạo ra nhóm, khi đó ta thu hẹp giới hạn để tìm $V$ <br>


### 2. Công thức chính xác cho $V$
