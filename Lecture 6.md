# Lý Thuyết Trò Chơi (phần 2) 
### 2. Giải trò chơi và khái niệm điểm cân bằng (tiếp theo) <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *d. Trực giác đằng sau những cân bằng* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Một cách lý giải về điểm cân bằng trong các trò chơi như *Qua cầu* là lý giải tiến hóa. Nếu thợ săn và người chạy trốn/tổ tiên của họ thường xuyên chơi các trò chơi có cấu trúc tương tự trong quá khứ thì sức ép từ những thói quen/văn hóa/sinh học là thứ đưa cả 2 tới việc chơi các chiến lược NE và duy lý hóa hành động đó (sẽ nói rõ hơn khi thảo luận về *"Lý thuyết trò chơi tiến hóa"*). Cách hiểu như vậy rất phù hợp với các mô hình xã hội quy mô lớn, đặc biệt trong kinh tế học, nơi mà một hệ thống kinh tế được diễn giải như mạng lưới của các mối quan hệ nhân quả, thường nằm trong sự cân bằng và chỉ bị xáo trộn khi có sự can thiệp của một lực lượng ngoại sinh. Nhưng một số người lại coi LTTC là một lý thuyết về suy lý chiến lược đơn thuần mà với họ, lời giải của trò chơi phải là một kết quả dự đoán được bằng cách sử dụng duy nhất các cơ chế tính toán duy lý. Các lý thuyết gia này phải đối mặt với những vướng mắc đã đề cập ***cuối mục 0/***. Vấn đề sẽ được giải quyết nếu ta thừa nhận rằng tính duy lý trong LTTC có thể do người chơi tự tính toán hoặc được bao hàm trong những cấu trúc hành vi hình thành bởi sự chọn lọc kinh tế, văn hóa hoặc tự nhiên. <br>
### 3. Tinh chỉnh cân bằng Nash <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bộ lọc cân bằng Nash* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bởi các đặc tính của NE, nếu trò chơi chỉ có 1 kết quả NE thì nó phải là lời giải duy nhất. Tuy nhiên, ở các trò chơi có nhiều NE, không phải tất cả các NE đều trông hợp lý. Hãy xem trò chơi sau <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/69634713-e24f-4ee9-8d01-2d2e7dce72a1)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Trò chơi này có 2 NE với chiến lược thuần túy: $\left( {{s_1},{t_1}} \right),\left( {{s_2},{t_2}} \right)$  và 1 NE với chiến lược hỗn hợp: $\left( {\frac{1}{{11}}{s_1} + \frac{{10}}{{11}}{s_2},\frac{1}{{11}}{t_1} + \frac{{10}}{{11}}{t_2}} \right)$ (Player I phân phối xác suất cho ${s_1},{s_2}$ lần lượt là $\frac{1}{{11}}$ và $\frac{10}{{11}}$ ; tương tự với Player II <br>
&nbsp;&nbsp;&nbsp;&nbsp;Nếu NE là khái niệm giải pháp duy nhất thì 3 kết quả này đều phải được coi là lời giải của trò chơi. Nhưng có điều gì đó đã bị bỏ quên: những người chơi duy lý và có đầy đủ thông tin chắc chắn sẽ hội tụ vào $\left( {{s_1},{t_1}} \right)$   ? <br>
&nbsp;&nbsp;&nbsp;&nbsp;Xem tiếp ví dụ sau:
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/889e17dd-b9f9-4ecf-a30d-21864ae45095)
</div>

Trò chơi có các NE là: 
```math
\left\{ \begin{array}{l}
\left( {{s_1},{t_2}} \right)\
\left( {r{s_1} + \left( {1 - r} \right){s_2},{\rm{ }}{t_1}} \right)
\end{array} \right.  ,{\rm{      }} \text{      } r \le \frac{1}{3}
```
&nbsp;&nbsp;&nbsp;&nbsp;Không có chiến lược nào thống trị / bị thống trị nghiêm ngặt. Tuy nhiên, hàng $s_1$ "thống trị yếu" $s_2$ , nghĩa là phần thưởng của Player I khi chơi $s_1$ luôn lớn hơn hoặc ít nhất cũng bằng phần thưởng khi chơi $s_2$ dù Player II chơi bất cứ cột nào. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy chúng ta có nên xóa đi hàng $s_2$ bị thống trị yếu để cho $\( s_{1} ; t_{2} \)$ trở thành NE duy nhất không? Để kiểm chứng, ta thử thay đổi các khoản tiện ích của trò chơi một chút (qua *ví dụ* mới dưới đây). <br>
<div align="center">

![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/67ffa881-7779-460f-b040-0cc9ace973a6)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Nhận thấy $s_2$ vẫn bị thống trị yếu, nhưng NE $\( s_{2} ; t_{1} \)$  giờ đây là hấp dẫn nhất đối với cả 2 người chơi. Vậy thì tại sao các nhà phân tích lại muốn loại bỏ nó? Lý lẽ cho việc loại bỏ các chiến lược bị thống trị yếu là ở chỗ Player I có thể sợ rằng Player II *không hoàn toàn duy lý* - chơi $t_2$ bằng một xác suất dương. Vì vậy Player I muốn tránh kết quả tệ nhất của mình, $\( s_{2} ; t_{2} \)$ , và cái giá cho sự đảm bảo này là giảm tiện ích từ 10 xuống 5. Player II-biết Player I nghĩ gì, sẽ có động cơ để chơi $t_2$ ; và thế là Player I-biết Player II biết mình nghĩ gì, càng tin vào quyết định chơi $s_1$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Mặt khác, có thể nghĩ về kịch bản 2 người chơi đã giao tiếp với nhau trước khi chơi và đồng ý chơi các chiến lược dẫn đến $\( s_{2} ; t_{1} \)$ , bằng cách loại bỏ sự không chắc chắn về đối phương <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$ Qua 3 ví dụ trên, phần nào minh họa một sự thật rằng NE là một ***<ins><khái niệm giải pháp tương đối yếu</ins>***, thường không dự đoán được các kết quả nhạy cảm về mặt trực giác vì nếu áp dụng đơn độc, nó sẽ không cho người chơi sử dụng các nguyên tắc lựa chọn mà nếu không dựa trên tính duy lý thì ít nhất cũng không phải là phi lý. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bất cứ nguyên tắc nào giải quyết các trò chơi bằng cách loại bỏ 1 hoặc nhiều NE khỏi sự xem xét thì đều được coi là bộ lọc của NE. Trong trường hợp ở ảnh 3 thì việc loại bỏ các chiến lược bị thống trị yếu chính là một bộ lọc vì nó giữ lại duy nhất NE $\( s_{1} ; t_{2} \)$  và lọc đi tất cả các NE khác, và song song là một bộ lọc khác, giữ lại mỗi NE $\( s_{2} ; t_{1} \)$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;Vậy thì bộ lọc nào thích hợp hơn với vai trò là một khái niệm giải pháp? Ưu khuyết của chúng và một số lượng lớn các bộ lọc khác đều cần phải bàn thêm. <br>
#### &nbsp;&nbsp;&nbsp;&nbsp; *b. Sự cân bằng hoàn hảo của trò chơi con* <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta xét 2 ví dụ tương ứng với 2 trò chơi như sau: 














