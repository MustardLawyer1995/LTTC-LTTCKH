# Trò chơi "Máy nói dối" (Liar Detector Game)
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Mô phỏng trò chơi:</ins>* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có một trò chơi giữa một người và một máy tính: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Có 6 cái hộp, máy tính sẽ bỏ số 0 hoặc 1 vào từng rương, số trong từng rương được kí hiệu từ $B_{0}$ tới $B_{5}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Người chơi được quyền hỏi $n$ câu hỏi, mỗi câu hỏi chỉ được sử dụng các toán tử, toán hạng, biến sau: $=,\( , \) , 0 , 1 , \text{ and }, \text{ or }, B_{0}, B_{1}, B_{2}, B_{3}, B_{4}, B_{5}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Máy tính sẽ trả lời là True hoặc False và máy tính có thể trả lời sai không quá 2 lần. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cần hỏi bao nhiểu câu  để người chơi có thể tìm ra bộ 6 số đúng với độ chính xác 100% ? <br>

## Lời giải
&nbsp;&nbsp;&nbsp;&nbsp;Trước tiên ta phải xem với những toán tử đã cho ở trên thì có thể đặt được một câu hỏi như thế nào. Điều này quan trọng, suy nghĩ đúng hướng thì vấn đề không còn quá phức tạp nữa. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi vì $A \text{ and } \( B \text{ or } C \)$ tương đương với $\( A \text{ and } B \) \text{ or } \( A \text{ and } C \)$ nên một câu hỏi đặt theo quy tắc trên luôn có dạng: $M_{1} \text{ } \text{or} \text{ } M_{2} \text{ } \text{or} \text{ } M_{3} \text{ } \text{or} \text{ } ...$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $M_{k}$ là các mệnh đề chứa $\text{and}$ . Ta có thể cho $M_{k}$ là một mệnh đề theo kiểu: “ bộ 6 số cần tìm $\( B_{0} \text{ } B_{1} \text{ } ... \text{ } B_{5} \) = \[ \text{  } \]$ ”, vì nó tương đương với $B_{0} = \[ \text{ } \] \text{ and } B_{1} = \[  \text{ } \] \text{ } \text{ and } ... B_{5} = \[ \text{ } \]$. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Thế thì mỗi $M_k$ ở đây là một bộ 6 số $\( B_{0};B_{1};...;B_{5} \)$ , và ta đang hỏi máy là: bộ 6 số có phải là một trong những bộ số này $\( M_{1}; M_{2}; M_{3};... \)$ không ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;Có $2^{6} = 64$ bộ số khả thể. Và mỗi câu hỏi ta đặt ra là để "lọc" bớt chúng. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Trước tiên, ta thấy ngay rằng nếu mọi câu trả lời của máy là nói thật thì chỉ cần 6 câu hỏi là đủ xác định cả 6 số. 6 câu có dạng:  $B_{0} = \[ \text{ } \], B_{1} = \[ \text{ } \], B_{2} = \[ \text{ } \],...B_{5} = \[ \text{ } \]$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với 6 câu trả lời True/False, ta sẽ xác định được một bộ 6 số (B0 B1 B2...B5). Tất nhiên là chưa chắc cả 6 câu trả lời là nói thật nên có các khả năng sau xảy ra: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Cả 6 câu trả lời là nói thật, khi đó đáp án sẽ là bộ 6 số mà ta vừa thu được ở trên, tạm gọi là bộ số $N$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Có 1 câu trả lời là nói dối, tức là ở câu này, câu trả lời phải đảo ngược lại (True $\rightarrow$ False, False $\rightarrow$ True) $\Rightarrow$ bộ số đúng phải là bộ số $N$ bị thay đổi lại ở một số $\( 0 \rightarrow 1 , 1 \rightarrow 0 \)$ ứng với câu mà máy nói dối. Có tất cả 6 bộ số như vậy (máy nói dối ở một trong 6 câu nên có 6 trường hợp), ta gọi chúng là $P_{1}, P_{2}, ..., P_{6}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Có 2 câu trả lời là nói dối, tương tự như trên, bộ số đúng sẽ rơi vào một trong 15 bộ số (bởi vì có $C_6^2 = 15$ cách chọn ra 2 câu nói dối trong 6 câu), ta cũng ký hiệu chúng là $Q_{1}, Q_{2}, Q_{3}, ..., Q_{15}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy là chỉ với 6 câu hỏi, ta đã thu hẹp phạm vi của đáp án xuống còn 22 bộ số. Ta sẽ dùng 7 câu hỏi còn lại để lọc những đáp án sai.
Ta đặt ra một khái niệm là "mạng sống" của bộ số 🐧. Khi một bộ số (trong 22 bộ số trên) còn $0$ mạng sống tức là nó không thể là đáp án, ta có thể loại nó. Bộ số $N$ còn đủ 3 mạng sống vì nó ứng với trường hợp mà máy chưa nói dối câu nào cả, để loại được $N$ , ta sẽ cần máy "phủ nhận $N$ là đáp án" 3 lần, nguyên do rất đơn giản, bởi vì khi đó $N$ chỉ có thể là đáp án đúng nếu cả 3 lần "phủ nhận" của máy đều là nói dối, vi phạm điều kiện "không nói dối quá 2 lần". Tương tự, các bộ số $P$ đều có 2 mạng và các bộ số $Q$ đều chỉ còn 1 mạng. Mỗi lần máy phủ nhận một bộ số là đáp án thì bộ số đó mất đi 1 mạng sống.<br>
&nbsp;&nbsp;&nbsp;&nbsp;Giai đoạn tiếp theo, ta sẽ đặt những câu hỏi có dạng: $M_{1} \text{ } \text{or} \text{ } M_{2} \text{ } \text{or} \text{ } M_{3} \text{ } \text{or} \text{ } ...$ . Trong đó $M_{1},M_{2},...,M_{n}$ là một nhóm các bộ số được chọn ra từ tập hợp các bộ số "có khả năng là đáp án" (nói cách khác là những bộ số còn mạng sống). Điều này nghĩa là ở mỗi thời điểm của trò chơi, ta phải chia tập hợp những bộ số "còn mạng" thành 2 nhóm, một trong 2 nhóm này sẽ được đưa vào trong câu hỏi $\( M_{1},M_{2},...,M_{n} \)$ , nếu câu trả lời là True tức là máy đã "thừa nhận" đáp án nằm trong nhóm $\( M_{1},M_{2},...,M_{n} \)$ đồng thời "phủ nhận" nhóm còn lại, ngược lại, nếu câu trả lời là False thì máy đã phủ nhận nhóm $\( M_{1},M_{2},...,M_{n} \)$ và thừa nhận đáp án nằm trong nhóm còn lại. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Giờ ta sẽ vận dụng nguyên lý trên để lọc ra đáp án đúng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Chia 22 bộ số thành 2 nhóm: $N$ , 1 bộ số $P$ bất kỳ, 7 bộ số $Q$ (bất kỳ)} và {5 bộ số $P$ còn lại, 8 bộ số $Q$ còn lại}. Cho một trong 2 nhóm vào câu hỏi (thứ 7). <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bắt đầu từ đây, để thuận tiện, ta sẽ gọi chung những bộ số còn 3 mạng là $N'$ , còn 2 mạng là $P'$ , còn 1 mạng là $Q'$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Máy trả lời câu 7, những bộ số bị phủ nhận sẽ mất đi 1 mạng, bộ số nào còn 0 mạng sẽ bị loại. Những bộ số còn trụ lại sau câu 7 (2 trường hợp nhỏ như sau): $\[1N', 1P', 12Q' \] / \[6P', 9Q' \]$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;Cách chơi trong giai đoạn còn lại như sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Quy ước</ins>*: $\rightarrow$ để chỉ thao tác chia ra 2 nhóm bộ số. $\longrightarrow$ để chỉ những bộ số còn trụ lại sau câu hỏi. “ / ” để chia ra 2 trường hợp có thể xảy ra, nếu 2 trường hợp gần tương đồng nhau, ta sẽ chỉ xét những trường hợp xui xẻo nhất, tức là có ít bộ số bị loại nhất. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\[ 1N', 1P', 12Q' \] \rightarrow \\{ 1N', 6Q' \\} \wedge \\{ 1P', 6Q' \\} \longrightarrow \[ 1N', 7Q' \] / \[ 2P', 6Q' \]$ (còn 5 câu hỏi). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 6P', 9Q' \] \rightarrow \\{ 3P', 4Q' \\} \wedge \\{ 3P', 5Q' \\}$. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 3P', 8Q' \] \rightarrow \\{ 1P', 4Q' \\} \wedge \\{ 2P', 4Q' \\}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 2P', 5Q' \] \rightarrow \\{ 1P', 2Q' \\} \wedge \\{ 1P', 3Q' \\}$ .<br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1P', 4Q' \]$ (còn 3 câu hỏi). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 1N', 7Q' \] \rightarrow \\{ 1N', 3Q' \\} \wedge \\{ 4Q' \\}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1N', 3Q' \] / \[ 1P', 4Q' \]$ (còn 4 câu). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 2P', 6Q' \] \rightarrow \\{ 1P', 3Q' \\} \wedge \\{ 1P', 3Q' \\}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1P', 4Q' \]$ (còn 4 câu). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 1N', 3Q' \] \rightarrow \\{ 1N', 1Q' \\} \wedge \\{ 2Q' \\}$. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1N', 1Q' \] / \[ 1P', 2Q' \]$ (còn 3 câu). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 1P' , 4Q' \] \rightarrow \\{ 1P', 1Q' \\} \wedge \\{ 3Q' \\}$. <br> 
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1P', 1Q' \] / \[ 4Q' \]$ (còn 2 câu). <br>

&nbsp;&nbsp;&nbsp;&nbsp; $\[ 1P', 2Q' \] \rightarrow \\{ 1P', 1Q' \\} \wedge \\{ 1Q' \\}$. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\longrightarrow \[ 1P', 1Q' \]$ (còn 2 câu). <br>

&nbsp;&nbsp;&nbsp;&nbsp;Cuối cùng ta chỉ còn phải xét các trường hợp sau, rất dễ nên chỉ cần nói qua: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\[ 1N', 1Q' \]$ (còn 3 câu): chỉ còn 2 bộ số, nên cứ chia chúng ra 2 nhóm rồi hỏi, vì $N'$ có 3 mạng nên chỉ cần tối đa 3 lần hỏi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\[ 1P', 1Q' \]$ (còn 2 câu): tương tự như trên, nhưng $P'$ có 2 mạng nên chỉ cần 2 lần hỏi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- $\[ 4Q' \]$ (còn 2 câu): liên tục chia những bộ số còn lại thành 2 phần bằng nhau, mỗi câu hỏi lọc được một nửa các bộ số => chỉ cần 2 lần hỏi. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Như vậy, chỉ cần 13 câu hỏi được thiết lập theo những quy tắc trên là đủ để tìm ra bộ 6 số đúng với độ chính xác 100%. <br>













