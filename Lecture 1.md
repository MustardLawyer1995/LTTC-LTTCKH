# Sheep Game
- <ins>Không gian giới hạn của trò chơi:</ins> Cánh đồng có kích thước $n \times 1$ gồm các ô vuông thành phần có kích thước $1 \times 1$
- <ins>Mô phỏng luật chơi</ins>: Sau mỗi lượt con cừu ở vị trí (0) sẻ nhảy qua con cừu 2, con cừu 2 nhảy qua con cừu 3 và kế đến con cừu 3 nhảy về con cừu 1 (tất cả con cừu phải nhảy qua điểm đối xứng, chẳng hạn như con cừu 1 nhảy qua con cừu 2 và rơi xuống điểm đối xứng). Hỏi phải đặt 3 con cừu như thế nào để chúng nhảy không vượt qua cánh đồng đó
## Lời giải
<ins>Phân tích:</ins> Để biểu diễn tương quan mô hình chuyển động của 3 con cừu trên, ta cần lập ra phương trình chuyển động như sau:
Gọi ${a_i},{b_i},{c_i}|\forall i = \overline {0,1,2,...}$ lần lượt là các vị trí sau mỗi lần $i$ di chuyển của con cừu 1,2 và 3. Khi ấy ta có hệ phương trình sau:
```math
\left\{ \begin{array}{l}
{a_1} = 2{b_0} - {a_0}\\
{b_1} = 2{c_0} - {b_0}\\
{c_1} = 2{a_1} - {c_0} = 2\left( {2{b_0} - {a_0}} \right) - {c_0} =  - 2{a_0} + 4{b_0} - {c_0}
\end{array} \right.
```
