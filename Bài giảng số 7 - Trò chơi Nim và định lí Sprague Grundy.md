# Trò chơi Nim và định lí Sprague Grundy 
### 1. Trò chơi Nim<br>
&nbsp;&nbsp;&nbsp;&nbsp;Nim là một trò chơi có 2 người chơi, thực hiện nước đi theo lượt. <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Luật chơi:</ins>* Có một số lượng các vật thể (hòn đá/que diêm/đồng xu/...)-tạm gọi là "quân", được xếp thành nhiều đống khác nhau. Ở mỗi lượt, người chơi phải lấy ít nhất 1 quân và có thể lấy bất kỳ số lượng nào miễn là tất cả các quân bị lấy đều trong cùng một đống. <br>

&nbsp;&nbsp;&nbsp;&nbsp;Nim thường được chơi theo luật misère, trong đó người chơi lấy quân cuối cùng sẽ thua. Nim cũng có thể được chơi theo luật "normal", trong đó người chơi lấy quân cuối cùng sẽ thắng. Đây được gọi là cách chơi "normal" bởi vì nước đi cuối là nước thắng trong hầu hết các trò chơi, mặc dù đó không phải là cách mà Nim thường được chơi. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Các biến thể của Nim đã được chơi từ thời cổ đại. Trò chơi này được cho là bắt nguồn từ Trung Quốc, rất giống với trò chơi 捡石子 (kiểm thạch tử/nhặt đá) của Trung Quốc. các tài liệu tham khảo sớm nhất ở châu Âu về Nim là từ đầu thế kỷ 16. Tên hiện tại của nó được đặt ra bởi Charles L. Bouton của Đại học Harvard , người cũng đã phát triển lý thuyết hoàn chỉnh của trò chơi vào năm 1901, nhưng nguồn gốc của cái tên không bao giờ được giải thích đầy đủ. <br>
&nbsp;&nbsp;&nbsp;&nbsp;Phiên bản mặc định của Nim game (người nào lấy được quân cuối cùng thì thắng) tồn tại một chiến lược tất thắng, đó là phép cộng chuỗi nhị phân theo xor, được định nghĩa như sau: để tính a xor b, chuyển a và b về dạng nhị phân, sau đó viết chúng theo 2 hàng và tính tổng xor mỗi hàng theo quy tắc: $0 \text{  } xor \text{  } 1 =1; 0 \text{  } xor \text{  } 0 = 1 \text{  } xor \text{  } 1 =0$ <br>

&nbsp;&nbsp;&nbsp;&nbsp;*<ins>Ví dụ:</ins>* <br>

#### &nbsp;&nbsp;&nbsp;&nbsp; *a. Bản chất tiện ích* <br>
