# REVIEW ĐỀ THI HSG CẤP TỈNH THPT 2021
## NGÀY 1: 9/3/2021

### Bài 01: HÀNH TRÌNH KEPLE
#### Dạng bài: Số học, Làm việc với ngày/tháng/năm
- Một lưu ý cực kì quan trọng: Tính ngày **trước đó** hoặc **sau đó**. 
- Nếu tính được khoảng cách giữa 2 ngày --> bài toán được giải quyết
- Đây là bài đầu tiên của đề nhưng có vẻ khó hơn mọi năm, làm hơi mất thời gian
### Bài 02:
#### Dạng bài: Mảng + dãy con
- Dùng 2 for lồng để duyệt, nhưng phải xử lý khéo, so sánh cập nhật kết quả liên tục
- Tránh xử lý trên từng dãy con riêng lẻ --> chương trình sẽ chạy rất chậm. Mà biết tận dụng kết quả của dãy con trước, so sánh và tính toán lại cho dãy con hiện tại.
- Nhìn chung cũng là 1 bài gây khó chịu về mặt thời gian.
- Theo anh, có thể có cách giải theo hướng khác tốt hơn.

### Bài 03:
#### Dạng bài: Mảng 2 chiều
- Đây là 1 bài khá dễ, nhưng đòi hỏi phải thiết kế thuật toán cho hợp lý.
- **Đề yêu cầu:** Với mỗi [i,j] hãy tìm trong ma trận ban đầu: từ [1,1] đến [i,j] số không âm nhỏ nhất không xuất hiện trong hình chữ nhật đó. Tập hợp các kết quả tìm được, ta được ma trận kết quả.

### Bài 04:
#### Dạng bài: Mảng 2 chiều

- Đọc đề thì thấy bài hoàn toàn không khó, nhưng dù sao đây cũng là bài cần phải suy nghĩ nhiều hơn để tìm giải thuật hợp lý
- Test thứ 2:

```
1 1 1 1
1 1 1 1
1 0 1 0
1 0 1 1
1 0 1 1
```

- Test thứ 1:

```
1 1 1
1 0 1
1 1 0
1 1 1
```

- Theo anh, 1 ô không tới dc nếu nó bị chặn ở 2 đầu (hàng & cột)

Cả 2 số (2 số 1 ở test 2), trên cùng hàng phía trước có số 0 chặn nên ko tới dc, trên cùng cột cũng có số 0 chặn nên cũng ko tới được

