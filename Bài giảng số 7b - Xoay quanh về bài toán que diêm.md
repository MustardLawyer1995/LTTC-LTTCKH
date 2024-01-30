# Xoay quanh về bài toán que diêm

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ 3.7:</ins>* Hãy tìm chiến lược thắng **<ins>tốt nhất</ins>** cho trò chơi sau:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Có 27 que diêm, hai người chơi lần lượt nhặt diêm vào tay mình. Mỗi lần chỉ được phép nhặt tối thiểu 1 que và tối đa 4 que. Sau khi nhặt hết diêm, trong tay người chơi nào có số diêm chẵn thì người đó thắng cuộc <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lời giải cho ví dụ trên:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Gọi số quân (que diêm) trên bàn là $n$ . Nếu 2 người chơi đều đi những nước có lợi nhất cho mình thì kết cục trò chơi đã được quyết định ngay từ lúc bắt đầu - phụ thuộc vào giá trị $n$ và người đi trước đang có chẵn hay lẻ quân - theo quy luật sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Quy ước: "người đi trước": là người được đi nước tiếp theo - nói cách khác - là người đi trước trong giai đoạn còn lại của trò chơi <br>
<div align="center">

|  |  |
|----------|----------|
| $n \equiv \\{ 0,5 \\} \text{   } \( \text{ mod } 6 \)$ | Người đi trước đang sở hữu số diêm chẵn thì thắng, nếu lẻ thì thua |
| $n \equiv 1 \text{   } \( \text{ mod } 6 \)$ | Người đi trước đang sở hữu số diêm chẵn thì thua, nếu lẻ thì thắng |
| $n \equiv \\{ 2,3,4 \\} \text{   } \( \text{ mod } 6 \)$ | Đi trước thì thắng |
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Theo cách "ấn định" các thế thắng/thua của quy luật trên, dễ thấy rằng nếu người đi trước đang ở thế thắng, luôn tồn tại một nước đi để thế cục trò chơi ở lượt tiếp theo là thế thua của đối thủ: giả sử $n \equiv 2 \text{   } \( \text{ mod } 6 \)$ , lấy $1,2,3$ hoặc $4$ quân sẽ đưa $n$ về các mức lần lượt là $1,0,5,4 \text{   } \( \text{ mod } 6 \)$ , nếu đối thủ đang có chẵn quân, người đi trước chỉ cần lấy 1 quân để $n \equiv 1 \text{   } \( \text{ mod } 6 \)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Lượt tiếp theo đối thủ rơi vào thế thua (xem lại quy luật ở trên), nếu đối thủ đang có lẻ quân, lấy 2 hoặc 3 để $n \equiv \\{ 0,5 \\} \text{   } \( \text{ mod } 6 \)$ , lượt tiếp theo đối thủ thua (thực hiện ***chứng minh tương tự*** với trường hợp $n \equiv \\{ 3,4,5,1 \\} \text{   } \( \text{ mod } 6 \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, khi người đi trước đang ở thế thua, bất cứ nước đi nào của anh ta cũng dẫn đến thế cục mà đối thủ thắng: giả sử $n \equiv 0 \text{   } \( \text{ mod } 6 \)$ ( $n$ chẵn), người đi trước đang có số quân lẻ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Người đi sau đang có số quân chẵn (vì tổng số quân là lẻ), người đi trước chọn lấy số quân từ 1 đến 4, sẽ đưa $n$ về các giá trị lần lượt là $5,4,3,2 \text{   } \( \text{ mod } 6 \)$ , phải tránh đưa thế trận về các số $4,3,2$ (thế thắng của đối thủ), nhưng nếu lấy 1 quân thì đưa thế trận về $n \equiv 5 \text{   } \( \text{ mod } 6 \)$ , đối thủ (đang có số quân chẵn) vẫn thắng (thực hiện ***chứng minh tương tự*** cho các trường hợp $n \equiv \\{ 1,5 \\} \text{   } \( \text{ mod } 6 \)$ ). <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Từ đây có thể thấy, nếu trò chơi bắt đầu ở thế thắng cho một người chơi và anh ta sử dụng chiến thuật trên, thế cục trò chơi sẽ được giữ nguyên như vậy (thế thắng cho anh ta - thế thua cho đối thủ) cho tới khi $n≤5$ , mà ta thấy rằng quy luật trên luôn đúng với $n≤5$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow$ Quy luật đúng với mọi giá trị $n$ và đây là chiến thuật tốt nhất của trò chơi. <br>
