# Trò chơi Luật Thiểu Số 
<ins>Mô phỏng luật chơi:</ins> Mỗi người chơi đều bỏ phiếu (Yes/No) tùy ý theo vòng, ai thuộc bên có số phiếu nhiều hơn bị loại (đúng như tên gọi của trò này), nếu bằng nhau thì bỏ phiếu lại lần nữa. Những người thắng đi vào vòng bỏ phiếu tiếp, loại dần cho tới khi chỉ còn 1 hoặc 2 người ở lại. <br>

<ins>Chiến thuật trong truyện (nguyên tác): </ins> <br>
Có 22 người, lập ra nhóm 8 người rồi chia đôi ra nửa đội bỏ Yes nửa đội bỏ No, nên sẽ luôn có 1 nửa đội ở lại sau mỗi vòng. Tác giả trò chơi này tức Ngô Thanh Liêm đã sáng tạo hơn khi nghĩ ra cách là lập team 2 người lúc bắt đầu và chỉ kết nạp thêm 1 người vào đội sau mỗi vòng, như vậy hạn chế được số người trong team và số Tiền thưởng chia ra được nhiều hơn. Nhưng trong bài này ta sẽ không làm vậy, hơn nữa lập team kiểu đó cũng có rất nhiều rủi ro so với việc lập 1 team hoàn chỉnh ngay khi mới bắt đầu. <br>

Khi cho tổng quát với $n$ người, việc chọn lựa sẽ khó khăn hơn, nhất là phải xét đến trường hợp mà team bị lẻ người ở 1 vòng nào đó, vì không phải lúc nào cũng chọn được số người có dạng $2^{k}$ (số chính phương).

## Lời giải 
### 1. Thu hẹp phạm vi tìm kiếm
