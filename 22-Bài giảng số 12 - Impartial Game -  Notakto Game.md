# Impartial Game - Notakto Game
&nbsp;&nbsp;&nbsp;&nbsp;<ins>Giới thiệu:</ins> ***<ins>Notakto</ins>*** là một biến thể của trò tic-tac-toe, còn được gọi là *tic-tac-toe trung tính* hoặc *impartial tic-tac-toe*. Trò chơi này là sự kết hợp của tic-tac-toe và Nim, được chơi trên một hoặc nhiều bảng $3 \times 3$ với hai người chơi lần lượt đánh chữ X vào các ô. Khi một bảng có 3 chữ X thẳng hàng, nó bị khóa-không ai có thể sử dụng nó nữa, người chơi nào thực hiện nước đi cuối cùng thì thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Notakto là một impartial game, trong đó các nước đi được phép chỉ phụ thuộc vào trạng thái của trò chơi chứ không phụ thuộc vào việc đến lượt người chơi nào. Khi chơi trên nhiều bảng, nó là một trò chơi khác nhau. Trò chơi được cho là do giáo sư/người chơi backgammon Bob Koca, phát minh ra vào năm 2010, khi cháu trai 5 tuổi của ông đề nghị chơi một trò chơi tic-tac-toe với cả hai người chơi là "X". <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chiến lược tất thắng (hình 1)</ins>*
<div align="center">
 
Hình 1            | Hình 2
:-------------------------:|:-------------------------:
![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/71b34373-6ef3-474d-8ca5-f4050f327c95)  | ![image](https://github.com/MustardLawyer1995/LTTC-LTTCKH/assets/156400720/e05c1b28-2ac7-4352-b5b5-40e161d67429)
</div>

&nbsp;&nbsp;&nbsp;&nbsp;*Chiến lược tối ưu* cho trò chơi 1 bảng của Notakto cho phép người chơi đầu tiên giành chiến thắng. Người chơi đầu tiên đặt X ở trung tâm và sau đó đi các ô cách xa các ô của đối thủ theo chiều di chuyển của một quân mã. Chiến lược này hoạt động vì nó tạo ra một cấu trúc giống như chiếc giày, được gọi là "bẫy giày" (hình 2). Ở trạng thái bẫy giày, người đi trước luôn thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Với 2 bảng, người chơi thứ hai trong lượt đầu tiên của mình nên đánh X ở ô trung tâm của bảng trống (bảng không có chữ X trong đó). Sau đó, người chơi thứ hai hy sinh một trong các bảng (bằng cách tạo 3 X liên tiếp) nếu có thể. Giờ đây, trò chơi trở thành trò chơi 1 bảng của Notakto, do đó người chơi thứ hai sử dụng chiến lược bẫy giày để giành chiến thắng. Cụ thể, (đánh số các cột là 1,2,3; các hàng của bảng 1 là a,b,c; các hàng của bảng 2 là A,B,C) mạch của trò chơi có thể diễn tiến theo 3 hướng tùy vào nước đi đầu tiên của player1: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•1) b2 $\rightarrow$ B2 $\rightarrow$ a1/a2 $\rightarrow$ c3/c2 $\rightarrow$ khóa bảng 1, giờ đến lượt player1 đánh ở bảng 2, nơi mà đã có nước B2 do player2 đánh từ trước $\rightarrow$ player2 áp dụng chiến thuật như khi chơi notakto 1 bảng, player1 thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•2) a1 $\rightarrow$ B2 $\rightarrow$ b3/c2 (nếu player1 đi ở các ô khác ngoài b3 và c2 thì player2 có thể tạo 3 chữ X khóa bảng 1 ngay lập tức, player1 thua) $\rightarrow$ c2/b3 $\rightarrow$ giờ player1 đánh ở bất cứ đâu trên bảng 1, player2 sẽ khóa bảng 1 ngay, nên player1 chỉ còn cách đi ở bảng 2 (đã có X ở B2), player2 chỉ cần áp dụng chiến thuật bẫy giày để khiến player1 là người khóa bảng 2, sau đó player2 được quyền đánh trước ở bảng 1: c3 $\rightarrow$ a2/b1 $\rightarrow$ b1/a2 $\rightarrow$ player1 thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•3) a2 $\rightarrow$ B2 $\rightarrow$ b1/b3/c1/c3 (tương tự như •2, player1 không thể đi những ô nằm ngoài 4 ô này) $\rightarrow$ c3/c1/b3/b1 $\rightarrow$ thế trận trở về như trường hợp •2. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•4) a1 $\rightarrow$ B2 $\rightarrow$ nếu player1 đi ở bảng 2, player2 theo chiến thuật bẫy giày để cho player1 khóa bảng 2, player2 bây giờ đánh trước ở bảng 1: c3 $\rightarrow$ a2 $\rightarrow$ c2 $\rightarrow$ b1 $\rightarrow$ b3 (tạo các nước đi đối xứng tâm với player1, nếu nước đầu của player1 là a2 thay cho a1 thì cũng áp dụng cách tương tự) $\rightarrow$ player1 thua. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Phỏng đoán</ins>*: bất kỳ notakto nào có nhiều hơn 2 bảng luôn có thể giành chiến thắng bởi người chơi thứ nhất (trên một số bảng lẻ) hoặc bởi người chơi thứ hai (trên số bảng chẵn) nếu dùng lối đánh tương tự. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Lời giải</ins>*:Ta sẽ dựa vào những hiểu biết có được từ kịch bản notakto 1 bảng và 2 bảng. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Bảng chỉ có 1 X ở trung tâm thì người đi trước luôn thua (người đi sau dùng bẫy giày), gọi là bảng type I. Bảng chỉ có 1 X nhưng không ở trung tâm thì người đi trước thắng (sử dụng chiến thuật đối xứng tâm), bảng có 3 X ở a1 b3 c2 cũng cùng kết cục (người đi trước đánh ở c3 là thắng), gọi chúng là bảng type IIa. Bảng IIa sau khi bị đánh 1 nước tối ưu trở thành bảng type IIb, tất nhiên với loại bảng này người đi trước thua. Bảng rỗng là bảng type 0, người đi trước thắng (chỉ cần đánh ở trung tâm). <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Bổ đề</ins>*: thế $W$ gồm những thế sau đây: chỉ gồm {một số lượng bất kỳ bảng IIa, ít nhất 1 bảng I, một số chẵn bảng 0} hoặc {một số lượng bất kỳ bảng IIa, một số chẵn $≥ 2$ bảng 0} hoặc {một số lượng bất kỳ bảng IIa, 1 bảng IIb} (số lượng bất kỳ bao gồm cả 0); và thế $W$ là thế tất bại cho người đi trước. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Chứng minh bổ đề</ins>*: <br>
&nbsp;&nbsp;&nbsp;&nbsp;Ta sẽ chỉ ra rằng ở thế W, người đi trước đi bất cứ nước nào thì người đi sau cũng có 1 nước đi để đưa trò chơi trở lại thế $W$ , và vòng lặp tiếp diễn đến khi người đi trước thua. Thật vậy có các trường hợp sau: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 1:</ins>* trạng thái chỉ gồm các bảng IIa và 1 bảng IIb và đến lượt bạn <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-Bạn đi 1 nước ở bảng IIa có X ở a1, nếu bạn đánh ở b3/c2 $\rightarrow$ đối thủ chỉ cần đánh ở c2/b3, bảng này vẫn là IIa; bạn đánh ở 1 ô khác b3/c2 $\rightarrow$ đối thủ tạo 3 X thẳng hàng và khóa bảng này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-Tương tự nếu bạn đánh vào bảng IIa có sẵn 3 X ở a1,b3,c2, đối thủ luôn có thể tạo 3 X thẳng hàng và khóa nó. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-Nếu đánh vào bảng IIb, đối thủ sẽ dùng chiến thuật đối xứng tâm để ép bạn đi nước cuối cùng khóa bảng này, lượt tiếp theo đối thủ đánh nước tối ưu ở 1 bảng IIa và biến nó thành bảng IIb; nếu trong quá trình đấu ở bảng IIb, bạn dùng 1 lượt của mình đánh sang bảng IIa khác, đối thủ sẽ tạo 3 X và khóa bảng đó ngay. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Tóm lại bạn sẽ luôn bị đưa trở lại trạng thái như case (1) dù muốn hay không, trong khi số lượng các bảng phải liên tục giảm dần, sẽ đến thời điểm chỉ còn 1 bảng IIb và đến lượt bạn, bạn thua. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 2:</ins>* Trạng thái gồm các bảng IIa, số chẵn bảng 0, ít nhất 1 bảng I <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Bạn đánh vào 1 bảng 0 làm nó trở thành I hoặc IIa, đối thủ làm tương tự ở 1 bảng 0 khác (có chẵn bảng 0).  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Nếu bạn đánh vào bảng IIa, kết cục như ở case1, nếu bạn đánh vào bảng I: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ Nếu có > 1 bảng I, đối thủ khóa bảng này. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ Nếu chỉ có 1 bảng I, tùy vào số lượng bảng 0 đang có mặt, nếu là 0, đối thủ áp chiến thuật bẫy giày vào bảng I bạn vừa đi, kết cục sẽ giống như ở case1 khi bạn đánh vào bảng IIb duy nhất giữa các bảng IIa; nếu có ≥2 bảng 0, đối thủ sẽ hủy ngay bảng I bạn vừa đi, bạn bị đưa về case3. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Trường hợp 3:</ins>* Trạng thái gồm các bảng IIa, một số chẵn ≥ 2 các bảng 0 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-  Bạn đánh vào bảng IIa, kết cục như ở case1. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-  Bạn đánh vào bảng 0, nó trở thành bảng I hoặc IIa $\rightarrow$ đối thủ đánh vào 1 bảng 0 khác và biến nó thành bảng I $\rightarrow$ bạn về trạng thái case2. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\Rightarrow$ Từ 3 trường hợp, ta thấy rằng nếu 1 người chơi bị đưa vào thế W thì sẽ ở đó mãi. Mặt khác số lượng các bảng luôn giảm đến khi tàn cục, các thế W đơn giản nhất là: 1 bảng IIb, 1 bảng I và 2 bảng 0. <br>
&nbsp;&nbsp;&nbsp;&nbsp; $\Longrightarrow$Đây đều là các thế thua cho người đi trước. Bổ đề đã được chứng minh. <br>
   
&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Nhận xét</ins>*   
&nbsp;&nbsp;&nbsp;&nbsp;Từ bổ đề, nếu trò chơi bắt đầu với số lẻ bảng, người chơi trước chỉ cần đánh vào trung tâm của 1 bảng và trò chơi bị rơi vào thế $W$ ở lượt sau $\rightarrow$ Người chơi đầu tiên thắng; nếu trò chơi bắt đầu với chẵn bảng thì bản thân trạng thái này đã là thế $W$ theo định nghĩa rồi $\rightarrow$ Người chơi trước thua. <br>













