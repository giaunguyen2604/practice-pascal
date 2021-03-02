# RULE CODE 
Nhằm giúp các em viết code sạch hơn, hay nói đúng hơn với một từ khoa học mà dân code hay xài đó chính là **Clean code** .
Vậy vấn đề đặt ra là: 
- `Clean code để làm gì?`
-  `Có lợi ích gì không?` 
-  `Dùng khi nào và không dùng khi nào?` 
Vậy bây giờ, thử so sánh 2 đoạn code sau đây:
**Đoạn code 1:**
```
for (int j=0; j<34; j++) {
    s += (t[j]*4)/5;
}
```
với **Đoạn code 2**
```
int realDaysPerIdealDay = 4;
const int WORK_DAYS_PER_WEEK = 5;
int sum = 0;
for (int j=0; j < NUMBER_OF_TASKS; j++) {
    int realTaskDays = taskEstimate[j] * realDaysPerIdealDay;
    int realTaskWeeks = (realdays / WORK_DAYS_PER_WEEK);
    sum += realTaskWeeks;
}
```
Thoạt nhìn....
Ủa, Đoạn 1 nhìn ngắn hơn, dễ nhìn hơn, dĩ nhiên chọn đoạn 1 để viết....
Nhưng, điều đó chỉ đúng khi đoạn code 1 luôn luôn đúng đắn và đặc biệt chỉ dành cho mình bạn đọc và đọc chỉ 1 lần duy nhất...
Dám chắc vài tuần sau quay lại không biết 34, 4, 5 là gì? Khi đó bạn phải đọc lại đề, dò xem từ số xem nó là gì và tại sao mình lại tính toán bằng công thức như vậy?
Còn đối với đoạn code 2 mọi thứ đã tường minh thông qua việc khai báo biến có ý nghĩa. Bạn có thể nhìn vào code và liên tưởng đến yêu cầu của đề bài là gì?

**Vậy tóm lại, `Clean Code` có các công dụng sau:**

> - Code đọc sẽ dễ hiểu cho bản thân mình, bạn bè, thầy cô.
> - Code dễ bảo trì (sửa lỗi khi phát hiện lỗi)
> - Đặc biệt, với những bài toán phức tạp, bạn sẽ tốn rất nhiều thời gian nếu không phát huy được tính tái sử dụng của code.

Trả lời cho câu hỏi: `Khi nào thực hiện điều đó?`
--> Nên tạo thói quen này trong mọi lúc bắt tay vào code. Sẽ có những lúc trở thành điều dư thừa, nhưng rất có ích cho sau này.
***Bản thân đã trải nghiệm, đã bị chửi nhiều lần, nên biết, khỏi thắc mắc :)***
## RULE
Kể từ bây giờ, khi bắt tay vào code nộp bài cho anh thì tuân thủ theo các rule này nhé:

- KHÔNG viết code có lề trên cùng 1 hàng, phải thục ra thục vào (sử dụng tab hoặc space)
- KHÔNG được đặt tên biến bằng tiếng Việt, chỉ xuất hiện tiếng việt đối với text hay dữ liệu mà đề bài cho.
- Tên biến phải viết hoa ở đầu mỗi chữ cái. Ví dụ: FullName, InfoUser,...
- Tên hàm, procedure đặt giống tên biến, tuy nhiên không viết hoa chữ cái đầu. Ví dụ: getInfoUser, findStudent, sortStudent,...
- Tên hàm, procedure, tên biến phải được đặt có ý nghĩa, KHÔNG được đặt x, y, z; `ngoại trừ những biến được đề bài cho tên sẵn, nhưng phải comment ý nghĩa tên biến bằng dấu //` 
- KHÔNG được xử lý LOGIC trong `chương trình chính`, phải được xử lý ở hàm hoặc procedure.
- Kể từ bây giờ phải nhập xuất file.

## Hướng dẫn nộp bài
1. Đầu tiên xem cách viết document dùng markdown tại đây: https://guides.github.com/features/mastering-markdown/ 
2. Mỗi đứa phải có 1 tài khoản github
3. Anh sẽ gửi link cho edit vào đó (github) (dùng markdown để soạn tài liệu)
4. Code xong bài nào thì upcode lên https://ideone.com/ và dán link vào file anh gửi ở mục 3
5. Từ giờ về sau, đây là kho tài liệu học tập luôn, tất cả được lưu trữ online, khi cần chỉ vào github.com lục lại, OK, quá tiện lợi phải không nào?

- **Nếu có khó khăn ở khâu nào, thì inbox facebook, từ từ làm, không vội**

## AMAZING! GOOD JOB :) 