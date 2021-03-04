# ĐỀ TIỀN GIANG 2017

### Bài 1:
- Chi tiết đề (nếu có) có thể là hình ảnh hoặc văn bản

- Chi tiết bộ test (nếu có)

**Source code**

```
uses crt;
var a,b,c,x1,x2,d:real;
BEGIN
 clrscr;
 write('Nhap a: ');readln(a);
 write('Nhap b: ');readln(b);
 write('Nhap c: ');readln(c);
 d:=b*b-4*a*c;
 if d>0 then
  begin
   x1:=(-b+sqrt(d))/(2*a);
   x2:=(-b-sqrt(d))/(2*a);
   writeln('2 nghiem PT la: ',x1:0:2,' va: ',x2:0:2);
  end
 else if d=0 then
  begin
   x1:=(-b)/(2*a);
   writeln('PT co nghiem kep la: ',x1:0:2);
  end
 else writeln('PT vo nghiem');
 readln
END.
```

Link: https://ideone.com/VqOCVz

### Bài 2
