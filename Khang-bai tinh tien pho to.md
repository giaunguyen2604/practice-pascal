## hinh anh:
<img width="243" alt="Screenshot (5)" src="https://user-images.githubusercontent.com/80033114/111141062-a6dce000-85b5-11eb-8b3f-584568e3e015.png">
# Bai lam:

```
uses crt;
var n,t:longint;
procedure nhap;
begin
        readln(n);
end;
procedure xuli;
begin
  if n div 2>100 then t:=t+(n div 2)*280 else
  if n div 2<=100 then t:=t+(n div 2)*300;
  if n mod 2<>0 then t:=t+250;
write(t);
end;
begin
        nhap;
        xuli;
end.
```

[x] Đã xem
