## <center> ĐỀ THI THỬ HSG CẤP TỈNH THCS </center>

#### <center>NGÀY KIỂM TRA: 21/03/2021</center>

#### <center>Thời gian làm bài: 180 phút</center>

Nội dung đề bài:

#### BÀI 1: TRIBONACCI (5 ĐIỂM) Tên chương trình: TRIBONACCI.PAS

<div style="text-align: justify">
Nói đến dãy số Fibonacci, chắc chắn ai trong chúng ta ít nhiều cũng đã biết tới. Bờm vừa được thầy của mình dạy cho về dãy Fibonacci, anh ta rất thích thú với dãy số này nhưng lại cảm thấy công thức của dãy số này quá đơn giản, do đó Bờm nghĩ đến một dãy số phức tạp hơn có công thức gần giống với dãy Fibonacci, Bờm đặt tên cho dãy đó là Tribonacci.

Dãy Tribonacci là dãy số có công thức như sau:
`𝑇(𝑖)=𝑖;` với mọi số nguyên dương 𝑖 ≤ 3
`𝑇(𝑖)=𝑇(𝑖−1)+𝑇(𝑖−2)+𝑇(𝑖−3);` với mọi số nguyên dương 𝑖 > 3
Bờm khoe dãy số mới với Tèo, vốn là một người rất thông minh nhưng cũng rất gian xảo nên Tèo đố bờm có thể tính được tổng 𝑁 phần tử đầu tiên của dãy Tribonacci này. Tức là Bờm cần tính giá trị:
`𝐹(𝑁)=𝑇(1)+𝑇(2)+𝑇(3)+⋯+𝑇(𝑁−1)+𝑇(𝑁)`
Do giá trị 𝑁 rất lớn nên hãy giúp Bờm tính và trả lời kết quả cho câu đố của Tèo nhé. Do giá trị rất lớn nên Bờm chỉ cần trả lời phần dư của kết quả sau khi chia cho 10<sup>15</sup></sup> + 7.

</div>

**Dữ liệu vào:** Vào từ file văn bản **TRIBONACCI.INP:** chứa số nguyên dương 𝑁.

**Kết quả:** Ghi ra file văn bản **TRIBONACCI.OUT:** gồm 1 dòng là kết quả tìm được. Do kết quả rất lớn nên chỉ cần trả về phần dư cho 10<sup>15</sup> + 7
  
<div >

|              TRIBONACCI.INP              |         TRIBONACCI.OUT          |
| :-----------------------------: | :---------------------: |
| 1| 1 |
|2|3|
|3|6|
|4|12|
|5|23|
</div>

#### BÀI 2: SUBSTRING (4 ĐIỂM) Tên chương trình: SUBSTRING.PAS

<div style="text-align: justify">
<strong>hgminh</strong> là một thành viên mới của tập đoàn trách nhiệm hữu hạn nhiều thành viên phi lợi nhuận đào tạo coder: Cờ Một Một.

Không may thay, khi vừa vào anh bị tổ trưởng điểm danh Cà Dốt chơi khó, anh cần tìm số thứ tự trong danh sách nhân viên. Cà Dốt cho anh một xâu 𝑆 độ dài 𝑛, tên của hgminh trong danh sách là xâu 𝐵 độ dài 𝑚. Để tìm ra số thứ tự của mình, hgminh cần phải đếm số xâu con (định nghĩa xâu con xem ở dưới) phân biệt của xâu 𝑆 thỏa mãn:

- 2 ký tự kề nhau trong xâu con phải khác nhau
- Có thứ tự từ điển không nhỏ hơn xâu 𝐵

Vì kết quả rất to mà hgminh chưa học số lớn nên Cà Dốt quyết định sẽ yêu cầu hgminh đưa ra kết quả sau khi mod 1000000007 (10<sup>9</sup>+7)
Xâu 𝑎 gọi là xâu con của 𝑆 nếu tồn tại 1 dãy 𝑥 thỏa mãn 0<𝑥1<𝑥2<⋯<𝑥<sub>𝑙𝑒𝑛𝑔𝑡ℎ(𝑎)</sub>≤ 𝑙𝑒𝑛𝑔𝑡ℎ(𝑆) và 𝑎<sub>i</sub>=𝑆<sub>𝑋𝑖</sub> với mọi 𝑖 từ 1 đến 𝑙𝑒𝑛𝑔𝑡ℎ(𝑎).

`Ví dụ:` xâu "aba" có 6 xâu con phân biệt khác rỗng là: "a", "b", "ab", "ba", "aa", "aba"

**Dữ liệu:** Vào từ file văn bản **SUBSTRING.INP:**

- Dòng 1: số nguyên dương 𝑡 là số test (𝑡≤5)
- Mỗi test có định dạng như sau:
  - Dòng 1: xâu 𝑆 độ dài 𝑛
  - Dòng 2: xâu 𝐵 độ dài 𝑚

**Kết quả:** Ghi ra file văn bản **SUBSTRING.OUT:**

- Gồm 𝑡 dòng, dòng thứ 𝑖 là kết quả của test thứ 𝑖 sau khi mod 1000000007 (10<sup>9</sup>+7)

**Scoring**
Trong tất cả các test 𝑛, 𝑚 ≥ 1,
Xâu 𝑆, 𝐵 chỉ gồm chữ thường từ 'a' ... 'z'
Trong 20% số test, 𝑛, 𝑚 ≤ 20
Trong 40% số test tiếp theo, 𝑛, 𝑚 ≤ 1000 (10<sup>3</sup>)
Trong 40% số test tiếp theo, 𝑛, 𝑚 ≤ 100000 (10<sup>5</sup>)

</div>
<div>

|           SUBSTRING.INP            | SUBSTRING.OUT |
| :------------------------: | :----: |
| 2<br>bab<br>aa<br>cac<br>b | 4<br>3 |

</div>

**Note**

- Xâu "bab" có 4 xâu con thỏa mãn là: "b", "ab", "ba", "bab"

- Xâu "cac" có 3 xâu con thỏa mãn là: "c", "ca", "cac"

#### BÀI 3: GAME (4 ĐIỂM) Tên chương trình: GAME.PAS
Mỗi khi bị kẹt xe trên đường vì tắt đường. An thường nghĩ ra trò chơi để giải trí. Một trong những trò chơi đó là An đọc N số từ các biển số xe và tìm số nguyên M (M > 1) sao cho N số đã đọc đều có cùng số dư khi chia cho M. An muốn tìm được càng nhiều số M như thế càng tốt. Bạn hãy giúp An tìm tất cả các số M thoả mãn yêu cầu.
**Dữ liệu:** vào từ file **GAME.INP**

- Dòng đầu tiên chứa số nguyên N (2 ≤ N ≤ 100)
- N dòng tiếp theo, dòng thứ i chứa số nguyên B<sub>i</sub> thuộc đoạn [1;10<sup>9</sup>]. Tất cả số nguyên đôi 1 khác nhau. Dữ liệu vào đảm bảo tồn tại ít nhất một số M thoả mãn yêu cầu.

**Kết quả:** Ghi ra file **GAME.OUT** tất cả các số M tìm được theo thứ tự tăng dần, các số ghi cách nhau bởi dấu cách.

<div >

| GAME.INP | GAME.OUT |
| :----: | :----: |
| 3<br>6<br>34<br>38| 2<br>4 |
| 5<br>5<br>17<br>23<br>14<br>83 | 3 |

</div>

#### BÀI 4: SỐ RÕ RÀNG (3 ĐIỂM)   Tên chương trình: ***CLEARNUM.PAS***

<div style="text-align: justify">
Bờm mới tìm được một tài liệu định nghĩa số rõ ràng như sau: Với số nguyên dương n, ta tạo số mới bằng cách lấy tổng bình phương các chữ số của nó, với số mới này ta lại lặp lại công việc trên. Nếu trong quá trình đó, ta nhận được số mới là 1, thì số n ban đầu được gọi là số rõ ràng. Ví dụ, với n = 19, ta có:

`19 → 82 (= 12 +92) → 68 → 100 → 1` 
Như vậy, 19 là số rõ ràng.
Không phải mọi số đều rõ ràng. 
Ví dụ, với n = 12, ta có:
`12 → 5 → 25 → 29 → 85 → 89 → 145 → 42 → 20 → 4 → 16 → 37 → 58 → 89 → 145`
Bờm rất thích thú với định nghĩa số rõ ràng này và thách đố phú ông: Cho một số nguyên dương n, tìm số S(n) là số rõ ràng liền sau số n, tức là S(n) là số rõ ràng nhỏ nhất lớn hơn n. 
Tuy nhiên, câu hỏi đó quá dễ với phú ông và phú ông đã đố lại Bờm: Cho hai số nguyên dương n và m (1 ≤ n,m ≤ 10<sup>15</sup>), hãy tìm số S<sup>m</sup>(n)=S(S(…S(n) )) là số rõ ràng liền sau thứ m của n.
    Bạn hãy giúp Bờm giải câu đố này nhé!
**Dữ liệu:** Vào từ file văn bản **CLEARNUM.INP** một dòng chứa 2 số nguyên n và m.

**Kết quả:** Ghi ra file văn bản **CLEARNUM.OUT** một dòng là kết quả tìm được.


</div>
<div >

| CLEARNUM.INP       | CLEARNUM.OUT      |
| :----:             |    :----:   | 
| 18 1        |     19      | 
| 1 14567807  | 1000000000  | 

</div>

**Giải thích:**
- Test 1: Số rõ ràng thứ 1 sau số 18 là 19.
- Test 2: Số rõ ràng thứ 14567807 sau số 1 là số 1000000000.

#### BÀI 5: HAI GIÁ TRỊ (3 ĐIỂM) Tên chương trình: TWOVALS.PAS
Cho dãy số nguyên a<sub>1</sub>, a<sub>2</sub>,...,a<sub>N</sub>. Tìm độ dài dãy con dài nhất chỉ bao gồm 2 giá trị khác nhau. Ví dụ dãy 1, 3, 2, 3, 3, 1, 2 thì đoạn dài nhất cần tìm là 3, 2, 3, 3 có độ dài 4 gồm 2 giá trị là 2 và 3.
**Dữ liệu:** Vào từ file văn bản **TWOVALS.INP**
- Dòng đầu tiên ghi số nguyên N (1 ≤ N ≤ 10<sup>9</sup>)
- Dòng thứ 2 ghi N số nguyên (a<sub>1</sub>, a<sub>2</sub>,...,a<sub>N</sub>) (1 ≤ a<sub>i</sub> ≤ 10<sup>9</sup>)

**Kết quả:** Ghi ra file văn bản **TWOVALS.OUT** một số nguyên duy nhất là độ dài dài nhất tìm được.
<div style="margin-left: 0%">

| TWOVALS.INP | TWOVALS.OUT |
| :----: | :----: |
| 7<br>1 3 2 3 3 1 2| 4 |
</div>

---
<center>Không giải thích gì thêm!</center>
