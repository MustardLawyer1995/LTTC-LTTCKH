# Trò chơi Ma sói (Werewolf Game)
- <ins>Mô phỏng luật chơi:</ins> Ở một làng có người dân và ma sói (trá hình người) chung sống, ban ngày tất cả mọi người sẽ bầu chọn 1 người để đem treo cổ nếu trúng con sói thì coi như gameover, sói thua, tất nhiên sói cũng được bầu chọn vì không ai biết nó là sói, nếu giết nhầm dân thường thì đêm đó (mọi người ngủ hết) sói sẽ giết 1 người. Chơi theo nhiều vòng, mỗi vòng là 1 ngày cho đến khi sói hoặc dân bị giết hết. Tất cả mọi người chơi đều lý tính tuyệt đối (tính toán tối ưu để phe mình thắng), được quyền thuyết phục lẫn nhau. Mỗi vòng bầu chọn (mỗi người chỉ 1 phiếu bầu và không được phép không bầu) chỉ kết thúc khi *phần lớn mọi người đều thống nhất với kết quả bầu, được phép bầu lại*, nếu có 2 người trở lên có số phiếu bầu ngang nhau và lớn nhất thì kết quả là hòa và không có ai bị treo cổ cả. Tính tỉ lệ win của phe dân trong các trường hợp: <br>
$a.$	2 dân 1 sói <br>
$b.$	3 dân 1 sói <br>
$c.$	Tổng quát cho $n$ dân và 1 sói <br>
$d.$ Tổng quát cho trường hợp số dân và số sói là tùy ý
- ***Lưu ý:*** mỗi 1 vòng vote thực chất đã bao hàm 2 lượt vote ở trong, lượt vote đầu để chọn ra người sẽ bị xử tử, lượt vote sau để quyết định xem có nên xử tử người đó không (có thể diễn đạt khác lại là *"phần lớn mọi người đều thống nhất với kết quả bầu"*, ngụ ý rằng nó cũng là 1 hình thức vote) - mỗi vote là Có/Không và tất cả người chơi (trừ quản trò) bắt buộc phải vote, tất nhiên không tính lượt vote của người đang sắp bị xử (vì không ai lại đồng ý với việc mình phải chết bao giờ cả).
## Lời giải 
### $a.$ 2 dân 1 sói <br>
- Trước hết ta phân tích 1 lời giải sai như sau:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mỗi người sẽ bầu chọn cho 1 trong 2 người còn lại (loại bỏ trường hợp người đó tự bầu chính mình) với xác suất là $\frac{1}{2}$ , sói bị giết khi 2 người dân đều bầu cho sói, nên khả năng để sói bị giết là $\frac{1}{2} \times \frac{1}{2} = \frac{1}{4}$ <br>
-----------------------------------------------------------------------------------------------------------------------------------------
<ins>Nhận xét:</ins> Sai lầm thường gặp nhất là coi kết quả của cuộc bỏ phiếu là ngẫu nhiên. <br>
$\Longrightarrow$ ***Sai*** vì vì họ đã quên mất rằng tất cả người chơi đều *duy lý tuyệt đối* (lường trước được tất cả các kịch bản
của game và luôn hành động để tăng tối đa khả năng thắng cho bản thân), kết quả  $\frac{1}{4}$ ở trên đã bao gồm cả trường hợp bỏ phiếu "hòa" (3 người bầu cho nhau theo vòng tròn), nếu mọi người đều đồng ý với kết quả này và không yêu cầu bỏ phiếu lại thì sẽ không có ai bị treo cổ cả. Nhưng làm vậy thì phe dân chỉ thua nhanh hơn vì sói sẽ thịt 1 người vào đêm đó, sau đó chỉ còn 1 dân và 1 sói, phe dân không còn cơ hội thắng! Nếu 2 người dân đều duy lý, họ sẽ không chấp nhận kết quả hòa và yêu cầu bỏ phiếu lại, vì ít nhất có cơ hội giết được sói. Nói cách khác, xác suất để giết được sói nếu loại bỏ kết quả hòa (luôn có 1 người bị treo cổ) là   $\frac{1}{3}$ cao hơn hẳn khi bầu theo kiểu ngẫu nhiên là  $\frac{1}{4}$ , nên không có lý do gì để người dân không tối đa hóa khả năng thắng của họ.  <br><br>
<ins>Phân tích:</ins> *Sự duy lý* không chỉ dừng lại ở việc tính toán tối ưu các chiến lược để tăng khả năng chiến thắng, duy lý có nghĩa là mọi người chơi đều biết rõ các suy tính của nhau bằng cách thử đặt mình vào vị trí đối phương nên mọi trò tiểu xảo lừa lọc để phát giác sói đều không có giá trị (dân nghĩ gì thì sói cũng nghĩ được như thế) $\rightarrow$ việc chọn trúng sói trong 3 người hoàn toàn là may rủi  $\frac{1}{3}$, mặt khác sói cũng phải ngoan ngoãn làm theo những kế hoạch mà mọi người bàn luận và thống nhất với nhau vì nếu không sẽ lộ thân phận và thua ngay lập tức (nên nhớ phe dân đông hơn:v). Đây là 2 điểm mấu chốt để giải được cả ba câu nêu trên.<br><br>
$\Longrightarrow$ Đáp số cuối cùng: $\frac{1}{3}$
### $b.$ 2 dân 1 sói <br>
- Theo *tính chất duy lý tuyệt đối* đã nêu trên, những lựa chọn duy nhất mà phe dân có thể thực hiện là: 
   - *(1)* Chọn ra 1 người (ngẫu nhiên) để giết
   - *(2)* Không giết ai ("dàn xếp" tạo ra kết quả hòa)
   - *(3)* Hoặc 1 lựa chọn khác là nhập nhằng của 2 phương án trên: bầu chọn ngẫu nhiên. Nếu $p$ là xác suất giết được sói bằng *(1)*,   $q$ là xác suất giết được sói bằng *(2)*, $a$ là xác suất để kết quả bầu chọn ngẫu nhiên không phải là hòa, $b$ là xác suất để kết quả bầu chọn ngẫu nhiên là hòa ( $a+b=1$ ) <br>
   
$\rightarrow$ Các xác suất giết được sói nếu bầu chọn ngẫu nhiên là $ap+bq$, hiển nhiên nếu $p > q \to p > ap + bq > q$ và ngược lại, nếu $p < q \to p < ap + bq < q$ . Ta thấy rằng để tối đa hóa khả năng giết được sói, phe dân sẽ luôn chọn *(1)* hoặc *(2)*, bầu chọn ngẫu nhiên không bao giờ là 1 ý kiến hay cả. <br>
- Với tình huống 3 dân 1 sói, xác suất giết được sói nếu chọn ra 1 người để xử tử là $\frac{1}{4}$ , nếu dàn xếp kết quả hòa để không ai bị xử tử, tối sói sẽ thịt 1 người và sau đó còn 2 dân 1 sói, rơi vào trường hợp như câu **a)**, xác suất giết sói là $\frac{1}{3}$ . Như vậy nghịch lý của câu **b)** là thay vì cứ cố sống chết tìm ra sói càng sớm càng tốt và xử tử, người dân cứ để mặc cho sói giết 1 người vào ngày thứ 1 lại tăng cơ hội chiến thắng của họ lên rất nhiều. <br><br>
$\Longrightarrow$ Đáp số cuối cùng: $\frac{1}{3}$
### $c.$ Tổng quát cho $n$ dân 1 sói <br>
- Trước hết gọi $r_{n}$ là khả năng chiến thắng của phe dân khi có $n$ dân và 1 sói, thử làm mẫu với các giá trị $n$ nhỏ để tìm ra quy luật:
```math
{r_0} = {r_1} = 0;{r_2} = {r_3} = \frac{1}{3};{r_4} = {r_5} = \frac{7}{{15}};.....
```
- Dự đoán được quy luật: ${r_{2k}} = {r_{2k + 1}}$ , chứng minh bởi quy nạp, giả sử quy luật đúng với $n \le 2m + 1$ . <br>
Thật vậy, ta có: $r_{2m} = r_{2m + 1} = r$ với $n = 2m + 2$ <br>
Giết 1 người thì xác suất trúng sói là: $s = \frac{1}{{2m + 3}}$ , nếu giết nhầm thì xác suất là $1-s$ thì phe dân mất 2 người, quy về trường hợp $n=2m$ , khả năng thắng là $r$ . <br>
Viết giết nhầm dẫn đến khả năng thắng là hai công việc có liên kết nhau nên ta sử dụng quy tắc nhân, cộng thêm trường hợp giết 1 người trúng sói dẫn đến khả năng thắng ta thực hiện quy tắc cộng. <br>

$\Longrightarrow$ Tóm lại, khả năng thắng nếu chọn phương án giết 1 người: $s + \left( {1 - s} \right)r$ (áp dụng quy tắc cộng và nhân đơn thuần)  

- Tiếp đến, ta thấy nếu không giết ai thì mất 1 người, quy về trường hợp $n=2m+$ , khả năng thắng là $r$ <br>
Khi đó hiển nhiên: $s + \left( {1 - s} \right)r > r$ , vì $s\left( {1 - r} \right) > 0{\rm{ }}\left( {0 < s,r < 1} \right)$ nên suy ra ta chọn giết 1 người để nâng tối đa cơ hội thắng. <br>
Tương tự với $n=2m+3$ , giết 1 người thì cơ hội thắng là $s' + \left( {1 - s'} \right)r{\rm{ }}\left( {s' = \frac{1}{{2m + 4}}} \right)$ <br>
Không giết ai thì cơ hội thắng là $s + \left( {1 - s} \right)r$ <br>
Hiển nhiên vì $r\left( {s - s'} \right) < s - s'$ nên suy ra $s' + \left( {1 - s'} \right)r < s + \left( {1 - s} \right)r{\rm{ }}$ <br>
$\Longrightarrow$ Suy ra nên chọn không giết ai trong ngày đầu tiên để nâng tối đa cơ hội thắng <br>

$\Longrightarrow$ Khi ấy ta kết luận ${r_{2m + 2}} = {r_{2m + 3}} = s + \left( {1 - s} \right)r$ , quy luật lúc này tiếp tục đúng với $n = 2m + 2$ và $n = 2m + 3$ kéo theo đó quy luật đúng với mọi $n$ . <br><br>
<ins>Nhận xét:</ins> Trong quá trình chứng minh còn giúp ta biết cách đưa ra chiến thuật tối ưu cho phe dân: giết 1 người trong ngày đầu tiên nếu $n$ chẵn và dàn xếp tạo kết quả bỏ phiếu hòa nếu $n$ lẻ. <br>
- Tuy nhiên ta vẫn chưa biết công thức tổng quát cho $r_n$ , nhưng vì $r_{2k} = r_{2k + 1}$ , ta chỉ cần xét các trường hợp $n$ chẵn. Khi đó $r_{2k} = u_{k}$ tạo ra một dãy số truy hồi:
```math
\boxed{{{u_0} = 0,{\rm{ }}{u_k} = \frac{1}{{2k + 1}} + \frac{{2k}}{{2k + 1}}{u_{k - 1}}}}
```
&nbsp; $\Longrightarrow$ Tới đây ta chỉ cần giải dãy số truy hồi trên <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ta có: $\left( {2k + 1} \right){u_k} = 1 + 2k{u_{k - 1}} \Leftrightarrow \left( {2k + 1} \right)\left( {{u_k} - 1} \right) = 2k\left( {{u_{k - 1}} - 1} \right)$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Đặt ${v_k} = {u_k} - 1$ thì khi đó ta có: 
```math
\frac{{{v_k}}}{{{v_{k - 1}}}} = \frac{{2k}}{{2k + 1}} \rightarrow \frac{{{v_m}}}{{{v_0}}} = \frac{{{v_1}}}{{{v_0}}}.\frac{{{v_2}}}{{{v_1}}}.....\frac{{{v_{m - 1}}}}{{{v_{m - 2}}}}.\frac{{{v_m}}}{{{v_{m - 1}}}} = \frac{{2.4.6.....2m}}{{3.5.7....\left( {2m + 1} \right)}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Từ đó ta suy ra: 
```math
\frac{{{v_m}}}{{{v_0}}} = \frac{{2.4.6.....2m}}{{3.5.7....\left( {2m + 1} \right)}} = \frac{{{{\left[ {2.4.6....\left( {2m} \right)} \right]}^2}}}{{\left[ {1.3.5.7....\left( {2m + 1} \right)} \right]\left[ {2.4.6....\left( {2m} \right)} \right]}} = \frac{{{{\left( {{2^m}} \right)}^2}{{\left[ {1.2....\left( m \right)} \right]}^2}}}{{1.2.3.4.5.6.7....\left( {2m} \right)\left( {2m + 1} \right)}} = \frac{{{4^m}{{\left( {m!} \right)}^2}}}{{\left( {2m} \right)!\left( {2m + 1} \right)}}$
```
```math
 = \frac{{\left( {2m - m} \right)!m!}}{{\left( {2m} \right)!}}.\frac{{{4^m}}}{{\left( {2m + 1} \right)}} = \frac{1}{{C_{2m}^m}}.\frac{{{4^m}}}{{\left( {2m + 1} \right)}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mà ${v_k} = {u_k} - 1$ tức ${v_m} = {u_m} - 1$ nên suy ra:
```math
\frac{{1 - {u_m}}}{{1 - {u_0}}} = \frac{{1 - {u_m}}}{{1 - 0}} = \frac{1}{{C_{2m}^m}}.\frac{{{4^m}}}{{\left( {2m + 1} \right)}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Từ đó ta suy ra: 
```math
{u_m} = 1 - \frac{{{4^m}}}{{C_{2m}^m\left( {2m + 1} \right)}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Khi ấy ta kết luận: 
```math
{r_{2m}} = {r_{2m + 1}} = 1 - \frac{{{4^m}}}{{C_{2m}^m\left( {2m + 1} \right)}}
```
### $d.$ Tổng quát cho trường hợp số dân và số sói là tùy ý <br>
Trong bài này, ta vẫn chỉ xem xét trò chơi Ma Sói phiên bản cổ điển - mà luật chơi đã được đề cập ở 3 ý trước đã giải, cùng với giả định rằng tất cả người chơi đều lựa chọn những nước đi tối ưu cho phe mình. Về chiến lược của sói, có lẽ không cần bàn luận quá nhiều khi mỗi đêm chúng chỉ việc cắn chết 1 người dân nào đó. Thực ra trong một vài phiên bản, đàn sói có thể có một lựa chọn là "không cắn ai" trong lượt của mình. Nhưng nếu ta chấp nhận điều luật này, trò chơi có thể (thậm chí với tần suất rất lớn) sẽ rơi vào thế hoà khi phe sói không chịu cắn ai và phe dân cũng không chịu treo cổ ai. Ta sẽ làm cho trò chơi chặt chẽ hơn bằng quy định rằng đàn sói phải cắn chết 1 người dân vào lượt của mình. Điều này khá công bằng bởi phe sói có lợi thế hơn nhiều so với phe dân khi chúng biết chính xác ai là đồng loại của mình. Hơn nữa việc trò chơi bị mắc kẹt ở thế hoà cũng tương đương với việc người dân trong làng sống yên ổn mãi mãi mà không lo bị sói cắn, đây cũng có thể xem như một chiến thắng của dân làng và thất bại của phe sói, vì vậy phe sói không được phép để kết quả hoà xảy ra. Từ những điểm trên, ta chỉ tập trung vào chiến lược của phe dân. Thật bất ngờ là chiến lược tối ưu của phe dân có một khuôn mẫu rất đơn giản:
#### <ins>Mệnh đề 1:</ins> Ở lượt chơi của phe dân, nếu tổng số người chơi (bao gồm cả dân và sói) là lẻ, hãy treo cổ 1 người chơi, nếu tổng số người chơi là chẵn, hãy bỏ phiếu để tạo ra kết quả hoà (không treo cổ ai cả). <br>
- Đặt $r_{m,n}$ là tỉ lệ thắng của phe dân trong tình huống có $m$ sói, $n$ dân và đang ở lượt đi của phe dân. Hiển nhiên ta có ngay $r_{m,n}=0$ khi $m \ge n$ và $r_{0,n} = 1$ khi $n \ge 1$ . Bởi vậy từ khúc này ta thống nhất rằng chỉ (cần) xét các giá trị $r_{m,n}$ với $0 \le m \le n$ .
- Để chỉ ra rằng *mệnh đề 1/* là chiến lược tối ưu, ta sẽ chứng minh một mệnh đề bao quát hơn:
#### <ins>Mệnh đề 2:</ins> Chiến lược ở *mệnh đề 1/* là chiến lược tối ưu cho phe dân và ${r_{m - 1,n + 1}} > {r_{m,n}}$ với $1 \le m \le n$  
- Đầu tiên, dễ thấy rằng mệnh đề đúng khi tổng số người chơi $≤ 2$. Ta sẽ chỉ ra rằng: giả sử *mệnh đề 2/* đúng khi tổng số người chơi  $\le k-1$ cũng đúng khi tổng số người chơi là $k$ . Thật vậy, ta lập luận như sau: <br>
Với mỗi cặp $(m,n)$ thoả mãn $m+n=k$ , xét một tình huống có $m$ sói, $n$ dân và đang ở lượt của phe dân, khi đó: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tỉ lệ của phe dân khi chọn "treo cổ 1 người chơi" là: <br>
```math
     \frac{m}{k}{r_{m - 1,n - 1}} + \frac{n}{k}{r_{m,n - 2}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Tỉ lệ của phe dân khi chọn "không treo cổ 1 ai" là: ${r_{m,n - 1}}$
- Khi đó ta chia thành hai trường hợp như sau: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>Trường hợp $k$ lẻ</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bởi $m + n - 1 = k - 1$ (chẵn) nên theo quy nạp ta có: ${r_{m,n - 1}} = {r_{m,n - 2}}$ <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mà ${r_{m - 1,n - 1}} > {r_{m,n - 2}}$ (quy nạp) nên $\frac{m}{k}{r_{m - 1,n - 1}} + \frac{n}{k}{r_{m,n - 2}} > {r_{m,n - 2}} = {r_{m,n - 1}}$ <br>
$\Longrightarrow$  Lựa chọn "treo cổ 1 người chơi" đem lại tỉ lệ thắng cao hơn cho phe dân, nói cách khác: <br>
```math
{r_{m,n}} = \frac{m}{k}{r_{m - 1,n - 1}} + \frac{n}{k}{r_{m,n - 2}} \rightarrow {r_{m - 1,n - 1}} > {r_{m,n}} > {r_{m,n - 2}   } \text{ 
  }( \text{do  } {r_{m - 1,n - 1}} > {r_{m,n - 2}}) \text{ }(*)
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<ins>Trường hợp $k$ chẵn</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bởi $m + n - 1 = k - 1$ (lẻ) và $m + n - 2 = k - 2$ (chẵn) nên theo quy nạp ta có: 
```math
{r_{m - 1,n - 1}} = {r_{m - 1,n - 2}};{r_{m,n - 2}} = {r_{m,n - 3}} \text{   và   } {r_{m,n - 1}} = \frac{m}{{k - 1}}{r_{m - 1,n - 2}} + \frac{{n - 1}}{{k - 1}}{r_{m,n - 3}}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Do theo quy nạp ta có ${r_{m - 1,n - 2}} > {r_{m,n - 3}}$ , nên ta suy ra: 
```math
\frac{m}{k}{r_{m - 1,n - 1}} + \frac{n}{k}{r_{m,n - 2}} = \frac{m}{k}{r_{m - 1,n - 2}} + \frac{n}{k}{r_{m,n - 3}} < \frac{m}{{k - 1}}{r_{m - 1,n - 2}} + \frac{{n - 1}}{{k - 1}}{r_{m,n - 3}} = {r_{m,n - 1}}
```
$\Longrightarrow$ Lựa chọn "không treo cổ ai" đem lại tỉ lệ thắng cao hơn cho phe dân, tức là: ${r_{m,n}} = {r_{m,n - 1}}$ . <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Từ đó ta suy ra: ${r_{m - 1,n + 1}} = {r_{m - 1,n}} > {r_{m,n - 1}} = {r_{m,n}}$ (có ${r_{m - 1,n}} > {r_{m,n - 1}}$ theo giả thiết quy nạp). <br>
- Từ 2 trường hợp $k$ lẻ và $k$ chẵn, ta thấy rằng: Nếu *mệnh đề 2/* đúng khi tổng số người chơi $\le k-1$ thì nó cũng đúng khi tổng số người chơi là $k$ chẵn. Quá trình quy nạp hoàn tất tức ta hoàn tất chứng minh. <br>

<ins>Nhận xét:</ins> Bởi *mệnh đề 2/* đã được chứng minh nên từ giờ ta có thể khẳng định chiến lược ở *mệnh đề 1/* là chiến lược tối ưu. Có vài điểm may mắn ở đây. Đầu tiên, việc tìm công thức tường minh cho dãy số $r_{m,n}$ là rất khó, nhưng quá trình quy nạp để chứng minh *mệnh đề 2/* lại không yêu cầu ta phải biết chính xác các giá trị $r_{m,n}$ . Ngoài ra, theo luật chơi thì dân làng không thể biết được người chơi đã bị treo cổ là sói hay dân. Do đó họ không biết chính xác số sói và số dân còn lại sau mỗi lượt. Như vậy, có vẻ ta sẽ gặp rắc rối khi phải phân tích hàng đống khả năng có thể xảy ra ở mỗi lượt chơi. Tuy nhiên, bởi nội dung của *mệnh đề 1/* chỉ liên quan đến tổng số người chơi nên lựa chọn của phe dân ở mỗi lượt không phụ thuộc vào số sói và số dân cụ thể. Do đó quá trình lập luận bằng quy nạp không gặp phải cản trở nào cả. 






















  












